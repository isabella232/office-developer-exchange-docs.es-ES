---
title: Escritor de Exchange en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: Obtenga información sobre el escritor de Exchange en Exchange 2013 para copia de seguridad y restaurar las operaciones.
ms.openlocfilehash: a4dc5963ab24a83969efc6e425b38a35276f3aa3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762974"
---
# <a name="exchange-writer-in-exchange-2013"></a>Escritor de Exchange en Exchange 2013

Obtenga información sobre el escritor de Exchange en Exchange 2013 para copia de seguridad y restaurar las operaciones. 
  
**Se aplica a:** Exchange Server 2013 
  
El escritor de Exchange es responsable de la copia de seguridad y restauración de bases de datos de Exchange Server 2013 activos. El escritor de Exchange también admite la funcionalidad de copia de seguridad de una base de datos seleccionado donde la instantánea se toma frente a la instancia replicada de la base de datos y transacciones los archivos de registro. 
  
## <a name="overview-of-the-exchange-writer"></a>Información general sobre el escritor de Exchange
<a name="bk_Overview"> </a>

Exchange 2013 incluye las características de movilidad de base de datos, que permiten a las bases de datos se replican entre los servidores de Exchange diferentes para mejorar la disponibilidad de base de datos y resistencia de sitios. Las demás copias de base de datos en un grupo de disponibilidad de base de datos (DAG) ofrecen una oportunidad valiosos para las copias de seguridad de Exchange utilizar los recursos adicionales que están disponibles en la ubicación de copia. Además, debido a que la copia en lugar del patrón de la base de datos activo se hace una copia, la copia puede ser no está disponible durante la copia de seguridad para un período de tiempo más largo. 
  
El escritor de Exchange se coordina con los servicios de Exchange (en funcionamiento en nombre del solicitante) para preparar los archivos de base de datos para las copias de seguridad, inmovilizar la actividad de entrada y salida procedentes de transacciones de Exchange antes de realizar la copia de seguridad de la base de datos y, a continuación, liberar y truncar archivos de registro una vez finalizada la copia de seguridad.
  
Durante una restauración, la aplicación de copia de seguridad y restauración indica el escritor de Exchange para coordinar con el almacén de Exchange (en funcionamiento en nombre del solicitante) para comprobar los destinos de restauración, el nombre del archivo de base de datos si es necesario y, a continuación, reproducir la transacción registros según sea necesario. El escritor de Exchange es compatible con las copias de seguridad y restauraciones.
  
El escritor de Exchange está disponible en cualquier servidor de Exchange que tenga instalado el rol de servidor de buzón de correo. 
  
## <a name="exchange-writer-configuration-settings"></a>Opciones de configuración del escritor de Exchange
<a name="bk_ExchangeWriterConfig"> </a>

El escritor de VSS de Exchange utiliza una variedad de opciones y valores que se deben establecer correctamente y se conservan durante las operaciones de copia de seguridad y restauración. Estas opciones de configuración se almacenan en el documento de metadatos del escritor de Exchange. Si la aplicación de copia de seguridad no conservar estas opciones de configuración, es posible que experimenta errores inesperados al intentar realizar una copia de seguridad de las bases de datos de Exchange. 
  
En la siguiente tabla se enumera las interfaces VSS que exponen los metadatos sobre los componentes de la copia de seguridad de la base de datos. Estas interfaces son necesarias para que al escritor de Exchange documento de metadatos que se utiliza para realizar una copia de seguridad del almacén de Exchange.
  
**La tabla 1. Interfaces VSS**

|**Interfaz VSS**|**Descripción**|
|:-----|:-----|
|IVssWMComponent  <br/> |Permite el acceso a la información de componente almacenada en el escritor de Exchange.  <br/> |
|IVssExamineWriterMetadata  <br/> |Permite a la aplicación solicitante de copia de seguridad y restauración examinar los metadatos del escritor de Exchange. El documento de metadatos del escritor de Exchange contiene valores específicos de Exchange 2013 y los parámetros que requiere la aplicación de copia de seguridad y restauración solicitante para que pueden especificar correctamente los componentes adecuados para copia de seguridad.  <br/> |
|IVssComponent  <br/> |Contiene métodos para examinar y modificar la información acerca de los componentes contenidos en el documento de componentes de copia de seguridad de un solicitante. Sólo se pueden obtener objetos para los componentes que se han agregado explícitamente a este documento por el método [IVssBackupComponents::AddComponent](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382646%28v=vs.85%29.aspx) .  <br/> |
|IVssBackupComponents  <br/> |Usa la aplicación de copia de seguridad y restauración solicitante para sondear el escritor de Exchange acerca del estado de archivo y para ejecutar copia de seguridad y restaurar las operaciones. El método [IVssBackupComponents:: SetBackupState](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382833%28v=vs.85%29.aspx) define si la operación de copia de seguridad es una completa, copia, incremental, o una copia de seguridad diferencial. El método [IVssBackupComponents::AddRestoreSubcomponent](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382649%28v=vs.85%29.aspx) define los subcomponentes de una base de datos de Exchange 2013 que puede seleccionar para una operación de restauración.  <br/> |
   
En el sistema de archivos de Windows Server, una base de datos de Exchange 2013 se almacena como un archivo de base de datos único con una extensión *.edb. El escritor de Exchange expone la *.edb como el componente de base de datos, mientras que los registros de transacciones (*. log) y archivos de punto de comprobación (*.chk) se combinan en un solo componente, que se conoce como el componente de registro. Para obtener más información acerca de los archivos de base de datos de Exchange, consulte [conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md).
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Las interacciones entre el escritor, VSS y VSS de Exchange los solicitantes
<a name="bk_interactions"> </a>

La interacción de alto nivel entre el VSS, el escritor de Exchange y Exchange 2013 durante las operaciones de copia de seguridad es como sigue:
  
1. El programa copia de seguridad (o el agente) se ejecuta un trabajo programado. 
    
2. El solicitante VSS en la aplicación de copia de seguridad y restauración envía un comando al VSS para que realice una instantánea de las bases de datos de Exchange 2013 seleccionados. 
    
3. VSS se comunica con el escritor de Exchange para preparar una copia de seguridad de la instantánea. Exchange 2013 prohíbe acciones administrativas frente a las bases de datos, comprueba las dependencias del volumen y suspende todas las operaciones de escritura a la instancia seleccionada de los archivos de registro de transacciones y de base de datos al tiempo que permite el acceso de solo lectura. 
    
4. VSS se comunica con el proveedor de almacenamiento correspondiente para crear una instantánea del volumen de almacenamiento que contiene las bases de datos de Exchange 2013. 
    
5. VSS libera 2013 de Exchange para reanudar las operaciones normales. 
    
6. El solicitante VSS, comprueba la coherencia física de la copia de seguridad antes de que la copia de seguridad tuvo éxito de señalización. Exchange 2013 trunca los registros de transacciones (si la base de datos forma parte de un DAG, el truncamiento del registro se replica entre todas las copias) y la hora de la última copia de seguridad de la base de datos de registros.
    
VSS serializa la interacción de los solicitantes con el escritor de Exchange con el método [OnPrepareBackup](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381571%28v=vs.85%29.aspx) iniciales y finales con el método [OnPostSnapshot](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381568%28v=vs.85%29.aspx) . Normalmente, la mayor parte del tiempo que dedica a trabajar con la copia de la sombra el escritor de Exchange se produce después del método **OnPostSnapshot** , cuando se comprueba la coherencia de la instantánea antes de la finalización de las copias de seguridad. El escritor de Exchange admite copias de seguridad paralelas entre **OnPostSnapshot** y [OnBackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381557%28v=vs.85%29.aspx).
  
Exchange 2013 no admite las copias de seguridad simultáneas de la misma base de datos. Sólo un trabajo de copia de seguridad a la vez puede ejecutar en una base de datos determinada. Cuando se ejecuta la copia de seguridad, el almacén de Exchange coloca la base de datos en un estado de copia de seguridad en curso. Este estado en memoria está desactivada ya sea en la finalización del proceso de copia de seguridad o cuando se reinicia el servicio. El estado de copia de seguridad en curso en la memoria y los datos asociados se pierden cuando se reinicia el servicio que hospeda el escritor de Exchange, cuando se reinicie el sistema operativo, o cuando se produce una conmutación por error del clúster. Cualquiera de estos eventos hará que el trabajo de copia de seguridad se lleve a cabo.
  
Truncamiento de archivo de registro de transacciones iniciadas por la copia de seguridad se desencadena en función del tipo de copia de seguridad que se debe realizar. En las configuraciones que no sean DAG, el escritor de Exchange truncará los archivos de registro de transacciones en la realización de copias de seguridad completas o incrementales correctas. En DAG replicado las configuraciones, se retrasará el truncamiento del registro por el servicio de replicación hasta que todos los archivos de registro necesarios se reproducen en todas las demás copias. El servicio de replicación, eliminará la copia de seguridad de los archivos de registro que tanto desde el activo y la copia del registro las rutas de acceso de archivo después de comprobar que los archivos de registro se han aplicado correctamente a la base de datos de la copia y ambas bases de datos activo y ha pasado el punto de control de copias de base de datos los archivos de registro que se va a eliminar.
  
## <a name="see-also"></a>Vea también

- [Los registros de transacciones y archivos de punto de comprobación de copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    


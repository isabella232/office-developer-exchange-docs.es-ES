---
title: Escritor de Exchange en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: Busque información sobre el escritor de Exchange en Exchange 2013 para operaciones de copia de seguridad y restauración.
ms.openlocfilehash: 44270a87c38b08d274d389fa6e46f3864da13ed2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452891"
---
# <a name="exchange-writer-in-exchange-2013"></a>Escritor de Exchange en Exchange 2013

Busque información sobre el escritor de Exchange en Exchange 2013 para operaciones de copia de seguridad y restauración. 
  
**Se aplica a:** Exchange Server 2013 
  
El escritor de Exchange es responsable de la copia de seguridad y restauración de las bases de datos activas de Exchange Server 2013. El escritor de Exchange también admite la funcionalidad de copia de seguridad para una base de datos seleccionada en la que se realiza la instantánea en la instancia replicada de los archivos de base de datos y de registro de transacciones. 
  
## <a name="overview-of-the-exchange-writer"></a>Información general del escritor de Exchange
<a name="bk_Overview"> </a>

Exchange 2013 incluye características de movilidad de bases de datos, lo que permite que las bases de datos se repliquen entre diferentes servidores de Exchange para mejorar la disponibilidad de la base de datos y la resistencia de sitios. Las demás copias de bases de datos de un grupo de disponibilidad de base de datos (DAG) proporcionan una oportunidad valiosa para que las copias de seguridad de Exchange usen los recursos adicionales que están disponibles en la ubicación de la copia. Además, dado que se realiza una copia de seguridad de la copia en lugar del patrón de base de datos activo, la copia puede no estar disponible durante el período de tiempo de la copia de seguridad durante un período más largo. 
  
El escritor de Exchange coordina los servicios de Exchange (que operan en nombre del solicitante) para preparar los archivos de base de datos para las copias de seguridad, inmovilizar la actividad de e/s resultante de las transacciones de Exchange antes de realizar copias de seguridad de la base de datos y, a continuación, liberar y truncar los archivos de registro una vez completada la copia de seguridad
  
Durante una restauración, la aplicación de copia de seguridad y restauración indica al escritor de Exchange que coordine con el almacén de Exchange (que opere en nombre del solicitante) para comprobar los destinos de restauración, cambiar el nombre del archivo de base de datos si es necesario y, a continuación, reproducir los registros de transacciones según sea necesario. El escritor de Exchange admite copias de seguridad y restauraciones.
  
El escritor de Exchange está disponible en cualquier servidor de Exchange que tenga instalado el rol de servidor buzón de correo. 
  
## <a name="exchange-writer-configuration-settings"></a>Opciones de configuración del escritor de Exchange
<a name="bk_ExchangeWriterConfig"> </a>

El escritor de Exchange para VSS usa una variedad de opciones de configuración y valores que se deben establecer correctamente y conservar durante las operaciones de copia de seguridad y restauración. Estas opciones de configuración se almacenan en el documento de metadatos del escritor de Exchange. Si la aplicación de copia de seguridad no conserva esta configuración, es posible que se produzcan errores inesperados al intentar realizar una copia de seguridad de las bases de datos de Exchange. 
  
En la siguiente tabla se enumeran las interfaces VSS que exponen metadatos sobre los componentes de la copia de seguridad de la base de datos. Estas interfaces son necesarias para obtener el documento de metadatos del escritor de Exchange que se usa para realizar una copia de seguridad del almacén de Exchange.
  
**Tabla 1. Interfaces VSS**

|**Interfaz de VSS**|**Descripción**|
|:-----|:-----|
|IVssWMComponent  <br/> |Permite el acceso a la información del componente almacenada en el escritor de Exchange.  <br/> |
|IVssExamineWriterMetadata  <br/> |Permite que la aplicación de copia de seguridad y restauración solicitada examine los metadatos del escritor de Exchange. El documento de metadatos del escritor de Exchange contiene valores y parámetros específicos de Exchange 2013 que la aplicación de copia de seguridad y restauración solicitada necesita para que pueda especificar correctamente los componentes adecuados para la copia de seguridad.  <br/> |
|IVssComponent  <br/> |Contiene métodos para examinar y modificar información sobre componentes contenidos en el documento de componentes de copia de seguridad de un solicitante. Los objetos solo se pueden obtener para los componentes que el método [IVssBackupComponents:: AddComponent](https://msdn.microsoft.com/library/windows/desktop/aa382646%28v=vs.85%29.aspx) agregó explícitamente a este documento.  <br/> |
|IVssBackupComponents  <br/> |Usada por la aplicación de copia de seguridad y restauración solicitada para sondear el escritor de Exchange sobre el estado de los archivos y ejecutar operaciones de copia de seguridad y restauración. El método [IVssBackupComponents:: SetBackupState](https://msdn.microsoft.com/library/windows/desktop/aa382833%28v=vs.85%29.aspx) define si la operación de copia de seguridad es una copia de seguridad completa, copia, incremental o diferencial. El método [IVssBackupComponents:: AddRestoreSubcomponent](https://msdn.microsoft.com/library/windows/desktop/aa382649%28v=vs.85%29.aspx) define los subcomponentes de una base de datos de Exchange 2013 que se puede seleccionar para una operación de restauración.  <br/> |
   
En el sistema de archivos de Windows Server, una base de datos de Exchange 2013 se almacena como un único archivo de base de datos con la extensión *. edb. El escritor de Exchange expone el archivo *. edb como el componente de base de datos, mientras que los registros de transacciones (*. log) y los archivos de punto de control (*. chk) se combinan en un único componente, al que se hace referencia como el componente de registro. Para obtener más información acerca de los archivos de base de datos de Exchange, vea [conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md).
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Interacciones entre el escritor de Exchange, los solicitantes de VSS y VSS
<a name="bk_interactions"> </a>

La interacción de alto nivel entre VSS, el escritor de Exchange y Exchange 2013 durante las operaciones de copia de seguridad es la siguiente:
  
1. El programa copia de seguridad (o el agente) se ejecuta un trabajo programado. 
    
2. El solicitante de VSS en la aplicación de copia de seguridad y restauración envía un comando a VSS para que realice una instantánea de las bases de datos de Exchange 2013 seleccionadas. 
    
3. VSS se comunica con el escritor de Exchange para preparar una copia de seguridad de instantáneas. Exchange 2013 prohíbe acciones administrativas en las bases de datos, comprueba las dependencias de volumen y suspende todas las operaciones de escritura en la instancia seleccionada de los archivos de base de datos y de registro de transacciones, a la vez que se permite el acceso de solo lectura. 
    
4. VSS se comunica con el proveedor de almacenamiento adecuado para crear una instantánea del volumen de almacenamiento que contiene las bases de datos de Exchange 2013. 
    
5. VSS libera Exchange 2013 para reanudar las operaciones ordinarias. 
    
6. El solicitante de VSS comprueba la coherencia física del conjunto de copia de seguridad antes de indicar que la copia de seguridad se realizó correctamente. Exchange 2013 trunca los registros de transacciones (si la base de datos forma parte de un DAG, el truncamiento de registros se replica entre todas las copias) y registra el tiempo de la última copia de seguridad de la base de datos.
    
VSS serializa la interacción de los solicitantes con el escritor de Exchange comenzando con el método [OnPrepareBackup](https://msdn.microsoft.com/library/windows/desktop/aa381571%28v=vs.85%29.aspx) y terminando con el método [OnPostSnapshot](https://msdn.microsoft.com/library/windows/desktop/aa381568%28v=vs.85%29.aspx) . Normalmente, la mayor parte del tiempo que dedica el escritor de Exchange a trabajar con la instantánea se produce después del método **OnPostSnapshot** , cuando se comprueba la coherencia de la instantánea antes de completar las copias de seguridad. El escritor de Exchange admite copias de seguridad en paralelo entre **OnPostSnapshot** y [OnBackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa381557%28v=vs.85%29.aspx).
  
Exchange 2013 no permite realizar copias de seguridad simultáneas de la misma base de datos. Solo se puede ejecutar un trabajo de copia de seguridad en una base de datos determinada al mismo tiempo. Cuando se ejecuta la copia de seguridad, el almacén de Exchange coloca la base de datos en un estado de copia de seguridad en curso. Este estado en memoria se borra al finalizar el proceso de copia de seguridad o cuando se reinicia el servicio. El estado en curso de la copia de seguridad en la memoria y sus datos asociados se pierden cuando se reinicia el servicio que hospeda el escritor de Exchange, cuando se reinicia el sistema operativo o cuando se produce una conmutación por error del clúster. Cualquiera de estos eventos hará que se produzca un error en el trabajo de copia de seguridad.
  
El truncamiento del archivo de registro de transacciones iniciada por una copia de seguridad se desencadena en función del tipo de copia de seguridad que se va a realizar. En las configuraciones que no sean DAG, el escritor de Exchange truncará los archivos de registro de transacciones al finalizar las copias de seguridad completas o incrementales correctas. En las configuraciones replicadas de DAG, el servicio de replicación retrasará el truncamiento de registros hasta que se reproduzcan todos los archivos de registro necesarios en todas las demás copias. El servicio de replicación eliminará los archivos de registro de los que se ha realizado una copia de seguridad de las rutas de acceso del archivo de registro activo y de la copia después de comprobar que los archivos de registro se han aplicado correctamente a la base de datos de copia, y que la base de datos activa y las copias de seguridad del punto de control han superado los archivos de registro.
  
## <a name="see-also"></a>Vea también

- [Registros de transacciones y archivos de controles para la copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    


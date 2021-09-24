---
title: Exchange escritor en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: Busque información sobre el escritor de Exchange en Exchange 2013 para operaciones de copia de seguridad y restauración.
ms.openlocfilehash: 7c50c2aa014308b05bdbc1acf0f2a91e33717ed6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516240"
---
# <a name="exchange-writer-in-exchange-2013"></a>Exchange escritor en Exchange 2013

Busque información sobre el escritor de Exchange en Exchange 2013 para operaciones de copia de seguridad y restauración. 
  
**Se aplica a:** Exchange Server 2013 
  
El Exchange es responsable de la copia de seguridad y restauración de las bases de datos Exchange Server 2013. El Exchange también admite la funcionalidad de copia de seguridad de una base de datos seleccionada donde se toma la instantánea en la instancia replicada de los archivos de registro de transacciones y base de datos. 
  
## <a name="overview-of-the-exchange-writer"></a>Información general sobre el Exchange escritor
<a name="bk_Overview"> </a>

Exchange 2013 incluye características de movilidad de bases de datos, que permiten replicar bases de datos entre diferentes servidores Exchange para mejorar la disponibilidad de la base de datos y la resistencia del sitio. Las otras copias de base de datos de un grupo de disponibilidad de base de datos (DAG) proporcionan una oportunidad valiosa para que Exchange copias de seguridad usen los recursos adicionales disponibles en la ubicación de copia. Además, dado que se hace una copia de seguridad de la copia en lugar del patrón de base de datos activo, la copia puede no estar disponible durante la copia de seguridad durante un período de tiempo más largo. 
  
El escritor de Exchange se coordina con los servicios de Exchange (que funcionan en nombre del solicitante) para preparar los archivos de base de datos para las copias de seguridad, inmovilizar la actividad de E/S resultante de transacciones Exchange antes de hacer una copia de seguridad de la base de datos y, a continuación, descongelar y truncar los archivos de registro una vez completada la copia de seguridad.
  
Durante una restauración, la aplicación de copia de seguridad y restauración indica al escritor de Exchange que coordine con el almacén de Exchange (que funciona en nombre del solicitante) para comprobar los destinos de restauración, cambiar el nombre del archivo de base de datos si es necesario y, a continuación, reproducir los registros de transacciones según sea necesario. El Exchange es compatible con copias de seguridad y restauraciones.
  
El Exchange está disponible en cualquier servidor Exchange que tenga instalado el rol de servidor Buzón de correo. 
  
## <a name="exchange-writer-configuration-settings"></a>Exchange de configuración del escritor
<a name="bk_ExchangeWriterConfig"> </a>

El Exchange para VSS usa una variedad de valores y configuraciones que deben establecerse correctamente y conservarse durante las operaciones de copia de seguridad y restauración. Estas opciones de configuración se almacenan en el Exchange de metadatos del escritor. Si la aplicación de copia de seguridad no conserva esta configuración, es posible que experimente errores inesperados al intentar realizar una copia de seguridad de las bases de datos Exchange copia de seguridad. 
  
En la tabla siguiente se enumeran las interfaces vss que exponen metadatos sobre los componentes de la copia de seguridad de la base de datos. Estas interfaces son necesarias para obtener el documento de metadatos Exchange escritor que se usa para realizar una copia de seguridad del Exchange almacén.
  
**Tabla 1. Interfaces vss**

|**Interfaz VSS**|**Descripción**|
|:-----|:-----|
|IVssWMComponent  <br/> |Permite el acceso a la información del componente almacenada en el Exchange escritor.  <br/> |
|IVssExamineWriterMetadata  <br/> |Permite que la aplicación de copia de seguridad y restauración solicitante examine los metadatos del Exchange escritor. El documento de metadatos del escritor de Exchange contiene Exchange valores y parámetros específicos de 2013 que requiere la aplicación de copia de seguridad y restauración para que pueda especificar correctamente los componentes adecuados para la copia de seguridad.  <br/> |
|IVssComponent  <br/> |Contiene métodos para examinar y modificar información sobre los componentes contenidos en el documento de componentes de copia de seguridad de un solicitante. Los objetos solo se pueden obtener para los componentes que se han agregado explícitamente a este documento mediante el método [IVssBackupComponents::AddComponent.](https://msdn.microsoft.com/library/windows/desktop/aa382646%28v=vs.85%29.aspx)  <br/> |
|IVssBackupComponents  <br/> |La aplicación que solicita copia de seguridad y restauración usa para sondear el Exchange sobre el estado del archivo y para ejecutar operaciones de copia de seguridad y restauración. El [método IVssBackupComponents::SetBackupState ](https://msdn.microsoft.com/library/windows/desktop/aa382833%28v=vs.85%29.aspx) define si la operación de copia de seguridad es una copia de seguridad completa, copia, incremental o diferencial. El [método IVssBackupComponents::AddRestoreSubcomponent](https://msdn.microsoft.com/library/windows/desktop/aa382649%28v=vs.85%29.aspx) define los subcomponentes de una base de datos de Exchange 2013 que se puede seleccionar para una operación de restauración.  <br/> |
   
En el Windows de archivos de Exchange 2013, se almacena una base de datos de Exchange como un único archivo de base de datos con una extensión *.edb. El escritor de Exchange expone *.edb** como componente de base de datos, mientras que los registros de transacciones ( .log) y los archivos de punto de control ( .chk) se combinan en un solo componente, denominado componente de registro. Para obtener más información acerca de Exchange de base de datos, vea Conceptos de copia de seguridad y restauración [para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md).
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Interacciones entre el escritor Exchange, VSS y los solicitantes vss
<a name="bk_interactions"> </a>

La interacción de alto nivel entre VSS, el escritor de Exchange y Exchange 2013 durante las operaciones de copia de seguridad es la siguiente:
  
1. El programa copia de seguridad (o el agente) se ejecuta un trabajo programado. 
    
2. El solicitante de VSS en la aplicación de copia de seguridad y restauración envía un comando a VSS para tomar una instantánea de las bases de datos Exchange 2013. 
    
3. VSS se comunica con el Exchange para preparar una copia de seguridad de instantáneas. Exchange 2013 prohíbe las acciones administrativas en las bases de datos, comprueba las dependencias de volumen y suspende todas las operaciones de escritura en la instancia seleccionada de la base de datos y los archivos de registro de transacciones, al tiempo que permite el acceso de solo lectura. 
    
4. VSS se comunica con el proveedor de almacenamiento adecuado para crear una instantánea del volumen de almacenamiento que contiene las bases de datos Exchange 2013. 
    
5. Vss releases Exchange 2013 to resume ordinary operations. 
    
6. El solicitante vss comprueba la coherencia física del conjunto de copia de seguridad antes de indicar que la copia de seguridad se ha realizado correctamente. Exchange 2013 trunca los registros de transacciones (si la base de datos forma parte de un DAG, el truncamiento de registros se replica entre todas las copias) y registra la hora de la última copia de seguridad de la base de datos.
    
VSS serializa la interacción de los solicitantes con el escritor Exchange a partir del método [OnPrepareBackup](https://msdn.microsoft.com/library/windows/desktop/aa381571%28v=vs.85%29.aspx) y terminando con el [método OnPostSnapshot.](https://msdn.microsoft.com/library/windows/desktop/aa381568%28v=vs.85%29.aspx) Normalmente, la mayor parte del tiempo que el escritor de Exchange pasa trabajando con la instantánea se produce después del método **OnPostSnapshot,** cuando se comprueba la coherencia de la instantánea antes de completar las copias de seguridad. El Exchange admite copias de seguridad paralelas **entre OnPostSnapshot** y [OnBackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa381557%28v=vs.85%29.aspx).
  
Exchange 2013 no permite copias de seguridad simultáneas de la misma base de datos. Solo se puede ejecutar un trabajo de copia de seguridad en una base de datos determinada a la vez. Cuando se ejecuta la copia de seguridad, el Exchange coloca la base de datos en un estado de copia de seguridad en curso. Este estado en la memoria se borra al finalizar el proceso de copia de seguridad o cuando se reinicia el servicio. El estado de copia de seguridad en curso en memoria y sus datos asociados se pierden cuando se reinicia el servicio que hospeda el escritor de Exchange, cuando se reinicia el sistema operativo o cuando se produce una conmutación por error del clúster. Cualquiera de estos eventos provocará un error en el trabajo de copia de seguridad.
  
El truncamiento del archivo de registro de transacciones iniciado por copia de seguridad se desencadena en función del tipo de copia de seguridad que se va a realizar. En las configuraciones que no son dag, el escritor de Exchange truncará los archivos de registro de transacciones al finalizar las copias de seguridad completas o incrementales correctas. En las configuraciones replicadas del DAG, el servicio de replicación retrasará el truncamiento de registros hasta que todos los archivos de registro necesarios se repropliquen en todas las demás copias. El servicio de replicación eliminará los archivos de registro de copia de seguridad de las rutas de acceso del archivo de registro activo y de copia después de comprobar que los archivos de registro se han aplicado correctamente a la base de datos de copia y tanto la base de datos activa como el punto de control de copias de base de datos han pasado los archivos de registro que se van a eliminar.
  
## <a name="see-also"></a>Ver también

- [Registros de transacciones y archivos de punto de control para copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    


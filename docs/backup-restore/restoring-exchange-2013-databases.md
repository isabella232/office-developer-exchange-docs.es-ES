---
title: Restauración de bases de datos de Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: Busque información sobre las distintas formas que puede restaurar las bases de datos de Exchange 2013.
ms.openlocfilehash: d3ca3a884b0ad30f7d7968a9ed435b02aaf205e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763007"
---
# <a name="restoring-exchange-2013-databases"></a>Restauración de bases de datos de Exchange 2013

Busque información sobre las distintas formas que puede restaurar las bases de datos de Exchange 2013. 
  
**Se aplica a:** Exchange Server 2013 
  
El escritor de Exchange que se incluye en Exchange que Server 2013 permite cierta flexibilidad en cómo restaurar las bases de datos de Exchange. Mediante el escritor de Exchange en Exchange 2013, puede restaurar las copias de seguridad de copia sombra en las ubicaciones siguientes:
  
- La base de datos original, independientemente de si se ha modificado la configuración de ruta de acceso de un archivo de registro base de datos o transacciones.
    
- Una base de datos de recuperación.
    
- Base de datos de cualquier producción, independientemente de si el nombre de base de datos para mostrar coincide con el nombre de un conjunto de copia de seguridad de VSS.
    
Cuando la aplicación de restauración restaura la información a la base de datos original, se deben restaurar los archivos de registro para la ruta de acceso del directorio especificado en los servicios de dominio de Active Directory (AD DS) para esa base de datos. Si la aplicación restaura una base de datos a una ubicación diferente, se deben restaurar los archivos de registro a una carpeta denominada **_restoredLogs** que se encuentra dentro del directorio de archivo de registro de base de datos. 
  
Al restaurar a un servidor o base de datos que es diferente de la base de datos original, la aplicación de restauración debe asegurarse de que las rutas de acceso del directorio de base de datos proporcionados a VSS coinciden con los de AD DS. Puede usar el cmdlet del Shell de administración de Exchange de [get-MailboxDatabase](http://technet.microsoft.com/en-us/library/bb124924%28v=exchg.150%29.aspx)para obtener información acerca de bases de datos existentes. Para obtener más información acerca de la consola de administración de Exchange, consulte [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
En la siguiente figura muestra la secuencia de eventos en una restauración típica de una base de datos de Exchange que se administra mediante el servicio de copia de instantáneas de volumen (VSS).
  
**En la figura 1. Secuencia de eventos para restaurar las bases de datos**

![Diagrama que muestra la secuencia de eventos del proceso de restauración. La secuencia comienza con el inicio de los almacenes de Exchange y continúa por los numerosos pasos entre el escritor de Exchange, VSS y la aplicación cliente.](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>Restauración de bases de datos de Exchange en la ubicación original
<a name="bk_OriginalLocation"> </a>

El escritor de Exchange permite que las aplicaciones restaurar las bases de datos y los archivos de registro de transacciones en sus ubicaciones originales en el servidor de Exchange. De forma predeterminada, el escritor de Exchange reproduce los archivos de registro de transacciones después de que el solicitante confirma que la restauración está completa durante la operación de [OnPostRestore](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381566%28v=vs.85%29.aspx) . La aplicación de restauración debe usar el método VSS [SetAdditionalRestores](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382829%28v=vs.85%29.aspx) para evitar que los archivos de registro reproducidos. Los archivos de registro se pueden reproducir en un momento posterior cuando el Administrador de Exchange o la aplicación vuelve a la base de datos restaurada. 
  
Al restaurar las bases de datos a su base de datos original objetos (que el GUID de destino en la base de datos coinciden con los del conjunto de copia de seguridad), pero a las rutas de acceso de archivo diferente, debe determinar las rutas de acceso de archivo actual y restaurar los archivos de copia de seguridad para la aplicación de la correspondientes rutas de acceso de archivo especificados en las propiedades de la base de datos. El solicitante debe llamar al método [AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para comunicarse con el escritor de Exchange la ubicación donde se restauran los archivos antes de que el escritor puede continuar con el resto del proceso de restauración. Si no se llama a **AddNewTarget** , el escritor de Exchange se da por supuesto que se restauran las copias de seguridad en las rutas de acceso de archivo especificados en el documento de metadatos de copia de seguridad. 
  
Normalmente, la aplicación no tiene que especificar una nueva ruta de acceso para las copias de seguridad que se realizan desde una copia de grupo de disponibilidad de base de datos (DAG). Los administradores de Exchange no cambie normalmente rutas de acceso de archivo de registro o base de datos. En una configuración de DAG, sin embargo, la aplicación de copia de seguridad deberían especificar la base de datos activo de registro y las rutas de acceso, debido a que las rutas de acceso de copia de DAG siempre son diferentes de las rutas de acceso.
  
Tenga en cuenta que Exchange 2013 no admite la restauración de copias de base de datos de DAG inactivos. DAG copias pueden restaurarse desde los datos de copia de seguridad sólo cuando se restaura la copia de la base de datos activa. Uso de diferentes conjuntos de datos de copia de seguridad o intentar restaurar un subconjunto de las copias de base de datos puede provocar se convierten en puede montar la base de datos. Las aplicaciones de copia de seguridad no es necesario llamar a la función de [SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx) en este caso, debido a que las copias de seguridad se restauran a los objetos de base de datos original que se crearon desde. Sin embargo, si la aplicación de copia de seguridad llama a **SetRestoreOptions** y el documento de metadatos XML tenga los parámetros correctos, el resultado no es un error. 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>Restauración de bases de datos de Exchange en una base de datos de recuperación
<a name="bk_RecoveryDatabase"> </a>

El escritor de Exchange permite restaurar datos directamente en una base de datos de recuperación. Los datos recuperados como una base de datos de recuperación de montaje permite al administrador de Exchange restaurar buzones individuales y elementos incluso individuales en un buzón de correo.
  
Si ya existe una base de datos de recuperación, la aplicación puede desmontar la base de datos, restaurar los datos en los archivos de registro y base de datos de recuperación y, a continuación, vuelva a montar la base de datos.
  
Cada servidor de Exchange 2013 permite sólo una base de datos de recuperación que va a montar a la vez. El servidor puede contener tantas bases de datos recuperadas como permita el espacio en disco, pero sólo uno se puede montar como la base de datos de recuperación. La base de datos montada como la base de datos de recuperación se cuenta el número máximo de bases de datos que se puede montar en un momento. Una base de datos recuperada montado como base de datos de recuperación de un servidor no está asociado con el buzón original en modo alguno.
  
Para recuperar una base de datos de recuperación, la aplicación debe llamar al método [SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx) y proporcionar un documento XML que indica el origen y los GUID de base de datos de destino. El GUID de origen debe coincidir con las del conjunto de copia de seguridad y el GUID de destino debe coincidir con las entradas de la base de datos de destino en AD DS. La aplicación de copia de seguridad también debe llamar al método [AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para especificar la ruta de acceso del directorio donde se restauran los archivos a. Si necesitan cambiar el nombre de los archivos de base de datos, el escritor de Exchange va a cambiar el nombre de la base de datos durante la operación de [OnPostRestore](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381566%28v=vs.85%29.aspx) . Exchange requiere que los archivos de registro de transacciones que desea restaurar en una subcarpeta ( **_restoredLogs**) en la ruta de acceso del archivo de registro de transacciones actual. Si se restauran los archivos de registro en cualquier otra ubicación, el escritor de Exchange devolverá un error. Dado que las bases de datos se monte como la base de datos de recuperación no se restauran a su ubicación original, que necesitan entra en estado de cierre limpio antes de que se pueden montar. De forma predeterminada, el escritor de Exchange llevará todas las bases de datos restauradas a un estado de cierre limpio durante post-restore. Si la aplicación de copia de seguridad llama al método [SetAdditionalRestores](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382829%28v=vs.85%29.aspx) , el escritor de Exchange no volverá a reproducir los archivos de registro y el administrador o la aplicación de copia de seguridad que se necesita para incorporar la base de datos en un estado de cierre limpio antes de montaje el base de datos. 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>Restauración de bases de datos de Exchange en un servidor de recuperación
<a name="bk_RecoveryServer"> </a>

En algunos casos, es posible que necesite recuperar una copia de seguridad establecida en otro servidor; Por ejemplo, es posible que necesite recuperarse de un error de servidor tras errores graves por traslado de la base de datos de buzones de correo a otro servidor de Exchange 2013 en la misma organización de Exchange o restaurar en un servidor dedicado fuera del entorno de producción para recuperar el buzón de correo y datos de carpetas públicas. 
  
En estos escenarios, las rutas de acceso de archivo de la base de datos de destino, así como su GUID de objeto son diferentes de los de la base de datos original. Por lo tanto, la aplicación tiene que llamar al método [SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx) con un documento XML que indica el origen y la información de la base de datos de destino y la llamada al método [AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para especificar las rutas de acceso de Active directory para restaurar los archivos de copia de seguridad para . Para el escritor de Exchange, esta restauración es la misma que la restauración de una base de datos de recuperación. Para obtener más información, vea [Exchange restaurar las bases de datos a una base de datos de recuperación](restoring-exchange-2013-databases.md#bk_RecoveryDatabase) anteriormente en este artículo. 
  
## <a name="see-also"></a>Ver también
<a name="bk_AdditionalResources"> </a>

- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Crear copia de seguridad y restauración de aplicaciones para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Referencia de clase CChkSGFiles](cchksgfiles-class-reference.md)
    


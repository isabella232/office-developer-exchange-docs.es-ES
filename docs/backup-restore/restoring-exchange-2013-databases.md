---
title: Restauración de Exchange bases de datos de 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: Encuentre información sobre las diferentes formas de restaurar las bases de datos Exchange 2013.
ms.openlocfilehash: 522128026bcbef893ce4909174d3fd9a95f1e8a9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513279"
---
# <a name="restoring-exchange-2013-databases"></a>Restauración de Exchange bases de datos de 2013

Encuentre información sobre las diferentes formas de restaurar las bases de datos Exchange 2013. 
  
**Se aplica a:** Exchange Server 2013 
  
El Exchange que se incluye en Exchange Server 2013 permite cierta flexibilidad en la forma de restaurar las bases Exchange datos. Mediante el escritor Exchange en Exchange 2013, puede restaurar las copias de seguridad de instantáneas en las siguientes ubicaciones:
  
- La base de datos original, independientemente de si se ha modificado la configuración de la ruta de acceso del archivo de registro de transacciones o de la base de datos.
    
- Una base de datos de recuperación.
    
- Cualquier base de datos de producción, independientemente de si el nombre para mostrar de la base de datos coincide con el nombre de un conjunto de copia de seguridad de VSS.
    
Cuando la aplicación de restauración restaura información en la base de datos original, los archivos de registro deben restaurarse en la ruta de acceso de directorio especificada en Servicios de dominio de Active Directory (AD DS) para esa base de datos. Si la aplicación restaura una base de datos en una ubicación diferente, los archivos de registro deben restaurarse en una carpeta denominada **_restoredLogs** que se encuentra dentro del directorio de archivos de registro de base de datos. 
  
Al restaurar en un servidor o base de datos que sea diferente de la base de datos original, la aplicación de restauración debe asegurarse de que las rutas de acceso de directorio de base de datos proporcionadas a VSS coincidan con las de AD DS. Puede usar el cmdlet [get-MailboxDatabase](https://technet.microsoft.com/library/bb124924%28v=exchg.150%29.aspx)Exchange Shell de administración para obtener información sobre bases de datos existentes. Para más información sobre el Shell de Administración de Exchange, consulte [Exchange Server PowerShell (Shell de Administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
En la siguiente figura se muestra la secuencia de eventos de una restauración típica de una base de datos Exchange que administra el Servicio de instantáneas de volumen (VSS).
  
**Figura 1. Secuencia de eventos para restaurar bases de datos**

![Diagrama que muestra la secuencia de eventos del proceso de restauración. La secuencia comienza con el inicio de los almacenes de Exchange y continúa por los numerosos pasos entre el escritor de Exchange, VSS y la aplicación cliente.](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>Restauración de Exchange bases de datos en la ubicación original
<a name="bk_OriginalLocation"> </a>

El Exchange permite a las aplicaciones restaurar bases de datos y archivos de registro de transacciones en sus ubicaciones originales en el Exchange servidor. De forma predeterminada, el Exchange reproduce los archivos de registro de transacciones después de que el solicitante confirme que la restauración se ha completado durante la operación [OnPostRestore.](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) La aplicación de restauración debe usar el método [SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) de VSS para evitar que se reproproguen los archivos de registro. Los archivos de registro se pueden reproducir más adelante cuando el administrador de Exchange o la aplicación vuelva a montar la base de datos restaurada. 
  
Al restaurar las bases de datos en sus objetos de base de datos originales (de forma que los GUID de destino de la base de datos coincidan con los del conjunto de copia de seguridad), pero en rutas de archivo diferentes, la aplicación debe determinar las rutas de acceso de archivo actuales y restaurar los archivos de copia de seguridad en las rutas de acceso de archivo correspondientes especificadas en las propiedades de la base de datos. El solicitante debe llamar al método [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para comunicar al escritor de Exchange la ubicación donde se restauran los archivos antes de que el escritor pueda continuar con el resto del proceso de restauración. Si no se llama a **AddNewTarget,** el escritor de Exchange supone que las copias de seguridad se restauran en las rutas de acceso de archivo especificadas en el documento de metadatos de copia de seguridad. 
  
Normalmente, la aplicación no tiene que especificar una nueva ruta de acceso para las copias de seguridad que se realizan desde una copia del Grupo de disponibilidad de base de datos (DAG). Exchange administradores no suelen cambiar las rutas de acceso de los archivos de registro o de base de datos. Sin embargo, en una configuración de DAG, es posible que la aplicación de copia de seguridad tenga que especificar las rutas de acceso de registro y la base de datos activas, ya que las rutas de acceso de copia de DAG siempre son diferentes de esas rutas de acceso.
  
Tenga en cuenta que Exchange 2013 no admite la restauración de copias de bases de datos de DAG inactivas. Las copias de DAG solo se pueden restaurar a partir de datos de copia de seguridad cuando se restaura la copia de base de datos activa. El uso de distintos conjuntos de datos de copia de seguridad o el intento de restaurar un subconjunto de las copias de base de datos puede hacer que la base de datos se pueda desmontar. Las aplicaciones de copia de seguridad no tienen que llamar a la [función SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) en este caso, ya que las copias de seguridad se restauran en los objetos de base de datos originales desde los que se crearon. Sin embargo, si la aplicación de copia de seguridad llama a **SetRestoreOptions** y el documento de metadatos XML tiene los parámetros correctos, el resultado no es un error. 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>Restauración de Exchange bases de datos en una base de datos de recuperación
<a name="bk_RecoveryDatabase"> </a>

El Exchange permite restaurar datos directamente en una base de datos de recuperación. El montaje de los datos recuperados como una base de datos de recuperación permite al administrador de Exchange restaurar buzones individuales e incluso elementos individuales en un buzón.
  
Si ya existe una base de datos de recuperación, la aplicación puede desmontar la base de datos, restaurar los datos en la base de datos de recuperación y los archivos de registro y, a continuación, volver a montar la base de datos.
  
Cada Exchange 2013 permite montar una sola base de datos de recuperación a la vez. El servidor puede contener tantas bases de datos recuperadas como el espacio en disco lo permita, pero solo se puede montar una como la base de datos de recuperación. La base de datos montada como base de datos de recuperación se cuenta en el número máximo de bases de datos que se pueden montar a la vez. Una base de datos recuperada montada como base de datos de recuperación de un servidor no está asociada al buzón original de ninguna manera.
  
Para recuperarse en una base de datos de recuperación, la aplicación debe llamar al método [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) y proporcionar un documento XML que indique los GUID de base de datos de origen y de destino. Los GUID de origen deben coincidir con los del conjunto de copia de seguridad y los GUID de destino deben coincidir con las entradas de la base de datos de destino en AD DS. La aplicación de copia de seguridad también debe llamar al [método AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para especificar la ruta de acceso del directorio en la que se restauran los archivos. Si es necesario cambiar el nombre de los archivos de base de datos, el Exchange cambiará el nombre de la base de datos durante la [operación OnPostRestore.](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) Exchange requiere que los archivos de registro de transacciones se restablezcan en una subcarpeta ( **_restoredLogs**) en la ruta de acceso del archivo de registro de transacciones actual. Si los archivos de registro se restauran en cualquier otra ubicación, Exchange escritor devolverá un error. Dado que las bases de datos que se están montando como la base de datos de recuperación no se restauran en su ubicación original, deben colocarse en estado de apagado limpio antes de poder montarse. De forma predeterminada, el Exchange de datos llevará todas las bases de datos restauradas a un estado de apagado limpio durante la restauración posterior a la restauración. Si la aplicación de copia de seguridad llama al método [SetAdditionalRestores,](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) el escritor de Exchange no reproducirá los archivos de registro y el administrador o la aplicación de copia de seguridad deben llevar la base de datos a un estado de apagado limpio antes de montar la base de datos. 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>Restauración de Exchange bases de datos en un servidor de recuperación
<a name="bk_RecoveryServer"> </a>

En algunos escenarios, es posible que deba recuperar un conjunto de copia de seguridad en otro servidor; Por ejemplo, es posible que necesite recuperarse de un error catastrófico del servidor mediante la porción de la base de datos de buzones de correo a otro servidor de Exchange 2013 de la misma organización de Exchange o restaurar en un servidor dedicado fuera del entorno de producción para recuperar los datos de buzones y carpetas públicas. 
  
En estos escenarios, las rutas de acceso de archivo de la base de datos de destino y sus GUID de objeto son diferentes de las de la base de datos original. Por lo tanto, la aplicación debe llamar al método [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) con un documento XML que indique la información de la base de datos de origen y de destino y llamar al método [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para especificar las rutas de acceso de directorio en las que restaurar los archivos de copia de seguridad. Para el Exchange, esta restauración es la misma que la restauración en una base de datos de recuperación. Para obtener más información, vea [Restoring Exchange databases to a recovery database](restoring-exchange-2013-databases.md#bk_RecoveryDatabase) earlier in this article. 
  
## <a name="see-also"></a>Ver también
<a name="bk_AdditionalResources"> </a>

- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Crear aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Referencia de la clase CChkSGFiles](cchksgfiles-class-reference.md)
    


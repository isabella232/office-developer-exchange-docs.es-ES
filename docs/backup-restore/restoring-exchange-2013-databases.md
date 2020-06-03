---
title: Restauración de bases de datos de Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: Busque información sobre las diferentes formas en que puede restaurar las bases de datos de Exchange 2013.
ms.openlocfilehash: 9fe417bda5dc728af619da02d62ada6e920f731d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528676"
---
# <a name="restoring-exchange-2013-databases"></a>Restauración de bases de datos de Exchange 2013

Busque información sobre las diferentes formas en que puede restaurar las bases de datos de Exchange 2013. 
  
**Se aplica a:** Exchange Server 2013 
  
El escritor de Exchange que se incluye en Exchange Server 2013 permite cierta flexibilidad en el modo de restaurar las bases de datos de Exchange. Mediante el uso del escritor de Exchange en Exchange 2013, puede restaurar las copias de seguridad de instantáneas en las siguientes ubicaciones:
  
- La base de datos original, independientemente de si se ha modificado la base de datos o la configuración de la ruta de acceso del archivo de registro de transacciones.
    
- Una base de datos de recuperación.
    
- Cualquier base de datos de producción, independientemente de si el nombre para mostrar de la base de datos coincide con el nombre de un conjunto de copia de seguridad de VSS.
    
Cuando la aplicación de restauración restaura la información en la base de datos original, los archivos de registro deben restaurarse en la ruta de acceso al directorio especificada en servicios de dominio de Active Directory (AD DS) para esa base de datos. Si la aplicación restaura una base de datos en una ubicación diferente, los archivos de registro deben restaurarse en una carpeta llamada **_restoredLogs** que se encuentra en el directorio del archivo de registro de la base de datos. 
  
Al restaurar en un servidor o una base de datos que sea diferente de la base de datos original, la aplicación de restauración debe asegurarse de que las rutas de directorio de base de datos proporcionadas a VSS coinciden con las de AD DS. Puede usar el cmdlet [Get-MailboxDatabase](https://technet.microsoft.com/library/bb124924%28v=exchg.150%29.aspx)de Shell de administración de Exchange para obtener información acerca de las bases de datos existentes. Para obtener más información acerca del shell de administración de Exchange, vea [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
En la siguiente figura se muestra la secuencia de eventos en una restauración típica de una base de datos de Exchange administrada por el servicio de instantáneas de volumen (VSS).
  
**Figura 1. Secuencia de eventos para restaurar bases de datos**

![Diagrama que muestra la secuencia de eventos del proceso de restauración. La secuencia comienza con el inicio de los almacenes de Exchange y continúa por los numerosos pasos entre el escritor de Exchange, VSS y la aplicación cliente.](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>Restauración de bases de datos de Exchange en la ubicación original
<a name="bk_OriginalLocation"> </a>

El escritor de Exchange permite a las aplicaciones restaurar bases de datos y archivos de registro de transacciones a sus ubicaciones originales en el servidor de Exchange. De forma predeterminada, el escritor de Exchange reproduce los archivos de registro de transacciones después de que el solicitante confirme que la restauración se ha completado durante la operación [OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) . La aplicación de restauración debe usar el método [SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) de VSS para evitar que se reproduzcan los archivos de registro. Los archivos de registro se pueden reproducir en un momento posterior cuando el administrador de Exchange o la aplicación vuelven a montar la base de datos restaurada. 
  
Al restaurar bases de datos en sus objetos de base de datos originales (de modo que los GUID de destino de la base de datos coinciden con los del conjunto de copia de seguridad) pero con distintas rutas de archivo, la aplicación debe determinar las rutas de archivo actuales y restaurar los archivos de copia de seguridad en las rutas de archivo correspondientes especificadas en las propiedades de la base de datos. El solicitante debe llamar al método [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para comunicarse con el escritor de Exchange la ubicación en la que se restauran los archivos antes de que el escritor pueda continuar con el resto del proceso de restauración. Si no se llama a **AddNewTarget** , el escritor de Exchange presupone que las copias de seguridad se restauran en las rutas de archivo especificadas en el documento de metadatos de copia de seguridad. 
  
Normalmente, la aplicación no tiene que especificar una nueva ruta de acceso para las copias de seguridad que se realizan desde una copia del grupo de disponibilidad de base de datos (DAG). Por lo general, los administradores de Exchange no cambian las rutas de la base de datos ni del archivo de registro. En una configuración de DAG, sin embargo, es posible que la aplicación de copia de seguridad tenga que especificar las rutas de acceso de registro y de base de datos activas, ya que las rutas de acceso de copia del DAG siempre son diferentes
  
Tenga en cuenta que Exchange 2013 no admite la restauración de copias de bases de datos de DAG inactivas. Las copias de DAG pueden restaurarse a partir de los datos de copia de seguridad solo cuando se restaura la copia de la base de datos activa. El uso de distintos conjuntos de datos de copia de seguridad o de intentar restaurar un subconjunto de las copias de la base de datos puede provocar que la base de datos no se pueda montar. Las aplicaciones de copia de seguridad no tienen que llamar a la función [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) en este caso, ya que las copias de seguridad se restauran en los objetos de base de datos originales desde los que se crearon. Sin embargo, si la aplicación de copia de seguridad llama a **SetRestoreOptions** y el documento de metadatos XML tiene los parámetros correctos, el resultado no es un error. 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>Restauración de bases de datos de Exchange en una base de datos de recuperación
<a name="bk_RecoveryDatabase"> </a>

El escritor de Exchange permite restaurar datos directamente en una base de datos de recuperación. El montaje de los datos recuperados como base de datos de recuperación permite al administrador de Exchange restaurar buzones individuales e incluso elementos individuales en un buzón.
  
Si ya existe una base de datos de recuperación, la aplicación puede desmontarla, restaurar los datos en la base de datos de recuperación y los archivos de registro y, a continuación, volver a montar la base de datos.
  
Cada servidor Exchange 2013 permite que solo se monte una base de datos de recuperación a la vez. El servidor puede contener tantas bases de datos recuperadas como permita el espacio en disco, pero solo se puede montar una como base de datos de recuperación. La base de datos montada como base de datos de recuperación se cuenta en el número máximo de bases de datos que se pueden montar a la vez. Una base de datos recuperada montada como base de datos de recuperación del servidor no está asociada con el buzón original de ninguna manera.
  
Para recuperar una base de datos de recuperación, la aplicación debe llamar al método [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) y proporcionar un documento XML que indique los GUID de la base de datos de origen y de destino. Los GUID de origen deben coincidir con los del conjunto de copia de seguridad y los GUID de destino deben coincidir con las entradas de la base de datos de destino en AD DS. La aplicación de copia de seguridad también debe llamar al método [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para especificar la ruta de acceso al directorio donde se restauran los archivos. Si es necesario cambiar el nombre de los archivos de base de datos, el escritor de Exchange cambiará el nombre de la base de datos durante la operación [OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) . Exchange requiere que los archivos de registro de transacciones se restauren en una subcarpeta ( **_restoredLogs**) en la ruta de acceso del archivo de registro de transacciones actual. Si los archivos de registro se restauran en cualquier otra ubicación, el escritor de Exchange devolverá un error. Debido a que las bases de datos que se montan como base de datos de recuperación no se restauran a su ubicación original, deben ponerse en el estado de cierre limpio antes de que se puedan montar. De forma predeterminada, el escritor de Exchange llevará todas las bases de datos restauradas a un estado de cierre limpio durante la restauración posterior. Si la aplicación de copia de seguridad llama al método [SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) , el escritor de Exchange no volverá a reproducir los archivos de registro, y el administrador o la aplicación de copia de seguridad deben poner la base de datos en un estado de cierre limpio antes de montar la base de datos. 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>Restauración de bases de datos de Exchange en un servidor de recuperación
<a name="bk_RecoveryServer"> </a>

En algunos escenarios, es posible que necesite recuperar un conjunto de copia de seguridad en otro servidor; Por ejemplo, es posible que deba recuperarse de un error catastrófico del servidor mediante la portabilidad de la base de datos de buzones a otro servidor Exchange 2013 de la misma organización de Exchange, o la restauración a un servidor dedicado fuera del entorno de producción para recuperar los datos de carpetas públicas y buzones de correo. 
  
En estos escenarios, las rutas de archivo de la base de datos de destino, así como sus GUID de objeto, son distintas de las de la base de datos original. Por lo tanto, la aplicación debe llamar al método [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) con un documento XML que indique la información de la base de datos de origen y de destino, y llamar al método [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) para especificar las rutas de directorio en las que se van a restaurar los archivos de copia de seguridad. Para el escritor de Exchange, esta restauración es la misma que la restauración en una base de datos de recuperación. Para obtener más información, vea restauración de bases de datos de [Exchange en una base de datos de recuperación](restoring-exchange-2013-databases.md#bk_RecoveryDatabase) anteriormente en este artículo. 
  
## <a name="see-also"></a>Vea también
<a name="bk_AdditionalResources"> </a>

- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Referencia de clase función cchksgfiles](cchksgfiles-class-reference.md)
    


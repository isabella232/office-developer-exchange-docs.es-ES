---
title: Tipos de operaciones de copia de seguridad para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: Encuentre información acerca de los distintos tipos de copias de seguridad se pueden realizar en el Exchange 2013 almacenar bases de datos, incluidos completa, copia, incremental y copias de seguridad diferenciales.
ms.openlocfilehash: 588bc0ffe896f286258006f7f123cf09d28b218c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763022"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a>Tipos de operaciones de copia de seguridad para Exchange 2013

Encuentre información acerca de los distintos tipos de copias de seguridad se pueden realizar en el Exchange 2013 almacenar bases de datos, incluidos completa, copia, incremental y copias de seguridad diferenciales.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se proporciona información acerca de los distintos tipos de copias de seguridad se pueden realizar en las bases de datos de Exchange Server 2013, y cómo afectan esas copias de seguridad a los archivos de base de datos. 
  
Copia de seguridad y restauración de las aplicaciones que usan el servicio de instantáneas de volumen (VSS) y el escritor de Exchange pueden realizar los tipos de copias de seguridad que aparecen en la siguiente tabla.
  
**La tabla 1. Tipos de operaciones de copia de seguridad**

|**Tipo de copia de seguridad**|**Descripción**|
|:-----|:-----|
|[Copias de seguridad completas](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |Realiza una copia de seguridad de las bases de datos (\*.edb), los registros de transacciones (\*. log), archivos de punto de comprobación (\*.chk) y, a continuación, se trunca los registros de transacciones de una base de datos específica.  <br/> |
|[Copiar las copias de seguridad](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |Realiza una copia de seguridad de la base de datos, registros de transacciones y archivos de punto de control. Copias de seguridad no truncan los registros de transacciones de la base de datos.  <br/> |
|[Copias de seguridad incrementales](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |Realiza una copia de los registros de transacciones para registrar los cambios desde la copia de seguridad por última vez completo o incremental y, a continuación, se trunca los registros de transacciones.  <br/> |
|[Copias de seguridad diferenciales](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |Realiza una copia de los registros de transacciones para registrar los cambios desde la copia de seguridad por última vez completo o incremental y no trunca los registros de transacciones.  <br/> |
   
Los componentes o archivos de base de datos, definidos por el escritor de Exchange representan los archivos de base de datos y los registros de transacciones dentro de las bases de datos de Exchange 2013. Esto permite que la aplicación de copia de seguridad y restauración mostrar los nombres de los componentes dentro de una base de datos de Exchange 2013 durante las operaciones de copia de seguridad. La aplicación de copia de seguridad no se puede realizar una copia de seguridad de componentes de base de datos individual, sin embargo; sólo puede hacer una copia seguridad de bases de datos de todo. 
  
El escritor de Exchange estandariza las rutas lógicas de componente base de datos, que se especifican en los metadatos del escritor de Exchange. El escritor de Exchange devuelve las rutas de acceso lógicas a la aplicación de copia de seguridad y restauración según sea necesario.
  
El escritor de Exchange proporciona lógicas rutas de acceso en el formulario: 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
Los componentes de servidor y base de datos son componentes del grupo de archivos, pero no tienen todos los archivos asociados. Tienen subcomponentes que especifican los archivos individuales. Una base de datos contiene sólo un componente de registro, denominado registros. Los nombres de componente de los componentes individuales de la base de datos son los GUID de las bases de datos, que se muestran como cadenas. 
  
El escritor de Exchange sólo enumera las bases de datos que se copia de seguridad pueden, basándose en directrices de marco de trabajo VSS. Las bases de datos que se montan la base de datos de recuperación de Exchange 2013, así como las bases de datos que no están montadas, no se puede realizar una copia y, por lo tanto, no aparecen en los metadatos del escritor de Exchange.
  
La siguiente ilustración muestra el escritor de Exchange proceso de copia de seguridad. 
  
**En la figura 1. Secuencia de eventos para el proceso de copia de seguridad**

![Diagrama que muestra la secuencia de eventos del proceso de copia de seguridad. La secuencia comienza con el inicio de los almacenes de Exchange y continúa por los numerosos pasos entre el escritor de Exchange, VSS y la aplicación cliente.](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>Copias de seguridad completas
<a name="bk_FullBackups"> </a>

Una copia de seguridad completa de una base de datos de Exchange implica crear y almacenar una copia del archivo de base de datos, los registros de transacciones y archivos de punto de control. Una base de datos de Exchange 2013 tiene un conjunto de archivos de registro de transacciones dedicado.
  
Una vez que ha sido una copia de seguridad de la base de datos, se truncan los archivos de registro de transacciones en el disco para que permanezcan sólo los cambios de base de datos que se ha producido una vez que se realizó la copia de seguridad. Durante este proceso, el escritor de Exchange elimina todas las entradas de registro hasta el punto de control, basado en la suposición de que las bases de datos ahora se copiaron en un estado coherente que contiene todos los cambios de seguridad para el punto de control más reciente. 
  
Si va a realizar una copia de la base de datos se desmonta durante la operación de copia de seguridad, Exchange 2013 no se truncarán los registros de transacciones y el resultado será el equivalente de una operación de copia de seguridad de copia, no una operación de copia de seguridad completa. 
  
Cuando se complete una copia de seguridad completa, los encabezados de la base de datos montada activo se actualizan con la información de copia de seguridad actual. En las implementaciones de replicada, esta información se compromete a un archivo de registro de transacciones y se replican en las demás copias DAG de la base de datos. Los encabezados de las copias de base de datos se actualizan como este archivo de registro de transacciones se reproduce en la copia de la base de datos.
  
Una copia de seguridad completa de sombra es necesario para poder ejecutar las copias de seguridad diferenciales o incrementales sombra. Las copias de seguridad completas pueden consultarse desde cualquier copia como es una instantánea de copia de seguridad.
  
Copias de seguridad completas se usan en los siguientes escenarios:
  
- Una base de datos se daña o se pierde, pero están intactos los archivos de registro de transacciones en el disco. En este escenario, los archivos de base de datos afectada pueden restaurar a partir de la copia de seguridad completa y, a continuación, recuperarse mediante la reproducción de los registros de transacciones que están todavía en disco. 
    
- Los archivos de registro de transacciones, así como el archivo de base de datos en el disco, se pierden. En este escenario, se restauran los archivos de registro de transacciones que se realizó la copia en el momento de la copia de seguridad completa junto con la base de datos.
    
En Exchange 2013, se puede restaurar registros sin tener que restaurar la base de datos aplicable a partir de un conjunto de copia de seguridad completa. Esta opción posibilita una copia de seguridad completa anterior que se restaurarán y se combinan con los archivos de registro de transacciones desde la copia de seguridad completa más reciente rehacer.
  
Cuando se establece la enumeración [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS a **VSS_BT_FULL** cuando el escritor de Exchange realiza una copia de seguridad, se incluyen los siguientes componentes en la copia de seguridad: 
  
- Una base de datos con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\> 
    
- Un archivo de registro con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\> 
    
## <a name="copy-backups"></a>Copiar las copias de seguridad
<a name="bk_CopyBackups"> </a>

Una copia de seguridad de una base de datos de Exchange implica la creación y almacenamiento de los mismos elementos que se incluyen en una copia de seguridad completa. Sin embargo, a diferencia de con una copia de seguridad completa, los archivos de registro de transacciones en el disco no se truncan cuando se haya completado la copia de seguridad. Copias de seguridad no están diseñados para fines de recuperación de datos. En su lugar, las copias de seguridad proporcionan una imagen de los datos para su uso en las pruebas de diagnóstico de problemas, o para la inicialización de una réplica.
  
Por ejemplo, un administrador de Exchange 2013 que está experimentando problemas con el almacén de Exchange puede realizar una copia copia de seguridad para su uso en un entorno de prueba sin que ello afecte al sistema de producción. Copias de seguridad no afectan a las programaciones de copia de seguridad regulares; Sin embargo, debido a que una copia de seguridad también pone el almacén de Exchange en un estado de copia de seguridad en curso, bloquea otras copias de seguridad programadas continúe hasta que la copia de seguridad se haya completado o cancelado. 
  
Cuando se establece la enumeración [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS en **VSS_BT_COPY**, se incluyen los siguientes componentes en una copia de seguridad: 
  
- Una base de datos con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\> 
    
- Un componente del archivo de registro con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\>
    
## <a name="incremental-backups"></a>Copias de seguridad incrementales
<a name="bk_IncrementalBackups"> </a>

Una copia de seguridad incremental de una base de datos de Exchange 2013 guarda los cambios realizados a la base de datos que se han producido desde la última copia de seguridad completa o incremental. Cuando se restauran todos los archivos de base de datos y los archivos de registro en el sistema, que se puede recuperar en el estado que se encontraban en el momento de la última copia de seguridad incremental. Los datos almacenados en una copia de seguridad incremental incluyen sólo los archivos de registro de transacciones hasta la hora actual. 
  
Una vez finalizada la copia de seguridad, el servidor de Exchange trunca los archivos de registro y marca el tiempo de copia de seguridad en los encabezados de la base de datos. Uso de una copia de seguridad incremental para recuperar una base de datos requiere al menos dos conjuntos de datos que desea restaurar: la última copia de seguridad completa y, a continuación, cada copia de seguridad incremental realizada después de la última completa de copia de seguridad. La ventaja de usar copias de seguridad incrementales es que las copias de seguridad individuales son mucho más pequeños que una copia de seguridad completa y copias de seguridad incrementales individuales son con frecuencia más pequeñas que las copias de seguridad diferenciales. 
  
La desventaja de utilizar copias de seguridad incrementales es que si se han realizado muchas copias de seguridad incrementales entre copias de seguridad completas, recuperación del almacén de Exchange puede implicar la recuperación de muchas copias de seguridad incrementales. Exchange no permite una copia de seguridad incremental que se produzca cuando no existe ninguna copia de seguridad completa anterior para establecer el punto de partida para los cambios incrementales. 
  
Una copia de seguridad completa realizada desde una ubicación de copia de DAG puede ir seguida de una copia de seguridad incremental de la ubicación activa y viceversa. Una restricción debe tener en cuenta es que el último estado de copia de seguridad se mantiene en el encabezado de la base de datos activa, y los cambios realizados en el encabezado de la base de datos se escriben en registros de transacciones, replicado y reproducir en la ubicación de la base de datos de copia al igual que todas las otras transacciones registros en las implementaciones de DAG. Debido a que las copias de seguridad y restauraciones interoperan, aplicaciones de copia de seguridad pueden proporcionar la funcionalidad para ejecutar las copias de seguridad exclusivamente en un nodo específico de DAG, independientemente de si el nodo está activo o pasivo, así como para ejecutar las copias de seguridad exclusivamente desde el nodo pasivo o exclusivamente desde el nodo activo.
  
Cuando se establece la enumeración [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS en **VSS_BT_INCREMENTAL**, se incluyen los siguientes componentes en una copia de seguridad incremental: 
  
- Una base de datos con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\> 
    
- Un archivo de registro con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\>
    
## <a name="differential-backups"></a>Copias de seguridad diferenciales
<a name="bk_DifferentialBackups"> </a>

Una copia de seguridad diferencial de una base de datos de Exchange 2013 guarda los cambios realizados a la base de datos que se han producido desde la última copia de seguridad completa o incremental. Cuando el sistema se restauran los archivos de base de datos y los archivos de registro, que se puede recuperar en el estado que se encontraban en la última copia de seguridad diferencial. 
  
Los datos almacenados en una copia de seguridad diferencial incluyen sólo los archivos de registro de transacciones hasta el punto de control actual. Copias de seguridad diferenciales no eliminar o cambiar los archivos de registro o cambiar los encabezados de la base de datos. Para usar una copia de seguridad diferencial para recuperar una base de datos, sólo necesita restaurar dos conjuntos de datos: la última copia de seguridad completa y, a continuación, en la copia de seguridad diferencial más reciente. 
  
La desventaja de utilizar copias de seguridad diferenciales es que las copias de seguridad diferenciales dupliquen la copia de seguridad de los datos en cada copia de seguridad hasta que se realiza una copia de seguridad completa. Si se toman muchas copias de seguridad diferenciales entre copias de seguridad completas, puede superar el espacio de almacenamiento necesario requiere el mismo número de copias de seguridad incrementales. Exchange no permite una copia de seguridad diferencial que se produzca cuando no ha habido una copia de seguridad completa o incremental para establecer el punto de partida para copias de seguridad diferenciales.
  
Una copia de seguridad completa realizada desde la ubicación de copia puede ir seguida de una copia de seguridad diferencial de la ubicación activa y viceversa. Una restricción debe tener en cuenta es que el último estado de copia de seguridad se mantiene en el encabezado de la base de datos activa, y los cambios realizados en el encabezado de la base de datos se escriben en registros de transacciones, replicado y reproducir en la ubicación de la base de datos de copia al igual que todas las otras transacciones registros en las implementaciones de DAG. Debido a que las copias de seguridad y restauraciones interoperan, aplicaciones de copia de seguridad proporcionan la funcionalidad para ejecutar todas las copias de seguridad exclusivamente en un nodo específico de DAG, independientemente de si el nodo está activo o pasivo, así como para ejecutar las copias de seguridad exclusivamente desde el nodo pasivo o exclusivamente desde el nodo activo.
  
Cuando se establece la enumeración [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS en **VSS_BT_DIFFERENTIAL**, se incluyen los siguientes componentes en una copia de seguridad diferencial: 
  
- Una base de datos con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\> 
    
- Un archivo de registro con la ruta de acceso lógica almacén de información de Exchange Server\Microsoft\\< nombre de servidor\>\\< GUID de base de datos\>
    
## <a name="see-also"></a>Vea también
<a name="bk_AdditionalResources"> </a>

- [Crear copia de seguridad y restauración de aplicaciones para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    
- [Validar la integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    


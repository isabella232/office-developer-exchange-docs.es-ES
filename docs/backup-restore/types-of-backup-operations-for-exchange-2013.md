---
title: Tipos de operaciones de copia de seguridad para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: Encuentre información sobre los distintos tipos de copias de seguridad que puede realizar en las bases de datos del almacén de Exchange 2013, incluidas las copias de seguridad completas, de copia, incrementales y diferenciales.
ms.openlocfilehash: 79fcdaa40409ee7cac4df44711c1551946b85ca1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520258"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a>Tipos de operaciones de copia de seguridad para Exchange 2013

Encuentre información sobre los distintos tipos de copias de seguridad que puede realizar en las bases de datos del almacén de Exchange 2013, incluidas las copias de seguridad completas, de copia, incrementales y diferenciales.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se proporciona información sobre los distintos tipos de copias de seguridad que puede realizar en las bases de datos de Exchange Server 2013 y cómo estas copias de seguridad afectan a los archivos de base de datos. 
  
Las aplicaciones de copia de seguridad y restauración que usan el Servicio de instantáneas de volumen (VSS) y el escritor de Exchange pueden realizar los tipos de copias de seguridad que se enumeran en la tabla siguiente.
  
**Tabla 1. Tipos de operaciones de copia de seguridad**

|**Tipo de copia de seguridad**|**Descripción**|
|:-----|:-----|
|[Copias de seguridad completas](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |Realiza una copia de seguridad de las bases de datos ( .edb), los registros de transacciones ( .log), los archivos de punto de \* \* control ( .chk) y, a continuación, trunca los registros de transacciones de \* una base de datos específica.  <br/> |
|[Copiar copias de seguridad](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |Copia de seguridad de la base de datos, los registros de transacciones y los archivos de punto de control. Las copias de seguridad de copia no truncan los registros de transacciones de la base de datos.  <br/> |
|[Copias de seguridad incrementales](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |Copia de seguridad de los registros de transacciones para registrar los cambios desde la última copia de seguridad completa o incremental y, a continuación, trunca los registros de transacciones.  <br/> |
|[Copias de seguridad diferenciales](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |Realiza una copia de seguridad de los registros de transacciones para registrar los cambios desde la última copia de seguridad completa o incremental y no trunca los registros de transacciones.  <br/> |
   
Los componentes o archivos de base de datos definidos por el escritor Exchange representan los archivos de base de datos y los registros de transacciones dentro de Exchange de 2013. Esto permite que la aplicación de copia de seguridad y restauración muestre los nombres de los componentes de una base de datos Exchange 2013 durante las operaciones de copia de seguridad. Sin embargo, la aplicación de copia de seguridad no puede hacer una copia de seguridad de componentes de base de datos individuales; solo puede hacer una copia de seguridad de bases de datos enteras. 
  
El Exchange escritor estandariza las rutas lógicas del componente de base de datos, que se especifican en los metadatos Exchange escritor. El Exchange devuelve las rutas lógicas a la aplicación de copia de seguridad y restauración según sea necesario.
  
El Exchange de escritura proporciona rutas lógicas con el formato: 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
Los componentes de servidor y base de datos son componentes de grupo de archivos, pero no tienen ningún archivo asociado. Tienen subcomponentes que especifican los archivos individuales. Una base de datos contiene solo un componente de registro, denominado Logs. Los nombres de componentes de los componentes de base de datos individuales son los GUID de las bases de datos, que se muestran como cadenas. 
  
El Exchange solo enumera las bases de datos que se pueden hacer una copia de seguridad, según las directrices del marco vss. Las bases de datos montadas como la base de datos de recuperación de Exchange 2013, así como las bases de datos que no están montadas, no se pueden realizar una copia de seguridad y, por lo tanto, no se enumeran en los metadatos del escritor de Exchange.
  
En la siguiente figura se muestra el Exchange de copia de seguridad del escritor. 
  
**Figura 1. Secuencia de eventos para el proceso de copia de seguridad**

![Diagrama que muestra la secuencia de eventos del proceso de copia de seguridad. La secuencia comienza con el inicio de los almacenes de Exchange y continúa por los numerosos pasos entre el escritor de Exchange, VSS y la aplicación cliente.](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>Copias de seguridad completas
<a name="bk_FullBackups"> </a>

Una copia de seguridad completa de una Exchange de datos implica crear y almacenar una copia del archivo de base de datos, los registros de transacciones y los archivos de punto de control. Una Exchange de 2013 tiene un conjunto de archivos de registro de transacciones dedicados.
  
Después de realizar una copia de seguridad de la base de datos, los archivos de registro de transacciones en el disco se truncan para que solo permanezcan los cambios en la base de datos que se produjeron después de realizar la copia de seguridad. Durante este proceso, el escritor de Exchange elimina todas las entradas de registro hasta el punto de control, en función de la suposición de que las bases de datos se han hecho una copia de seguridad en un estado coherente que contiene todos los cambios realizados hasta el punto de control más reciente. 
  
Si la base de datos que se está haciendo una copia de seguridad se desmonta durante la operación de copia de seguridad, Exchange 2013 no truncará los registros de transacciones y el resultado será el equivalente de una operación de copia de seguridad, no una operación de copia de seguridad completa. 
  
Cuando se completa una copia de seguridad completa, los encabezados de la base de datos montada activa se actualizan con la información de copia de seguridad actual. En implementaciones replicadas, esta información se confirma en un archivo de registro de transacciones y se replica en las otras copias de DAG de la base de datos. Los encabezados de las copias de base de datos se actualizan a medida que este archivo de registro de transacciones se reproduce en la copia de la base de datos.
  
Se requiere una copia de seguridad completa de instantáneas para ejecutar copias de seguridad incrementales o diferenciales de instantáneas. Las copias de seguridad completas se pueden realizar desde cualquier copia siempre que sea una copia de seguridad de instantáneas.
  
Las copias de seguridad completas se usan en los siguientes escenarios:
  
- Una base de datos se daña o se pierde, pero los archivos de registro de transacciones en el disco están intactos. En este escenario, los archivos de base de datos afectados se pueden restaurar a partir de la copia de seguridad completa y, a continuación, recuperarse reproduciendo los registros de transacciones que aún están en el disco. 
    
- Los archivos de registro de transacciones, así como el archivo de base de datos en el disco, se pierden. En este escenario, los archivos de registro de transacciones que se realizaron una copia de seguridad en el momento de la copia de seguridad completa se restauran junto con la base de datos.
    
En Exchange 2013, los registros se pueden restaurar sin tener que restaurar la base de datos aplicable desde un conjunto de copia de seguridad completo. Esta opción permite restaurar y combinar una copia de seguridad completa anterior con los archivos de registro de transacciones de la copia de seguridad completa más reciente.
  
Cuando la [enumeración VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS se establece en **VSS_BT_FULL** cuando el escritor de Exchange realiza una copia de seguridad, los siguientes componentes se incluyen en la copia de seguridad: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store<Nombre del \\ servidor<GUID de base de \> \\ datos\> 
    
- Un archivo de registro con la ruta de acceso lógica Exchange Server\Microsoft Information Store<Nombre del \\ servidor<GUID de base de \> \\ datos\> 
    
## <a name="copy-backups"></a>Copiar copias de seguridad
<a name="bk_CopyBackups"> </a>

Una copia de seguridad de una Exchange base de datos implica crear y almacenar los mismos elementos que se incluyen en una copia de seguridad completa. Sin embargo, a diferencia de una copia de seguridad completa, los archivos de registro de transacciones en el disco no se truncan cuando se completa la copia de seguridad. Las copias de seguridad de copia no están diseñadas para fines de recuperación de datos. En su lugar, las copias de seguridad de copia proporcionan una imagen de los datos para su uso en pruebas, diagnóstico de problemas o para la edación de una réplica.
  
Por ejemplo, un administrador de Exchange 2013 que tiene problemas con el almacén de Exchange puede realizar una copia de seguridad para su uso en un entorno de prueba sin afectar al sistema de producción. Las copias de seguridad de copia no afectan a las programaciones de copia de seguridad regulares; sin embargo, dado que una copia de seguridad también coloca el almacén de Exchange en un estado de copia de seguridad en curso, impide que otras copias de seguridad programadas avancen hasta que se complete o anule la copia de seguridad. 
  
Cuando la [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS se establece en **VSS_BT_COPY**, los siguientes componentes se incluyen en una copia de seguridad: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store<Nombre del \\ servidor<GUID de base de \> \\ datos\> 
    
- Un componente de archivo de registro con la ruta de acceso lógica Exchange Server\Microsoft Information Store<nombre de servidor \\<GUID de base de \> \\ datos\>
    
## <a name="incremental-backups"></a>Copias de seguridad incrementales
<a name="bk_IncrementalBackups"> </a>

Una copia de seguridad incremental de Exchange base de datos de 2013 guarda los cambios realizados en la base de datos desde la última copia de seguridad completa o incremental. Cuando todos los archivos de base de datos y los archivos de registro se restauran en el sistema, se pueden recuperar en el estado en el que se encontraban en el momento de la última copia de seguridad incremental. Los datos almacenados en una copia de seguridad incremental incluyen solo los archivos de registro de transacciones hasta la hora actual. 
  
Una vez completada la copia de seguridad, el servidor Exchange trunca los archivos de registro y marca el tiempo de copia de seguridad en los encabezados de la base de datos. El uso de una copia de seguridad incremental para recuperar una base de datos requiere al menos dos conjuntos de datos para restaurarse: la última copia de seguridad completa y, a continuación, todas las copias de seguridad incrementales realizadas después de la última copia de seguridad completa. La ventaja de usar copias de seguridad incrementales es que las copias de seguridad individuales son mucho más pequeñas que una copia de seguridad completa y las copias de seguridad incrementales individuales suelen ser más pequeñas que las copias de seguridad diferenciales. 
  
La desventaja de usar copias de seguridad incrementales es que si se realizaron muchas copias de seguridad incrementales entre copias de seguridad completas, la recuperación del almacén Exchange puede implicar la recuperación de muchas copias de seguridad incrementales. Exchange no permite que se produzca una copia de seguridad incremental cuando no existe ninguna copia de seguridad completa anterior para establecer el punto de partida de los cambios incrementales. 
  
Una copia de seguridad completa tomada desde una ubicación de copia del DAG puede ir seguida de una copia de seguridad incremental de la ubicación activa y viceversa. Una restricción que se debe tener en cuenta es que el último estado de copia de seguridad se mantiene en el encabezado de la base de datos activa y los cambios en el encabezado de la base de datos se escriben en los registros de transacciones, se replican y se reproducen en la ubicación de la base de datos de copia, al igual que todos los demás registros de transacciones en implementaciones de DAG. Dado que las copias de seguridad y restauraciones interoperan, las aplicaciones de copia de seguridad pueden proporcionar la funcionalidad de ejecutar copias de seguridad exclusivamente en un nodo de DAG específico, independientemente de si el nodo es activo o pasivo, así como para ejecutar copias de seguridad exclusivamente desde el nodo pasivo o exclusivamente desde el nodo activo.
  
Cuando la [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS se establece en **VSS_BT_INCREMENTAL**, los siguientes componentes se incluyen en una copia de seguridad incremental: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store<Nombre del \\ servidor<GUID de base de \> \\ datos\> 
    
- Un archivo de registro con la ruta de acceso lógica Exchange Server\Microsoft Information Store<Nombre del \\ servidor<GUID de base de \> \\ datos\>
    
## <a name="differential-backups"></a>Copias de seguridad diferenciales
<a name="bk_DifferentialBackups"> </a>

Una copia de seguridad diferencial de una Exchange base de datos de 2013 guarda los cambios realizados en la base de datos desde la última copia de seguridad completa o incremental. Cuando el sistema restaura los archivos de base de datos y los archivos de registro, se pueden recuperar en el estado en que se encontraban en la última copia de seguridad diferencial. 
  
Los datos almacenados en una copia de seguridad diferencial solo incluyen los archivos de registro de transacciones hasta el punto de control actual. Las copias de seguridad diferenciales no eliminan ni cambian los archivos de registro ni cambian los encabezados de la base de datos. Para usar una copia de seguridad diferencial para recuperar una base de datos, solo necesita restaurar dos conjuntos de datos: la última copia de seguridad completa y, a continuación, la copia de seguridad diferencial más reciente. 
  
La desventaja de usar copias de seguridad diferenciales es que las copias de seguridad diferenciales duplican los datos de copia de seguridad de cada copia de seguridad hasta que se realiza una copia de seguridad completa. Si se toman muchas copias de seguridad diferenciales entre copias de seguridad completas, el espacio de almacenamiento necesario puede superar el requerido por el mismo número de copias de seguridad incrementales. Exchange no permite que se produzca una copia de seguridad diferencial cuando no haya habido una copia de seguridad completa o incremental para establecer el punto de partida de las copias de seguridad diferenciales.
  
Una copia de seguridad completa tomada de la ubicación de copia puede ir seguida de una copia de seguridad diferencial de la ubicación activa y viceversa. Una restricción que se debe tener en cuenta es que el último estado de copia de seguridad se mantiene en el encabezado de la base de datos activa y los cambios en el encabezado de la base de datos se escriben en los registros de transacciones, se replican y se reproducen en la ubicación de la base de datos de copia, al igual que todos los demás registros de transacciones en implementaciones de DAG. Dado que las copias de seguridad y restauraciones interoperan, las aplicaciones de copia de seguridad proporcionan la funcionalidad para ejecutar todas las copias de seguridad exclusivamente en un nodo de DAG específico, independientemente de si el nodo está activo o pasivo, así como para ejecutar copias de seguridad exclusivamente desde el nodo pasivo o exclusivamente desde el nodo activo.
  
Cuando la [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) en VSS se establece en **VSS_BT_DIFFERENTIAL**, los siguientes componentes se incluyen en una copia de seguridad diferencial: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store<Nombre del \\ servidor<GUID de base de \> \\ datos\> 
    
- Un archivo de registro con la ruta de acceso lógica Exchange Server\Microsoft Information Store<Nombre del \\ servidor<GUID de base de \> \\ datos\>
    
## <a name="see-also"></a>Ver también
<a name="bk_AdditionalResources"> </a>

- [Crear aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Restauración de Exchange bases de datos de 2013](restoring-exchange-2013-databases.md)
    
- [Validar la integridad de copia de seguridad mediante la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Validar la integridad de copia de seguridad mediante la herramienta Eseutil en Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    


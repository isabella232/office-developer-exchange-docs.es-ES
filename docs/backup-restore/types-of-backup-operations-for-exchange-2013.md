---
title: Tipos de operaciones de copia de seguridad para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: Busque información sobre los diferentes tipos de copias de seguridad que puede realizar en las bases de datos de almacenamiento de Exchange 2013, incluidas las copias de seguridad completas, de copia, incrementales y diferenciales.
ms.openlocfilehash: dd07226acb3a3bb055e98f861a5c01375ee50dda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456291"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a>Tipos de operaciones de copia de seguridad para Exchange 2013

Busque información sobre los diferentes tipos de copias de seguridad que puede realizar en las bases de datos de almacenamiento de Exchange 2013, incluidas las copias de seguridad completas, de copia, incrementales y diferenciales.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se proporciona información acerca de los diferentes tipos de copias de seguridad que se pueden realizar en las bases de datos de Exchange Server 2013 y cómo afectan a los archivos de base de datos. 
  
Las aplicaciones de copia de seguridad y restauración que usan el servicio de instantáneas de volumen (VSS) y el escritor de Exchange pueden realizar los tipos de copias de seguridad que se enumeran en la tabla siguiente.
  
**Tabla 1. Tipos de operaciones de copia de seguridad**

|**Tipo de copia de seguridad**|**Descripción**|
|:-----|:-----|
|[Copias de seguridad completas](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |Realiza una copia de seguridad de las bases de datos ( \* . edb), los registros de transacciones ( \* . log), los archivos de punto de comprobación ( \* . chk) y, a continuación, trunca los registros de transacciones de una base de datos específica.  <br/> |
|[Copia de seguridad](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |Realiza una copia de seguridad de la base de datos, los registros de transacciones y los archivos de punto de control. Las copias de seguridad de copia no truncan los registros de transacciones de la base de datos.  <br/> |
|[Copias de seguridad incrementales](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |Realiza una copia de seguridad de los registros de transacciones para registrar los cambios desde la última copia de seguridad completa o incremental y, a continuación, trunca los registros de transacciones.  <br/> |
|[Copias de seguridad diferenciales](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |Realiza una copia de seguridad de los registros de transacciones para registrar los cambios desde la última copia de seguridad completa o incremental, y no trunca los registros de transacciones.  <br/> |
   
Los componentes o archivos de base de datos que define el escritor de Exchange representan los archivos de base de datos y los registros de transacciones dentro de las bases de datos de Exchange 2013. Esto permite que la aplicación de copia de seguridad y restauración muestre los nombres de los componentes dentro de una base de datos de Exchange 2013 durante las operaciones de copia de seguridad. La aplicación de copia de seguridad no puede realizar copias de seguridad de componentes de bases de datos individuales; solo puede hacer una copia de seguridad de las bases de datos completas. 
  
El escritor de Exchange estandariza las rutas lógicas del componente de base de datos, que se especifican en los metadatos del escritor de Exchange. El escritor de Exchange devuelve las rutas lógicas a la aplicación de copia de seguridad y restauración según sea necesario.
  
El escritor de Exchange proporciona rutas lógicas con el formato: 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
Los componentes de servidor y base de datos son componentes de grupo de archivos, pero no tienen archivos asociados. Tienen subcomponentes que especifican los archivos individuales. Una base de datos contiene sólo un componente de registro, denominado registros. Los nombres de componente de los componentes de base de datos individuales son los GUID de las bases de datos, mostrados como cadenas. 
  
El escritor de Exchange solo muestra las bases de datos de las que se puede hacer una copia de seguridad, en función de las instrucciones del marco VSS. No se puede realizar una copia de seguridad de las bases de datos que se montan como la base de datos de recuperación 2013 de Exchange, así como las bases de datos que no están montadas, y, por lo tanto, no se enumeran en los metadatos del escritor de Exchange.
  
La siguiente figura muestra el proceso de copia de seguridad del escritor de Exchange. 
  
**Figura 1. Secuencia de eventos para el proceso de copia de seguridad**

![Diagrama que muestra la secuencia de eventos del proceso de copia de seguridad. La secuencia comienza con el inicio de los almacenes de Exchange y continúa por los numerosos pasos entre el escritor de Exchange, VSS y la aplicación cliente.](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>Copias de seguridad completas
<a name="bk_FullBackups"> </a>

Una copia de seguridad completa de una base de datos de Exchange implica crear y almacenar una copia del archivo de base de datos, los registros de transacciones y los archivos de punto de control. Una base de datos de Exchange 2013 tiene un conjunto de archivos de registro de transacciones dedicado.
  
Una vez que se ha realizado la copia de seguridad de la base de datos, los archivos de registro de transacciones en el disco se truncan para que solo se mantengan los cambios que se realizaron después de la copia de seguridad. Durante este proceso, el escritor de Exchange elimina todas las entradas del registro hasta el punto de control, en función de la hipótesis de que se ha realizado una copia de seguridad de las bases de datos en un estado coherente que contiene todos los cambios hasta el punto de control más reciente. 
  
Si la base de datos a la que se hace la copia de seguridad se desmonta durante la operación de copia de seguridad, Exchange 2013 no truncará los registros de transacciones y el resultado será el equivalente a una operación de copia de seguridad de copia, no una operación de copia de seguridad completa. 
  
Cuando se completa una copia de seguridad completa, los encabezados de la base de datos montada activa se actualizan con la información de copia de seguridad actual. En las implementaciones replicadas, esta información se confirmará en un archivo de registro de transacciones y se replicará en las demás copias del DAG de la base de datos. Los encabezados de las copias de base de datos se actualizan a medida que este archivo de registro de transacciones se reproduce en la copia de la base de datos.
  
Se necesita una copia de seguridad de instantáneas completa para poder ejecutar copias de seguridad de instantáneas incrementales o diferenciales. Las copias de seguridad completas se pueden tomar a partir de cualquier copia, siempre que sea una copia de seguridad de instantáneas.
  
Las copias de seguridad completas se usan en las siguientes situaciones:
  
- Una base de datos se daña o se pierde, pero los archivos de registro de transacciones en el disco están intactos. En este escenario, los archivos de base de datos afectados pueden restaurarse a partir de la copia de seguridad completa y, a continuación, recuperarse mediante la reproducción de los registros de transacciones que todavía están en el disco. 
    
- Los archivos de registro de transacciones, así como el archivo de base de datos en el disco, se pierden. En este escenario, los archivos de registro de transacciones de los que se realizó una copia de seguridad en el momento de la copia de seguridad completa se restauran junto con la base de datos.
    
En Exchange 2013, los registros se pueden restaurar sin tener que restaurar la base de datos aplicable a partir de un conjunto de copia de seguridad completo. Esta opción permite que se restaure una copia de seguridad completa anterior y se combine con los archivos de registro de transacciones desde la copia de seguridad completa más reciente para aplicar el reenvío.
  
Cuando la enumeración [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) de VSS se establece en **VSS_BT_FULL** cuando el escritor de Exchange realiza una copia de seguridad, se incluyen los siguientes componentes en la copia de seguridad: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store \\<el nombre del servidor \> \\<GUID de la base de datos\> 
    
- Un archivo de registro con la ruta de acceso lógica Exchange Server\Microsoft Information Store \\<el nombre del servidor \> \\<GUID de la base de datos\> 
    
## <a name="copy-backups"></a>Copia de seguridad
<a name="bk_CopyBackups"> </a>

Una copia de seguridad de una copia de seguridad de una base de datos de Exchange implica crear y almacenar los mismos elementos que se incluyen en una copia de seguridad completa. Sin embargo, a diferencia de una copia de seguridad completa, los archivos de registro de transacciones en el disco no se truncan cuando se completa la copia de seguridad. Las copias de seguridad de copia no están diseñadas para fines de recuperación de datos. En su lugar, las copias de seguridad de copia proporcionan una imagen de los datos para su uso en pruebas, diagnóstico de problemas o para inicializar una réplica.
  
Por ejemplo, un administrador de Exchange 2013 que tiene problemas con el almacén de Exchange puede realizar una copia de seguridad de copia para usarla en un entorno de prueba sin afectar al sistema de producción. Las copias de seguridad de copia no afectan a las programaciones de copia de seguridad periódicas; sin embargo, puesto que una copia de seguridad de copia también pone el almacén de Exchange en un estado de copia de seguridad en curso, bloquea otras copias de seguridad programadas para que no se continúen hasta que la copia de seguridad de copia se haya completado o anulado. 
  
Cuando la enumeración [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) de VSS se establece en **VSS_BT_COPY**, se incluyen los siguientes componentes en una copia de seguridad de copia: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store \\<el nombre del servidor \> \\<GUID de la base de datos\> 
    
- Un componente de archivo de registro con la ruta lógica Exchange Server\Microsoft de información del \\ servidor<el nombre del servidor \> \\<GUID de la base de datos\>
    
## <a name="incremental-backups"></a>Copias de seguridad incrementales
<a name="bk_IncrementalBackups"> </a>

Una copia de seguridad incremental de una base de datos de Exchange 2013 guarda los cambios en la base de datos que se han producido desde la última copia de seguridad completa o incremental. Cuando todos los archivos de base de datos y los archivos de registro se restauran en el sistema, se pueden recuperar al estado en el que estaban en el momento de la última copia de seguridad incremental. Los datos almacenados en una copia de seguridad incremental incluyen sólo los archivos de registro de transacciones hasta la hora actual. 
  
Una vez completada la copia de seguridad, el servidor Exchange trunca los archivos de registro y marca la hora de la copia de seguridad en los encabezados de la base de datos. El uso de una copia de seguridad incremental para recuperar una base de datos requiere que se restauren al menos dos conjuntos de datos: la última copia de seguridad completa y todas las copias de seguridad incrementales realizadas después de la última copia de seguridad completa. La ventaja de usar copias de seguridad incrementales es que las copias de seguridad individuales son mucho más pequeñas que las copias de seguridad completas y las copias de seguridad incrementales individuales suelen ser más pequeñas que las diferenciales. 
  
La desventaja de usar copias de seguridad incrementales es que si se realizan muchas copias de seguridad incrementales entre copias de seguridad completas, la recuperación del almacén de Exchange puede implicar la recuperación de muchas copias de seguridad incrementales. Exchange no permite que se realice una copia de seguridad incremental cuando no existe ninguna copia de seguridad completa anterior para establecer el punto de inicio de los cambios incrementales. 
  
Una copia de seguridad completa realizada desde una ubicación de copia de DAG puede ir seguida de una copia de seguridad incremental de la ubicación activa y viceversa. Una restricción a tener en cuenta es que el último estado de copia de seguridad se mantiene en el encabezado de la base de datos activa, y los cambios en el encabezado de la base de datos se escriben en los registros de transacciones, se replican y reproducen en la ubicación de la base de datos de copia igual que todos los registros de transacciones de las implementaciones de DAG. Debido a que las copias de seguridad y restauraciones interoperan, las aplicaciones de copia de seguridad pueden proporcionar la funcionalidad necesaria para ejecutar copias de seguridad exclusivamente en un nodo DAG específico, independientemente de si el nodo está activo o pasivo, así como de ejecutar copias de seguridad exclusivamente desde el nodo pasivo o exclusivamente desde el nodo activo.
  
Cuando la enumeración [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) de VSS se establece en **VSS_BT_INCREMENTAL**, se incluyen los siguientes componentes en una copia de seguridad incremental: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store \\<el nombre del servidor \> \\<GUID de la base de datos\> 
    
- Un archivo de registro con la ruta de acceso lógica Exchange Server\Microsoft Information Store \\<el nombre del servidor \> \\<GUID de la base de datos\>
    
## <a name="differential-backups"></a>Copias de seguridad diferenciales
<a name="bk_DifferentialBackups"> </a>

Una copia de seguridad diferencial de una base de datos de Exchange 2013 guarda los cambios en la base de datos que se han producido desde la última copia de seguridad completa o incremental. Cuando el sistema restaura los archivos de base de datos y los archivos de registro, se pueden recuperar en el estado en que se encontraban en la última copia de seguridad diferencial. 
  
Los datos almacenados en una copia de seguridad diferencial incluyen sólo los archivos de registro de transacciones hasta el punto de comprobación actual. Las copias de seguridad diferenciales no eliminan ni cambian los archivos de registro ni cambian los encabezados de la base de datos. Para usar una copia de seguridad diferencial para recuperar una base de datos, sólo tiene que restaurar dos conjuntos de datos: la última copia de seguridad completa y la copia de seguridad diferencial más reciente. 
  
La desventaja de usar copias de seguridad diferenciales es que las copias de seguridad diferenciales duplican los datos de copia de seguridad en cada copia hasta que se realiza una copia de seguridad completa. Si se realizan varias copias de seguridad diferenciales entre las copias de seguridad completas, el espacio de almacenamiento necesario puede exceder el requerido por el mismo número de copias de seguridad incrementales. Exchange no permite que se realice una copia de seguridad diferencial cuando no ha habido una copia de seguridad completa o incremental para establecer el punto de inicio de las copias de seguridad diferenciales.
  
Una copia de seguridad completa realizada desde la ubicación de la copia puede ir seguida de una copia de seguridad diferencial desde la ubicación activa y viceversa. Una restricción a tener en cuenta es que el último estado de copia de seguridad se mantiene en el encabezado de la base de datos activa, y los cambios en el encabezado de la base de datos se escriben en los registros de transacciones, se replican y reproducen en la ubicación de la base de datos de copia igual que todos los registros de transacciones de las implementaciones de DAG. Como las copias de seguridad y restauraciones interoperables, las aplicaciones de copia de seguridad proporcionan la funcionalidad para ejecutar todas las copias de seguridad exclusivamente en un nodo DAG específico, independientemente de si el nodo está activo o pasivo, así como de ejecutar copias de seguridad exclusivamente desde el nodo pasivo o exclusivamente desde el nodo activo.
  
Cuando la enumeración [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) de VSS se establece en **VSS_BT_DIFFERENTIAL**, se incluyen los siguientes componentes en una copia de seguridad diferencial: 
  
- Una base de datos con la ruta de acceso lógica Exchange Server\Microsoft Information Store \\<el nombre del servidor \> \\<GUID de la base de datos\> 
    
- Un archivo de registro con la ruta de acceso lógica Exchange Server\Microsoft Information Store \\<el nombre del servidor \> \\<GUID de la base de datos\>
    
## <a name="see-also"></a>Vea también
<a name="bk_AdditionalResources"> </a>

- [Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    
- [Validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    


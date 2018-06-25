---
title: Conceptos de copia de seguridad y restauración para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: Obtenga información acerca de las bases de datos de Exchange que le ayudarán a crear la copia de seguridad y restauración de aplicaciones para Exchange 2013.
ms.openlocfilehash: 5fa62c3d34ffbe8f0bab852c6d41c49220e2883a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762983"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Conceptos de copia de seguridad y restauración para Exchange 2013

Obtenga información acerca de las bases de datos de Exchange que le ayudarán a crear la copia de seguridad y restauración de aplicaciones para Exchange 2013.
  
Antes de crear la copia de seguridad y restauración de aplicaciones para Exchange Server 2013, debe estar familiarizado con la estructura de archivos de base de datos de Exchange. Mediante el uso de los archivos de base de datos del almacén de Exchange, puede hacer una copia de seguridad de los datos en el almacén y restaurar en un momento posterior, según sea necesario. Si están limitados en el espacio de disco, el administrador podría implementar el registro circular y esto afectará a su capacidad para realizar una copia de seguridad de la base de datos. También puede aprovechar las ventajas de la característica de movilidad de la base de datos en Exchange 2013 para copia de seguridad y restaurar datos de Exchange. Movilidad de la base de datos, en combinación con la aplicación de copia de seguridad y restauración, es una buena medida de redundancia para la recuperación ante desastres.

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Archivos de base de datos de almacén de Exchange

Exchange 2013 incluye compatibilidad con bases de datos de hasta 100. Cada base de datos de Exchange 2013 contiene los archivos enumerados en la siguiente tabla. 
  
**La tabla 1. Archivos de base de datos de Exchange 2013**

|Tipo de archivo|Extensión|Descripción|
|:-----|:-----|:-----|
|Archivo de base de datos  <br/> |\*.edb  <br/> |Registra todos los cambios que se han confirmado en la base de datos en memoria.  <br/> |
|Secuencia de registro de transacciones  <br/> |\*.log  <br/> |Operaciones de registros, como la creación o modificación de un mensaje, que se confirman en la base de datos. Limitada en tamaño a 1 MB.  <br/> |
|Archivo de punto de comprobación  <br/> |\*.chk  <br/> |Se han escrito los registros que registran las transacciones a los archivos de base de datos en disco.  <br/> |
   
Exchange 2013 mantiene un único conjunto de archivos de registro de transacciones para cada base de datos. Los registros de transacciones son importantes para las operaciones de copia de seguridad y recuperación. Al crear una copia de seguridad y restauración de la aplicación que usa el servicio de instantáneas de volumen (VSS), debe asegurarse de que estos registros se controlan correctamente. Para obtener más información, vea [los registros de transacciones y archivos de punto de comprobación de copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md). Para realizar una copia de seguridad de una base de datos y la secuencia de registro, debe realizar copia de seguridad de todo el volumen que contiene la base de datos y los registros. Se producirá el truncamiento del registro sólo después de la finalización correcta de una copia de seguridad completa de un volumen o las carpetas que contienen una base de datos de Exchange.
  
En cada servidor de Exchange, puede montar sólo una base de datos de recuperación a la vez. Puede tener acceso a la base de datos de recuperación mediante el uso de los cmdlets del Shell de administración de Exchange como **New-MailboxRestoreRequest**. Para obtener más información acerca de las bases de datos de recuperación de Exchange, vea [Bases de datos de recuperación](http://technet.microsoft.com/en-us/library/dd876954%28v=exchg.150%29.aspx) en TechNet. Para obtener más información acerca de los cmdlets del Shell de administración de Exchange, consulte [Exchange 2013 Cmdlets](http://technet.microsoft.com/en-us/library/bb124413.aspx) en TechNet. 
  
## <a name="circular-logging"></a>Registro circular
<a name="bk_circularlogging"> </a>

Si la capacidad de almacenamiento es un problema, el administrador puede habilitar el registro circular. Cuando está habilitado el registro circular, Exchange escribe los registros de transacciones como de costumbre, pero cuando un archivo de punto de comprobación es avanzado, se trunca la parte inactiva del registro de transacciones. El administrador no debe configurar las bases de datos de Exchange 2013 para usar el registro circular si planea usar VSS para habilitar la copia de seguridad personalizado y operaciones de restauración. El registro circular crea las siguientes restricciones: 
  
- Si se habilita esta opción durante la operación de copia de seguridad o la operación de recuperación, no se puede restaurar las bases de datos individuales.
    
- Sólo las operaciones de tiempo de punto de recuperación son posibles. Cuando está habilitado el registro circular, puede eliminar los registros de transacciones en el mismo directorio cuando se restaura una base de datos, aunque estos registros pueden ser parte de una base de datos de Exchange 2013 diferente. 
    
- No se puede realizar operaciones de copia de seguridad diferenciales o incrementales. Para obtener más información acerca de estos tipos de copias de seguridad, vea [tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md).
    
Si habilita el registro circular es, el administrador debe deshabilitarlo tan pronto como sea posible para asegurarse de que las copias de seguridad VSS no producirá un error. Para obtener más información, consulte la entrada de blog [registro Circular de Exchange y copias de seguridad de VSS](http://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx). 
  
## <a name="exchange-database-mobility"></a>Movilidad de la base de datos de Exchange
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 permite la movilidad de la base de datos mejorar la disponibilidad y la confiabilidad de buzón de correo. Movilidad de la base de datos le permite realizar copias de la base de datos de almacén de Exchange, desconecte la base de datos del servidor y almacenar en otro servidor. En un grupo de disponibilidad para el base de datos (DAG) de 2013 de Exchange Server, varias copias de la base de datos se almacenan en equipos diferentes. Cuando una o más copias de la base de datos se pierden debido a hardware u otro error del sistema, información de las demás copias puede utilizarse para reinicializar la base de datos a través de operaciones de replicación normal.
  
Para las operaciones de copia de seguridad, si las bases de datos de Exchange 2013 que están realizar copias de seguridad están configurados en un DAG, la aplicación de copia de seguridad mejor para evitar interferencias entre la instantánea y el rendimiento del servidor activo, tomar la instantánea en uno de los inactivos copias de base de datos. Debido a que las copias de base de datos para la mayor parte están sincronizadas, la aplicación de copia de seguridad puede tomar instantáneas de diferentes copias de la base de datos y, más adelante se reconstruir desde las piezas.
  
Es el único método admitido de restauración de bases de datos de DAG partir de los datos de copia de seguridad restaurar todas las copias de la base de datos mediante el uso de los mismos datos de copia de seguridad. Debido a que los archivos de registro de la base de datos pueden ser ligeramente diferentes entre las copias, restaurar copias individuales de la base de datos con datos diferentes puede provocar se convierten en puede montar la base de datos.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Los registros de transacciones y archivos de punto de comprobación de copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Escritor de Exchange en Exchange 2013](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollo de Exchange y Exchange Online](../exchange-server-development.md) 
- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    


---
title: Conceptos de copia de seguridad y restauración para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: Encuentre información acerca de las bases de datos de Exchange que le ayudarán a crear las aplicaciones de copia de seguridad y restauración para Exchange 2013.
ms.openlocfilehash: fd35699839af105dd3fe285776b071c1d03d58dd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44437987"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Conceptos de copia de seguridad y restauración para Exchange 2013

Encuentre información acerca de las bases de datos de Exchange que le ayudarán a crear las aplicaciones de copia de seguridad y restauración para Exchange 2013.
  
Antes de crear aplicaciones de copia de seguridad y restauración para Exchange Server 2013, debe estar familiarizado con la estructura de archivos de base de datos de Exchange. Mediante el uso de los archivos de base de datos de almacén de Exchange, puede realizar una copia de seguridad de los datos de la tienda y restaurarlos posteriormente según sea necesario. Si el espacio en disco es limitado, el administrador puede implementar el registro circular y esto afectará a la capacidad de realizar una copia de seguridad de la base de datos. También puede aprovechar la característica de movilidad de base de datos de Exchange 2013 para realizar copias de seguridad y restaurar datos de Exchange. La movilidad de la base de datos, junto con la aplicación de copia de seguridad y restauración, es una buena medida de redundancia para la recuperación ante desastres.

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Archivos de base de datos de almacén de Exchange

Exchange 2013 incluye compatibilidad con hasta 100 bases de datos. Cada base de datos de Exchange 2013 contiene los archivos que se enumeran en la tabla siguiente. 
  
**Tabla 1. Archivos de base de datos de Exchange 2013**

|Tipo de archivo|Extensión|Descripción|
|:-----|:-----|:-----|
|Archivo de base de datos  <br/> |\*. edb  <br/> |Registra todos los cambios que se han confirmado en la base de datos en memoria.  <br/> |
|Secuencia de registro de transacciones  <br/> |\*. log  <br/> |Registra las operaciones, como la creación o modificación de un mensaje, que se confirmarán en la base de datos. Tiene un tamaño limitado de 1 MB cada uno.  <br/> |
|Archivo de punto de control  <br/> |\*. chk  <br/> |Registra qué transacciones registradas se han escrito en los archivos de la base de datos en el disco.  <br/> |
   
Exchange 2013 mantiene un único conjunto de archivos de registro de transacciones para cada base de datos. Los registros de transacciones son importantes para las operaciones de copia de seguridad y recuperación. Al crear una aplicación de copia de seguridad y restauración que usa el servicio de instantáneas de volumen (VSS), debe asegurarse de administrar estos registros correctamente. Para obtener más información, consulte [registros de transacciones y archivos de punto de control para copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md). Para hacer una copia de seguridad de una base de datos y su secuencia de registro, debe hacer una copia de seguridad de todo el volumen que contiene la base de datos y los registros. El truncamiento de registros solo se producirá después de que se complete correctamente una copia de seguridad completa de un volumen o carpetas que contengan una base de datos de Exchange.
  
En cada servidor de Exchange, solo puede montar una base de datos de recuperación a la vez. Puede tener acceso a la base de datos de recuperación con los cmdlets del shell de administración de Exchange, como **New-MailboxRestoreRequest**. Para obtener más información acerca de las bases de datos de recuperación de Exchange, vea [bases de datos de recuperación](https://technet.microsoft.com/library/dd876954%28v=exchg.150%29.aspx) en TechNet. Para obtener más información acerca de los cmdlets del shell de administración de Exchange, consulte [cmdlets de exchange 2013](https://technet.microsoft.com/library/bb124413.aspx) en TechNet. 
  
## <a name="circular-logging"></a>Registro circular
<a name="bk_circularlogging"> </a>

Si la capacidad de almacenamiento es un problema, el administrador puede habilitar el registro circular. Cuando el registro circular está habilitado, Exchange escribe los registros de transacciones de la manera habitual, pero cuando un archivo de punto de control es avanzado, se trunca la parte inactiva del registro de transacciones. El administrador no debe configurar las bases de datos de Exchange 2013 para que usen el registro circular si también va a usar VSS para habilitar las operaciones de copia de seguridad y restauración personalizadas. El registro circular crea las siguientes restricciones: 
  
- Si se habilita durante la operación de copia de seguridad o la operación de recuperación, no podrá restaurar bases de datos individuales.
    
- Solo son posibles las operaciones de recuperación de un momento dado. Cuando el registro circular está habilitado, puede eliminar los registros de transacciones en el mismo directorio cuando se restaura una base de datos, aunque dichos registros puedan formar parte de una base de datos de Exchange 2013 diferente. 
    
- No se pueden realizar operaciones de copia de seguridad diferenciales o incrementales. Para obtener más información acerca de estos tipos de copias de seguridad, vea [tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md).
    
Si el registro circular está habilitado, el administrador debe deshabilitarlo tan pronto como sea posible para asegurarse de que no se produzcan errores en las copias de seguridad de VSS. Para obtener más información, consulte el blog post [Exchange Logging and VSS backups](https://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx). 
  
## <a name="exchange-database-mobility"></a>Movilidad de base de datos de Exchange
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 permite la movilidad de bases de datos para mejorar la confiabilidad y la disponibilidad de los buzones. La movilidad de la base de datos permite realizar copias de la base de datos de almacén de Exchange, desconectar la base de datos del servidor y almacenarla en otro servidor. En un grupo de disponibilidad de base de datos de Exchange 2013 (DAG), se almacenan varias copias de la base de datos en equipos diferentes. Cuando se pierden una o varias copias de la base de datos debido a un error de hardware o de otro sistema, la información de las demás copias puede usarse para reinicializar la base de datos a través de operaciones de replicación normales.
  
Para las operaciones de copia de seguridad, si las bases de datos de Exchange 2013 de las que se va a realizar una copia de seguridad se configuran en un DAG, la aplicación de copia de seguridad puede evitar mejor la interferencia entre la instantánea y el rendimiento del servidor activo tomando la instantánea en una de las copias de base de datos inactivas. Debido a que las copias de la base de datos son para la mayoría de las partes sincronizadas, la aplicación de copia de seguridad puede tomar instantáneas de diferentes copias de la base de datos y volver a construyerlas a partir de las partes.
  
El único método admitido para restaurar las bases de datos de DAG a partir de los datos de copia de seguridad es restaurar todas las copias de la base de datos con los mismos datos de copia de seguridad. Debido a que los archivos de registro de la base de datos pueden ser ligeramente diferentes entre las copias, la restauración de las copias de bases de datos individuales con datos diferentes puede provocar que la base de datos no se pueda montar.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Registros de transacciones y archivos de controles para la copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Escritor de Exchange en Exchange 2013](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollo de Exchange y Exchange Online](../exchange-server-development.md) 
- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    


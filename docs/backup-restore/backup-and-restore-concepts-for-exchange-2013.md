---
title: Conceptos de copia de seguridad y restauración para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: Encuentre información sobre Exchange bases de datos que le ayudarán a crear las aplicaciones de copia de seguridad y restauración para Exchange 2013.
ms.openlocfilehash: c0b2e0269c3668779f980bf6984d84aff76573f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510528"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Conceptos de copia de seguridad y restauración para Exchange 2013

Encuentre información sobre Exchange bases de datos que le ayudarán a crear las aplicaciones de copia de seguridad y restauración para Exchange 2013.
  
Antes de crear aplicaciones de copia de seguridad y restauración para Exchange Server 2013, debe estar familiarizado con la estructura de archivos Exchange base de datos. Al usar los Exchange de base de datos del almacén, puede hacer una copia de seguridad de los datos en el almacén y restaurarlos más adelante según sea necesario. Si el espacio en disco es limitado, el administrador podría implementar el registro circular, lo que afectará a la capacidad de hacer una copia de seguridad de la base de datos. También puede aprovechar la característica de movilidad de bases de datos en Exchange 2013 para realizar copias de seguridad y restaurar Exchange datos. La movilidad de la base de datos, en combinación con la aplicación de copia de seguridad y restauración, es una buena medida de redundancia para la recuperación ante desastres.

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Exchange almacenar archivos de base de datos

Exchange 2013 incluye compatibilidad con hasta 100 bases de datos. Cada Exchange base de datos de 2013 contiene los archivos enumerados en la tabla siguiente. 
  
**Tabla 1. Exchange de base de datos de 2013**

|Tipo de archivo|Extensión|Descripción|
|:-----|:-----|:-----|
|Archivo de base de datos  <br/> |\*.edb  <br/> |Registra todos los cambios confirmados en la base de datos en memoria.  <br/> |
|Secuencia de registro de transacciones  <br/> |\*.log  <br/> |Registra operaciones, como la creación o modificación de un mensaje, que se confirman en la base de datos. Tamaño limitado a 1 MB cada uno.  <br/> |
|Archivo de punto de control  <br/> |\*.chk  <br/> |Registros que las transacciones registradas se han escrito en los archivos de base de datos en disco.  <br/> |
   
Exchange 2013 mantiene un único conjunto de archivos de registro de transacciones para cada base de datos. Los registros de transacciones son importantes para las operaciones de copia de seguridad y recuperación. Al crear una aplicación de copia de seguridad y restauración que usa el Servicio de instantáneas de volumen (VSS), debe asegurarse de que controla estos registros correctamente. Para obtener más información, vea Registros de transacciones y archivos de punto de control para copia de seguridad y restauración [en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md). Para realizar una copia de seguridad de una base de datos y su secuencia de registros, debe realizar una copia de seguridad de todo el volumen que contiene la base de datos y los registros. El truncamiento del registro se producirá solo después de completar correctamente una copia de seguridad completa de un volumen o carpetas que contienen una base Exchange datos.
  
En cada Exchange, solo puede montar una base de datos de recuperación a la vez. Puede obtener acceso a la base de datos de recuperación Exchange cmdlets del Shell de administración como **New-MailboxRestoreRequest**. Para obtener más información acerca de Exchange de recuperación, vea [Recovery Databases](https://technet.microsoft.com/library/dd876954%28v=exchg.150%29.aspx) on TechNet. Para obtener más información acerca Exchange cmdlets del Shell de administración, [vea Exchange cmdlets de 2013](https://technet.microsoft.com/library/bb124413.aspx) en TechNet. 
  
## <a name="circular-logging"></a>Registro circular
<a name="bk_circularlogging"> </a>

Si la capacidad de almacenamiento es un problema, el administrador podría habilitar el registro circular. Cuando se habilita el registro circular, Exchange los registros de transacciones como de costumbre, pero cuando se avanza un archivo de punto de control, se trunca la parte inactiva del registro de transacciones. El administrador no debe configurar Exchange bases de datos de 2013 para usar el registro circular si también tiene previsto usar VSS para habilitar las operaciones de copia de seguridad y restauración personalizadas. El registro circular crea las siguientes restricciones: 
  
- Si se habilita durante la operación de copia de seguridad o la operación de recuperación, no se pueden restaurar bases de datos individuales.
    
- Solo es posible realizar operaciones de recuperación en un momento dado. Cuando se habilita el registro circular, puede eliminar registros de transacciones en el mismo directorio cuando se restaura una base de datos, aunque esos registros pueden formar parte de una base de datos Exchange 2013. 
    
- No puede realizar operaciones de copia de seguridad incrementales o diferenciales. Para obtener más información acerca de estos tipos de copias de seguridad, vea Tipos de operaciones de copia de [seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md).
    
Si el registro circular está habilitado, el administrador debe deshabilitarlo lo antes posible para garantizar que las copias de seguridad de VSS no fallen. Para obtener más información, consulte la entrada de blog [Exchange Registro circular y copias de seguridad de VSS](https://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx). 
  
## <a name="exchange-database-mobility"></a>Exchange de base de datos
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 permite la movilidad de bases de datos para mejorar la disponibilidad y la confiabilidad del buzón. La movilidad de la base de datos permite realizar copias de la base de datos Exchange almacén, desconectar la base de datos del servidor y almacenarla en otro servidor. En un Exchange de disponibilidad de base de datos (DAG) de 2013, varias copias de la base de datos se almacenan en equipos diferentes. Cuando una o varias copias de la base de datos se pierden debido a un error de hardware u otro sistema, la información de las otras copias se puede usar para volver a sesar la base de datos mediante operaciones de replicación normales.
  
Para las operaciones de copia de seguridad, si las bases de datos de Exchange 2013 que se van a realizar una copia de seguridad están configuradas en un DAG, la aplicación de copia de seguridad puede evitar mejor las interferencias entre la instantánea y el rendimiento del servidor activo tomando la instantánea en una de las copias de base de datos inactivas. Dado que las copias de base de datos están sincronizadas en su mayor parte, la aplicación de copia de seguridad puede tomar instantáneas de diferentes copias de la base de datos y, posteriormente, reconstruirla a partir de las piezas.
  
El único método admitido para restaurar bases de datos de DAG a partir de datos de copia de seguridad es restaurar todas las copias de la base de datos mediante los mismos datos de copia de seguridad. Dado que los archivos de registro de la base de datos pueden ser ligeramente diferentes entre las copias, la restauración de copias de bases de datos individuales con datos diferentes puede hacer que la base de datos se pueda desmontar.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Registros de transacciones y archivos de punto de control para copia de seguridad y restauración en Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange escritor en Exchange 2013](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>Ver también

- [Desarrollo de Exchange y Exchange Online](../exchange-server-development.md) 
- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restauración de Exchange bases de datos de 2013](restoring-exchange-2013-databases.md)
    


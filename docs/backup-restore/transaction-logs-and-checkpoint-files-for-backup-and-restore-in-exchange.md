---
title: Los registros de transacciones y archivos de punto de comprobación de copia de seguridad y restauración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: Obtenga información acerca de los registros de transacciones y archivos de punto de control y cómo se usan para realizar una copia de y restaurar datos de Exchange 2013.
ms.openlocfilehash: 53f128348bb2e8895bc1eefaf62402fa348c81ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763004"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>Los registros de transacciones y archivos de punto de comprobación de copia de seguridad y restauración de Exchange

Obtenga información acerca de los registros de transacciones y archivos de punto de control y cómo se usan para realizar una copia de y restaurar datos de Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se describe cómo Exchange Server 2013 usa los registros de transacciones y archivos de punto de comprobación para ayudar a evitar la pérdida de datos. Es importante tener en cuenta esta información cuando desarrolle copia de seguridad y restaurar las aplicaciones que usan el servicio de instantáneas de volumen (VSS) en las versiones de Windows Server 2008 a partir de Windows Server.
  
## <a name="transaction-logs-in-exchange-2013"></a>Los registros de transacciones en Exchange 2013

Exchange 2013 mantiene un único conjunto de archivos de registro de transacciones para cada base de datos. Una transacción se define como cualquier operación que cambia el estado o el contenido de la base de datos. Los archivos de registro de transacciones para un registro de base de datos individual, todas las transacciones se realizan en la base de datos. Registros de las transacciones se escriben en los registros de transacciones antes de que se realizan en la base de datos, para asegurarse de que todas las transacciones confirmadas se pueden recuperar en caso de error de base de datos. Registros de transacciones de base de datos de Exchange 2013 se almacenan en el disco antes de que las transacciones se confirman en el archivo de base de datos. 
  
La grabación de las transacciones antes de que se actualice la base de datos se denomina registro de escritura anticipada. Para ayudar a garantizar que la base de datos correctamente vuelve al estado correcto, Exchange 2013 escribe los datos en los archivos de base de datos mediante el uso de los puntos de control y escrituras basada en la página. Durante las operaciones habituales, el almacén de Exchange en primer lugar los cambios de la base de datos de registros en los registros de transacciones y, a continuación, realiza los cambios en una copia en memoria de la base de datos. Los registros de transacciones registran del principio y del final de cada transacción. Esto garantiza que suficiente información está disponible más adelante deshacer o revertir las operaciones en la base de datos.
  
Durante la recuperación de errores en el que el archivo de base de datos en el disco está dañado, pero los registros de transacciones están intactos, la aplicación de restauración en primer lugar debe restaurar una copia del archivo de base de datos conocida.
  
El almacén de Exchange reproduce las transacciones de la transacción con copia de seguridad de los registros y, a continuación, reproduce las transacciones restantes desde los archivos de registro de transacciones en disco. Tenga en cuenta que a veces, las transacciones se pueden perder si el sistema se produce un error entre cuando las transacciones se registran en los registros de transacciones y cuando en realidad se escriben en los archivos de base de datos. 
  
Periódicamente, el almacén de Exchange comprueba la imagen de la base de datos en memoria y, a continuación, determina las páginas que han cambiado. El almacén de Exchange combina los cambios pendientes y, a continuación, escribe las páginas en el archivo de base de datos en el disco.
  
## <a name="checkpoint-files-in-exchange-2013"></a>Archivos de punto de comprobación en Exchange 2013

Se han escrito una registros del archivo de punto de comprobación que registran las transacciones a los archivos de base de datos en disco. El punto de comprobación es avanzado cuando todas las páginas de la base de datos que se han modificado las entradas de los registros de transacciones se escriben correctamente en el disco. Debido a que el archivo de punto de comprobación registra las transacciones que ya están en la imagen de la base de datos en disco, el almacén de Exchange sólo se necesita reproducir las transacciones que se realizaron después del punto de control. Según el período de tiempo entre las copias de seguridad, esto puede disminuir considerablemente el número de transacciones que se deben reproducir en la base de datos si se produce un error del sistema.
  
## <a name="see-also"></a>Ver también

- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    


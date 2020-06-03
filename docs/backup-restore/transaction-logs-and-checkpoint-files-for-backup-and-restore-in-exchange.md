---
title: Registros de transacciones y archivos de controles para la copia de seguridad y restauración en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: Obtenga información sobre los registros de transacciones y los archivos de punto de comprobación y cómo se usan para realizar copias de seguridad y restauraciones de datos de Exchange 2013.
ms.openlocfilehash: 5b01fc6924f82e76943795df877ae84b1fde087b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456391"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>Registros de transacciones y archivos de controles para la copia de seguridad y restauración en Exchange

Obtenga información sobre los registros de transacciones y los archivos de punto de comprobación y cómo se usan para realizar copias de seguridad y restauraciones de datos de Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se describe cómo Exchange Server 2013 usa registros de transacciones y archivos de controles para ayudar a evitar la pérdida de datos. Es importante tener en cuenta esta información al desarrollar aplicaciones de copia de seguridad y restauración que usan el servicio de instantáneas de volumen (VSS) en versiones de Windows Server que comienzan con Windows Server 2008.
  
## <a name="transaction-logs-in-exchange-2013"></a>Registros de transacciones en Exchange 2013

Exchange 2013 mantiene un único conjunto de archivos de registro de transacciones para cada base de datos. Una transacción se define como cualquier operación que cambie el estado o el contenido de la base de datos. Los archivos de registro de transacciones de una base de datos individual registran todas las transacciones realizadas en la base de datos. Los registros de las transacciones se escriben en los registros de transacciones antes de que se realicen en la base de datos, para asegurarse de que se pueden recuperar todas las transacciones confirmadas en caso de que se produzca un error en la base de datos. Los registros de transacciones de base de datos de Exchange 2013 se almacenan en el disco antes de que se confirmen en el archivo de base de datos. 
  
La grabación de las transacciones antes de que se actualice la base de datos se denomina registro de escritura anticipada. Para ayudar a garantizar que la base de datos vuelve correctamente al estado adecuado, Exchange 2013 escribe datos en los archivos de la base de datos mediante la escritura y los puntos de control basados en página. Durante las operaciones normales, el almacén de Exchange registra primero los cambios de la base de datos en los registros de transacciones y, a continuación, realiza los cambios en una copia en memoria de la base de datos. Los registros de transacciones registran el principio y el final de cada transacción. De este modo, se garantiza la disponibilidad de la información suficiente para las operaciones de deshacer o revertir más adelante en la base de datos.
  
Al recuperarse de los errores en los que el archivo de base de datos en disco está dañado, pero los registros de transacciones están intactos, la aplicación de restauración debe restaurar primero una copia en buen lugar del archivo de base de datos.
  
El almacén de Exchange reproduce las transacciones de los registros de transacciones a los que se ha realizado previamente una copia de seguridad y, a continuación, reproduce las transacciones restantes de los archivos de registro de transacciones en el disco. Tenga en cuenta que a veces se pueden perder las transacciones si se produce un error en el sistema entre el momento en que las transacciones se registran en los registros de transacciones y el momento en que se escriben realmente en los archivos de base de datos. 
  
Periódicamente, el almacén de Exchange comprueba la imagen de la base de datos en memoria y, a continuación, determina las páginas que han cambiado. El almacén de Exchange combina los cambios pendientes y, a continuación, escribe las páginas en el archivo de base de datos en el disco.
  
## <a name="checkpoint-files-in-exchange-2013"></a>Archivos de punto de comprobación en Exchange 2013

Un archivo de controles registra las transacciones registradas que se han escrito en los archivos de base de datos en el disco. El punto de control es avanzado cuando todas las páginas de base de datos que han sido modificadas por entradas en los registros de transacciones se escriben correctamente en el disco. Debido a que el archivo de controles registra qué transacciones ya están en la imagen de la base de datos en disco, el almacén de Exchange solo necesita reproducir las transacciones que se produjeron después del punto de control. En función del período de tiempo entre las copias de seguridad, se puede reducir en gran medida el número de transacciones que deben reproducirse en la base de datos si se produce un error en el sistema.
  
## <a name="see-also"></a>Vea también

- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    


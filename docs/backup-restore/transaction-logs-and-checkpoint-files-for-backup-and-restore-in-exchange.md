---
title: Registros de transacciones y archivos de punto de control para copia de seguridad y restauración en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: Busque información sobre los registros de transacciones y los archivos de punto de control y cómo se usan para realizar copias de seguridad y restaurar Exchange datos de 2013.
ms.openlocfilehash: ae47c7757a1001f28c467ea58ec87b4ddbc5a5c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513265"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>Registros de transacciones y archivos de punto de control para copia de seguridad y restauración en Exchange

Busque información sobre los registros de transacciones y los archivos de punto de control y cómo se usan para realizar copias de seguridad y restaurar Exchange datos de 2013.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se describe cómo Exchange Server 2013 usa registros de transacciones y archivos de punto de control para ayudar a evitar la pérdida de datos. Es importante tener en cuenta esta información al desarrollar aplicaciones de copia de seguridad y restauración que usan el Servicio de instantáneas de volumen (VSS) en versiones de Windows Server a partir de Windows Server 2008.
  
## <a name="transaction-logs-in-exchange-2013"></a>Registros de transacciones en Exchange 2013

Exchange 2013 mantiene un único conjunto de archivos de registro de transacciones para cada base de datos. Una transacción se define como cualquier operación que cambie el estado o el contenido de la base de datos. Los archivos de registro de transacciones de una base de datos individual registran todas las transacciones realizadas en la base de datos. Los registros de las transacciones se escriben en los registros de transacciones antes de realizarse en la propia base de datos, para garantizar que todas las transacciones confirmadas se puedan recuperar en caso de error en la base de datos. Exchange registros de transacciones de base de datos de 2013 se almacenan en el disco antes de que las transacciones se confirman en el archivo de base de datos. 
  
El registro de las transacciones antes de actualizar la base de datos se denomina registro de escritura previa. Para ayudar a garantizar que la base de datos vuelva al estado correcto, Exchange 2013 escribe datos en los archivos de base de datos mediante escrituras basadas en páginas y puntos de control. Durante las operaciones regulares, el Exchange primero registra los cambios de la base de datos en los registros de transacciones y, a continuación, realiza esos cambios en una copia en memoria de la base de datos. Los registros de transacciones registran el principio y el final de cada transacción. Esto garantiza que hay suficiente información disponible para deshacer o revertir operaciones posteriores en la base de datos.
  
Al recuperarse de errores en los que el archivo de base de datos del disco está dañado, pero los registros de transacciones están intactos, la aplicación de restauración primero debe restaurar una copia buena conocida del archivo de base de datos.
  
El Exchange reproduce las transacciones de los registros de transacciones de copia de seguridad anteriores y, a continuación, reproduce las transacciones restantes de los archivos de registro de transacciones en disco. Tenga en cuenta que a veces las transacciones pueden perderse si el sistema produce un error entre el momento en que las transacciones se registran en los registros de transacciones y cuando se escriben realmente en los archivos de base de datos. 
  
Periódicamente, el Exchange comprueba la imagen de base de datos en memoria y, a continuación, determina qué páginas han cambiado. El Exchange combina los cambios pendientes y, a continuación, escribe esas páginas en el archivo de base de datos en el disco.
  
## <a name="checkpoint-files-in-exchange-2013"></a>Archivos de punto de control Exchange 2013

Un archivo de punto de control registra las transacciones registradas que se han escrito en los archivos de base de datos en disco. El punto de control está avanzado cuando todas las páginas de base de datos modificadas por las entradas de los registros de transacciones se escriben correctamente en el disco. Dado que el archivo de punto de control registra las transacciones que ya están en la imagen de base de datos en disco, el almacén de Exchange solo necesita reproducir las transacciones que se produjeron después del punto de control. Según el período de tiempo entre las copias de seguridad, esto puede disminuir considerablemente el número de transacciones que deben reproducirse en la base de datos si se produce un error del sistema.
  
## <a name="see-also"></a>Ver también

- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restauración de Exchange bases de datos de 2013](restoring-exchange-2013-databases.md)
    


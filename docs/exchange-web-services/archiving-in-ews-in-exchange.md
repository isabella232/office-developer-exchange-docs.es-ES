---
title: Archivado en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Obtenga información sobre el archivado en EWS en Exchange.
ms.openlocfilehash: f2ca4cc783556b089b732c75d166b77c0dcd891c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520230"
---
# <a name="archiving-in-ews-in-exchange"></a>Archivado en EWS en Exchange

Obtenga información sobre el archivado en EWS en Exchange.
  
Los buzones de archivo son buzones secundarios asociados con un usuario. Los buzones de archivo se usan normalmente para administrar los límites de almacenamiento de correo electrónico. Por ejemplo, es posible que los elementos de correo electrónico más antiguos se puedan mover periódicamente de la Bandeja de entrada al buzón de archivo. 
  
Exchange Online, Exchange Online como parte de Office 365 y Exchange Server 2013 presentan dos nuevas operaciones de Exchange Web Services (EWS) que puede usar para archivar un conjunto de elementos de correo de un buzón principal. De este modo, los elementos de la Bandeja de entrada de archivado conservan la jerarquía de carpetas de los elementos. Además, los buzones de archivo ahora se pueden almacenar localmente en un cliente, o de forma remota, de una forma que sea principalmente opaca para un usuario, mediante una ruta de acceso de carpeta para apuntar al contenido del archivo.
  
## <a name="archiving-operations-in-ews"></a>Operaciones de archivado en EWS

En la tabla siguiente se enumeran las operaciones de archivado que se introdujeron en Exchange 2013. 
  
|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |Mueve un elemento del buzón principal al buzón de archivo.  <br/> |
|[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Crea un URI que apunta a la ubicación de almacenamiento del buzón de archivo.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


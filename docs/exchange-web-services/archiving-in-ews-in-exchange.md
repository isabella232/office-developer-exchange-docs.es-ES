---
title: Archivado en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Obtenga información sobre el archivado en EWS en Exchange.
ms.openlocfilehash: bc282a7774bb74e57550bc663512987839324b83
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762987"
---
# <a name="archiving-in-ews-in-exchange"></a>Archivado en EWS en Exchange

Obtenga información sobre el archivado en EWS en Exchange.
  
Buzones de archivo son buzones secundarios que están asociados con un usuario. Buzones de archivo se suelen usar para administrar los límites de almacenamiento de correo electrónico. Por ejemplo, los elementos de correo electrónico más antiguos es posible que periódicamente moverse desde la Bandeja de entrada para el buzón de archivo. 
  
Exchange Online, Exchange Online como parte de Office 365 y Exchange Server 2013 presentan dos nuevas operaciones de Exchange Web Services (EWS) que puede utilizar para archivar un conjunto de elementos de correo desde un buzón principal. Archivar los elementos de la Bandeja de entrada de este modo, conserva a la jerarquía de carpetas de los elementos. Además, ahora se pueden almacenar buzones de archivo localmente en un cliente, o de forma remota, de una manera que sea opaca a un usuario, principalmente mediante el uso de una ruta de acceso de carpeta para que apunte al contenido del archivo.
  
## <a name="archiving-operations-in-ews"></a>Las operaciones de EWS de archiving

En la siguiente tabla se enumera las operaciones de archivado que se introdujeron en Exchange 2013. 
  
|**Nombre de la operación**|**Descripción**|
|:-----|:-----|
|[ArchiveItem](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |Mueve un elemento desde el buzón principal para el buzón de archivo.  <br/> |
|[CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Crea un identificador URI que señala a la ubicación de almacenamiento para el buzón de archivo.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


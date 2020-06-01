---
title: Archivado en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Obtenga información sobre el archivado en EWS en Exchange.
ms.openlocfilehash: b433b9f88905ee255720e8b341d560fa0e464975
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456216"
---
# <a name="archiving-in-ews-in-exchange"></a>Archivado en EWS en Exchange

Obtenga información sobre el archivado en EWS en Exchange.
  
Los buzones de archivo son buzones secundarios que están asociados a un usuario. Los buzones de archivo se usan normalmente para administrar los límites de almacenamiento de correo electrónico. Por ejemplo, es posible que los elementos de correo electrónico antiguos se muevan periódicamente de la bandeja de entrada al buzón de archivo. 
  
Exchange Online, Exchange online como parte de Office 365 y Exchange Server 2013 introducen dos nuevas operaciones de servicios web Exchange (EWS) que puede usar para archivar un conjunto de elementos de correo desde un buzón principal. Archivar elementos de la bandeja de entrada de esta manera conserva la jerarquía de carpetas de los elementos. Además, los buzones de archivo ahora se pueden almacenar de forma local en un cliente, o de forma remota, de forma que sea prácticamente opaca para un usuario, mediante una ruta de acceso de carpeta que apunte al contenido del archivo.
  
## <a name="archiving-operations-in-ews"></a>Operaciones de archivado en EWS

En la siguiente tabla se enumeran las operaciones de archivado que se introdujeron en Exchange 2013. 
  
|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |Mueve un elemento del buzón de correo principal al buzón de archivo.  <br/> |
|[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Crea un URI que apunta a la ubicación de almacenamiento del buzón de archivo.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


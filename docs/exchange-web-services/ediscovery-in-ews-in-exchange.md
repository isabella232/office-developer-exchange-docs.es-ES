---
title: Exhibición de documentos electrónicos en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Obtenga información sobre la exhibición de documentos electrónicos en EWS en Exchange.
ms.openlocfilehash: 0b4f211e7f8a6ec085fd03ada1cc5a35187106e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512313"
---
# <a name="ediscovery-in-ews-in-exchange"></a>Exhibición de documentos electrónicos en EWS en Exchange

Obtenga información sobre la exhibición de documentos electrónicos en EWS en Exchange.
  
eDiscovery es un servicio web de consulta federada que permite a las aplicaciones externas realizar consultas de Exchange datos.
  
La detección consta de varias fases, incluida la identificación y conservación de datos clave, la selección y revisión de los datos y la producción de datos en los tribunales. Las consultas de exhibición de documentos electrónicos facilitan el proceso de detección proporcionando un único flujo de trabajo de detección en Exchange y SharePoint.
  
## <a name="ediscovery-operations"></a>Operaciones de exhibición de documentos electrónicos

La funcionalidad de exhibición de documentos electrónicos expuesta por EWS está disponible a través de operaciones introducidas en Exchange Online, Exchange Online como parte de Office 365 y versiones de Exchange a partir de Exchange 2013. 
  
**Tabla 1. Nuevas operaciones para eDiscovery**

|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |Obtiene información de configuración para las retenciones locales, las búsquedas de detección guardadas y los buzones habilitados para la búsqueda de detección.  <br/> |
|[GetHoldOnMailboxes](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |Obtiene el estado de una retención basada en consultas, que se establece mediante la [operación SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).  <br/> |
|[GetNonIndexableItemDetails](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |Recupera detalles sobre los elementos que no se pueden indizar. Esto incluye, pero no se limita a, el identificador del elemento, un código de error, una descripción del error, cuando se intentó indizar el elemento e información adicional sobre el archivo.  <br/> |
|[GetNonIndexableItemStatistics](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |Recupera el recuento de elementos que no se pueden indizar en un buzón.  <br/> |
|[GetSearchableMailboxes](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |Obtiene una lista de buzones en los que el cliente tiene permiso para buscar o realizar exhibición de documentos electrónicos.  <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |Busca elementos en buzones específicos que coincidan con palabras clave de consulta.  <br/> |
|[SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |Establece una retención basada en consultas en elementos.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


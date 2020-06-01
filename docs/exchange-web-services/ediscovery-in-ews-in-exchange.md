---
title: eDiscovery en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Obtenga información sobre eDiscovery en EWS en Exchange.
ms.openlocfilehash: 48e3fdb3a2f21f7dcfcb7eed21b586e099b249a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456097"
---
# <a name="ediscovery-in-ews-in-exchange"></a>eDiscovery en EWS en Exchange

Obtenga información sobre eDiscovery en EWS en Exchange.
  
eDiscovery es un servicio Web de consulta federada que permite a las aplicaciones externas realizar consultas de datos de Exchange.
  
La detección consta de varias fases, incluidas la identificación y conservación de datos clave, la selección y la revisión de los datos, y la generación de datos en el Tribunal. las consultas de exhibición de documentos electrónicos facilitan el proceso de detección al proporcionar un único flujo de trabajo de detección en Exchange y SharePoint.
  
## <a name="ediscovery-operations"></a>operaciones de eDiscovery

La funcionalidad de eDiscovery que expone EWS está disponible a través de operaciones incluidas en Exchange Online, Exchange online como parte de Office 365 y versiones de Exchange a partir de Exchange 2013. 
  
**Tabla 1. Nuevas operaciones para eDiscovery**

|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |Obtiene información de configuración para las suspensiones locales, las búsquedas de detección guardadas y los buzones que están habilitados para la búsqueda de detección.  <br/> |
|[GetHoldOnMailboxes](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |Obtiene el estado de una suspensión basada en consulta, que se establece mediante la [operación SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).  <br/> |
|[GetNonIndexableItemDetails](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |Recupera detalles sobre los elementos que no se pueden indizar. Esto incluye, entre otros, el identificador de elemento, un código de error, una descripción de error, cuando se realizó un intento de indizar el elemento e información adicional sobre el archivo.  <br/> |
|[GetNonIndexableItemStatistics](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |Recupera el recuento de elementos que no se pueden indizar en un buzón.  <br/> |
|[GetSearchableMailboxes](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |Obtiene una lista de buzones en los que el cliente tiene permiso para buscar o realizar la exhibición de documentos electrónicos en.  <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |Busca elementos en buzones específicos que coinciden con las palabras clave de consulta.  <br/> |
|[SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |Establece una retención basada en consultas en elementos.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


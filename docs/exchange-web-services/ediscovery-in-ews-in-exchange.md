---
title: exhibición de documentos electrónicos en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Obtenga información acerca de la exhibición de documentos electrónicos en EWS en Exchange.
ms.openlocfilehash: 6491fdd9f2246870a89bfa89bf7d97b972d67c92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762997"
---
# <a name="ediscovery-in-ews-in-exchange"></a>exhibición de documentos electrónicos en EWS en Exchange

Obtenga información acerca de la exhibición de documentos electrónicos en EWS en Exchange.
  
exhibición de documentos electrónicos es un servicio web de consulta federada que permite a las aplicaciones externas realizar consultas de datos de Exchange.
  
Detección consta de varias fases, incluida la identificación y preservar los datos clave, selección hacia abajo y revisar los datos y producir datos en Tribunal. las consultas de exhibición de documentos electrónicos facilitan el proceso de detección, ya que proporciona un flujo de trabajo de detección único a través de Exchange y SharePoint.
  
## <a name="ediscovery-operations"></a>operaciones de exhibición de documentos electrónicos

La funcionalidad de exhibición de documentos electrónicos expuestos por EWS está disponible a través de operaciones que se introdujo en Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013. 
  
**La tabla 1. Nuevas operaciones de exhibición de documentos electrónicos**

|**Nombre de la operación**|**Descripción**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |Obtiene la información de configuración de las suspensiones en contexto, guarda las búsquedas de detección y los buzones de correo que están habilitados para la búsqueda de detección.  <br/> |
|[GetHoldOnMailboxes](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |Obtiene el estado de una suspensión basada en consultas, que se establece mediante la [operación de SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).  <br/> |
|[GetNonIndexableItemDetails](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |Recupera los detalles acerca de los elementos que no se pueden indizar. Esto incluye, pero no se limita a, el identificador de elemento, un código de error, una descripción del error, cuando se ha intentado el elemento y obtener información adicional acerca del archivo de índice.  <br/> |
|[GetNonIndexableItemStatistics](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |Recupera el recuento de elementos que no se pueden indizar en un buzón de correo.  <br/> |
|[GetSearchableMailboxes](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |Obtiene una lista de buzones de correo que el cliente tiene permiso para buscar o realizar la exhibición de documentos electrónicos en.  <br/> |
|[SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |Busca elementos en los buzones de correo específicos que coinciden con palabras clave de consulta.  <br/> |
|[SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |Mantenga conjuntos basada en una consulta en los elementos.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


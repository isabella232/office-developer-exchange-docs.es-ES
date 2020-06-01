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
# <a name="ediscovery-in-ews-in-exchange"></a><span data-ttu-id="6d29f-103">eDiscovery en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6d29f-103">eDiscovery in EWS in Exchange</span></span>

<span data-ttu-id="6d29f-104">Obtenga información sobre eDiscovery en EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d29f-104">Learn about eDiscovery in EWS in Exchange.</span></span>
  
<span data-ttu-id="6d29f-105">eDiscovery es un servicio Web de consulta federada que permite a las aplicaciones externas realizar consultas de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d29f-105">eDiscovery is a federated query web service that enables external applications to perform queries of Exchange data.</span></span>
  
<span data-ttu-id="6d29f-106">La detección consta de varias fases, incluidas la identificación y conservación de datos clave, la selección y la revisión de los datos, y la generación de datos en el Tribunal.</span><span class="sxs-lookup"><span data-stu-id="6d29f-106">Discovery consists of several phases, including identifying and preserving key data, culling down and reviewing the data, and producing data in court.</span></span> <span data-ttu-id="6d29f-107">las consultas de exhibición de documentos electrónicos facilitan el proceso de detección al proporcionar un único flujo de trabajo de detección en Exchange y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6d29f-107">eDiscovery queries facilitate the discovery process by providing a single discovery workflow across Exchange and SharePoint.</span></span>
  
## <a name="ediscovery-operations"></a><span data-ttu-id="6d29f-108">operaciones de eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6d29f-108">eDiscovery operations</span></span>

<span data-ttu-id="6d29f-109">La funcionalidad de eDiscovery que expone EWS está disponible a través de operaciones incluidas en Exchange Online, Exchange online como parte de Office 365 y versiones de Exchange a partir de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="6d29f-109">The eDiscovery functionality that is exposed by EWS is available via operations introduced in Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013.</span></span> 
  
<span data-ttu-id="6d29f-110">**Tabla 1. Nuevas operaciones para eDiscovery**</span><span class="sxs-lookup"><span data-stu-id="6d29f-110">**Table 1. New operations for eDiscovery**</span></span>

|<span data-ttu-id="6d29f-111">**Nombre de operación**</span><span class="sxs-lookup"><span data-stu-id="6d29f-111">**Operation name**</span></span>|<span data-ttu-id="6d29f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d29f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d29f-113">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d29f-113">GetDiscoverySearchConfiguration</span></span>](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |<span data-ttu-id="6d29f-114">Obtiene información de configuración para las suspensiones locales, las búsquedas de detección guardadas y los buzones que están habilitados para la búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="6d29f-114">Gets configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span>  <br/> |
|[<span data-ttu-id="6d29f-115">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="6d29f-115">GetHoldOnMailboxes</span></span>](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |<span data-ttu-id="6d29f-116">Obtiene el estado de una suspensión basada en consulta, que se establece mediante la [operación SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d29f-116">Gets the status of a query-based hold, which is set by using the [SetHoldOnMailboxes operation](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).</span></span>  <br/> |
|[<span data-ttu-id="6d29f-117">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="6d29f-117">GetNonIndexableItemDetails</span></span>](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |<span data-ttu-id="6d29f-118">Recupera detalles sobre los elementos que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="6d29f-118">Retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="6d29f-119">Esto incluye, entre otros, el identificador de elemento, un código de error, una descripción de error, cuando se realizó un intento de indizar el elemento e información adicional sobre el archivo.</span><span class="sxs-lookup"><span data-stu-id="6d29f-119">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span>  <br/> |
|[<span data-ttu-id="6d29f-120">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="6d29f-120">GetNonIndexableItemStatistics</span></span>](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |<span data-ttu-id="6d29f-121">Recupera el recuento de elementos que no se pueden indizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="6d29f-121">Retrieves the count of items that cannot be indexed in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6d29f-122">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="6d29f-122">GetSearchableMailboxes</span></span>](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |<span data-ttu-id="6d29f-123">Obtiene una lista de buzones en los que el cliente tiene permiso para buscar o realizar la exhibición de documentos electrónicos en.</span><span class="sxs-lookup"><span data-stu-id="6d29f-123">Gets a list of mailboxes that the client has permission to search or perform eDiscovery on.</span></span>  <br/> |
|[<span data-ttu-id="6d29f-124">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="6d29f-124">SearchMailboxes</span></span>](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |<span data-ttu-id="6d29f-125">Busca elementos en buzones específicos que coinciden con las palabras clave de consulta.</span><span class="sxs-lookup"><span data-stu-id="6d29f-125">Searches for items in specific mailboxes that match query keywords.</span></span>  <br/> |
|[<span data-ttu-id="6d29f-126">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="6d29f-126">SetHoldOnMailboxes</span></span>](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |<span data-ttu-id="6d29f-127">Establece una retención basada en consultas en elementos.</span><span class="sxs-lookup"><span data-stu-id="6d29f-127">Sets a query-based hold on items.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d29f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d29f-128">See also</span></span>

- [<span data-ttu-id="6d29f-129">Desarrollar clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="6d29f-129">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="6d29f-130">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="6d29f-130">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="6d29f-131">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="6d29f-131">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    


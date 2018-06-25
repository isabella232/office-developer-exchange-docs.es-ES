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
# <a name="ediscovery-in-ews-in-exchange"></a><span data-ttu-id="2e31d-103">exhibición de documentos electrónicos en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e31d-103">eDiscovery in EWS in Exchange</span></span>

<span data-ttu-id="2e31d-104">Obtenga información acerca de la exhibición de documentos electrónicos en EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e31d-104">Learn about eDiscovery in EWS in Exchange.</span></span>
  
<span data-ttu-id="2e31d-105">exhibición de documentos electrónicos es un servicio web de consulta federada que permite a las aplicaciones externas realizar consultas de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e31d-105">eDiscovery is a federated query web service that enables external applications to perform queries of Exchange data.</span></span>
  
<span data-ttu-id="2e31d-106">Detección consta de varias fases, incluida la identificación y preservar los datos clave, selección hacia abajo y revisar los datos y producir datos en Tribunal.</span><span class="sxs-lookup"><span data-stu-id="2e31d-106">Discovery consists of several phases, including identifying and preserving key data, culling down and reviewing the data, and producing data in court.</span></span> <span data-ttu-id="2e31d-107">las consultas de exhibición de documentos electrónicos facilitan el proceso de detección, ya que proporciona un flujo de trabajo de detección único a través de Exchange y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2e31d-107">eDiscovery queries facilitate the discovery process by providing a single discovery workflow across Exchange and SharePoint.</span></span>
  
## <a name="ediscovery-operations"></a><span data-ttu-id="2e31d-108">operaciones de exhibición de documentos electrónicos</span><span class="sxs-lookup"><span data-stu-id="2e31d-108">eDiscovery operations</span></span>

<span data-ttu-id="2e31d-109">La funcionalidad de exhibición de documentos electrónicos expuestos por EWS está disponible a través de operaciones que se introdujo en Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="2e31d-109">The eDiscovery functionality that is exposed by EWS is available via operations introduced in Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013.</span></span> 
  
<span data-ttu-id="2e31d-110">**La tabla 1. Nuevas operaciones de exhibición de documentos electrónicos**</span><span class="sxs-lookup"><span data-stu-id="2e31d-110">**Table 1. New operations for eDiscovery**</span></span>

|<span data-ttu-id="2e31d-111">**Nombre de la operación**</span><span class="sxs-lookup"><span data-stu-id="2e31d-111">**Operation name**</span></span>|<span data-ttu-id="2e31d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e31d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e31d-113">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e31d-113">GetDiscoverySearchConfiguration</span></span>](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |<span data-ttu-id="2e31d-114">Obtiene la información de configuración de las suspensiones en contexto, guarda las búsquedas de detección y los buzones de correo que están habilitados para la búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="2e31d-114">Gets configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span>  <br/> |
|[<span data-ttu-id="2e31d-115">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2e31d-115">GetHoldOnMailboxes</span></span>](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |<span data-ttu-id="2e31d-116">Obtiene el estado de una suspensión basada en consultas, que se establece mediante la [operación de SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e31d-116">Gets the status of a query-based hold, which is set by using the [SetHoldOnMailboxes operation](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).</span></span>  <br/> |
|[<span data-ttu-id="2e31d-117">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="2e31d-117">GetNonIndexableItemDetails</span></span>](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |<span data-ttu-id="2e31d-118">Recupera los detalles acerca de los elementos que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="2e31d-118">Retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="2e31d-119">Esto incluye, pero no se limita a, el identificador de elemento, un código de error, una descripción del error, cuando se ha intentado el elemento y obtener información adicional acerca del archivo de índice.</span><span class="sxs-lookup"><span data-stu-id="2e31d-119">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span>  <br/> |
|[<span data-ttu-id="2e31d-120">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="2e31d-120">GetNonIndexableItemStatistics</span></span>](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |<span data-ttu-id="2e31d-121">Recupera el recuento de elementos que no se pueden indizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2e31d-121">Retrieves the count of items that cannot be indexed in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2e31d-122">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="2e31d-122">GetSearchableMailboxes</span></span>](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |<span data-ttu-id="2e31d-123">Obtiene una lista de buzones de correo que el cliente tiene permiso para buscar o realizar la exhibición de documentos electrónicos en.</span><span class="sxs-lookup"><span data-stu-id="2e31d-123">Gets a list of mailboxes that the client has permission to search or perform eDiscovery on.</span></span>  <br/> |
|[<span data-ttu-id="2e31d-124">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="2e31d-124">SearchMailboxes</span></span>](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |<span data-ttu-id="2e31d-125">Busca elementos en los buzones de correo específicos que coinciden con palabras clave de consulta.</span><span class="sxs-lookup"><span data-stu-id="2e31d-125">Searches for items in specific mailboxes that match query keywords.</span></span>  <br/> |
|[<span data-ttu-id="2e31d-126">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2e31d-126">SetHoldOnMailboxes</span></span>](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |<span data-ttu-id="2e31d-127">Mantenga conjuntos basada en una consulta en los elementos.</span><span class="sxs-lookup"><span data-stu-id="2e31d-127">Sets a query-based hold on items.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e31d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e31d-128">See also</span></span>

- [<span data-ttu-id="2e31d-129">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="2e31d-129">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="2e31d-130">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="2e31d-130">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="2e31d-131">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="2e31d-131">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    


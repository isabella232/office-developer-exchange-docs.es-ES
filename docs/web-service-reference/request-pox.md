---
title: Solicitud (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: El elemento de solicitud contiene la solicitud para el servicio Detección automática.
ms.openlocfilehash: ed6b0a80e83e160287f382a881dc5405bfb47a37
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837124"
---
# <a name="request-pox"></a><span data-ttu-id="9404d-103">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="9404d-103">Request (POX)</span></span>

<span data-ttu-id="9404d-104">El elemento de **solicitud** contiene la solicitud para el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="9404d-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
[<span data-ttu-id="9404d-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="9404d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="9404d-106">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="9404d-106">Request (POX)</span></span>](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9404d-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9404d-107">Attributes and elements</span></span>

<span data-ttu-id="9404d-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9404d-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9404d-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="9404d-109">Attributes</span></span>

<span data-ttu-id="9404d-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9404d-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9404d-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9404d-111">Child elements</span></span>

|<span data-ttu-id="9404d-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="9404d-112">**Element**</span></span>|<span data-ttu-id="9404d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9404d-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9404d-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="9404d-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="9404d-115">Identifica el esquema de una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="9404d-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="9404d-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="9404d-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="9404d-117">Identifica la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="9404d-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="9404d-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="9404d-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="9404d-119">Identifica el buzón de un usuario por su nombre distintivo (DN) heredado.</span><span class="sxs-lookup"><span data-stu-id="9404d-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9404d-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9404d-120">Parent elements</span></span>

|<span data-ttu-id="9404d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="9404d-121">**Element**</span></span>|<span data-ttu-id="9404d-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9404d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9404d-123">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="9404d-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="9404d-124">El elemento raíz en una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="9404d-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9404d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9404d-125">See also</span></span>



[<span data-ttu-id="9404d-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="9404d-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)


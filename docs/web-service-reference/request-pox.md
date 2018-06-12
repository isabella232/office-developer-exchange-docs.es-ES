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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837124"
---
# <a name="request-pox"></a><span data-ttu-id="fc2fe-103">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="fc2fe-103">Request (POX)</span></span>

<span data-ttu-id="fc2fe-104">El elemento de **solicitud** contiene la solicitud para el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="fc2fe-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
[<span data-ttu-id="fc2fe-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="fc2fe-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="fc2fe-106">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="fc2fe-106">Request (POX)</span></span>](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="fc2fe-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fc2fe-107">Attributes and elements</span></span>

<span data-ttu-id="fc2fe-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fc2fe-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc2fe-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc2fe-109">Attributes</span></span>

<span data-ttu-id="fc2fe-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fc2fe-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc2fe-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc2fe-111">Child elements</span></span>

|<span data-ttu-id="fc2fe-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc2fe-112">**Element**</span></span>|<span data-ttu-id="fc2fe-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc2fe-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc2fe-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="fc2fe-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="fc2fe-115">Identifica el esquema de una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="fc2fe-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="fc2fe-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="fc2fe-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="fc2fe-117">Identifica la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc2fe-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="fc2fe-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="fc2fe-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="fc2fe-119">Identifica el buzón de un usuario por su nombre distintivo (DN) heredado.</span><span class="sxs-lookup"><span data-stu-id="fc2fe-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fc2fe-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fc2fe-120">Parent elements</span></span>

|<span data-ttu-id="fc2fe-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc2fe-121">**Element**</span></span>|<span data-ttu-id="fc2fe-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc2fe-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc2fe-123">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="fc2fe-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="fc2fe-124">El elemento raíz en una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="fc2fe-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc2fe-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="fc2fe-125">See also</span></span>



[<span data-ttu-id="fc2fe-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="fc2fe-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)


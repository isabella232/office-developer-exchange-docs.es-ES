---
title: Request (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: El elemento de solicitud contiene la solicitud para el servicio Detección automática.
ms.openlocfilehash: 3f5d5258a92840fe79c4936370323b78aa4715b3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354431"
---
# <a name="request-pox"></a><span data-ttu-id="a779c-103">Request (POX)</span><span class="sxs-lookup"><span data-stu-id="a779c-103">Request (POX)</span></span>

<span data-ttu-id="a779c-104">El elemento de **solicitud** contiene la solicitud para el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="a779c-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="a779c-105">AutoDiscover (POX)</span><span class="sxs-lookup"><span data-stu-id="a779c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="a779c-106">Request (POX)</span><span class="sxs-lookup"><span data-stu-id="a779c-106">Request (POX)</span></span>](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

```xml
<Request>
   <AcceptableResponseSchema/> 
   <LegacyDN/>
</Request>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a779c-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a779c-107">Attributes and elements</span></span>

<span data-ttu-id="a779c-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a779c-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a779c-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="a779c-109">Attributes</span></span>

<span data-ttu-id="a779c-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a779c-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a779c-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a779c-111">Child elements</span></span>

|<span data-ttu-id="a779c-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="a779c-112">**Element**</span></span>|<span data-ttu-id="a779c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a779c-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a779c-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="a779c-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="a779c-115">Identifica el esquema de una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="a779c-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="a779c-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="a779c-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="a779c-117">Identifica la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="a779c-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="a779c-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="a779c-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="a779c-119">Identifica el buzón de un usuario por su nombre distintivo (DN) heredado.</span><span class="sxs-lookup"><span data-stu-id="a779c-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a779c-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a779c-120">Parent elements</span></span>

|<span data-ttu-id="a779c-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="a779c-121">**Element**</span></span>|<span data-ttu-id="a779c-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a779c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a779c-123">AutoDiscover (POX)</span><span class="sxs-lookup"><span data-stu-id="a779c-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="a779c-124">El elemento raíz en una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="a779c-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a779c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a779c-125">See also</span></span>

- [<span data-ttu-id="a779c-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="a779c-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)


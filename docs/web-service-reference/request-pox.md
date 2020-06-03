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
description: El elemento request contiene la solicitud al servicio Detección automática.
ms.openlocfilehash: bc215d614441ed8f12c0f1490f4abdbb7b574ad0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459549"
---
# <a name="request-pox"></a><span data-ttu-id="ee0d1-103">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-103">Request (POX)</span></span>

<span data-ttu-id="ee0d1-104">El elemento **request** contiene la solicitud al servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="ee0d1-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="ee0d1-106">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-106">Request (POX)</span></span>](request-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="ee0d1-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ee0d1-107">Attributes and elements</span></span>

<span data-ttu-id="ee0d1-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee0d1-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee0d1-109">Attributes</span></span>

<span data-ttu-id="ee0d1-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee0d1-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee0d1-111">Child elements</span></span>

|<span data-ttu-id="ee0d1-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ee0d1-112">**Element**</span></span>|<span data-ttu-id="ee0d1-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee0d1-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee0d1-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="ee0d1-115">Identifica el esquema para una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ee0d1-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="ee0d1-117">Identifica la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="ee0d1-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="ee0d1-119">Identifica el buzón de un usuario mediante el nombre distintivo heredado.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ee0d1-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ee0d1-120">Parent elements</span></span>

|<span data-ttu-id="ee0d1-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ee0d1-121">**Element**</span></span>|<span data-ttu-id="ee0d1-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee0d1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee0d1-123">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="ee0d1-124">El elemento raíz en una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee0d1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee0d1-125">See also</span></span>

- [<span data-ttu-id="ee0d1-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="ee0d1-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)


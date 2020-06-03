---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: El elemento LegacyDN identifica el buzón de un usuario mediante el nombre distintivo heredado.
ms.openlocfilehash: b9af4278a5421dc932573396c3563a64a78de41e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526385"
---
# <a name="legacydn-pox"></a><span data-ttu-id="3499c-103">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="3499c-103">LegacyDN (POX)</span></span>

<span data-ttu-id="3499c-104">El elemento **LegacyDN** identifica el buzón de un usuario mediante el nombre distintivo heredado.</span><span class="sxs-lookup"><span data-stu-id="3499c-104">The **LegacyDN** element identifies a user's mailbox by legacy distinguished name.</span></span> 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="3499c-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3499c-105">Attributes and elements</span></span>

<span data-ttu-id="3499c-106">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3499c-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3499c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3499c-107">Attributes</span></span>

<span data-ttu-id="3499c-108">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3499c-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3499c-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3499c-109">Child elements</span></span>

<span data-ttu-id="3499c-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3499c-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3499c-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3499c-111">Parent elements</span></span>

|<span data-ttu-id="3499c-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3499c-112">**Element**</span></span>|<span data-ttu-id="3499c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3499c-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3499c-114">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="3499c-114">Request (POX)</span></span>](request-pox.md) <br/> |<span data-ttu-id="3499c-115">Contiene la solicitud al servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="3499c-115">Contains the request to the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="3499c-116">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="3499c-116">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="3499c-117">Proporciona información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="3499c-117">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3499c-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3499c-118">Text value</span></span>

<span data-ttu-id="3499c-119">El valor de texto representa una dirección de correo electrónico heredada de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3499c-119">The text value represents a user's legacy e-mail address.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3499c-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3499c-120">Remarks</span></span>

<span data-ttu-id="3499c-121">El elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) es un elemento alternativo para una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="3499c-121">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is an alternative element for an Autodiscover request.</span></span> <span data-ttu-id="3499c-122">Se usa cuando existe un buzón de correo en un equipo que ejecuta Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3499c-122">It is used when a mailbox exists on a computer that is running Microsoft Exchange Server 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3499c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3499c-123">See also</span></span>

- [<span data-ttu-id="3499c-124">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="3499c-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)


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
description: El elemento LegacyDN identifica el buzón de un usuario por su nombre distintivo (DN) heredado.
ms.openlocfilehash: f7ec1dea29a7d3ad6d470ef7812390d179fe1d2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836243"
---
# <a name="legacydn-pox"></a><span data-ttu-id="4169d-103">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="4169d-103">LegacyDN (POX)</span></span>

<span data-ttu-id="4169d-104">El elemento **LegacyDN** identifica el buzón de un usuario por su nombre distintivo (DN) heredado.</span><span class="sxs-lookup"><span data-stu-id="4169d-104">The **LegacyDN** element identifies a user's mailbox by legacy distinguished name.</span></span> 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4169d-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4169d-105">Attributes and elements</span></span>

<span data-ttu-id="4169d-106">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4169d-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4169d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="4169d-107">Attributes</span></span>

<span data-ttu-id="4169d-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4169d-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4169d-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4169d-109">Child elements</span></span>

<span data-ttu-id="4169d-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4169d-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4169d-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4169d-111">Parent elements</span></span>

|<span data-ttu-id="4169d-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="4169d-112">**Element**</span></span>|<span data-ttu-id="4169d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4169d-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4169d-114">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="4169d-114">Request (POX)</span></span>](request-pox.md) <br/> |<span data-ttu-id="4169d-115">Contiene la solicitud para el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="4169d-115">Contains the request to the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="4169d-116">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="4169d-116">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="4169d-117">Proporciona información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="4169d-117">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4169d-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4169d-118">Text value</span></span>

<span data-ttu-id="4169d-119">El valor de texto representa la dirección de correo electrónico heredado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="4169d-119">The text value represents a user's legacy e-mail address.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4169d-120">Notas</span><span class="sxs-lookup"><span data-stu-id="4169d-120">Remarks</span></span>

<span data-ttu-id="4169d-121">El elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) es un elemento alternativo para una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="4169d-121">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is an alternative element for an Autodiscover request.</span></span> <span data-ttu-id="4169d-122">Se utiliza cuando existe un buzón de correo en un equipo que ejecuta Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="4169d-122">It is used when a mailbox exists on a computer that is running Microsoft Exchange Server 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4169d-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="4169d-123">See also</span></span>

- [<span data-ttu-id="4169d-124">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="4169d-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)


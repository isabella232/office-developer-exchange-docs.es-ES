---
title: Año
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Year
api_type:
- schema
ms.assetid: 93bf2847-53fa-496c-9a1e-dc9a9ffd0b9f
description: El elemento Year se usa para definir una zona horaria que cambia según el año. Este elemento es opcional. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 95d75f9c6166fc26e86534346fb07292a7fb3dcd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19841029"
---
# <a name="year"></a><span data-ttu-id="2f14d-105">Año</span><span class="sxs-lookup"><span data-stu-id="2f14d-105">Year</span></span>

<span data-ttu-id="2f14d-106">El elemento **Year** se usa para definir una zona horaria que cambia según el año.</span><span class="sxs-lookup"><span data-stu-id="2f14d-106">The **Year** element is used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="2f14d-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="2f14d-107">This element is optional.</span></span> <span data-ttu-id="2f14d-108">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2f14d-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Year/>
```

<span data-ttu-id="2f14d-109">**string**</span><span class="sxs-lookup"><span data-stu-id="2f14d-109">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2f14d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2f14d-110">Attributes and elements</span></span>

<span data-ttu-id="2f14d-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2f14d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f14d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f14d-112">Attributes</span></span>

<span data-ttu-id="2f14d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f14d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f14d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f14d-114">Child elements</span></span>

<span data-ttu-id="2f14d-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f14d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f14d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2f14d-116">Parent elements</span></span>

|<span data-ttu-id="2f14d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f14d-117">**Element**</span></span>|<span data-ttu-id="2f14d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f14d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f14d-119">StandardTime</span><span class="sxs-lookup"><span data-stu-id="2f14d-119">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="2f14d-120">Representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC) que está representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="2f14d-120">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span>  <br/> |
|[<span data-ttu-id="2f14d-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="2f14d-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="2f14d-122">Representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC) que está representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2f14d-122">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f14d-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2f14d-123">Text value</span></span>

<span data-ttu-id="2f14d-124">El elemento Year acepta una cadena que representa un año.</span><span class="sxs-lookup"><span data-stu-id="2f14d-124">The Year element accepts a string that represents a year.</span></span> <span data-ttu-id="2f14d-125">El formato de año es aaaa.</span><span class="sxs-lookup"><span data-stu-id="2f14d-125">The year format is YYYY.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f14d-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f14d-126">Remarks</span></span>

<span data-ttu-id="2f14d-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2f14d-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f14d-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2f14d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f14d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2f14d-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f14d-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2f14d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2f14d-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2f14d-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="2f14d-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2f14d-132">Validation File</span></span>  <br/> |<span data-ttu-id="2f14d-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2f14d-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f14d-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2f14d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f14d-135">False</span><span class="sxs-lookup"><span data-stu-id="2f14d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f14d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f14d-136">See also</span></span>

- [<span data-ttu-id="2f14d-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2f14d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


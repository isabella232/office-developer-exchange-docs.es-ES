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
ms.openlocfilehash: cc83f9b2137f151f3f8ef0ceaf603ec036989961
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465173"
---
# <a name="year"></a><span data-ttu-id="ddeff-105">Año</span><span class="sxs-lookup"><span data-stu-id="ddeff-105">Year</span></span>

<span data-ttu-id="ddeff-106">El elemento **Year** se usa para definir una zona horaria que cambia según el año.</span><span class="sxs-lookup"><span data-stu-id="ddeff-106">The **Year** element is used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="ddeff-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="ddeff-107">This element is optional.</span></span> <span data-ttu-id="ddeff-108">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ddeff-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Year/>
```

<span data-ttu-id="ddeff-109">**string**</span><span class="sxs-lookup"><span data-stu-id="ddeff-109">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ddeff-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ddeff-110">Attributes and elements</span></span>

<span data-ttu-id="ddeff-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ddeff-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ddeff-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ddeff-112">Attributes</span></span>

<span data-ttu-id="ddeff-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ddeff-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ddeff-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ddeff-114">Child elements</span></span>

<span data-ttu-id="ddeff-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ddeff-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ddeff-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ddeff-116">Parent elements</span></span>

|<span data-ttu-id="ddeff-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ddeff-117">**Element**</span></span>|<span data-ttu-id="ddeff-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ddeff-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddeff-119">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="ddeff-119">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="ddeff-120">Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) que se representa mediante el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="ddeff-120">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span>  <br/> |
|[<span data-ttu-id="ddeff-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="ddeff-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="ddeff-122">Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) que se representa mediante el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="ddeff-122">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ddeff-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ddeff-123">Text value</span></span>

<span data-ttu-id="ddeff-124">El elemento Year acepta una cadena que representa un año.</span><span class="sxs-lookup"><span data-stu-id="ddeff-124">The Year element accepts a string that represents a year.</span></span> <span data-ttu-id="ddeff-125">El formato del año es AAAA.</span><span class="sxs-lookup"><span data-stu-id="ddeff-125">The year format is YYYY.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddeff-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddeff-126">Remarks</span></span>

<span data-ttu-id="ddeff-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ddeff-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddeff-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ddeff-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddeff-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddeff-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ddeff-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ddeff-130">Schema Name</span></span>  <br/> |<span data-ttu-id="ddeff-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ddeff-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ddeff-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ddeff-132">Validation File</span></span>  <br/> |<span data-ttu-id="ddeff-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ddeff-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ddeff-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ddeff-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ddeff-135">Falso</span><span class="sxs-lookup"><span data-stu-id="ddeff-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddeff-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddeff-136">See also</span></span>

- [<span data-ttu-id="ddeff-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ddeff-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: IsWorkTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsWorkTime
api_type:
- schema
ms.assetid: 5243dd19-3593-4a81-bb2d-90496e04cb98
description: El elemento IsWorkTime indica si la hora de la reunión sugerida se produce durante las horas de trabajo programadas.
ms.openlocfilehash: c687b29df226ebb28cdf01d3a2da62590f790924
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836135"
---
# <a name="isworktime"></a><span data-ttu-id="e93bb-103">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="e93bb-103">IsWorkTime</span></span>

<span data-ttu-id="e93bb-104">El elemento **IsWorkTime** indica si la hora de la reunión sugerida se produce durante las horas de trabajo programadas.</span><span class="sxs-lookup"><span data-stu-id="e93bb-104">The **IsWorkTime** element represents whether the suggested meeting time occurs during scheduled work hours.</span></span> 
  
[<span data-ttu-id="e93bb-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e93bb-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="e93bb-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="e93bb-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="e93bb-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="e93bb-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="e93bb-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="e93bb-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="e93bb-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="e93bb-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="e93bb-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="e93bb-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="e93bb-111">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="e93bb-111">IsWorkTime</span></span>](isworktime.md)
  
```xml
<IsWorkTime>true or false</IsWorkTime>
```

 <span data-ttu-id="e93bb-112">**boolean**</span><span class="sxs-lookup"><span data-stu-id="e93bb-112">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e93bb-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e93bb-113">Attributes and elements</span></span>

<span data-ttu-id="e93bb-114">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e93bb-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e93bb-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="e93bb-115">Attributes</span></span>

<span data-ttu-id="e93bb-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e93bb-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e93bb-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e93bb-117">Child elements</span></span>

<span data-ttu-id="e93bb-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e93bb-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e93bb-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e93bb-119">Parent elements</span></span>

|<span data-ttu-id="e93bb-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="e93bb-120">**Element**</span></span>|<span data-ttu-id="e93bb-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e93bb-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e93bb-122">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="e93bb-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="e93bb-123">Representa una sola sugerencia de tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="e93bb-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="e93bb-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="e93bb-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e93bb-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e93bb-125">Text value</span></span>

<span data-ttu-id="e93bb-126">Se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="e93bb-126">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e93bb-127">Notas</span><span class="sxs-lookup"><span data-stu-id="e93bb-127">Remarks</span></span>

<span data-ttu-id="e93bb-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e93bb-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e93bb-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e93bb-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e93bb-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e93bb-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e93bb-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e93bb-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e93bb-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e93bb-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e93bb-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e93bb-133">Validation File</span></span>  <br/> |<span data-ttu-id="e93bb-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e93bb-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e93bb-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e93bb-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e93bb-136">False</span><span class="sxs-lookup"><span data-stu-id="e93bb-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e93bb-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="e93bb-137">See also</span></span>



[<span data-ttu-id="e93bb-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="e93bb-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="e93bb-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e93bb-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="e93bb-140">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="e93bb-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


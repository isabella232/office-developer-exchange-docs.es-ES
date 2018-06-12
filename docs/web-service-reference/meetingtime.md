---
title: MeetingTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingTime
api_type:
- schema
ms.assetid: 6e6d2d8b-e8a2-43e6-a715-0fc7d6dd44b9
description: El elemento MeetingTime representa una hora de reunión sugerida.
ms.openlocfilehash: 1ea79be394124431aa1279ee94d5e5c6331d377b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836435"
---
# <a name="meetingtime"></a><span data-ttu-id="df94b-103">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="df94b-103">MeetingTime</span></span>

<span data-ttu-id="df94b-104">El elemento **MeetingTime** representa una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="df94b-104">The **MeetingTime** element represents a suggested meeting time.</span></span> 
  
[<span data-ttu-id="df94b-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="df94b-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="df94b-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="df94b-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="df94b-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="df94b-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="df94b-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="df94b-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="df94b-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="df94b-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="df94b-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="df94b-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="df94b-111">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="df94b-111">MeetingTime</span></span>](meetingtime.md)
  
```xml
<MeetingTime>...</MeetingTime
```

 <span data-ttu-id="df94b-112">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="df94b-112">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df94b-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="df94b-113">Attributes and elements</span></span>

<span data-ttu-id="df94b-114">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="df94b-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df94b-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="df94b-115">Attributes</span></span>

<span data-ttu-id="df94b-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df94b-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df94b-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="df94b-117">Child elements</span></span>

<span data-ttu-id="df94b-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df94b-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="df94b-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="df94b-119">Parent elements</span></span>

|<span data-ttu-id="df94b-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="df94b-120">**Element**</span></span>|<span data-ttu-id="df94b-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df94b-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df94b-122">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="df94b-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="df94b-123">Representa una sola sugerencia de tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="df94b-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="df94b-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="df94b-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="df94b-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="df94b-125">Text value</span></span>

<span data-ttu-id="df94b-126">Se requiere un valor de texto que representa un valor **dateTime** .</span><span class="sxs-lookup"><span data-stu-id="df94b-126">A text value that represents a **dateTime** value is required.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="df94b-127">Notas</span><span class="sxs-lookup"><span data-stu-id="df94b-127">Remarks</span></span>

<span data-ttu-id="df94b-128">El elemento [MeetingTime](meetingtime.md) es un elemento secundario necesario del elemento [Sugerencia](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="df94b-128">The [MeetingTime](meetingtime.md) element is a required child element of the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="df94b-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="df94b-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df94b-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="df94b-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df94b-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df94b-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="df94b-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="df94b-132">Schema Name</span></span>  <br/> |<span data-ttu-id="df94b-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="df94b-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="df94b-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="df94b-134">Validation File</span></span>  <br/> |<span data-ttu-id="df94b-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="df94b-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="df94b-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="df94b-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="df94b-137">False</span><span class="sxs-lookup"><span data-stu-id="df94b-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df94b-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="df94b-138">See also</span></span>



[<span data-ttu-id="df94b-139">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="df94b-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="df94b-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="df94b-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="df94b-141">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="df94b-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


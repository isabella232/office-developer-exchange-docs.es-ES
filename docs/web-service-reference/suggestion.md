---
title: Sugerencia
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Suggestion
api_type:
- schema
ms.assetid: 040a5c8f-b62f-4d1d-9d2c-dc3c5e01481f
description: El elemento Sugerencia representa una sugerencia de reunión única.
ms.openlocfilehash: 24e2db1e0eabe35f7c971b0f1dbcbd333358f171
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840597"
---
# <a name="suggestion"></a><span data-ttu-id="1acac-103">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="1acac-103">Suggestion</span></span>

<span data-ttu-id="1acac-104">El elemento **Sugerencia** representa una sugerencia de reunión única.</span><span class="sxs-lookup"><span data-stu-id="1acac-104">The **Suggestion** element represents a single meeting suggestion.</span></span> 
  
[<span data-ttu-id="1acac-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1acac-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1acac-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1acac-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="1acac-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="1acac-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="1acac-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="1acac-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="1acac-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="1acac-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="1acac-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="1acac-110">Suggestion</span></span>](suggestion.md)
  
```xml
<Suggestion>
   <MeetingTime>...</MeetingTime>
   <IsWorkTime>...</IsWorkTime>
   <SuggestionQuality>...</SuggestionQuality>
   <AttendeeConflictDataArray>...</AttendeeConflictDataArray>
</Suggestion>
```

 <span data-ttu-id="1acac-111">**Sugerencia**</span><span class="sxs-lookup"><span data-stu-id="1acac-111">**Suggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1acac-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1acac-112">Attributes and elements</span></span>

<span data-ttu-id="1acac-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1acac-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1acac-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="1acac-114">Attributes</span></span>

<span data-ttu-id="1acac-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1acac-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1acac-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1acac-116">Child elements</span></span>

|<span data-ttu-id="1acac-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1acac-117">**Element**</span></span>|<span data-ttu-id="1acac-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1acac-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1acac-119">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="1acac-119">MeetingTime</span></span>](meetingtime.md) <br/> |<span data-ttu-id="1acac-120">Representa una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1acac-120">Represents a suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="1acac-121">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="1acac-121">IsWorkTime</span></span>](isworktime.md) <br/> |<span data-ttu-id="1acac-122">Representa si el tiempo de la reunión sugerida se produce durante las horas de trabajo programadas.</span><span class="sxs-lookup"><span data-stu-id="1acac-122">Represents whether the suggested meeting time occurs during scheduled work hours.</span></span>  <br/> |
|[<span data-ttu-id="1acac-123">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="1acac-123">SuggestionQuality</span></span>](suggestionquality.md) <br/> |<span data-ttu-id="1acac-124">Representa la calidad de la hora de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1acac-124">Represents the quality of the suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="1acac-125">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="1acac-125">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="1acac-126">Contiene una matriz de la información que describe los conflictos entre los usuarios y recursos y el tiempo de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1acac-126">Contains an array of information that describes conflicts between users and resources and the suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1acac-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1acac-127">Parent elements</span></span>

|<span data-ttu-id="1acac-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="1acac-128">**Element**</span></span>|<span data-ttu-id="1acac-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1acac-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1acac-130">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="1acac-130">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="1acac-131">Contiene una matriz de las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1acac-131">Contains an array of suggested meeting times.</span></span>  <br/> <span data-ttu-id="1acac-132">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="1acac-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1acac-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1acac-133">Remarks</span></span>

<span data-ttu-id="1acac-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1acac-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1acac-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1acac-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1acac-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1acac-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1acac-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1acac-137">Schema Name</span></span>  <br/> |<span data-ttu-id="1acac-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1acac-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="1acac-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1acac-139">Validation File</span></span>  <br/> |<span data-ttu-id="1acac-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1acac-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1acac-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1acac-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="1acac-142">False</span><span class="sxs-lookup"><span data-stu-id="1acac-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1acac-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="1acac-143">See also</span></span>



[<span data-ttu-id="1acac-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1acac-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1acac-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1acac-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1acac-146">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1acac-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


---
title: Alguna
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
description: El elemento de sugerencia representa una sola sugerencia de reunión.
ms.openlocfilehash: 25821abd5463ddba86a487709c8d2f8d928a94cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530383"
---
# <a name="suggestion"></a><span data-ttu-id="49eb6-103">Alguna</span><span class="sxs-lookup"><span data-stu-id="49eb6-103">Suggestion</span></span>

<span data-ttu-id="49eb6-104">El elemento de **sugerencia** representa una sola sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="49eb6-104">The **Suggestion** element represents a single meeting suggestion.</span></span> 
  
[<span data-ttu-id="49eb6-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="49eb6-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="49eb6-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="49eb6-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="49eb6-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="49eb6-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="49eb6-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="49eb6-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="49eb6-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="49eb6-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="49eb6-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="49eb6-110">Suggestion</span></span>](suggestion.md)
  
```xml
<Suggestion>
   <MeetingTime>...</MeetingTime>
   <IsWorkTime>...</IsWorkTime>
   <SuggestionQuality>...</SuggestionQuality>
   <AttendeeConflictDataArray>...</AttendeeConflictDataArray>
</Suggestion>
```

 <span data-ttu-id="49eb6-111">**Alguna**</span><span class="sxs-lookup"><span data-stu-id="49eb6-111">**Suggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49eb6-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="49eb6-112">Attributes and elements</span></span>

<span data-ttu-id="49eb6-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="49eb6-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49eb6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="49eb6-114">Attributes</span></span>

<span data-ttu-id="49eb6-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="49eb6-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49eb6-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="49eb6-116">Child elements</span></span>

|<span data-ttu-id="49eb6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="49eb6-117">**Element**</span></span>|<span data-ttu-id="49eb6-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="49eb6-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49eb6-119">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="49eb6-119">MeetingTime</span></span>](meetingtime.md) <br/> |<span data-ttu-id="49eb6-120">Representa una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="49eb6-120">Represents a suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="49eb6-121">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="49eb6-121">IsWorkTime</span></span>](isworktime.md) <br/> |<span data-ttu-id="49eb6-122">Representa si la hora de reunión sugerida se produce durante las horas laborables programadas.</span><span class="sxs-lookup"><span data-stu-id="49eb6-122">Represents whether the suggested meeting time occurs during scheduled work hours.</span></span>  <br/> |
|[<span data-ttu-id="49eb6-123">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="49eb6-123">SuggestionQuality</span></span>](suggestionquality.md) <br/> |<span data-ttu-id="49eb6-124">Representa la calidad de la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="49eb6-124">Represents the quality of the suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="49eb6-125">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="49eb6-125">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="49eb6-126">Contiene una matriz de información que describe los conflictos entre los usuarios y los recursos y la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="49eb6-126">Contains an array of information that describes conflicts between users and resources and the suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="49eb6-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="49eb6-127">Parent elements</span></span>

|<span data-ttu-id="49eb6-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="49eb6-128">**Element**</span></span>|<span data-ttu-id="49eb6-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="49eb6-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49eb6-130">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="49eb6-130">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="49eb6-131">Contiene una matriz de horas sugeridas para las reuniones.</span><span class="sxs-lookup"><span data-stu-id="49eb6-131">Contains an array of suggested meeting times.</span></span>  <br/> <span data-ttu-id="49eb6-132">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="49eb6-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49eb6-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49eb6-133">Remarks</span></span>

<span data-ttu-id="49eb6-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="49eb6-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49eb6-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="49eb6-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49eb6-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="49eb6-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49eb6-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="49eb6-137">Schema Name</span></span>  <br/> |<span data-ttu-id="49eb6-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="49eb6-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="49eb6-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="49eb6-139">Validation File</span></span>  <br/> |<span data-ttu-id="49eb6-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="49eb6-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49eb6-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="49eb6-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="49eb6-142">Falso</span><span class="sxs-lookup"><span data-stu-id="49eb6-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49eb6-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="49eb6-143">See also</span></span>



[<span data-ttu-id="49eb6-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="49eb6-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="49eb6-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="49eb6-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="49eb6-146">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="49eb6-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


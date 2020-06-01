---
title: TooBigGroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TooBigGroupAttendeeConflictData
api_type:
- schema
ms.assetid: 1512428d-ce22-4da9-b1c1-446b4bcd0a21
description: El elemento TooBigGroupAttendeeConflictData representa un asistente que se resolvió como una lista de distribución pero la lista de distribución era demasiado grande para expandirse.
ms.openlocfilehash: 407a4a49e5f32c81439063f47df2e131dd663a4f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468603"
---
# <a name="toobiggroupattendeeconflictdata"></a><span data-ttu-id="bf733-103">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="bf733-103">TooBigGroupAttendeeConflictData</span></span>

<span data-ttu-id="bf733-104">El elemento **TooBigGroupAttendeeConflictData** representa un asistente que se resolvió como una lista de distribución pero la lista de distribución era demasiado grande para expandirse.</span><span class="sxs-lookup"><span data-stu-id="bf733-104">The **TooBigGroupAttendeeConflictData** element represents an attendee that was resolved as a distribution list but the distribution list was too large to expand.</span></span> 
  
[<span data-ttu-id="bf733-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="bf733-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="bf733-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="bf733-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="bf733-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="bf733-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="bf733-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="bf733-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="bf733-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="bf733-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="bf733-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="bf733-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="bf733-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="bf733-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="bf733-112">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="bf733-112">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md)
  
```xml
<TooBigGroupAttendeeConflictData/>
```

 <span data-ttu-id="bf733-113">**TooBigGroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="bf733-113">**TooBigGroupAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf733-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bf733-114">Attributes and elements</span></span>

<span data-ttu-id="bf733-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bf733-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf733-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf733-116">Attributes</span></span>

<span data-ttu-id="bf733-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bf733-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf733-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bf733-118">Child elements</span></span>

<span data-ttu-id="bf733-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bf733-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bf733-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bf733-120">Parent elements</span></span>

|<span data-ttu-id="bf733-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bf733-121">**Element**</span></span>|<span data-ttu-id="bf733-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf733-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf733-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="bf733-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="bf733-124">Contiene una matriz de datos conflictivos para los asistentes identificados en el [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span><span class="sxs-lookup"><span data-stu-id="bf733-124">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="bf733-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="bf733-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf733-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf733-126">Remarks</span></span>

<span data-ttu-id="bf733-127">Las listas de distribución que contienen más de 100 miembros no se pueden expandir.</span><span class="sxs-lookup"><span data-stu-id="bf733-127">Distribution lists that contain more than 100 members cannot be expanded.</span></span>
  
<span data-ttu-id="bf733-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="bf733-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf733-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bf733-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf733-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf733-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bf733-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bf733-131">Schema Name</span></span>  <br/> |<span data-ttu-id="bf733-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bf733-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="bf733-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bf733-133">Validation File</span></span>  <br/> |<span data-ttu-id="bf733-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="bf733-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bf733-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bf733-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="bf733-136">Falso</span><span class="sxs-lookup"><span data-stu-id="bf733-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf733-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf733-137">See also</span></span>



[<span data-ttu-id="bf733-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="bf733-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="bf733-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="bf733-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="bf733-140">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="bf733-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


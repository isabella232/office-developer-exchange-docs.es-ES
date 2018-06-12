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
description: El elemento TooBigGroupAttendeeConflictData representa a un asistente que se resuelve como una lista de distribución pero era demasiado grande para expandir la lista de distribución.
ms.openlocfilehash: 1137368d13cb5b88fd2a7866cadc6d69b783c75b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840716"
---
# <a name="toobiggroupattendeeconflictdata"></a><span data-ttu-id="104c6-103">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="104c6-103">TooBigGroupAttendeeConflictData</span></span>

<span data-ttu-id="104c6-104">El elemento **TooBigGroupAttendeeConflictData** representa a un asistente que se resuelve como una lista de distribución pero era demasiado grande para expandir la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="104c6-104">The **TooBigGroupAttendeeConflictData** element represents an attendee that was resolved as a distribution list but the distribution list was too large to expand.</span></span> 
  
[<span data-ttu-id="104c6-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="104c6-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="104c6-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="104c6-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="104c6-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="104c6-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="104c6-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="104c6-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="104c6-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="104c6-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="104c6-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="104c6-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="104c6-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="104c6-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="104c6-112">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="104c6-112">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md)
  
```xml
<TooBigGroupAttendeeConflictData/>
```

 <span data-ttu-id="104c6-113">**TooBigGroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="104c6-113">**TooBigGroupAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="104c6-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="104c6-114">Attributes and elements</span></span>

<span data-ttu-id="104c6-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="104c6-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="104c6-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="104c6-116">Attributes</span></span>

<span data-ttu-id="104c6-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="104c6-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="104c6-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="104c6-118">Child elements</span></span>

<span data-ttu-id="104c6-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="104c6-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="104c6-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="104c6-120">Parent elements</span></span>

|<span data-ttu-id="104c6-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="104c6-121">**Element**</span></span>|<span data-ttu-id="104c6-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="104c6-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="104c6-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="104c6-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="104c6-124">Contiene una matriz de datos en conflicto para los asistentes identificados en el [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span><span class="sxs-lookup"><span data-stu-id="104c6-124">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="104c6-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="104c6-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="104c6-126">Notas</span><span class="sxs-lookup"><span data-stu-id="104c6-126">Remarks</span></span>

<span data-ttu-id="104c6-127">No se puede expandir las listas de distribución que contienen a más de 100 miembros.</span><span class="sxs-lookup"><span data-stu-id="104c6-127">Distribution lists that contain more than 100 members cannot be expanded.</span></span>
  
<span data-ttu-id="104c6-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="104c6-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="104c6-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="104c6-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="104c6-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="104c6-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="104c6-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="104c6-131">Schema Name</span></span>  <br/> |<span data-ttu-id="104c6-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="104c6-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="104c6-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="104c6-133">Validation File</span></span>  <br/> |<span data-ttu-id="104c6-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="104c6-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="104c6-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="104c6-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="104c6-136">False</span><span class="sxs-lookup"><span data-stu-id="104c6-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="104c6-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="104c6-137">See also</span></span>



[<span data-ttu-id="104c6-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="104c6-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="104c6-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="104c6-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="104c6-140">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="104c6-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


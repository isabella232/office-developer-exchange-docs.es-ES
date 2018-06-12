---
title: IndividualAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndividualAttendeeConflictData
api_type:
- schema
ms.assetid: d45d3c34-abe1-40da-afd3-23bc5c3ef474
description: El elemento IndividualAttendeeConflictData contiene un usuario o estado de disponibilidad del contacto para una ventana de tiempo que se produce al mismo tiempo, como el tiempo de la reunión sugerida identificada en el elemento de sugerencia.
ms.openlocfilehash: 0bd164e08a6f3685415452b7c82a4220cf69d792
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835930"
---
# <a name="individualattendeeconflictdata"></a><span data-ttu-id="6f3c4-103">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="6f3c4-103">IndividualAttendeeConflictData</span></span>

<span data-ttu-id="6f3c4-104">El elemento **IndividualAttendeeConflictData** contiene un usuario o estado de disponibilidad del contacto para una ventana de tiempo que se produce al mismo tiempo, como el tiempo de la reunión sugerida identificados en el elemento de [Sugerencia](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="6f3c4-104">The **IndividualAttendeeConflictData** element contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
[<span data-ttu-id="6f3c4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="6f3c4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="6f3c4-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="6f3c4-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="6f3c4-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="6f3c4-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="6f3c4-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="6f3c4-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="6f3c4-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="6f3c4-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="6f3c4-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="6f3c4-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="6f3c4-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="6f3c4-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="6f3c4-112">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="6f3c4-112">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md)
  
```xml
<IndividualAttendeeConflictData>
   <BusyType>...</BusyType>
</IndividualAttendeeConflictData>
```

 <span data-ttu-id="6f3c4-113">**IndividualAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-113">**IndividualAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f3c4-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f3c4-114">Attributes and elements</span></span>

<span data-ttu-id="6f3c4-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f3c4-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f3c4-116">Attributes</span></span>

<span data-ttu-id="6f3c4-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f3c4-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f3c4-118">Child elements</span></span>

|<span data-ttu-id="6f3c4-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-119">**Element**</span></span>|<span data-ttu-id="6f3c4-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f3c4-121">BusyType</span><span class="sxs-lookup"><span data-stu-id="6f3c4-121">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="6f3c4-122">Representa el estado de disponibilidad de un usuario para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-122">Represents the free/busy status of a user for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f3c4-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f3c4-123">Parent elements</span></span>

|<span data-ttu-id="6f3c4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-124">**Element**</span></span>|<span data-ttu-id="6f3c4-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f3c4-126">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="6f3c4-126">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="6f3c4-127">Contiene una matriz de datos en conflicto para los asistentes identificados en el [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span><span class="sxs-lookup"><span data-stu-id="6f3c4-127">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="6f3c4-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="6f3c4-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f3c4-129">Notas</span><span class="sxs-lookup"><span data-stu-id="6f3c4-129">Remarks</span></span>

<span data-ttu-id="6f3c4-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f3c4-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6f3c4-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f3c4-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f3c4-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f3c4-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6f3c4-133">Schema Name</span></span>  <br/> |<span data-ttu-id="6f3c4-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6f3c4-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f3c4-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6f3c4-135">Validation File</span></span>  <br/> |<span data-ttu-id="6f3c4-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f3c4-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f3c4-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f3c4-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f3c4-138">False</span><span class="sxs-lookup"><span data-stu-id="6f3c4-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f3c4-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="6f3c4-139">See also</span></span>



[<span data-ttu-id="6f3c4-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="6f3c4-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="6f3c4-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="6f3c4-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="6f3c4-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="6f3c4-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


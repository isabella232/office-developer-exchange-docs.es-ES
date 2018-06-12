---
title: AttendeeConflictDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeConflictDataArray
api_type:
- schema
ms.assetid: 1d758547-28c5-4649-8334-427480c282d6
description: El elemento AttendeeConflictDataArray contiene una matriz de datos en conflicto para los asistentes consultados identificados en la operación GetUserAvailability.
ms.openlocfilehash: 169312b8a3d37c014ba58fbfe094d786b134fc90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763575"
---
# <a name="attendeeconflictdataarray"></a><span data-ttu-id="505b0-103">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="505b0-103">AttendeeConflictDataArray</span></span>

<span data-ttu-id="505b0-104">El elemento **AttendeeConflictDataArray** contiene una matriz de datos en conflicto para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="505b0-104">The **AttendeeConflictDataArray** element contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>
  
- [<span data-ttu-id="505b0-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="505b0-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="505b0-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="505b0-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
- [<span data-ttu-id="505b0-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="505b0-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
- [<span data-ttu-id="505b0-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="505b0-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
- [<span data-ttu-id="505b0-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="505b0-109">SuggestionArray</span></span>](suggestionarray.md)
  
- [<span data-ttu-id="505b0-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="505b0-110">Suggestion</span></span>](suggestion.md)
  
- [<span data-ttu-id="505b0-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="505b0-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 <span data-ttu-id="505b0-112">**ArrayOfAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="505b0-112">**ArrayOfAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="505b0-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="505b0-113">Attributes and elements</span></span>

<span data-ttu-id="505b0-114">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="505b0-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="505b0-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="505b0-115">Attributes</span></span>

<span data-ttu-id="505b0-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="505b0-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="505b0-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="505b0-117">Child elements</span></span>

|<span data-ttu-id="505b0-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="505b0-118">**Element**</span></span>|<span data-ttu-id="505b0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="505b0-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="505b0-120">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="505b0-120">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md) <br/> |<span data-ttu-id="505b0-121">Representa un asistente no se puede resolver o un asistente que no es un usuario, una lista de distribución o un contacto.</span><span class="sxs-lookup"><span data-stu-id="505b0-121">Represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span>  <br/> |
|[<span data-ttu-id="505b0-122">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="505b0-122">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="505b0-123">Contiene el estado de disponibilidad de un usuario o un contacto para una ventana de tiempo que se produce al mismo tiempo como la sugerida hora identificado en el elemento de la [Sugerencia](suggestion.md) de reunión.</span><span class="sxs-lookup"><span data-stu-id="505b0-123">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span>  <br/> |
|[<span data-ttu-id="505b0-124">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="505b0-124">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md) <br/> |<span data-ttu-id="505b0-125">Representa a un asistente que se resuelve como una lista de distribución que era demasiado grande para expandir.</span><span class="sxs-lookup"><span data-stu-id="505b0-125">Represents an attendee that resolved as a distribution list that was too large to expand.</span></span>  <br/> |
|[<span data-ttu-id="505b0-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="505b0-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="505b0-127">Contiene información de conflicto agregado sobre el número de usuarios disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="505b0-127">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="505b0-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="505b0-128">Parent elements</span></span>

|<span data-ttu-id="505b0-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="505b0-129">**Element**</span></span>|<span data-ttu-id="505b0-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="505b0-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="505b0-131">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="505b0-131">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="505b0-132">Representa una sola sugerencia de tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="505b0-132">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="505b0-133">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="505b0-133">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="505b0-134">Notas</span><span class="sxs-lookup"><span data-stu-id="505b0-134">Remarks</span></span>

<span data-ttu-id="505b0-135">La posición de cada elemento en el **AttendeeConflictDataArray** corresponde a la posición de los asistentes consultados en el elemento [MailboxDataArray](mailboxdataarray.md) .</span><span class="sxs-lookup"><span data-stu-id="505b0-135">The position of each element in the **AttendeeConflictDataArray** corresponds to the position of the queried attendees in the [MailboxDataArray](mailboxdataarray.md) element.</span></span> <span data-ttu-id="505b0-136">Cada asistente consultado debe corresponder a uno de los elementos secundarios de **AttendeeConflictDataArray** .</span><span class="sxs-lookup"><span data-stu-id="505b0-136">Each queried attendee must correspond to one of the **AttendeeConflictDataArray** child elements.</span></span> <span data-ttu-id="505b0-137">Estos elementos representan un único conflicto con la hora de la reunión sugerida identificada en el elemento de [Sugerencia](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="505b0-137">These elements represent a single conflict with the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="505b0-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="505b0-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="505b0-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="505b0-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="505b0-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="505b0-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="505b0-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="505b0-141">Schema Name</span></span>  <br/> |<span data-ttu-id="505b0-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="505b0-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="505b0-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="505b0-143">Validation File</span></span>  <br/> |<span data-ttu-id="505b0-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="505b0-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="505b0-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="505b0-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="505b0-146">False</span><span class="sxs-lookup"><span data-stu-id="505b0-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="505b0-147">Ver también</span><span class="sxs-lookup"><span data-stu-id="505b0-147">See also</span></span>

- [<span data-ttu-id="505b0-148">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="505b0-148">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="505b0-149">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="505b0-149">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="505b0-150">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="505b0-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


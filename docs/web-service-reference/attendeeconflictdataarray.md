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
description: El elemento AttendeeConflictDataArray contiene una matriz de datos conflictivos para los asistentes consultados identificados en la operación GetUserAvailability.
ms.openlocfilehash: 770e8c00ca248ec3562180dc9d3626fd5b58f4d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455803"
---
# <a name="attendeeconflictdataarray"></a><span data-ttu-id="1cf06-103">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="1cf06-103">AttendeeConflictDataArray</span></span>

<span data-ttu-id="1cf06-104">El elemento **AttendeeConflictDataArray** contiene una matriz de datos conflictivos para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="1cf06-104">The **AttendeeConflictDataArray** element contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>
  
- [<span data-ttu-id="1cf06-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1cf06-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="1cf06-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1cf06-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
- [<span data-ttu-id="1cf06-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="1cf06-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
- [<span data-ttu-id="1cf06-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="1cf06-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
- [<span data-ttu-id="1cf06-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="1cf06-109">SuggestionArray</span></span>](suggestionarray.md)
  
- [<span data-ttu-id="1cf06-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="1cf06-110">Suggestion</span></span>](suggestion.md)
  
- [<span data-ttu-id="1cf06-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="1cf06-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 <span data-ttu-id="1cf06-112">**ArrayOfAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="1cf06-112">**ArrayOfAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1cf06-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1cf06-113">Attributes and elements</span></span>

<span data-ttu-id="1cf06-114">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1cf06-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1cf06-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="1cf06-115">Attributes</span></span>

<span data-ttu-id="1cf06-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1cf06-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1cf06-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1cf06-117">Child elements</span></span>

|<span data-ttu-id="1cf06-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1cf06-118">**Element**</span></span>|<span data-ttu-id="1cf06-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1cf06-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1cf06-120">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="1cf06-120">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md) <br/> |<span data-ttu-id="1cf06-121">Representa un asistente no resuelta o un asistente que no es un usuario, una lista de distribución o un contacto.</span><span class="sxs-lookup"><span data-stu-id="1cf06-121">Represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span>  <br/> |
|[<span data-ttu-id="1cf06-122">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="1cf06-122">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="1cf06-123">Contiene el estado de disponibilidad de un usuario o contacto para una ventana de tiempo que se produce al mismo tiempo que la hora de reunión sugerida identificada en el elemento de [sugerencia](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf06-123">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span>  <br/> |
|[<span data-ttu-id="1cf06-124">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="1cf06-124">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md) <br/> |<span data-ttu-id="1cf06-125">Representa un asistente que se resolvió como una lista de distribución demasiado grande para expandirse.</span><span class="sxs-lookup"><span data-stu-id="1cf06-125">Represents an attendee that resolved as a distribution list that was too large to expand.</span></span>  <br/> |
|[<span data-ttu-id="1cf06-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="1cf06-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="1cf06-127">Contiene información de conflicto de agregados sobre el número de usuarios disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1cf06-127">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1cf06-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1cf06-128">Parent elements</span></span>

|<span data-ttu-id="1cf06-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1cf06-129">**Element**</span></span>|<span data-ttu-id="1cf06-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1cf06-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1cf06-131">Alguna</span><span class="sxs-lookup"><span data-stu-id="1cf06-131">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="1cf06-132">Representa una sugerencia de hora de reunión única.</span><span class="sxs-lookup"><span data-stu-id="1cf06-132">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="1cf06-133">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="1cf06-133">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cf06-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1cf06-134">Remarks</span></span>

<span data-ttu-id="1cf06-135">La posición de cada elemento de **AttendeeConflictDataArray** corresponde a la posición de los asistentes consultados en el elemento [MailboxDataArray](mailboxdataarray.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf06-135">The position of each element in the **AttendeeConflictDataArray** corresponds to the position of the queried attendees in the [MailboxDataArray](mailboxdataarray.md) element.</span></span> <span data-ttu-id="1cf06-136">Cada asistente consultado debe corresponder a uno de los elementos secundarios **AttendeeConflictDataArray** .</span><span class="sxs-lookup"><span data-stu-id="1cf06-136">Each queried attendee must correspond to one of the **AttendeeConflictDataArray** child elements.</span></span> <span data-ttu-id="1cf06-137">Estos elementos representan un solo conflicto con la hora de reunión sugerida identificada en el elemento de [sugerencia](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf06-137">These elements represent a single conflict with the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="1cf06-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1cf06-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1cf06-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1cf06-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cf06-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cf06-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1cf06-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1cf06-141">Schema Name</span></span>  <br/> |<span data-ttu-id="1cf06-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1cf06-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="1cf06-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1cf06-143">Validation File</span></span>  <br/> |<span data-ttu-id="1cf06-144">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1cf06-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1cf06-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1cf06-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="1cf06-146">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf06-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cf06-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cf06-147">See also</span></span>

- [<span data-ttu-id="1cf06-148">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1cf06-148">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="1cf06-149">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1cf06-149">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="1cf06-150">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1cf06-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


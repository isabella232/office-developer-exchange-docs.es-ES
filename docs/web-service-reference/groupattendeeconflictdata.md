---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: El elemento GroupAttendeeConflictData contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una distribución de lista para una sugiere el momento de la reunión.
ms.openlocfilehash: 382b4d866c95de98bd444cd6226d71813889d4f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835757"
---
# <a name="groupattendeeconflictdata"></a><span data-ttu-id="431d1-103">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="431d1-103">GroupAttendeeConflictData</span></span>

<span data-ttu-id="431d1-104">El elemento **GroupAttendeeConflictData** contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución un período de tiempo de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="431d1-104">The **GroupAttendeeConflictData** element contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span> 
  
- [<span data-ttu-id="431d1-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="431d1-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="431d1-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="431d1-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
- [<span data-ttu-id="431d1-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="431d1-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
- [<span data-ttu-id="431d1-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="431d1-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
- [<span data-ttu-id="431d1-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="431d1-109">SuggestionArray</span></span>](suggestionarray.md)
- [<span data-ttu-id="431d1-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="431d1-110">Suggestion</span></span>](suggestion.md)
- [<span data-ttu-id="431d1-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="431d1-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
- [<span data-ttu-id="431d1-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="431d1-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

<span data-ttu-id="431d1-113">**GroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="431d1-113">**GroupAttendeeConflictData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="431d1-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="431d1-114">Attributes and elements</span></span>

<span data-ttu-id="431d1-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="431d1-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="431d1-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="431d1-116">Attributes</span></span>

<span data-ttu-id="431d1-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="431d1-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="431d1-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="431d1-118">Child elements</span></span>

|<span data-ttu-id="431d1-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="431d1-119">**Element**</span></span>|<span data-ttu-id="431d1-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="431d1-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="431d1-121">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="431d1-121">NumberOfMembers</span></span>](numberofmembers.md) <br/> |<span data-ttu-id="431d1-122">Representa el número de usuarios, recursos y salas en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="431d1-122">Represents the number of users, resources, and rooms in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="431d1-123">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="431d1-123">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md) <br/> |<span data-ttu-id="431d1-124">Representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="431d1-124">Represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="431d1-125">Este elemento representa a los miembros para los que el estado es **gratuita**.</span><span class="sxs-lookup"><span data-stu-id="431d1-125">This element represents members for whom the status is **Free**.</span></span>  <br/> |
|[<span data-ttu-id="431d1-126">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="431d1-126">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md) <br/> |<span data-ttu-id="431d1-127">Representa el número de miembros de la lista de distribución que tienen un conflicto con una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="431d1-127">Represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="431d1-128">Este elemento representa a los integrantes que tengan un estado **no disponible**, **fuera de la oficina**o **provisional** .</span><span class="sxs-lookup"><span data-stu-id="431d1-128">This element represents members who have a **Busy**, **OOF**, or **Tentative** status.</span></span>  <br/> |
|[<span data-ttu-id="431d1-129">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="431d1-129">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md) <br/> |<span data-ttu-id="431d1-130">Representa el número de miembros del grupo que no tienen datos de disponibilidad publicados que se compara con una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="431d1-130">Represents the number of group members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="431d1-131">Este elemento representa los miembros de una lista de distribución que es demasiado grande o los miembros que tienen el estado de **No haber datos** .</span><span class="sxs-lookup"><span data-stu-id="431d1-131">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="431d1-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="431d1-132">Parent elements</span></span>

|<span data-ttu-id="431d1-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="431d1-133">**Element**</span></span>|<span data-ttu-id="431d1-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="431d1-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="431d1-135">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="431d1-135">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="431d1-136">Contiene una matriz de datos en conflicto para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="431d1-136">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="431d1-137">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="431d1-137">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="431d1-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="431d1-138">Remarks</span></span>

<span data-ttu-id="431d1-139">El elemento **GroupAttendeeConflictData** está presente en la respuesta cuando un asistente en el [GetUserAvailabilityRequest](getuseravailabilityrequest.md) se resuelve en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="431d1-139">The **GroupAttendeeConflictData** element is present in the response when an attendee in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) is resolved to a distribution list.</span></span> <span data-ttu-id="431d1-140">El elemento **GroupAttendeeConflictData** identifica los tres estados para los miembros de una lista de distribución: disponibles, con conflictos, o sin datos.</span><span class="sxs-lookup"><span data-stu-id="431d1-140">The **GroupAttendeeConflictData** element identifies three states for members of a distribution list: available, conflicted, or no data.</span></span> <span data-ttu-id="431d1-141">Expansión de la lista de distribución será compatible con un máximo de 100 miembros.</span><span class="sxs-lookup"><span data-stu-id="431d1-141">Distribution list expansion will support up to 100 members.</span></span> <span data-ttu-id="431d1-142">Por lo tanto, el elemento de [NumberOfMembers](numberofmembers.md) puede contener un máximo de 100 miembros.</span><span class="sxs-lookup"><span data-stu-id="431d1-142">Therefore, the [NumberOfMembers](numberofmembers.md) element can contain a maximum of 100 members.</span></span> <span data-ttu-id="431d1-143">Expansión de la lista de distribución es recursiva.</span><span class="sxs-lookup"><span data-stu-id="431d1-143">Distribution list expansion is recursive.</span></span> <span data-ttu-id="431d1-144">Si una lista de distribución contiene una lista de distribución secundaria que se expande la pertenencia primario total a más de 100 miembros, la lista de distribución secundarios no se expandirán y se cuenta como una sola entrada de la cuenta de elementos [NumberOfMembersWithNoData](numberofmemberswithnodata.md) .</span><span class="sxs-lookup"><span data-stu-id="431d1-144">If a distribution list contains a child distribution list that expands the total parent membership to over 100 members, the child distribution list will not be expanded and will count as a single entry of the [NumberOfMembersWithNoData](numberofmemberswithnodata.md) element count.</span></span> <span data-ttu-id="431d1-145">Si se puede expandir una lista de distribución secundaria y no expandir la pertenencia de primario total a más de 100 miembros, su pertenencia al grupo se expande y se agregan los recuentos de miembros para los elementos secundarios del elemento **GroupAttendeeConflictData** .</span><span class="sxs-lookup"><span data-stu-id="431d1-145">If a child distribution list can be expanded and the total parent membership does not expand to over 100 members, its membership is expanded and the member counts are added to the child elements of the **GroupAttendeeConflictData** element.</span></span> 
  
<span data-ttu-id="431d1-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="431d1-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="431d1-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="431d1-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="431d1-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="431d1-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="431d1-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="431d1-149">Schema Name</span></span>  <br/> |<span data-ttu-id="431d1-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="431d1-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="431d1-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="431d1-151">Validation File</span></span>  <br/> |<span data-ttu-id="431d1-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="431d1-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="431d1-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="431d1-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="431d1-154">False</span><span class="sxs-lookup"><span data-stu-id="431d1-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="431d1-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="431d1-155">See also</span></span>

- [<span data-ttu-id="431d1-156">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="431d1-156">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="431d1-157">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="431d1-157">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="431d1-158">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="431d1-158">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


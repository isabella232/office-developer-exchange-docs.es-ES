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
description: El elemento GroupAttendeeConflictData contiene información sobre conflictos de agregación sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.
ms.openlocfilehash: c75a4e6f8fdff7fb2514f448350fee9f1acb9775
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462932"
---
# <a name="groupattendeeconflictdata"></a><span data-ttu-id="b7f01-103">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="b7f01-103">GroupAttendeeConflictData</span></span>

<span data-ttu-id="b7f01-104">El elemento **GroupAttendeeConflictData** contiene información sobre conflictos de agregación sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="b7f01-104">The **GroupAttendeeConflictData** element contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span> 
  
- [<span data-ttu-id="b7f01-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b7f01-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="b7f01-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="b7f01-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
- [<span data-ttu-id="b7f01-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="b7f01-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
- [<span data-ttu-id="b7f01-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="b7f01-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
- [<span data-ttu-id="b7f01-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="b7f01-109">SuggestionArray</span></span>](suggestionarray.md)
- [<span data-ttu-id="b7f01-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="b7f01-110">Suggestion</span></span>](suggestion.md)
- [<span data-ttu-id="b7f01-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="b7f01-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
- [<span data-ttu-id="b7f01-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="b7f01-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

<span data-ttu-id="b7f01-113">**GroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="b7f01-113">**GroupAttendeeConflictData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b7f01-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b7f01-114">Attributes and elements</span></span>

<span data-ttu-id="b7f01-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b7f01-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7f01-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7f01-116">Attributes</span></span>

<span data-ttu-id="b7f01-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b7f01-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7f01-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b7f01-118">Child elements</span></span>

|<span data-ttu-id="b7f01-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b7f01-119">**Element**</span></span>|<span data-ttu-id="b7f01-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7f01-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7f01-121">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="b7f01-121">NumberOfMembers</span></span>](numberofmembers.md) <br/> |<span data-ttu-id="b7f01-122">Representa el número de usuarios, recursos y salas de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="b7f01-122">Represents the number of users, resources, and rooms in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="b7f01-123">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="b7f01-123">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md) <br/> |<span data-ttu-id="b7f01-124">Representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="b7f01-124">Represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="b7f01-125">Este elemento representa los miembros para los que el estado es **libre**.</span><span class="sxs-lookup"><span data-stu-id="b7f01-125">This element represents members for whom the status is **Free**.</span></span>  <br/> |
|[<span data-ttu-id="b7f01-126">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="b7f01-126">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md) <br/> |<span data-ttu-id="b7f01-127">Representa el número de miembros de la lista de distribución que tienen un conflicto con la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="b7f01-127">Represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="b7f01-128">Este elemento representa los miembros que tienen un estado **ocupado**, **OOF**o **provisional** .</span><span class="sxs-lookup"><span data-stu-id="b7f01-128">This element represents members who have a **Busy**, **OOF**, or **Tentative** status.</span></span>  <br/> |
|[<span data-ttu-id="b7f01-129">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="b7f01-129">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md) <br/> |<span data-ttu-id="b7f01-130">Representa el número de miembros del grupo que no han publicado datos de disponibilidad para compararlos con una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="b7f01-130">Represents the number of group members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="b7f01-131">Este elemento representa los miembros de una lista de distribución que son demasiado grandes o miembros que no tienen el estado de los **datos** .</span><span class="sxs-lookup"><span data-stu-id="b7f01-131">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7f01-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b7f01-132">Parent elements</span></span>

|<span data-ttu-id="b7f01-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b7f01-133">**Element**</span></span>|<span data-ttu-id="b7f01-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7f01-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7f01-135">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="b7f01-135">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="b7f01-136">Contiene una matriz de datos conflictivos para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="b7f01-136">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="b7f01-137">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="b7f01-137">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7f01-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7f01-138">Remarks</span></span>

<span data-ttu-id="b7f01-139">El elemento **GroupAttendeeConflictData** está presente en la respuesta cuando un asistente de la [GetUserAvailabilityRequest](getuseravailabilityrequest.md) se resuelve en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="b7f01-139">The **GroupAttendeeConflictData** element is present in the response when an attendee in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) is resolved to a distribution list.</span></span> <span data-ttu-id="b7f01-140">El elemento **GroupAttendeeConflictData** identifica tres Estados para los miembros de una lista de distribución: available, conflicted o no Data.</span><span class="sxs-lookup"><span data-stu-id="b7f01-140">The **GroupAttendeeConflictData** element identifies three states for members of a distribution list: available, conflicted, or no data.</span></span> <span data-ttu-id="b7f01-141">La expansión de la lista de distribución admitirá hasta 100 miembros.</span><span class="sxs-lookup"><span data-stu-id="b7f01-141">Distribution list expansion will support up to 100 members.</span></span> <span data-ttu-id="b7f01-142">Por lo tanto, el elemento [NumberOfMembers](numberofmembers.md) puede contener un máximo de 100 miembros.</span><span class="sxs-lookup"><span data-stu-id="b7f01-142">Therefore, the [NumberOfMembers](numberofmembers.md) element can contain a maximum of 100 members.</span></span> <span data-ttu-id="b7f01-143">La expansión de la lista de distribución es recurrente.</span><span class="sxs-lookup"><span data-stu-id="b7f01-143">Distribution list expansion is recursive.</span></span> <span data-ttu-id="b7f01-144">Si una lista de distribución contiene una lista de distribución secundaria que expande el total de la pertenencia a 100 miembros, la lista de distribución secundaria no se expandirá y se contará como una entrada única del recuento de elementos [NumberOfMembersWithNoData](numberofmemberswithnodata.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f01-144">If a distribution list contains a child distribution list that expands the total parent membership to over 100 members, the child distribution list will not be expanded and will count as a single entry of the [NumberOfMembersWithNoData](numberofmemberswithnodata.md) element count.</span></span> <span data-ttu-id="b7f01-145">Si se puede expandir una lista de distribución secundaria y la pertenencia al elemento primario total no se expande a más de 100 miembros, se expande su pertenencia y los recuentos de miembros se agregan a los elementos secundarios del elemento **GroupAttendeeConflictData** .</span><span class="sxs-lookup"><span data-stu-id="b7f01-145">If a child distribution list can be expanded and the total parent membership does not expand to over 100 members, its membership is expanded and the member counts are added to the child elements of the **GroupAttendeeConflictData** element.</span></span> 
  
<span data-ttu-id="b7f01-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b7f01-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7f01-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b7f01-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f01-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7f01-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b7f01-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b7f01-149">Schema Name</span></span>  <br/> |<span data-ttu-id="b7f01-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b7f01-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="b7f01-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b7f01-151">Validation File</span></span>  <br/> |<span data-ttu-id="b7f01-152">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b7f01-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b7f01-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b7f01-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7f01-154">Falso</span><span class="sxs-lookup"><span data-stu-id="b7f01-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7f01-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7f01-155">See also</span></span>

- [<span data-ttu-id="b7f01-156">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="b7f01-156">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="b7f01-157">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b7f01-157">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="b7f01-158">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="b7f01-158">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


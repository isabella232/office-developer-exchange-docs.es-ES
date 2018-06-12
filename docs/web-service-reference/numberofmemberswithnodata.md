---
title: NumberOfMembersWithNoData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersWithNoData
api_type:
- schema
ms.assetid: 7ca9c57c-9519-442c-a9f4-dca2b0309716
description: El elemento NumberOfMembersWithNoData representa el número de miembros de la lista de distribución que no tienen datos de disponibilidad publicados que se compara con una hora de reunión sugerida. Este elemento representa los miembros de una lista de distribución que es demasiado grande o los miembros que tienen el estado de no haber datos.
ms.openlocfilehash: f73978df47bd8240dd5dabfbbf74523525e3270f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836637"
---
# <a name="numberofmemberswithnodata"></a><span data-ttu-id="fd022-104">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="fd022-104">NumberOfMembersWithNoData</span></span>

<span data-ttu-id="fd022-105">El elemento **NumberOfMembersWithNoData** representa el número de miembros de la lista de distribución que no tienen datos de disponibilidad publicados que se compara con una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="fd022-105">The **NumberOfMembersWithNoData** element represents the number of distribution list members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="fd022-106">Este elemento representa los miembros de una lista de distribución que es demasiado grande o los miembros que tienen el estado de **No haber datos** .</span><span class="sxs-lookup"><span data-stu-id="fd022-106">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span> 
  
[<span data-ttu-id="fd022-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fd022-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="fd022-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="fd022-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="fd022-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="fd022-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="fd022-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="fd022-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="fd022-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="fd022-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="fd022-112">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="fd022-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="fd022-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="fd022-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="fd022-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="fd022-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="fd022-115">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="fd022-115">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md)
  
```xml
<NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
```

 <span data-ttu-id="fd022-116">**int**</span><span class="sxs-lookup"><span data-stu-id="fd022-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd022-117">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fd022-117">Attributes and elements</span></span>

<span data-ttu-id="fd022-118">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fd022-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd022-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd022-119">Attributes</span></span>

<span data-ttu-id="fd022-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fd022-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd022-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fd022-121">Child elements</span></span>

<span data-ttu-id="fd022-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fd022-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd022-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fd022-123">Parent elements</span></span>

|<span data-ttu-id="fd022-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd022-124">**Element**</span></span>|<span data-ttu-id="fd022-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd022-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd022-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="fd022-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="fd022-127">Contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="fd022-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="fd022-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="fd022-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd022-129">Notas</span><span class="sxs-lookup"><span data-stu-id="fd022-129">Remarks</span></span>

<span data-ttu-id="fd022-130">Un contacto de un grupo que no tiene un buzón de correo es un ejemplo de un miembro de la lista de distribución que no tienen datos del calendario.</span><span class="sxs-lookup"><span data-stu-id="fd022-130">A contact in a group who does not have a mailbox is an example of a distribution list member who does not have calendar data.</span></span> <span data-ttu-id="fd022-131">Un contacto también puede tener el estado de **No haber datos** por los motivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd022-131">A contact may also have **No Data** status for the following reasons:</span></span> 
  
- <span data-ttu-id="fd022-132">Los permisos son insuficientes.</span><span class="sxs-lookup"><span data-stu-id="fd022-132">Permissions are insufficient.</span></span>
    
- <span data-ttu-id="fd022-133">La lista de distribución es demasiado grande para expandir.</span><span class="sxs-lookup"><span data-stu-id="fd022-133">The distribution list is too large to expand.</span></span>
    
- <span data-ttu-id="fd022-134">El servicio de directorio de Active Directory no está disponible.</span><span class="sxs-lookup"><span data-stu-id="fd022-134">The Active Directory directory service is unavailable.</span></span>
    
<span data-ttu-id="fd022-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="fd022-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd022-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fd022-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd022-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd022-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd022-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fd022-138">Schema Name</span></span>  <br/> |<span data-ttu-id="fd022-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fd022-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="fd022-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fd022-140">Validation File</span></span>  <br/> |<span data-ttu-id="fd022-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd022-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd022-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fd022-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd022-143">False</span><span class="sxs-lookup"><span data-stu-id="fd022-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd022-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="fd022-144">See also</span></span>



[<span data-ttu-id="fd022-145">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="fd022-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="fd022-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fd022-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="fd022-147">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="fd022-147">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


---
title: NumberOfMembersAvailable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersAvailable
api_type:
- schema
ms.assetid: e367a278-1622-4b65-955f-2d4b2fc6e4d7
description: El elemento NumberOfMembersAvailable representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida. Este elemento representa los miembros para los que el estado es libre.
ms.openlocfilehash: 947e1c133cc49fb7e322962e95e184fe77e09353
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462594"
---
# <a name="numberofmembersavailable"></a><span data-ttu-id="7393b-104">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="7393b-104">NumberOfMembersAvailable</span></span>

<span data-ttu-id="7393b-105">El elemento **NumberOfMembersAvailable** representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="7393b-105">The **NumberOfMembersAvailable** element represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="7393b-106">Este elemento representa los miembros para los que el estado es **libre**.</span><span class="sxs-lookup"><span data-stu-id="7393b-106">This element represents members for whom the status is **Free**.</span></span>
  
[<span data-ttu-id="7393b-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7393b-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="7393b-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="7393b-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="7393b-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="7393b-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="7393b-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="7393b-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="7393b-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="7393b-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="7393b-112">Alguna</span><span class="sxs-lookup"><span data-stu-id="7393b-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="7393b-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="7393b-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="7393b-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="7393b-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="7393b-115">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="7393b-115">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md)
  
```xml
<NumberOfMembersAvailable>...</NumberOfMembersAvailable>
```

 <span data-ttu-id="7393b-116">**int**</span><span class="sxs-lookup"><span data-stu-id="7393b-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7393b-117">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7393b-117">Attributes and elements</span></span>

<span data-ttu-id="7393b-118">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7393b-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7393b-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="7393b-119">Attributes</span></span>

<span data-ttu-id="7393b-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7393b-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7393b-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7393b-121">Child elements</span></span>

<span data-ttu-id="7393b-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7393b-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7393b-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7393b-123">Parent elements</span></span>

|<span data-ttu-id="7393b-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7393b-124">**Element**</span></span>|<span data-ttu-id="7393b-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7393b-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7393b-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="7393b-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="7393b-127">Contiene información de conflictos de agregados sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="7393b-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="7393b-128">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="7393b-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7393b-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7393b-129">Remarks</span></span>

<span data-ttu-id="7393b-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7393b-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7393b-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7393b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7393b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7393b-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7393b-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7393b-133">Schema Name</span></span>  <br/> |<span data-ttu-id="7393b-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7393b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="7393b-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7393b-135">Validation File</span></span>  <br/> |<span data-ttu-id="7393b-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7393b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7393b-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7393b-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="7393b-138">Falso</span><span class="sxs-lookup"><span data-stu-id="7393b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7393b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="7393b-139">See also</span></span>



[<span data-ttu-id="7393b-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="7393b-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="7393b-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7393b-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="7393b-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="7393b-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


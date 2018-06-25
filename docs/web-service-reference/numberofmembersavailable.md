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
description: El elemento NumberOfMembersAvailable representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida. Este elemento representa a los miembros para los que el estado es gratuita.
ms.openlocfilehash: 8669f61fbd640c160ad54739c5a15407b3dd470a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836641"
---
# <a name="numberofmembersavailable"></a><span data-ttu-id="f6791-104">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="f6791-104">NumberOfMembersAvailable</span></span>

<span data-ttu-id="f6791-105">El elemento **NumberOfMembersAvailable** representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="f6791-105">The **NumberOfMembersAvailable** element represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="f6791-106">Este elemento representa a los miembros para los que el estado es **gratuita**.</span><span class="sxs-lookup"><span data-stu-id="f6791-106">This element represents members for whom the status is **Free**.</span></span>
  
[<span data-ttu-id="f6791-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f6791-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="f6791-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="f6791-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="f6791-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="f6791-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="f6791-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="f6791-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="f6791-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="f6791-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="f6791-112">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="f6791-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="f6791-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="f6791-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="f6791-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f6791-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="f6791-115">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="f6791-115">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md)
  
```xml
<NumberOfMembersAvailable>...</NumberOfMembersAvailable>
```

 <span data-ttu-id="f6791-116">**int**</span><span class="sxs-lookup"><span data-stu-id="f6791-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6791-117">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f6791-117">Attributes and elements</span></span>

<span data-ttu-id="f6791-118">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f6791-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6791-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="f6791-119">Attributes</span></span>

<span data-ttu-id="f6791-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f6791-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6791-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f6791-121">Child elements</span></span>

<span data-ttu-id="f6791-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f6791-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f6791-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f6791-123">Parent elements</span></span>

|<span data-ttu-id="f6791-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6791-124">**Element**</span></span>|<span data-ttu-id="f6791-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6791-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6791-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f6791-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="f6791-127">Contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="f6791-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="f6791-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f6791-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6791-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6791-129">Remarks</span></span>

<span data-ttu-id="f6791-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f6791-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6791-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f6791-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6791-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6791-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6791-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f6791-133">Schema Name</span></span>  <br/> |<span data-ttu-id="f6791-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f6791-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f6791-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f6791-135">Validation File</span></span>  <br/> |<span data-ttu-id="f6791-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f6791-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6791-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f6791-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="f6791-138">False</span><span class="sxs-lookup"><span data-stu-id="f6791-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6791-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6791-139">See also</span></span>



[<span data-ttu-id="f6791-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f6791-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="f6791-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f6791-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="f6791-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="f6791-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


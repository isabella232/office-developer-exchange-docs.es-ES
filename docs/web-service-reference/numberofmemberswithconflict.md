---
title: NumberOfMembersWithConflict
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersWithConflict
api_type:
- schema
ms.assetid: e61154f7-d262-43ec-b2bf-1ba6804b28dc
description: El elemento NumberOfMembersWithConflict representa el número de miembros de la lista de distribución que tienen un conflicto con una hora de reunión sugerida. Este elemento representa a los integrantes que tengan un estado de ocupado, fuera de la oficina o provisional.
ms.openlocfilehash: 227783b4bed32686e8e098f88498fe8ebb25e3cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836634"
---
# <a name="numberofmemberswithconflict"></a><span data-ttu-id="0d786-104">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="0d786-104">NumberOfMembersWithConflict</span></span>

<span data-ttu-id="0d786-105">El elemento **NumberOfMembersWithConflict** representa el número de miembros de la lista de distribución que tienen un conflicto con una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="0d786-105">The **NumberOfMembersWithConflict** element represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="0d786-106">Este elemento representa a los integrantes que tengan un estado de **ocupado**, **fuera de la oficina**o **provisional**.</span><span class="sxs-lookup"><span data-stu-id="0d786-106">This element represents members who have a status of **Busy**, **OOF**, or **Tentative**.</span></span>
  
[<span data-ttu-id="0d786-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="0d786-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="0d786-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="0d786-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="0d786-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="0d786-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="0d786-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="0d786-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="0d786-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="0d786-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="0d786-112">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="0d786-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="0d786-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="0d786-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="0d786-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="0d786-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="0d786-115">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="0d786-115">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md)
  
```xml
<NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
```

 <span data-ttu-id="0d786-116">**int**</span><span class="sxs-lookup"><span data-stu-id="0d786-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d786-117">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d786-117">Attributes and elements</span></span>

<span data-ttu-id="0d786-118">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d786-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d786-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d786-119">Attributes</span></span>

<span data-ttu-id="0d786-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d786-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d786-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d786-121">Child elements</span></span>

<span data-ttu-id="0d786-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d786-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d786-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d786-123">Parent elements</span></span>

|<span data-ttu-id="0d786-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d786-124">**Element**</span></span>|<span data-ttu-id="0d786-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d786-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d786-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="0d786-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="0d786-127">Contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="0d786-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="0d786-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="0d786-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d786-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d786-129">Remarks</span></span>

<span data-ttu-id="0d786-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0d786-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d786-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d786-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d786-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d786-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d786-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d786-133">Schema Name</span></span>  <br/> |<span data-ttu-id="0d786-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0d786-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d786-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d786-135">Validation File</span></span>  <br/> |<span data-ttu-id="0d786-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0d786-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d786-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d786-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d786-138">False</span><span class="sxs-lookup"><span data-stu-id="0d786-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d786-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d786-139">See also</span></span>



[<span data-ttu-id="0d786-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="0d786-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="0d786-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="0d786-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="0d786-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="0d786-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


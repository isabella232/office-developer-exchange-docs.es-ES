---
title: NumberOfMembers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembers
api_type:
- schema
ms.assetid: 845fb877-de49-4e26-8885-6f026edd9ee9
description: El elemento NumberOfMembers representa el número de usuarios, recursos y salas de una lista de distribución.
ms.openlocfilehash: c91087f42d806afb0a0d3d607cc84f14a1a6c1b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462601"
---
# <a name="numberofmembers"></a><span data-ttu-id="ac70d-103">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="ac70d-103">NumberOfMembers</span></span>

<span data-ttu-id="ac70d-104">El elemento **NumberOfMembers** representa el número de usuarios, recursos y salas de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ac70d-104">The **NumberOfMembers** element represents the number of users, resources, and rooms in a distribution list.</span></span> 
  
[<span data-ttu-id="ac70d-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ac70d-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ac70d-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="ac70d-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="ac70d-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="ac70d-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="ac70d-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="ac70d-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="ac70d-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="ac70d-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="ac70d-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="ac70d-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="ac70d-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="ac70d-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="ac70d-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="ac70d-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="ac70d-113">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="ac70d-113">NumberOfMembers</span></span>](numberofmembers.md)
  
```xml
<NumberOfMembers>...</NumberOfMembers>
```

 <span data-ttu-id="ac70d-114">**int**</span><span class="sxs-lookup"><span data-stu-id="ac70d-114">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac70d-115">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ac70d-115">Attributes and elements</span></span>

<span data-ttu-id="ac70d-116">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ac70d-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac70d-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac70d-117">Attributes</span></span>

<span data-ttu-id="ac70d-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac70d-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac70d-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ac70d-119">Child elements</span></span>

<span data-ttu-id="ac70d-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac70d-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac70d-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ac70d-121">Parent elements</span></span>

|<span data-ttu-id="ac70d-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac70d-122">**Element**</span></span>|<span data-ttu-id="ac70d-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac70d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac70d-124">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="ac70d-124">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="ac70d-125">Contiene información de conflicto de agregados sobre el número de usuarios disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="ac70d-125">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="ac70d-126">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ac70d-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac70d-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac70d-127">Remarks</span></span>

<span data-ttu-id="ac70d-128">El valor máximo del elemento **NumberOfMembers** es 100.</span><span class="sxs-lookup"><span data-stu-id="ac70d-128">The maximum value of the **NumberOfMembers** element is 100.</span></span> 
  
<span data-ttu-id="ac70d-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ac70d-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac70d-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ac70d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac70d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac70d-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac70d-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ac70d-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ac70d-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ac70d-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac70d-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ac70d-134">Validation File</span></span>  <br/> |<span data-ttu-id="ac70d-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ac70d-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac70d-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ac70d-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac70d-137">Falso</span><span class="sxs-lookup"><span data-stu-id="ac70d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac70d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac70d-138">See also</span></span>



[<span data-ttu-id="ac70d-139">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ac70d-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ac70d-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ac70d-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ac70d-141">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ac70d-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


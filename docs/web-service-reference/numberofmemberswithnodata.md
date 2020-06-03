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
description: El elemento NumberOfMembersWithNoData representa el número de miembros de la lista de distribución que no han publicado datos de disponibilidad para compararlos con una hora de reunión sugerida. Este elemento representa los miembros de una lista de distribución que son demasiado grandes o miembros que no tienen el estado de los datos.
ms.openlocfilehash: df41adc14f4c35c0e24d0f3c54f74a63527859d6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462552"
---
# <a name="numberofmemberswithnodata"></a><span data-ttu-id="5a498-104">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="5a498-104">NumberOfMembersWithNoData</span></span>

<span data-ttu-id="5a498-105">El elemento **NumberOfMembersWithNoData** representa el número de miembros de la lista de distribución que no han publicado datos de disponibilidad para compararlos con una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="5a498-105">The **NumberOfMembersWithNoData** element represents the number of distribution list members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="5a498-106">Este elemento representa los miembros de una lista de distribución que son demasiado grandes o miembros que no tienen el estado de los **datos** .</span><span class="sxs-lookup"><span data-stu-id="5a498-106">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span> 
  
[<span data-ttu-id="5a498-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5a498-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="5a498-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="5a498-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="5a498-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="5a498-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="5a498-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="5a498-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="5a498-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="5a498-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="5a498-112">Alguna</span><span class="sxs-lookup"><span data-stu-id="5a498-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="5a498-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="5a498-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="5a498-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="5a498-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="5a498-115">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="5a498-115">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md)
  
```xml
<NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
```

 <span data-ttu-id="5a498-116">**int**</span><span class="sxs-lookup"><span data-stu-id="5a498-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a498-117">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5a498-117">Attributes and elements</span></span>

<span data-ttu-id="5a498-118">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5a498-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a498-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="5a498-119">Attributes</span></span>

<span data-ttu-id="5a498-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5a498-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a498-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a498-121">Child elements</span></span>

<span data-ttu-id="5a498-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5a498-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5a498-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5a498-123">Parent elements</span></span>

|<span data-ttu-id="5a498-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5a498-124">**Element**</span></span>|<span data-ttu-id="5a498-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a498-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a498-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="5a498-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="5a498-127">Contiene información de conflictos de agregados sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="5a498-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="5a498-128">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="5a498-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a498-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a498-129">Remarks</span></span>

<span data-ttu-id="5a498-130">Un contacto de un grupo que no tiene un buzón de correo es un ejemplo de un miembro de una lista de distribución que no tiene datos de calendario.</span><span class="sxs-lookup"><span data-stu-id="5a498-130">A contact in a group who does not have a mailbox is an example of a distribution list member who does not have calendar data.</span></span> <span data-ttu-id="5a498-131">Un contacto también puede no tener el estado de los **datos** por las siguientes razones:</span><span class="sxs-lookup"><span data-stu-id="5a498-131">A contact may also have **No Data** status for the following reasons:</span></span> 
  
- <span data-ttu-id="5a498-132">Permisos insuficientes.</span><span class="sxs-lookup"><span data-stu-id="5a498-132">Permissions are insufficient.</span></span>
    
- <span data-ttu-id="5a498-133">La lista de distribución es demasiado grande para expandirse.</span><span class="sxs-lookup"><span data-stu-id="5a498-133">The distribution list is too large to expand.</span></span>
    
- <span data-ttu-id="5a498-134">El servicio de directorio de Active Directory no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5a498-134">The Active Directory directory service is unavailable.</span></span>
    
<span data-ttu-id="5a498-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5a498-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a498-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5a498-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a498-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a498-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a498-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5a498-138">Schema Name</span></span>  <br/> |<span data-ttu-id="5a498-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5a498-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a498-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5a498-140">Validation File</span></span>  <br/> |<span data-ttu-id="5a498-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5a498-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a498-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5a498-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a498-143">Falso</span><span class="sxs-lookup"><span data-stu-id="5a498-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a498-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a498-144">See also</span></span>



[<span data-ttu-id="5a498-145">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="5a498-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="5a498-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5a498-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="5a498-147">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="5a498-147">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


---
title: IndividualAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndividualAttendeeConflictData
api_type:
- schema
ms.assetid: d45d3c34-abe1-40da-afd3-23bc5c3ef474
description: El elemento IndividualAttendeeConflictData contiene el estado de disponibilidad de un usuario o contacto para una ventana de tiempo que se produce al mismo tiempo que la hora de reunión sugerida identificada en el elemento de sugerencia.
ms.openlocfilehash: 55210230259b78e5ed9c4f0744aae003cf2e7ae5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459317"
---
# <a name="individualattendeeconflictdata"></a><span data-ttu-id="90f17-103">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="90f17-103">IndividualAttendeeConflictData</span></span>

<span data-ttu-id="90f17-104">El elemento **IndividualAttendeeConflictData** contiene el estado de disponibilidad de un usuario o contacto para una ventana de tiempo que se produce al mismo tiempo que la hora de reunión sugerida identificada en el elemento de [sugerencia](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="90f17-104">The **IndividualAttendeeConflictData** element contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
[<span data-ttu-id="90f17-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="90f17-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="90f17-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="90f17-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="90f17-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="90f17-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="90f17-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="90f17-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="90f17-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="90f17-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="90f17-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="90f17-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="90f17-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="90f17-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="90f17-112">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="90f17-112">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md)
  
```xml
<IndividualAttendeeConflictData>
   <BusyType>...</BusyType>
</IndividualAttendeeConflictData>
```

 <span data-ttu-id="90f17-113">**IndividualAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="90f17-113">**IndividualAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90f17-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="90f17-114">Attributes and elements</span></span>

<span data-ttu-id="90f17-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="90f17-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90f17-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="90f17-116">Attributes</span></span>

<span data-ttu-id="90f17-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="90f17-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90f17-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90f17-118">Child elements</span></span>

|<span data-ttu-id="90f17-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="90f17-119">**Element**</span></span>|<span data-ttu-id="90f17-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90f17-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90f17-121">BusyType</span><span class="sxs-lookup"><span data-stu-id="90f17-121">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="90f17-122">Representa el estado de disponibilidad de un usuario para una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="90f17-122">Represents the free/busy status of a user for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90f17-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="90f17-123">Parent elements</span></span>

|<span data-ttu-id="90f17-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="90f17-124">**Element**</span></span>|<span data-ttu-id="90f17-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90f17-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90f17-126">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="90f17-126">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="90f17-127">Contiene una matriz de datos conflictivos para los asistentes identificados en el [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span><span class="sxs-lookup"><span data-stu-id="90f17-127">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="90f17-128">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="90f17-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90f17-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90f17-129">Remarks</span></span>

<span data-ttu-id="90f17-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="90f17-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90f17-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="90f17-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90f17-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="90f17-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="90f17-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="90f17-133">Schema Name</span></span>  <br/> |<span data-ttu-id="90f17-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="90f17-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="90f17-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="90f17-135">Validation File</span></span>  <br/> |<span data-ttu-id="90f17-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="90f17-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="90f17-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="90f17-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="90f17-138">Falso</span><span class="sxs-lookup"><span data-stu-id="90f17-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90f17-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="90f17-139">See also</span></span>



[<span data-ttu-id="90f17-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="90f17-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="90f17-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="90f17-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="90f17-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="90f17-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


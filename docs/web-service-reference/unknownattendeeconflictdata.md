---
title: UnknownAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownAttendeeConflictData
api_type:
- schema
ms.assetid: 70e41268-c231-4587-9d23-e46927fe5272
description: El elemento UnknownAttendeeConflictData representa un asistente que no se ha podido resolver o un asistente que no es un usuario, una lista de distribución o un contacto.
ms.openlocfilehash: b4362e0117e3939c21342a1ab8079d95512aec79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459871"
---
# <a name="unknownattendeeconflictdata"></a><span data-ttu-id="8ed33-103">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="8ed33-103">UnknownAttendeeConflictData</span></span>

<span data-ttu-id="8ed33-104">El elemento **UnknownAttendeeConflictData** representa un asistente que no se ha podido resolver o un asistente que no es un usuario, una lista de distribución o un contacto.</span><span class="sxs-lookup"><span data-stu-id="8ed33-104">The **UnknownAttendeeConflictData** element represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span> 
  
[<span data-ttu-id="8ed33-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8ed33-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="8ed33-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="8ed33-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="8ed33-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="8ed33-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="8ed33-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="8ed33-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="8ed33-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="8ed33-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="8ed33-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="8ed33-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="8ed33-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="8ed33-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="8ed33-112">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="8ed33-112">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md)
  
```xml
<UnknownAttendeeConflictData/>
```

 <span data-ttu-id="8ed33-113">**UnknownAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="8ed33-113">**UnknownAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ed33-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8ed33-114">Attributes and elements</span></span>

<span data-ttu-id="8ed33-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8ed33-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ed33-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ed33-116">Attributes</span></span>

<span data-ttu-id="8ed33-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8ed33-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ed33-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8ed33-118">Child elements</span></span>

<span data-ttu-id="8ed33-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8ed33-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8ed33-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8ed33-120">Parent elements</span></span>

|<span data-ttu-id="8ed33-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8ed33-121">**Element**</span></span>|<span data-ttu-id="8ed33-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ed33-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ed33-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="8ed33-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="8ed33-124">Contiene una matriz de datos conflictivos para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="8ed33-124">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="8ed33-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="8ed33-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ed33-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ed33-126">Remarks</span></span>

<span data-ttu-id="8ed33-127">Un asistente es desconocido si no se puede resolver con un objeto del servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8ed33-127">An attendee is unknown if it cannot be resolved against an Active Directory directory service object.</span></span> <span data-ttu-id="8ed33-128">Un asistente no se resuelve si no se puede determinar que es un usuario, un grupo o un contacto.</span><span class="sxs-lookup"><span data-stu-id="8ed33-128">An attendee is unresolved if it cannot be determined to be a user, group, or contact.</span></span> <span data-ttu-id="8ed33-129">Por ejemplo, un asistente no se resolverá si es una carpeta pública habilitada para correo.</span><span class="sxs-lookup"><span data-stu-id="8ed33-129">For example, an attendee will not be resolved if it is a mail-enabled public folder.</span></span>
  
<span data-ttu-id="8ed33-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8ed33-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ed33-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8ed33-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ed33-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ed33-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ed33-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8ed33-133">Schema Name</span></span>  <br/> |<span data-ttu-id="8ed33-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8ed33-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="8ed33-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8ed33-135">Validation File</span></span>  <br/> |<span data-ttu-id="8ed33-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8ed33-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ed33-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8ed33-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ed33-138">Falso</span><span class="sxs-lookup"><span data-stu-id="8ed33-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ed33-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ed33-139">See also</span></span>



[<span data-ttu-id="8ed33-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="8ed33-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="8ed33-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8ed33-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="8ed33-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="8ed33-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


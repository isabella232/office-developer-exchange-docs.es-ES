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
description: El elemento UnknownAttendeeConflictData representa un asistente no se puede resolver o un asistente que no es un usuario, una lista de distribución o un contacto.
ms.openlocfilehash: 2363e243a833f580b4b5701b7d39d9ba9420f35a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840776"
---
# <a name="unknownattendeeconflictdata"></a><span data-ttu-id="320bd-103">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="320bd-103">UnknownAttendeeConflictData</span></span>

<span data-ttu-id="320bd-104">El elemento **UnknownAttendeeConflictData** representa un asistente no se puede resolver o un asistente que no es un usuario, una lista de distribución o un contacto.</span><span class="sxs-lookup"><span data-stu-id="320bd-104">The **UnknownAttendeeConflictData** element represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span> 
  
[<span data-ttu-id="320bd-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="320bd-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="320bd-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="320bd-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="320bd-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="320bd-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="320bd-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="320bd-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="320bd-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="320bd-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="320bd-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="320bd-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="320bd-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="320bd-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="320bd-112">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="320bd-112">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md)
  
```xml
<UnknownAttendeeConflictData/>
```

 <span data-ttu-id="320bd-113">**UnknownAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="320bd-113">**UnknownAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="320bd-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="320bd-114">Attributes and elements</span></span>

<span data-ttu-id="320bd-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="320bd-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="320bd-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="320bd-116">Attributes</span></span>

<span data-ttu-id="320bd-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="320bd-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="320bd-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="320bd-118">Child elements</span></span>

<span data-ttu-id="320bd-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="320bd-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="320bd-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="320bd-120">Parent elements</span></span>

|<span data-ttu-id="320bd-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="320bd-121">**Element**</span></span>|<span data-ttu-id="320bd-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="320bd-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="320bd-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="320bd-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="320bd-124">Contiene una matriz de datos en conflicto para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="320bd-124">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="320bd-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="320bd-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="320bd-126">Notas</span><span class="sxs-lookup"><span data-stu-id="320bd-126">Remarks</span></span>

<span data-ttu-id="320bd-127">Un asistente es desconocido, si no se resuelve en un objeto de servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="320bd-127">An attendee is unknown if it cannot be resolved against an Active Directory directory service object.</span></span> <span data-ttu-id="320bd-128">Un asistente está sin resolver si se no se puede determinar a ser un usuario, grupo o contacto.</span><span class="sxs-lookup"><span data-stu-id="320bd-128">An attendee is unresolved if it cannot be determined to be a user, group, or contact.</span></span> <span data-ttu-id="320bd-129">Por ejemplo, un asistente no se resuelven si es una carpeta pública habilitada para correo.</span><span class="sxs-lookup"><span data-stu-id="320bd-129">For example, an attendee will not be resolved if it is a mail-enabled public folder.</span></span>
  
<span data-ttu-id="320bd-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="320bd-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="320bd-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="320bd-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="320bd-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="320bd-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="320bd-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="320bd-133">Schema Name</span></span>  <br/> |<span data-ttu-id="320bd-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="320bd-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="320bd-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="320bd-135">Validation File</span></span>  <br/> |<span data-ttu-id="320bd-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="320bd-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="320bd-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="320bd-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="320bd-138">False</span><span class="sxs-lookup"><span data-stu-id="320bd-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="320bd-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="320bd-139">See also</span></span>



[<span data-ttu-id="320bd-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="320bd-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="320bd-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="320bd-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="320bd-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="320bd-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


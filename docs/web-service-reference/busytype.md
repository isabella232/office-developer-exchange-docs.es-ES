---
title: BusyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BusyType
api_type:
- schema
ms.assetid: 26d4fae0-8c78-4705-b5e8-d6033712c41e
description: El elemento BusyType representa el estado de libre/ocupado establecido para un evento del calendario.
ms.openlocfilehash: 6484bc70c6a05084e5d2bc1738b575fbebe4c132
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763693"
---
# <a name="busytype"></a><span data-ttu-id="7010f-103">BusyType</span><span class="sxs-lookup"><span data-stu-id="7010f-103">BusyType</span></span>

<span data-ttu-id="7010f-104">El elemento **BusyType** representa el estado de libre/ocupado establecido para un evento del calendario.</span><span class="sxs-lookup"><span data-stu-id="7010f-104">The **BusyType** element represents the free/busy status set for a calendar event.</span></span> 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 <span data-ttu-id="7010f-105">**BusyType**</span><span class="sxs-lookup"><span data-stu-id="7010f-105">**BusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7010f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7010f-106">Attributes and elements</span></span>

<span data-ttu-id="7010f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7010f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7010f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7010f-108">Attributes</span></span>

<span data-ttu-id="7010f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7010f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7010f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7010f-110">Child elements</span></span>

<span data-ttu-id="7010f-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7010f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7010f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7010f-112">Parent elements</span></span>

|<span data-ttu-id="7010f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7010f-113">**Element**</span></span>|<span data-ttu-id="7010f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7010f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7010f-115">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="7010f-115">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="7010f-116">Contiene el estado de disponibilidad de un usuario o un contacto para una ventana de tiempo que se produce al mismo tiempo, como el tiempo de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="7010f-116">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time.</span></span>  <br/> <span data-ttu-id="7010f-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="7010f-117">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[<span data-ttu-id="7010f-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="7010f-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="7010f-119">Representa una repetición del elemento de calendario único.</span><span class="sxs-lookup"><span data-stu-id="7010f-119">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="7010f-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="7010f-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7010f-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7010f-121">Text value</span></span>

<span data-ttu-id="7010f-122">Un valor de texto es necesario para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7010f-122">A text value is required for this element.</span></span> <span data-ttu-id="7010f-123">El valor es un tipo de cadena.</span><span class="sxs-lookup"><span data-stu-id="7010f-123">The value is a string type.</span></span> <span data-ttu-id="7010f-124">Los siguientes son los valores posibles para el elemento de [BusyType](busytype.md) :</span><span class="sxs-lookup"><span data-stu-id="7010f-124">The following are the possible values for the [BusyType](busytype.md) element:</span></span> 
  
- <span data-ttu-id="7010f-125">Gratuito</span><span class="sxs-lookup"><span data-stu-id="7010f-125">Free</span></span>
    
- <span data-ttu-id="7010f-126">Provisional</span><span class="sxs-lookup"><span data-stu-id="7010f-126">Tentative</span></span>
    
- <span data-ttu-id="7010f-127">Ocupado</span><span class="sxs-lookup"><span data-stu-id="7010f-127">Busy</span></span>
    
- <span data-ttu-id="7010f-128">FUERA DE LA OFICINA</span><span class="sxs-lookup"><span data-stu-id="7010f-128">OOF</span></span>
    
- <span data-ttu-id="7010f-129">NoData</span><span class="sxs-lookup"><span data-stu-id="7010f-129">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7010f-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7010f-130">Remarks</span></span>

<span data-ttu-id="7010f-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7010f-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7010f-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7010f-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7010f-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7010f-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7010f-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7010f-134">Schema Name</span></span>  <br/> |<span data-ttu-id="7010f-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7010f-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="7010f-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7010f-136">Validation File</span></span>  <br/> |<span data-ttu-id="7010f-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7010f-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7010f-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7010f-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="7010f-139">False</span><span class="sxs-lookup"><span data-stu-id="7010f-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7010f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7010f-140">See also</span></span>



[<span data-ttu-id="7010f-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="7010f-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="7010f-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7010f-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="7010f-143">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="7010f-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


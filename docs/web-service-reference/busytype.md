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
description: El elemento BusyType representa el estado de disponibilidad establecido para un evento de calendario.
ms.openlocfilehash: 7c2d18c21156a8603d3caeeb796a56c5d8afcba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459086"
---
# <a name="busytype"></a><span data-ttu-id="d8fd2-103">BusyType</span><span class="sxs-lookup"><span data-stu-id="d8fd2-103">BusyType</span></span>

<span data-ttu-id="d8fd2-104">El elemento **BusyType** representa el estado de disponibilidad establecido para un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-104">The **BusyType** element represents the free/busy status set for a calendar event.</span></span> 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 <span data-ttu-id="d8fd2-105">**BusyType**</span><span class="sxs-lookup"><span data-stu-id="d8fd2-105">**BusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8fd2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d8fd2-106">Attributes and elements</span></span>

<span data-ttu-id="d8fd2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8fd2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8fd2-108">Attributes</span></span>

<span data-ttu-id="d8fd2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8fd2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d8fd2-110">Child elements</span></span>

<span data-ttu-id="d8fd2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d8fd2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d8fd2-112">Parent elements</span></span>

|<span data-ttu-id="d8fd2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d8fd2-113">**Element**</span></span>|<span data-ttu-id="d8fd2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8fd2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8fd2-115">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="d8fd2-115">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="d8fd2-116">Contiene el estado de disponibilidad de un usuario o contacto para una ventana de tiempo que se produce al mismo tiempo que la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-116">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time.</span></span>  <br/> <span data-ttu-id="d8fd2-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="d8fd2-117">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[<span data-ttu-id="d8fd2-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="d8fd2-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="d8fd2-119">Representa una ocurrencia única del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-119">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="d8fd2-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="d8fd2-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d8fd2-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d8fd2-121">Text value</span></span>

<span data-ttu-id="d8fd2-122">Se requiere un valor de texto para este elemento.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-122">A text value is required for this element.</span></span> <span data-ttu-id="d8fd2-123">El valor es un tipo de cadena.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-123">The value is a string type.</span></span> <span data-ttu-id="d8fd2-124">A continuación se muestran los valores posibles para el elemento [BusyType](busytype.md) :</span><span class="sxs-lookup"><span data-stu-id="d8fd2-124">The following are the possible values for the [BusyType](busytype.md) element:</span></span> 
  
- <span data-ttu-id="d8fd2-125">Libre</span><span class="sxs-lookup"><span data-stu-id="d8fd2-125">Free</span></span>
    
- <span data-ttu-id="d8fd2-126">Provisional</span><span class="sxs-lookup"><span data-stu-id="d8fd2-126">Tentative</span></span>
    
- <span data-ttu-id="d8fd2-127">Ocupado</span><span class="sxs-lookup"><span data-stu-id="d8fd2-127">Busy</span></span>
    
- <span data-ttu-id="d8fd2-128">Oficina</span><span class="sxs-lookup"><span data-stu-id="d8fd2-128">OOF</span></span>
    
- <span data-ttu-id="d8fd2-129">NoData</span><span class="sxs-lookup"><span data-stu-id="d8fd2-129">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8fd2-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8fd2-130">Remarks</span></span>

<span data-ttu-id="d8fd2-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8fd2-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d8fd2-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8fd2-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8fd2-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8fd2-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d8fd2-134">Schema Name</span></span>  <br/> |<span data-ttu-id="d8fd2-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d8fd2-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="d8fd2-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d8fd2-136">Validation File</span></span>  <br/> |<span data-ttu-id="d8fd2-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d8fd2-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8fd2-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d8fd2-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8fd2-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d8fd2-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8fd2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8fd2-140">See also</span></span>



[<span data-ttu-id="d8fd2-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="d8fd2-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="d8fd2-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d8fd2-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="d8fd2-143">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="d8fd2-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


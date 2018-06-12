---
title: RecurrenceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: El elemento RecurrenceId se usa para identificar una instancia específica de un elemento periódico del calendario.
ms.openlocfilehash: 078bec85e1ca1530137f9935365d7dd3e530ea34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837005"
---
# <a name="recurrenceid"></a><span data-ttu-id="d633b-103">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="d633b-103">RecurrenceId</span></span>

<span data-ttu-id="d633b-104">El elemento **RecurrenceId** se usa para identificar una instancia específica de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="d633b-104">The **RecurrenceId** element is used to identify a specific instance of a recurring calendar item.</span></span> 
  
```xml
<RecurrenceId/>
```

 <span data-ttu-id="d633b-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="d633b-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d633b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d633b-106">Attributes and elements</span></span>

<span data-ttu-id="d633b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d633b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d633b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d633b-108">Attributes</span></span>

<span data-ttu-id="d633b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d633b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d633b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d633b-110">Child elements</span></span>

<span data-ttu-id="d633b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d633b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d633b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d633b-112">Parent elements</span></span>

|<span data-ttu-id="d633b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d633b-113">**Element**</span></span>|<span data-ttu-id="d633b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d633b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d633b-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d633b-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d633b-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d633b-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d633b-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="d633b-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="d633b-118">Representa un mensaje de reunión.</span><span class="sxs-lookup"><span data-stu-id="d633b-118">Represents a meeting message.</span></span>  <br/> |
|[<span data-ttu-id="d633b-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d633b-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d633b-120">Representa una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="d633b-120">Represents a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="d633b-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d633b-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="d633b-122">Representa una respuesta a la reunión.</span><span class="sxs-lookup"><span data-stu-id="d633b-122">Represents a meeting response.</span></span>  <br/> |
|[<span data-ttu-id="d633b-123">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="d633b-123">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="d633b-124">Representa la cancelación de la reunión.</span><span class="sxs-lookup"><span data-stu-id="d633b-124">Represents a meeting cancellation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d633b-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d633b-125">Text value</span></span>

<span data-ttu-id="d633b-126">El valor de texto representa un valor de fecha y hora que identifica una ocurrencia de calendario.</span><span class="sxs-lookup"><span data-stu-id="d633b-126">The text value represents a date/time value that identifies a calendar occurrence.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d633b-127">Notas</span><span class="sxs-lookup"><span data-stu-id="d633b-127">Remarks</span></span>

<span data-ttu-id="d633b-128">Esta propiedad se utiliza con la propiedad [UID](uid.md) para identificar una instancia específica de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="d633b-128">This property is used with the [UID](uid.md) property to identify a specific instance of a recurring calendar item.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d633b-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d633b-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d633b-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d633b-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d633b-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d633b-131">Schema Name</span></span>  <br/> |<span data-ttu-id="d633b-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d633b-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="d633b-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d633b-133">Validation File</span></span>  <br/> |<span data-ttu-id="d633b-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d633b-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d633b-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d633b-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="d633b-136">False</span><span class="sxs-lookup"><span data-stu-id="d633b-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d633b-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="d633b-137">See also</span></span>



- [<span data-ttu-id="d633b-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d633b-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


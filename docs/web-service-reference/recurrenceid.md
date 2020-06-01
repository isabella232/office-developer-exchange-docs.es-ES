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
description: El elemento RecurrenceId se usa para identificar una instancia específica de un elemento de calendario periódico.
ms.openlocfilehash: 58a379f2cffa7ff37181e93ad1c45c9752e84f1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461614"
---
# <a name="recurrenceid"></a><span data-ttu-id="6f936-103">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="6f936-103">RecurrenceId</span></span>

<span data-ttu-id="6f936-104">El elemento **RecurrenceId** se usa para identificar una instancia específica de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="6f936-104">The **RecurrenceId** element is used to identify a specific instance of a recurring calendar item.</span></span> 
  
```xml
<RecurrenceId/>
```

 <span data-ttu-id="6f936-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="6f936-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f936-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f936-106">Attributes and elements</span></span>

<span data-ttu-id="6f936-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f936-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f936-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f936-108">Attributes</span></span>

<span data-ttu-id="6f936-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6f936-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f936-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f936-110">Child elements</span></span>

<span data-ttu-id="6f936-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6f936-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f936-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f936-112">Parent elements</span></span>

|<span data-ttu-id="6f936-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f936-113">**Element**</span></span>|<span data-ttu-id="6f936-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f936-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f936-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="6f936-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="6f936-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f936-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="6f936-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="6f936-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="6f936-118">Representa un mensaje de reunión.</span><span class="sxs-lookup"><span data-stu-id="6f936-118">Represents a meeting message.</span></span>  <br/> |
|[<span data-ttu-id="6f936-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="6f936-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="6f936-120">Representa una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6f936-120">Represents a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6f936-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="6f936-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="6f936-122">Representa una respuesta a la reunión.</span><span class="sxs-lookup"><span data-stu-id="6f936-122">Represents a meeting response.</span></span>  <br/> |
|[<span data-ttu-id="6f936-123">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="6f936-123">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="6f936-124">Representa una cancelación de reunión.</span><span class="sxs-lookup"><span data-stu-id="6f936-124">Represents a meeting cancellation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f936-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6f936-125">Text value</span></span>

<span data-ttu-id="6f936-126">El valor de texto representa un valor de fecha y hora que identifica una ocurrencia del calendario.</span><span class="sxs-lookup"><span data-stu-id="6f936-126">The text value represents a date/time value that identifies a calendar occurrence.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f936-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f936-127">Remarks</span></span>

<span data-ttu-id="6f936-128">Esta propiedad se utiliza con la propiedad [UID](uid.md) para identificar una instancia específica de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="6f936-128">This property is used with the [UID](uid.md) property to identify a specific instance of a recurring calendar item.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6f936-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6f936-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f936-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f936-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f936-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6f936-131">Schema Name</span></span>  <br/> |<span data-ttu-id="6f936-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6f936-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f936-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6f936-133">Validation File</span></span>  <br/> |<span data-ttu-id="6f936-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6f936-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f936-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f936-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f936-136">Falso</span><span class="sxs-lookup"><span data-stu-id="6f936-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f936-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f936-137">See also</span></span>



- [<span data-ttu-id="6f936-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6f936-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


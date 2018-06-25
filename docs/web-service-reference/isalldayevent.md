---
title: IsAllDayEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAllDayEvent
api_type:
- schema
ms.assetid: 29140a64-9d7a-4a14-a10d-c98197c9831b
description: El elemento IsAllDayEvent indica si una convocatoria de reunión o elemento de calendario representa un evento de día completo.
ms.openlocfilehash: 81cf1e7d8338275540f264de7cbf194005e7770c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835983"
---
# <a name="isalldayevent"></a><span data-ttu-id="be54d-103">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="be54d-103">IsAllDayEvent</span></span>

<span data-ttu-id="be54d-104">El elemento **IsAllDayEvent** indica si una convocatoria de reunión o elemento de calendario representa un evento de día completo.</span><span class="sxs-lookup"><span data-stu-id="be54d-104">The **IsAllDayEvent** element indicates whether a calendar item or meeting request represents an all-day event.</span></span> 
  
```xml
<IsAllDayEvent/>
```

 <span data-ttu-id="be54d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="be54d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be54d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="be54d-106">Attributes and elements</span></span>

<span data-ttu-id="be54d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="be54d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be54d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="be54d-108">Attributes</span></span>

<span data-ttu-id="be54d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="be54d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be54d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="be54d-110">Child elements</span></span>

<span data-ttu-id="be54d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="be54d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="be54d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="be54d-112">Parent elements</span></span>

|<span data-ttu-id="be54d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="be54d-113">**Element**</span></span>|<span data-ttu-id="be54d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be54d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be54d-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="be54d-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="be54d-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="be54d-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="be54d-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="be54d-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="be54d-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="be54d-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="be54d-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="be54d-119">Text value</span></span>

<span data-ttu-id="be54d-120">Si este elemento se incluye, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="be54d-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="be54d-121">Un valor de **true** indica que el elemento representa un evento de día completo.</span><span class="sxs-lookup"><span data-stu-id="be54d-121">A value of **true** indicates that the item represents an all-day event.</span></span> <span data-ttu-id="be54d-122">Un valor de **false** indica que el elemento se ocupa menos de horas de trabajo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="be54d-122">A value of **false** indicates that the item spans less than a user's working hours.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="be54d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be54d-123">Remarks</span></span>

<span data-ttu-id="be54d-124">Un evento de día completo abarca la duración de horas de trabajo que se define para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="be54d-124">An all-day event spans the duration of working hours that is defined for a mailbox.</span></span>
  
<span data-ttu-id="be54d-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="be54d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be54d-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="be54d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be54d-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="be54d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be54d-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="be54d-128">Schema name</span></span>  <br/> |<span data-ttu-id="be54d-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="be54d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="be54d-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="be54d-130">Validation file</span></span>  <br/> |<span data-ttu-id="be54d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="be54d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="be54d-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="be54d-132">Can be empty</span></span>  <br/> |<span data-ttu-id="be54d-133">False</span><span class="sxs-lookup"><span data-stu-id="be54d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be54d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="be54d-134">See also</span></span>



- [<span data-ttu-id="be54d-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="be54d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


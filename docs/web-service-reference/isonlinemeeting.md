---
title: IsOnlineMeeting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsOnlineMeeting
api_type:
- schema
ms.assetid: c29df676-0f3a-4694-a42f-522c6d16872f
description: El elemento IsOnlineMeeting indica si la reunión está en línea.
ms.openlocfilehash: 5a56b0b9828d6f6bec83fc0ad0f8f9579b471a72
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836061"
---
# <a name="isonlinemeeting"></a><span data-ttu-id="8af66-103">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="8af66-103">IsOnlineMeeting</span></span>

<span data-ttu-id="8af66-104">El elemento **IsOnlineMeeting** indica si la reunión está en línea.</span><span class="sxs-lookup"><span data-stu-id="8af66-104">The **IsOnlineMeeting** element indicates whether the meeting is online.</span></span> 
  
```xml
<IsOnlineMeeting/>
```

 <span data-ttu-id="8af66-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8af66-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8af66-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8af66-106">Attributes and elements</span></span>

<span data-ttu-id="8af66-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8af66-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8af66-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8af66-108">Attributes</span></span>

<span data-ttu-id="8af66-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8af66-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8af66-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8af66-110">Child elements</span></span>

<span data-ttu-id="8af66-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8af66-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8af66-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8af66-112">Parent elements</span></span>

|<span data-ttu-id="8af66-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8af66-113">**Element**</span></span>|<span data-ttu-id="8af66-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8af66-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8af66-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8af66-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8af66-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8af66-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8af66-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8af66-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8af66-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8af66-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8af66-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8af66-119">Text value</span></span>

<span data-ttu-id="8af66-120">Si se usa este elemento, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="8af66-120">A text value that represents a Boolean value is required if this element is used.</span></span> <span data-ttu-id="8af66-121">Un valor de **true** indica que la reunión está en línea.</span><span class="sxs-lookup"><span data-stu-id="8af66-121">A value of **true** indicates that the meeting is online.</span></span> <span data-ttu-id="8af66-122">Un valor de **false** indica que la reunión no está en línea.</span><span class="sxs-lookup"><span data-stu-id="8af66-122">A value of **false** indicates that the meeting is not online.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8af66-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8af66-123">Remarks</span></span>

<span data-ttu-id="8af66-124">La propiedad IsOnlineMeeting es lectura escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="8af66-124">The IsOnlineMeeting property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="8af66-125">Es de sólo lectura para las convocatorias de reunión y elementos de calendario de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="8af66-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="8af66-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8af66-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8af66-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8af66-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8af66-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8af66-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8af66-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8af66-129">Schema name</span></span>  <br/> |<span data-ttu-id="8af66-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8af66-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="8af66-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8af66-131">Validation file</span></span>  <br/> |<span data-ttu-id="8af66-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8af66-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8af66-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8af66-133">Can be empty</span></span>  <br/> |<span data-ttu-id="8af66-134">False</span><span class="sxs-lookup"><span data-stu-id="8af66-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8af66-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8af66-135">See also</span></span>



- [<span data-ttu-id="8af66-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8af66-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


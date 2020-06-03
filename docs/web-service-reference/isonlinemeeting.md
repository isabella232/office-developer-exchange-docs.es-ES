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
ms.openlocfilehash: d2d60c8a51ad7e03c33b57709d9173e79d162268
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460403"
---
# <a name="isonlinemeeting"></a><span data-ttu-id="3a715-103">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="3a715-103">IsOnlineMeeting</span></span>

<span data-ttu-id="3a715-104">El elemento **IsOnlineMeeting** indica si la reunión está en línea.</span><span class="sxs-lookup"><span data-stu-id="3a715-104">The **IsOnlineMeeting** element indicates whether the meeting is online.</span></span> 
  
```xml
<IsOnlineMeeting/>
```

 <span data-ttu-id="3a715-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3a715-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a715-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a715-106">Attributes and elements</span></span>

<span data-ttu-id="3a715-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a715-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a715-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a715-108">Attributes</span></span>

<span data-ttu-id="3a715-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3a715-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a715-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a715-110">Child elements</span></span>

<span data-ttu-id="3a715-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3a715-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3a715-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a715-112">Parent elements</span></span>

|<span data-ttu-id="3a715-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a715-113">**Element**</span></span>|<span data-ttu-id="3a715-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a715-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a715-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3a715-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3a715-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a715-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a715-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3a715-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3a715-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a715-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a715-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3a715-119">Text value</span></span>

<span data-ttu-id="3a715-120">Si se usa este elemento, es necesario un valor de texto que represente un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="3a715-120">A text value that represents a Boolean value is required if this element is used.</span></span> <span data-ttu-id="3a715-121">Un valor de **true** indica que la reunión está en línea.</span><span class="sxs-lookup"><span data-stu-id="3a715-121">A value of **true** indicates that the meeting is online.</span></span> <span data-ttu-id="3a715-122">Un valor de **false** indica que la reunión no está en línea.</span><span class="sxs-lookup"><span data-stu-id="3a715-122">A value of **false** indicates that the meeting is not online.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3a715-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a715-123">Remarks</span></span>

<span data-ttu-id="3a715-124">La propiedad IsOnlineMeeting es de lectura y escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="3a715-124">The IsOnlineMeeting property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="3a715-125">Es de solo lectura para las convocatorias de reunión y para los elementos de calendario de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="3a715-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="3a715-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3a715-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a715-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a715-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a715-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a715-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a715-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a715-129">Schema name</span></span>  <br/> |<span data-ttu-id="3a715-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3a715-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a715-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a715-131">Validation file</span></span>  <br/> |<span data-ttu-id="3a715-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3a715-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a715-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a715-133">Can be empty</span></span>  <br/> |<span data-ttu-id="3a715-134">Falso</span><span class="sxs-lookup"><span data-stu-id="3a715-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a715-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a715-135">See also</span></span>



- [<span data-ttu-id="3a715-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3a715-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


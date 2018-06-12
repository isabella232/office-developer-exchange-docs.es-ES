---
title: ConferenceType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConferenceType
api_type:
- schema
ms.assetid: 6bcf6c18-2695-44b1-aabe-dadc52b2633a
description: El elemento ConferenceType describe el tipo de conferencia que se lleva a cabo con un elemento de calendario.
ms.openlocfilehash: d312420606c5e1914fe321ae7c7c512f0833199c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763764"
---
# <a name="conferencetype"></a><span data-ttu-id="e3575-103">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="e3575-103">ConferenceType</span></span>

<span data-ttu-id="e3575-104">El elemento **ConferenceType** describe el tipo de conferencia que se lleva a cabo con un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="e3575-104">The **ConferenceType** element describes the type of conferencing that is performed with a calendar item.</span></span> 
  
```xml
<ConferenceType/>
```

 <span data-ttu-id="e3575-105">**int**</span><span class="sxs-lookup"><span data-stu-id="e3575-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3575-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e3575-106">Attributes and elements</span></span>

<span data-ttu-id="e3575-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e3575-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3575-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e3575-108">Attributes</span></span>

<span data-ttu-id="e3575-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e3575-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3575-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e3575-110">Child elements</span></span>

<span data-ttu-id="e3575-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e3575-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3575-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e3575-112">Parent elements</span></span>

|<span data-ttu-id="e3575-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3575-113">**Element**</span></span>|<span data-ttu-id="e3575-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e3575-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3575-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e3575-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e3575-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3575-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e3575-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e3575-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e3575-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3575-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3575-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e3575-119">Text value</span></span>

<span data-ttu-id="e3575-120">Si se usa este elemento, se requiere un valor de texto que representa un valor entero.</span><span class="sxs-lookup"><span data-stu-id="e3575-120">A text value that represents an integer value is required if this element is used.</span></span> <span data-ttu-id="e3575-121">Los siguientes son los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="e3575-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="e3575-122">0 = NetMeeting</span><span class="sxs-lookup"><span data-stu-id="e3575-122">0 = NetMeeting</span></span>
    
- <span data-ttu-id="e3575-123">1 = NetShow</span><span class="sxs-lookup"><span data-stu-id="e3575-123">1 = NetShow</span></span>
    
- <span data-ttu-id="e3575-124">2 = chat</span><span class="sxs-lookup"><span data-stu-id="e3575-124">2 = Chat</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3575-125">Notas</span><span class="sxs-lookup"><span data-stu-id="e3575-125">Remarks</span></span>

<span data-ttu-id="e3575-126">La propiedad **MeetingWorkspaceUrl** es modificable para la lectura de elemento de calendario del organizador de la.</span><span class="sxs-lookup"><span data-stu-id="e3575-126">The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="e3575-127">Es de sólo lectura para las convocatorias de reunión y elementos de calendario del asistente.</span><span class="sxs-lookup"><span data-stu-id="e3575-127">It is read-only for meeting requests and for attendee's calendar items.</span></span> 
  
<span data-ttu-id="e3575-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e3575-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e3575-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e3575-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3575-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e3575-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3575-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e3575-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e3575-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e3575-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e3575-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e3575-133">Validation File</span></span>  <br/> |<span data-ttu-id="e3575-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e3575-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3575-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e3575-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3575-136">False</span><span class="sxs-lookup"><span data-stu-id="e3575-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3575-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="e3575-137">See also</span></span>



- [<span data-ttu-id="e3575-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e3575-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


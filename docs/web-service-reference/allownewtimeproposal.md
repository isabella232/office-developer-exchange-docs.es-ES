---
title: AllowNewTimeProposal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowNewTimeProposal
api_type:
- schema
ms.assetid: afdb4ec9-2daf-48a1-a0bb-a7f647f212f2
description: El elemento AllowNewTimeProposal indica si un asistente puede proponer una nueva hora de reunión para una reunión.
ms.openlocfilehash: d5deed5044769c477ffe54cc533d5261ba2e1932
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763427"
---
# <a name="allownewtimeproposal"></a><span data-ttu-id="1c65e-103">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="1c65e-103">AllowNewTimeProposal</span></span>

<span data-ttu-id="1c65e-104">El elemento **AllowNewTimeProposal** indica si un asistente puede proponer una nueva hora de reunión para una reunión.</span><span class="sxs-lookup"><span data-stu-id="1c65e-104">The **AllowNewTimeProposal** element indicates whether a new meeting time can be proposed for a meeting by an attendee.</span></span> 
  
```xml
<AllowNewTimeProposal/>
```

 <span data-ttu-id="1c65e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1c65e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c65e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1c65e-106">Attributes and elements</span></span>

<span data-ttu-id="1c65e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1c65e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c65e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1c65e-108">Attributes</span></span>

<span data-ttu-id="1c65e-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1c65e-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c65e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1c65e-110">Child elements</span></span>

<span data-ttu-id="1c65e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1c65e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1c65e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1c65e-112">Parent elements</span></span>

|<span data-ttu-id="1c65e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c65e-113">**Element**</span></span>|<span data-ttu-id="1c65e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1c65e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c65e-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1c65e-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1c65e-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1c65e-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1c65e-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1c65e-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1c65e-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1c65e-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1c65e-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1c65e-119">Text value</span></span>

<span data-ttu-id="1c65e-120">Se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="1c65e-120">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="1c65e-121">Un valor de **true** indica que se puede crear una nueva propuesta para el tiempo de la reunión; un valor de **false** indica que no se permiten nuevas propuestas de plazos.</span><span class="sxs-lookup"><span data-stu-id="1c65e-121">A value of **true** indicates that a new proposal for the meeting time can be created; a value of **false** indicates that new time proposals are not allowed.</span></span> <span data-ttu-id="1c65e-122">El organizador establece este valor en la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="1c65e-122">The organizer sets this value in the meeting request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1c65e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c65e-123">Remarks</span></span>

<span data-ttu-id="1c65e-124">La propiedad AllowNewTimeProposal es lectura escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="1c65e-124">The AllowNewTimeProposal property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="1c65e-125">Es de sólo lectura para las convocatorias de reunión y elementos de calendario de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="1c65e-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="1c65e-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1c65e-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1c65e-127">Servicios Web de Exchange no es compatible con los nuevos mensajes de propuesta de tiempo.</span><span class="sxs-lookup"><span data-stu-id="1c65e-127">Exchange Web Services does not support new time proposal messages.</span></span> <span data-ttu-id="1c65e-128">Para obtener las propiedades que están relacionadas con los nuevos mensajes de propuesta de tiempo, utilice las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="1c65e-128">To get properties that are related to new time proposal messages, use extended properties.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1c65e-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1c65e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c65e-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1c65e-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c65e-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1c65e-131">Schema name</span></span>  <br/> |<span data-ttu-id="1c65e-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1c65e-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="1c65e-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1c65e-133">Validation file</span></span>  <br/> |<span data-ttu-id="1c65e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1c65e-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c65e-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1c65e-135">Can be empty</span></span>  <br/> |<span data-ttu-id="1c65e-136">False</span><span class="sxs-lookup"><span data-stu-id="1c65e-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c65e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c65e-137">See also</span></span>

- [<span data-ttu-id="1c65e-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1c65e-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


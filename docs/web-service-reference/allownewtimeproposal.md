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
ms.openlocfilehash: b3f2c569bced08c66144680a4fddd6e8bac0cecf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464808"
---
# <a name="allownewtimeproposal"></a><span data-ttu-id="41493-103">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="41493-103">AllowNewTimeProposal</span></span>

<span data-ttu-id="41493-104">El elemento **AllowNewTimeProposal** indica si un asistente puede proponer una nueva hora de reunión para una reunión.</span><span class="sxs-lookup"><span data-stu-id="41493-104">The **AllowNewTimeProposal** element indicates whether a new meeting time can be proposed for a meeting by an attendee.</span></span> 
  
```xml
<AllowNewTimeProposal/>
```

 <span data-ttu-id="41493-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="41493-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41493-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="41493-106">Attributes and elements</span></span>

<span data-ttu-id="41493-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="41493-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41493-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="41493-108">Attributes</span></span>

<span data-ttu-id="41493-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="41493-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41493-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41493-110">Child elements</span></span>

<span data-ttu-id="41493-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="41493-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41493-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="41493-112">Parent elements</span></span>

|<span data-ttu-id="41493-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="41493-113">**Element**</span></span>|<span data-ttu-id="41493-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41493-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41493-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="41493-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="41493-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="41493-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="41493-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="41493-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="41493-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="41493-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41493-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="41493-119">Text value</span></span>

<span data-ttu-id="41493-120">Se requiere un valor de texto que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="41493-120">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="41493-121">Un valor de **true** indica que se puede crear una nueva propuesta para la hora de la reunión; un valor de **false** indica que no se permiten nuevas propuestas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="41493-121">A value of **true** indicates that a new proposal for the meeting time can be created; a value of **false** indicates that new time proposals are not allowed.</span></span> <span data-ttu-id="41493-122">El organizador establece este valor en la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="41493-122">The organizer sets this value in the meeting request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="41493-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41493-123">Remarks</span></span>

<span data-ttu-id="41493-124">La propiedad AllowNewTimeProposal es de lectura y escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="41493-124">The AllowNewTimeProposal property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="41493-125">Es de solo lectura para las convocatorias de reunión y para los elementos de calendario de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="41493-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="41493-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="41493-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="41493-127">Los servicios web Exchange no admiten nuevos mensajes de propuesta de hora.</span><span class="sxs-lookup"><span data-stu-id="41493-127">Exchange Web Services does not support new time proposal messages.</span></span> <span data-ttu-id="41493-128">Para obtener las propiedades relacionadas con los mensajes de nueva propuesta de hora, use propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="41493-128">To get properties that are related to new time proposal messages, use extended properties.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="41493-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="41493-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41493-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="41493-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41493-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="41493-131">Schema name</span></span>  <br/> |<span data-ttu-id="41493-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="41493-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="41493-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="41493-133">Validation file</span></span>  <br/> |<span data-ttu-id="41493-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="41493-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41493-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="41493-135">Can be empty</span></span>  <br/> |<span data-ttu-id="41493-136">Falso</span><span class="sxs-lookup"><span data-stu-id="41493-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41493-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="41493-137">See also</span></span>

- [<span data-ttu-id="41493-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="41493-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


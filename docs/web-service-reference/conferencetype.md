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
description: El elemento ConferenceType describe el tipo de conferencia que se realiza con un elemento de calendario.
ms.openlocfilehash: 482fc09d709e2b151b255107af59cb98de236aec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463933"
---
# <a name="conferencetype"></a><span data-ttu-id="b1ecc-103">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="b1ecc-103">ConferenceType</span></span>

<span data-ttu-id="b1ecc-104">El elemento **ConferenceType** describe el tipo de conferencia que se realiza con un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-104">The **ConferenceType** element describes the type of conferencing that is performed with a calendar item.</span></span> 
  
```xml
<ConferenceType/>
```

 <span data-ttu-id="b1ecc-105">**int**</span><span class="sxs-lookup"><span data-stu-id="b1ecc-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1ecc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1ecc-106">Attributes and elements</span></span>

<span data-ttu-id="b1ecc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1ecc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1ecc-108">Attributes</span></span>

<span data-ttu-id="b1ecc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1ecc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1ecc-110">Child elements</span></span>

<span data-ttu-id="b1ecc-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1ecc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1ecc-112">Parent elements</span></span>

|<span data-ttu-id="b1ecc-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b1ecc-113">**Element**</span></span>|<span data-ttu-id="b1ecc-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1ecc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1ecc-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b1ecc-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b1ecc-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b1ecc-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b1ecc-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b1ecc-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b1ecc-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b1ecc-119">Text value</span></span>

<span data-ttu-id="b1ecc-120">Si se usa este elemento, es necesario un valor de texto que represente un valor entero.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-120">A text value that represents an integer value is required if this element is used.</span></span> <span data-ttu-id="b1ecc-121">A continuación se muestran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b1ecc-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="b1ecc-122">0 = NetMeeting</span><span class="sxs-lookup"><span data-stu-id="b1ecc-122">0 = NetMeeting</span></span>
    
- <span data-ttu-id="b1ecc-123">1 = NetShow</span><span class="sxs-lookup"><span data-stu-id="b1ecc-123">1 = NetShow</span></span>
    
- <span data-ttu-id="b1ecc-124">2 = chat</span><span class="sxs-lookup"><span data-stu-id="b1ecc-124">2 = Chat</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1ecc-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1ecc-125">Remarks</span></span>

<span data-ttu-id="b1ecc-126">La propiedad **MeetingWorkspaceUrl** es de lectura y escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-126">The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="b1ecc-127">Es de solo lectura para las convocatorias de reunión y para los elementos de calendario del asistente.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-127">It is read-only for meeting requests and for attendee's calendar items.</span></span> 
  
<span data-ttu-id="b1ecc-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b1ecc-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b1ecc-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1ecc-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1ecc-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b1ecc-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b1ecc-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b1ecc-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b1ecc-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b1ecc-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b1ecc-133">Validation File</span></span>  <br/> |<span data-ttu-id="b1ecc-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b1ecc-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b1ecc-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1ecc-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1ecc-136">Falso</span><span class="sxs-lookup"><span data-stu-id="b1ecc-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1ecc-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1ecc-137">See also</span></span>



- [<span data-ttu-id="b1ecc-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b1ecc-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


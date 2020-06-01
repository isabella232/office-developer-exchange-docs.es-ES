---
title: ReplyTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyTo
api_type:
- schema
ms.assetid: 6b6ae792-e2c4-4aa0-95cb-b49b446f1e08
description: El elemento ReplyTo identifica una matriz de direcciones a la que se deben enviar las respuestas.
ms.openlocfilehash: 08f9edce76fd01111922a2a07d1a63e288a0c1ee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468330"
---
# <a name="replyto"></a><span data-ttu-id="6b6b0-103">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="6b6b0-103">ReplyTo</span></span>

<span data-ttu-id="6b6b0-104">El elemento **ReplyTo** identifica una matriz de direcciones a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-104">The **ReplyTo** element identifies an array of addresses to which replies should be sent.</span></span> 
  
```xml
<ReplyTo>
   <Mailbox/>
</ReplyTo>
```

 <span data-ttu-id="6b6b0-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="6b6b0-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b6b0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6b6b0-106">Attributes and elements</span></span>

<span data-ttu-id="6b6b0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b6b0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b6b0-108">Attributes</span></span>

<span data-ttu-id="6b6b0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b6b0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b6b0-110">Child elements</span></span>

|<span data-ttu-id="6b6b0-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6b6b0-111">**Element**</span></span>|<span data-ttu-id="6b6b0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b6b0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b6b0-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="6b6b0-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="6b6b0-114">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo al que se envía una respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-114">Identifies a mail-enabled Active Directory directory service object to which a reply is sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6b6b0-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b6b0-115">Parent elements</span></span>

|<span data-ttu-id="6b6b0-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6b6b0-116">**Element**</span></span>|<span data-ttu-id="6b6b0-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b6b0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b6b0-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="6b6b0-119">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-120">Mensaje</span><span class="sxs-lookup"><span data-stu-id="6b6b0-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6b6b0-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="6b6b0-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="6b6b0-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="6b6b0-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="6b6b0-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="6b6b0-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="6b6b0-127">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="6b6b0-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="6b6b0-129">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="6b6b0-131">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="6b6b0-133">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="6b6b0-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="6b6b0-137">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="6b6b0-139">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="6b6b0-141">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="6b6b0-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="6b6b0-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="6b6b0-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b6b0-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b6b0-144">Remarks</span></span>

<span data-ttu-id="6b6b0-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6b6b0-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b6b0-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b6b0-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b6b0-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b6b0-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b6b0-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6b6b0-148">Schema Name</span></span>  <br/> |<span data-ttu-id="6b6b0-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6b6b0-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="6b6b0-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6b6b0-150">Validation File</span></span>  <br/> |<span data-ttu-id="6b6b0-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6b6b0-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b6b0-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6b6b0-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="6b6b0-153">Falso</span><span class="sxs-lookup"><span data-stu-id="6b6b0-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b6b0-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b6b0-154">See also</span></span>



- [<span data-ttu-id="6b6b0-155">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6b6b0-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


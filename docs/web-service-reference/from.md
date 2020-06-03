---
title: From
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- From
api_type:
- schema
ms.assetid: 5a52d644-3677-4049-874c-12bd5c3080dc
description: El elemento from representa la dirección desde la que se envió el mensaje.
ms.openlocfilehash: c0d655731677e56cc02c7c029264ffc96f0a18c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459556"
---
# <a name="from"></a><span data-ttu-id="16512-103">From</span><span class="sxs-lookup"><span data-stu-id="16512-103">From</span></span>

<span data-ttu-id="16512-104">El elemento **from** representa la dirección desde la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="16512-104">The **From** element represents the address from which the message was sent.</span></span> 
  
```xml
<From>
   <Mailbox/>
</From>
```

 <span data-ttu-id="16512-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="16512-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16512-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="16512-106">Attributes and elements</span></span>

<span data-ttu-id="16512-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="16512-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16512-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="16512-108">Attributes</span></span>

<span data-ttu-id="16512-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="16512-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="16512-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="16512-110">Child elements</span></span>

|<span data-ttu-id="16512-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="16512-111">**Element**</span></span>|<span data-ttu-id="16512-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16512-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16512-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="16512-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="16512-114">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="16512-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="16512-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="16512-115">Parent elements</span></span>

|<span data-ttu-id="16512-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="16512-116">**Element**</span></span>|<span data-ttu-id="16512-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16512-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16512-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="16512-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="16512-119">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16512-120">Message</span><span class="sxs-lookup"><span data-stu-id="16512-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="16512-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="16512-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="16512-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="16512-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16512-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="16512-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="16512-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16512-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="16512-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="16512-127">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16512-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="16512-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="16512-129">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16512-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="16512-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="16512-131">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="16512-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="16512-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="16512-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="16512-133">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="16512-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="16512-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="16512-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="16512-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="16512-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="16512-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="16512-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="16512-137">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16512-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="16512-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="16512-139">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16512-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="16512-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="16512-141">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="16512-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="16512-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="16512-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="16512-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="16512-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="16512-144">PostItem</span><span class="sxs-lookup"><span data-stu-id="16512-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="16512-145">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16512-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="16512-146">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="16512-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16512-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16512-147">Remarks</span></span>

<span data-ttu-id="16512-148">Este elemento se usa para los correos electrónicos "enviar en nombre de".</span><span class="sxs-lookup"><span data-stu-id="16512-148">This element is used for "send on behalf of" e-mails.</span></span>
  
<span data-ttu-id="16512-149">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="16512-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16512-150">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="16512-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16512-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="16512-151">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="16512-152">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="16512-152">Schema Name</span></span>  <br/> |<span data-ttu-id="16512-153">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="16512-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="16512-154">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="16512-154">Validation File</span></span>  <br/> |<span data-ttu-id="16512-155">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="16512-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="16512-156">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="16512-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="16512-157">Falso</span><span class="sxs-lookup"><span data-stu-id="16512-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16512-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="16512-158">See also</span></span>



- [<span data-ttu-id="16512-159">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="16512-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


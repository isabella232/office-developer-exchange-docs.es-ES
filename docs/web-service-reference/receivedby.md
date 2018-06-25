---
title: ReceivedBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedBy
api_type:
- schema
ms.assetid: ac84c9c5-d2fe-4b6f-bf4d-0444131d835b
description: El elemento ReceivedBy identifica al delegado en un escenario de acceso delegado.
ms.openlocfilehash: 7918fa3320223e5cf02dd225912adfae3181e29c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836969"
---
# <a name="receivedby"></a><span data-ttu-id="657e8-103">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="657e8-103">ReceivedBy</span></span>

<span data-ttu-id="657e8-104">El elemento **ReceivedBy** identifica al delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="657e8-104">The **ReceivedBy** element identifies the delegate in a delegate access scenario.</span></span> 
  
```xml
<ReceivedBy>
   <Mailbox/>
</ReceivedBy>
```

 <span data-ttu-id="657e8-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="657e8-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="657e8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="657e8-106">Attributes and elements</span></span>

<span data-ttu-id="657e8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="657e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="657e8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="657e8-108">Attributes</span></span>

<span data-ttu-id="657e8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="657e8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="657e8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="657e8-110">Child elements</span></span>

|<span data-ttu-id="657e8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="657e8-111">**Element**</span></span>|<span data-ttu-id="657e8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="657e8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="657e8-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="657e8-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="657e8-114">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="657e8-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="657e8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="657e8-115">Parent elements</span></span>

|<span data-ttu-id="657e8-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="657e8-116">**Element**</span></span>|<span data-ttu-id="657e8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="657e8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="657e8-118">Message</span><span class="sxs-lookup"><span data-stu-id="657e8-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="657e8-119">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="657e8-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="657e8-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="657e8-121">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="657e8-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="657e8-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="657e8-123">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="657e8-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="657e8-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="657e8-125">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="657e8-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="657e8-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="657e8-127">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="657e8-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="657e8-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="657e8-129">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="657e8-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="657e8-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="657e8-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="657e8-131">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="657e8-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="657e8-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="657e8-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="657e8-133">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="657e8-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="657e8-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="657e8-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="657e8-135">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="657e8-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="657e8-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="657e8-137">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="657e8-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="657e8-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="657e8-139">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="657e8-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="657e8-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="657e8-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="657e8-141">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="657e8-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="657e8-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="657e8-142">Remarks</span></span>

<span data-ttu-id="657e8-143">El elemento **ReceivedRepresenting** se usa junto con el **de** y elementos de **ReceivedBy** en delegación escenarios de access.</span><span class="sxs-lookup"><span data-stu-id="657e8-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="657e8-144">En la siguiente tabla se enumera las entidades que estos elementos se representan en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="657e8-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="657e8-145">**Elementos en un escenario de acceso delegado**</span><span class="sxs-lookup"><span data-stu-id="657e8-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="657e8-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="657e8-146">**Element**</span></span>|<span data-ttu-id="657e8-147">**Entidad que representan el elemento**</span><span class="sxs-lookup"><span data-stu-id="657e8-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="657e8-148">From</span><span class="sxs-lookup"><span data-stu-id="657e8-148">From</span></span>](from.md) <br/> |<span data-ttu-id="657e8-149">Otros</span><span class="sxs-lookup"><span data-stu-id="657e8-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="657e8-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="657e8-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="657e8-151">Delegado</span><span class="sxs-lookup"><span data-stu-id="657e8-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="657e8-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="657e8-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="657e8-153">Principal</span><span class="sxs-lookup"><span data-stu-id="657e8-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="657e8-154">En un escenario de acceso delegado, si un otros envía una convocatoria de reunión a una entidad de seguridad que tiene un delegado, el delegado aparecerá una nueva convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="657e8-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="657e8-155">Estos elementos permiten delegados distinguir entre los mensajes que se envían a ellos debido a un delegado de desvío de regla y los mensajes que se envían directamente a ellos.</span><span class="sxs-lookup"><span data-stu-id="657e8-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="657e8-156">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="657e8-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="657e8-157">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="657e8-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="657e8-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="657e8-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="657e8-159">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="657e8-159">Schema Name</span></span>  <br/> |<span data-ttu-id="657e8-160">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="657e8-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="657e8-161">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="657e8-161">Validation File</span></span>  <br/> |<span data-ttu-id="657e8-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="657e8-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="657e8-163">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="657e8-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="657e8-164">False</span><span class="sxs-lookup"><span data-stu-id="657e8-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="657e8-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="657e8-165">See also</span></span>



- [<span data-ttu-id="657e8-166">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="657e8-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


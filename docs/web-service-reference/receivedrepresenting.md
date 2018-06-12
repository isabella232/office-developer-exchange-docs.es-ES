---
title: ReceivedRepresenting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedRepresenting
api_type:
- schema
ms.assetid: 1157b042-6dce-4cdc-9700-e22b749da39f
description: El elemento ReceivedRepresenting identifica la entidad de seguridad en un escenario de acceso delegado.
ms.openlocfilehash: 1587fcae6975b986711e7223e50c60658833cc80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836973"
---
# <a name="receivedrepresenting"></a><span data-ttu-id="cd761-103">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="cd761-103">ReceivedRepresenting</span></span>

<span data-ttu-id="cd761-104">El elemento **ReceivedRepresenting** identifica la entidad de seguridad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="cd761-104">The **ReceivedRepresenting** element identifies the principal in a delegate access scenario.</span></span> 
  
```xml
<ReceivedRepresenting>
   <Mailbox/>
</ReceivedRepresenting>
```

 <span data-ttu-id="cd761-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="cd761-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd761-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cd761-106">Attributes and elements</span></span>

<span data-ttu-id="cd761-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cd761-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd761-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd761-108">Attributes</span></span>

<span data-ttu-id="cd761-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cd761-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd761-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cd761-110">Child elements</span></span>

|<span data-ttu-id="cd761-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd761-111">**Element**</span></span>|<span data-ttu-id="cd761-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd761-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd761-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="cd761-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="cd761-114">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="cd761-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd761-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cd761-115">Parent elements</span></span>

|<span data-ttu-id="cd761-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd761-116">**Element**</span></span>|<span data-ttu-id="cd761-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd761-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd761-118">Message</span><span class="sxs-lookup"><span data-stu-id="cd761-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="cd761-119">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="cd761-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="cd761-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="cd761-121">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cd761-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="cd761-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="cd761-123">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cd761-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="cd761-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="cd761-125">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cd761-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="cd761-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="cd761-127">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cd761-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="cd761-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="cd761-129">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="cd761-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="cd761-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="cd761-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="cd761-131">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="cd761-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="cd761-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="cd761-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="cd761-133">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="cd761-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="cd761-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="cd761-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="cd761-135">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cd761-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="cd761-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="cd761-137">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cd761-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="cd761-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="cd761-139">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="cd761-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="cd761-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="cd761-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="cd761-141">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="cd761-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd761-142">Notas</span><span class="sxs-lookup"><span data-stu-id="cd761-142">Remarks</span></span>

<span data-ttu-id="cd761-143">El elemento **ReceivedRepresenting** se usa junto con el **de** y elementos de **ReceivedBy** en delegación escenarios de access.</span><span class="sxs-lookup"><span data-stu-id="cd761-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="cd761-144">En la siguiente tabla se enumera las entidades que estos elementos se representan en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="cd761-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="cd761-145">**Elementos en un escenario de acceso delegado**</span><span class="sxs-lookup"><span data-stu-id="cd761-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="cd761-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd761-146">**Element**</span></span>|<span data-ttu-id="cd761-147">**Entidad que representan el elemento**</span><span class="sxs-lookup"><span data-stu-id="cd761-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd761-148">From</span><span class="sxs-lookup"><span data-stu-id="cd761-148">From</span></span>](from.md) <br/> |<span data-ttu-id="cd761-149">Otros</span><span class="sxs-lookup"><span data-stu-id="cd761-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="cd761-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="cd761-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="cd761-151">Delegado</span><span class="sxs-lookup"><span data-stu-id="cd761-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="cd761-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="cd761-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="cd761-153">Principal</span><span class="sxs-lookup"><span data-stu-id="cd761-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="cd761-154">En un escenario de acceso delegado, si un otros envía una convocatoria de reunión a una entidad de seguridad que tiene un delegado, el delegado aparecerá una nueva convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="cd761-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="cd761-155">Estos elementos permiten delegados distinguir entre los mensajes que se envían a ellos debido a un delegado de desvío de regla y los mensajes que se envían directamente a ellos.</span><span class="sxs-lookup"><span data-stu-id="cd761-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="cd761-156">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd761-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd761-157">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cd761-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd761-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd761-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd761-159">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cd761-159">Schema Name</span></span>  <br/> |<span data-ttu-id="cd761-160">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cd761-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd761-161">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cd761-161">Validation File</span></span>  <br/> |<span data-ttu-id="cd761-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd761-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd761-163">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cd761-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd761-164">False</span><span class="sxs-lookup"><span data-stu-id="cd761-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd761-165">Ver también</span><span class="sxs-lookup"><span data-stu-id="cd761-165">See also</span></span>



- [<span data-ttu-id="cd761-166">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cd761-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


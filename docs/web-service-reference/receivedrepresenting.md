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
description: El elemento ReceivedRepresenting identifica la entidad de identidad en un escenario de acceso delegado.
ms.openlocfilehash: f444fb88be9c0df174f0c1490cf7c499cc0c0539
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468225"
---
# <a name="receivedrepresenting"></a><span data-ttu-id="07556-103">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="07556-103">ReceivedRepresenting</span></span>

<span data-ttu-id="07556-104">El elemento **ReceivedRepresenting** identifica la entidad de identidad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="07556-104">The **ReceivedRepresenting** element identifies the principal in a delegate access scenario.</span></span> 
  
```xml
<ReceivedRepresenting>
   <Mailbox/>
</ReceivedRepresenting>
```

 <span data-ttu-id="07556-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="07556-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07556-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07556-106">Attributes and elements</span></span>

<span data-ttu-id="07556-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07556-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07556-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="07556-108">Attributes</span></span>

<span data-ttu-id="07556-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="07556-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07556-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07556-110">Child elements</span></span>

|<span data-ttu-id="07556-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="07556-111">**Element**</span></span>|<span data-ttu-id="07556-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07556-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07556-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="07556-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="07556-114">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="07556-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07556-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07556-115">Parent elements</span></span>

|<span data-ttu-id="07556-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="07556-116">**Element**</span></span>|<span data-ttu-id="07556-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07556-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07556-118">Message</span><span class="sxs-lookup"><span data-stu-id="07556-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="07556-119">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="07556-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="07556-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="07556-121">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07556-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="07556-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="07556-123">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07556-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="07556-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="07556-125">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07556-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="07556-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="07556-127">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07556-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="07556-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="07556-129">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="07556-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="07556-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="07556-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="07556-131">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="07556-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="07556-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="07556-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="07556-133">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="07556-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="07556-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="07556-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="07556-135">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07556-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="07556-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="07556-137">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07556-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="07556-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="07556-139">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="07556-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="07556-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="07556-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="07556-141">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="07556-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07556-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07556-142">Remarks</span></span>

<span data-ttu-id="07556-143">El elemento **ReceivedRepresenting** se usa junto con los elementos **from** y **ReceivedBy** en escenarios de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="07556-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="07556-144">En la siguiente tabla se enumeran las entidades que estos elementos representan en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="07556-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="07556-145">**Elementos en un escenario de acceso delegado**</span><span class="sxs-lookup"><span data-stu-id="07556-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="07556-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="07556-146">**Element**</span></span>|<span data-ttu-id="07556-147">**Entidad que representa el elemento**</span><span class="sxs-lookup"><span data-stu-id="07556-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07556-148">From</span><span class="sxs-lookup"><span data-stu-id="07556-148">From</span></span>](from.md) <br/> |<span data-ttu-id="07556-149">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="07556-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="07556-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="07556-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="07556-151">Delegado</span><span class="sxs-lookup"><span data-stu-id="07556-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="07556-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="07556-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="07556-153">Director</span><span class="sxs-lookup"><span data-stu-id="07556-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="07556-154">En un escenario de acceso delegado, si un ThirdParty envía una convocatoria de reunión a una entidad de identidad que tiene un delegado, el delegado verá una nueva convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="07556-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="07556-155">Estos elementos permiten a los delegados distinguir entre los mensajes que se envían directamente a ellos y los que se les envían debido a una regla de reenvío de delegado.</span><span class="sxs-lookup"><span data-stu-id="07556-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="07556-156">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="07556-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07556-157">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07556-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07556-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="07556-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07556-159">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07556-159">Schema Name</span></span>  <br/> |<span data-ttu-id="07556-160">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="07556-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="07556-161">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07556-161">Validation File</span></span>  <br/> |<span data-ttu-id="07556-162">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="07556-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07556-163">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07556-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="07556-164">Falso</span><span class="sxs-lookup"><span data-stu-id="07556-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07556-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="07556-165">See also</span></span>



- [<span data-ttu-id="07556-166">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="07556-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


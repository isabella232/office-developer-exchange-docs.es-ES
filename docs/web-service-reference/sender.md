---
title: Remitente
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Sender
api_type:
- schema
ms.assetid: 26d1a46e-e1d3-44b8-a02d-fa6f83aa5cda
description: El elemento Sender identifica al remitente de un elemento.
ms.openlocfilehash: f056fefdd5c5832d4b5bf20416e07e376f6a03de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530582"
---
# <a name="sender"></a><span data-ttu-id="d69d1-103">Remitente</span><span class="sxs-lookup"><span data-stu-id="d69d1-103">Sender</span></span>

<span data-ttu-id="d69d1-104">El elemento **Sender** identifica al remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d69d1-104">The **Sender** element identifies the sender of an item.</span></span> 
  
```xml
<Sender>
   <Mailbox/>
</Sender>
```

 <span data-ttu-id="d69d1-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="d69d1-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d69d1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d69d1-106">Attributes and elements</span></span>

<span data-ttu-id="d69d1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d69d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d69d1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d69d1-108">Attributes</span></span>

<span data-ttu-id="d69d1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d69d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d69d1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d69d1-110">Child elements</span></span>

|<span data-ttu-id="d69d1-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d69d1-111">**Element**</span></span>|<span data-ttu-id="d69d1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d69d1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d69d1-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="d69d1-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="d69d1-114">Identifica un objeto de Active Directory habilitado para correo que identifica al remitente.</span><span class="sxs-lookup"><span data-stu-id="d69d1-114">Identifies a mail enabled Active Directory object that identifies the sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d69d1-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d69d1-115">Parent elements</span></span>

|<span data-ttu-id="d69d1-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d69d1-116">**Element**</span></span>|<span data-ttu-id="d69d1-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d69d1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d69d1-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="d69d1-119">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-120">Message</span><span class="sxs-lookup"><span data-stu-id="d69d1-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d69d1-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="d69d1-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="d69d1-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d69d1-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d69d1-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d69d1-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="d69d1-127">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="d69d1-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="d69d1-129">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="d69d1-131">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="d69d1-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="d69d1-133">Representa una respuesta aceptada provisionalmente a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="d69d1-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="d69d1-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="d69d1-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="d69d1-137">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="d69d1-139">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="d69d1-141">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d69d1-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="d69d1-143">Representa el objeto de respuesta usado para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="d69d1-143">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="d69d1-144">PostItem</span><span class="sxs-lookup"><span data-stu-id="d69d1-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="d69d1-145">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69d1-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="d69d1-146">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d69d1-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d69d1-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d69d1-147">Remarks</span></span>

<span data-ttu-id="d69d1-148">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d69d1-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d69d1-149">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d69d1-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d69d1-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="d69d1-150">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d69d1-151">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d69d1-151">Schema Name</span></span>  <br/> |<span data-ttu-id="d69d1-152">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d69d1-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="d69d1-153">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d69d1-153">Validation File</span></span>  <br/> |<span data-ttu-id="d69d1-154">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d69d1-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d69d1-155">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d69d1-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="d69d1-156">Falso</span><span class="sxs-lookup"><span data-stu-id="d69d1-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d69d1-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="d69d1-157">See also</span></span>



- [<span data-ttu-id="d69d1-158">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d69d1-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


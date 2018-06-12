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
description: El elemento de remitente identifica el remitente de un elemento.
ms.openlocfilehash: a7b06543fadd7cf7ae05f7ae8f86122138e11076
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837323"
---
# <a name="sender"></a><span data-ttu-id="577a5-103">Remitente</span><span class="sxs-lookup"><span data-stu-id="577a5-103">Sender</span></span>

<span data-ttu-id="577a5-104">El elemento de **remitente** identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="577a5-104">The **Sender** element identifies the sender of an item.</span></span> 
  
```xml
<Sender>
   <Mailbox/>
</Sender>
```

 <span data-ttu-id="577a5-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="577a5-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="577a5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="577a5-106">Attributes and elements</span></span>

<span data-ttu-id="577a5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="577a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="577a5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="577a5-108">Attributes</span></span>

<span data-ttu-id="577a5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="577a5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="577a5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="577a5-110">Child elements</span></span>

|<span data-ttu-id="577a5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="577a5-111">**Element**</span></span>|<span data-ttu-id="577a5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="577a5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="577a5-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="577a5-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="577a5-114">Identifica un objeto de Active Directory habilitado para correo que identifica al remitente.</span><span class="sxs-lookup"><span data-stu-id="577a5-114">Identifies a mail enabled Active Directory object that identifies the sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="577a5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="577a5-115">Parent elements</span></span>

|<span data-ttu-id="577a5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="577a5-116">**Element**</span></span>|<span data-ttu-id="577a5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="577a5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="577a5-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="577a5-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="577a5-119">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="577a5-120">Message</span><span class="sxs-lookup"><span data-stu-id="577a5-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="577a5-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="577a5-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="577a5-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="577a5-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="577a5-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="577a5-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="577a5-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="577a5-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="577a5-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="577a5-127">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="577a5-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="577a5-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="577a5-129">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="577a5-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="577a5-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="577a5-131">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="577a5-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="577a5-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="577a5-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="577a5-133">Representa una respuesta a una convocatoria de reunión aceptada provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="577a5-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="577a5-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="577a5-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="577a5-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="577a5-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="577a5-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="577a5-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="577a5-137">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="577a5-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="577a5-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="577a5-139">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="577a5-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="577a5-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="577a5-141">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="577a5-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="577a5-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="577a5-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="577a5-143">Representa el objeto de respuesta que se utiliza para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="577a5-143">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="577a5-144">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="577a5-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="577a5-145">Representa un elemento para exponer en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="577a5-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="577a5-146">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="577a5-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="577a5-147">Notas</span><span class="sxs-lookup"><span data-stu-id="577a5-147">Remarks</span></span>

<span data-ttu-id="577a5-148">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="577a5-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="577a5-149">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="577a5-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="577a5-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="577a5-150">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="577a5-151">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="577a5-151">Schema Name</span></span>  <br/> |<span data-ttu-id="577a5-152">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="577a5-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="577a5-153">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="577a5-153">Validation File</span></span>  <br/> |<span data-ttu-id="577a5-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="577a5-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="577a5-155">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="577a5-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="577a5-156">False</span><span class="sxs-lookup"><span data-stu-id="577a5-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="577a5-157">Ver también</span><span class="sxs-lookup"><span data-stu-id="577a5-157">See also</span></span>



- [<span data-ttu-id="577a5-158">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="577a5-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


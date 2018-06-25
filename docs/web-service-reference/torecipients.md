---
title: ToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToRecipients
api_type:
- schema
ms.assetid: 72dc3be8-30bb-4ae1-acf4-fb94ff490631
description: El elemento ToRecipients contiene una matriz de destinatarios de un elemento. Estos son los destinatarios principales de un elemento.
ms.openlocfilehash: 2913705cad52c041809769fe58efc3d616f40462
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840703"
---
# <a name="torecipients"></a><span data-ttu-id="e80ab-104">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="e80ab-104">ToRecipients</span></span>

<span data-ttu-id="e80ab-105">El elemento **ToRecipients** contiene una matriz de destinatarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e80ab-105">The **ToRecipients** element contains an array of recipients of an item.</span></span> <span data-ttu-id="e80ab-106">Estos son los destinatarios principales de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e80ab-106">These are the primary recipients of an item.</span></span> 
  
```xml
<ToRecipients>
   <Mailbox/>
</ToRecipients>
```

 <span data-ttu-id="e80ab-107">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="e80ab-107">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e80ab-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e80ab-108">Attributes and elements</span></span>

<span data-ttu-id="e80ab-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e80ab-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e80ab-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e80ab-110">Attributes</span></span>

<span data-ttu-id="e80ab-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e80ab-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e80ab-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e80ab-112">Child elements</span></span>

|<span data-ttu-id="e80ab-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e80ab-113">**Element**</span></span>|<span data-ttu-id="e80ab-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e80ab-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e80ab-115">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="e80ab-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e80ab-116">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="e80ab-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e80ab-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e80ab-117">Parent elements</span></span>

|<span data-ttu-id="e80ab-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e80ab-118">**Element**</span></span>|<span data-ttu-id="e80ab-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e80ab-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e80ab-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="e80ab-121">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-122">Message</span><span class="sxs-lookup"><span data-stu-id="e80ab-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e80ab-123">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-124">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e80ab-124">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e80ab-125">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-125">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e80ab-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e80ab-127">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-128">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e80ab-128">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e80ab-129">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-129">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e80ab-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e80ab-131">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-132">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-132">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="e80ab-133">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e80ab-133">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-134">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-134">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="e80ab-135">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e80ab-135">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-136">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-136">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="e80ab-137">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e80ab-137">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-138">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-138">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="e80ab-139">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-139">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-140">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-140">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="e80ab-141">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e80ab-141">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-142">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-142">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="e80ab-143">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e80ab-143">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="e80ab-144">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e80ab-144">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="e80ab-145">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="e80ab-145">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e80ab-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e80ab-146">Remarks</span></span>

<span data-ttu-id="e80ab-147">No se puede obtener **ToRecipients** mediante el uso de una solicitud de FindItem.</span><span class="sxs-lookup"><span data-stu-id="e80ab-147">You cannot get **ToRecipients** by using a FindItem request.</span></span> <span data-ttu-id="e80ab-148">Use una solicitud GetItem para obtener el **ToRecipients**.</span><span class="sxs-lookup"><span data-stu-id="e80ab-148">Use a GetItem request to get the **ToRecipients**.</span></span>
  
<span data-ttu-id="e80ab-149">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e80ab-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e80ab-150">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e80ab-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e80ab-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e80ab-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e80ab-152">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e80ab-152">Schema Name</span></span>  <br/> |<span data-ttu-id="e80ab-153">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e80ab-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="e80ab-154">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e80ab-154">Validation File</span></span>  <br/> |<span data-ttu-id="e80ab-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e80ab-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e80ab-156">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e80ab-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="e80ab-157">False</span><span class="sxs-lookup"><span data-stu-id="e80ab-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e80ab-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="e80ab-158">See also</span></span>



- [<span data-ttu-id="e80ab-159">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e80ab-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


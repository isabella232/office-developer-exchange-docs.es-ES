---
title: BccRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipients
api_type:
- schema
ms.assetid: c4e05168-d36b-4740-a526-4b7da53553c1
description: El elemento BccRecipients representa una colección de destinatarios para recibir una copia oculta (CCO) del mensaje de correo electrónico.
ms.openlocfilehash: 858fe74c32cb7d1ed624888c06bba4ffe09d489e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763611"
---
# <a name="bccrecipients"></a><span data-ttu-id="4dbc9-103">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="4dbc9-103">BccRecipients</span></span>

<span data-ttu-id="4dbc9-104">El elemento **BccRecipients** representa una colección de destinatarios para recibir una copia oculta (CCO) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-104">The **BccRecipients** element represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```xml
<BccRecipients>
   <Mailbox/>
</BccRecipients>
```

 <span data-ttu-id="4dbc9-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="4dbc9-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4dbc9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4dbc9-106">Attributes and elements</span></span>

<span data-ttu-id="4dbc9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4dbc9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4dbc9-108">Attributes</span></span>

<span data-ttu-id="4dbc9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4dbc9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4dbc9-110">Child elements</span></span>

|<span data-ttu-id="4dbc9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4dbc9-111">**Element**</span></span>|<span data-ttu-id="4dbc9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4dbc9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4dbc9-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="4dbc9-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="4dbc9-114">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4dbc9-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4dbc9-115">Parent elements</span></span>

|<span data-ttu-id="4dbc9-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4dbc9-116">**Element**</span></span>|<span data-ttu-id="4dbc9-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4dbc9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4dbc9-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="4dbc9-119">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-120">Message</span><span class="sxs-lookup"><span data-stu-id="4dbc9-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4dbc9-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="4dbc9-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="4dbc9-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4dbc9-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4dbc9-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="4dbc9-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="4dbc9-127">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="4dbc9-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="4dbc9-129">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="4dbc9-131">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="4dbc9-133">Representa una respuesta a una convocatoria de reunión aceptada provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="4dbc9-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="4dbc9-137">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="4dbc9-139">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="4dbc9-141">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="4dbc9-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="4dbc9-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="4dbc9-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dbc9-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4dbc9-144">Remarks</span></span>

<span data-ttu-id="4dbc9-145">No se puede obtener **BccRecipients** mediante el uso de una solicitud de FindItem.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-145">You cannot get **BccRecipients** by using a FindItem request.</span></span> <span data-ttu-id="4dbc9-146">Use una solicitud GetItem para obtener **BccRecipients**.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-146">Use a GetItem request to get **BccRecipients**.</span></span>
  
<span data-ttu-id="4dbc9-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4dbc9-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4dbc9-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4dbc9-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4dbc9-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4dbc9-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4dbc9-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4dbc9-150">Schema Name</span></span>  <br/> |<span data-ttu-id="4dbc9-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4dbc9-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="4dbc9-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4dbc9-152">Validation File</span></span>  <br/> |<span data-ttu-id="4dbc9-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4dbc9-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4dbc9-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4dbc9-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="4dbc9-155">False</span><span class="sxs-lookup"><span data-stu-id="4dbc9-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4dbc9-156">Ver también</span><span class="sxs-lookup"><span data-stu-id="4dbc9-156">See also</span></span>



- [<span data-ttu-id="4dbc9-157">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4dbc9-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


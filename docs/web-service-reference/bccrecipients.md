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
description: El elemento BccRecipients representa una colección de destinatarios para recibir una copia oculta (CCO) de un mensaje de correo electrónico.
ms.openlocfilehash: 96070415c6d92a893f6c560884d9d191c7d5f15b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529507"
---
# <a name="bccrecipients"></a><span data-ttu-id="e7b7e-103">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="e7b7e-103">BccRecipients</span></span>

<span data-ttu-id="e7b7e-104">El elemento **BccRecipients** representa una colección de destinatarios para recibir una copia oculta (CCO) de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-104">The **BccRecipients** element represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```xml
<BccRecipients>
   <Mailbox/>
</BccRecipients>
```

 <span data-ttu-id="e7b7e-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="e7b7e-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7b7e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e7b7e-106">Attributes and elements</span></span>

<span data-ttu-id="e7b7e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7b7e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7b7e-108">Attributes</span></span>

<span data-ttu-id="e7b7e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7b7e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e7b7e-110">Child elements</span></span>

|<span data-ttu-id="e7b7e-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7b7e-111">**Element**</span></span>|<span data-ttu-id="e7b7e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7b7e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7b7e-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="e7b7e-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e7b7e-114">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e7b7e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e7b7e-115">Parent elements</span></span>

|<span data-ttu-id="e7b7e-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7b7e-116">**Element**</span></span>|<span data-ttu-id="e7b7e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7b7e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7b7e-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="e7b7e-119">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-120">Message</span><span class="sxs-lookup"><span data-stu-id="e7b7e-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e7b7e-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e7b7e-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e7b7e-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e7b7e-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e7b7e-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e7b7e-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e7b7e-127">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e7b7e-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e7b7e-129">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="e7b7e-131">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="e7b7e-133">Representa una respuesta aceptada provisionalmente a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="e7b7e-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="e7b7e-137">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="e7b7e-139">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="e7b7e-141">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="e7b7e-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e7b7e-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="e7b7e-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7b7e-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7b7e-144">Remarks</span></span>

<span data-ttu-id="e7b7e-145">No se puede obtener **BccRecipients** mediante una solicitud FindItem.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-145">You cannot get **BccRecipients** by using a FindItem request.</span></span> <span data-ttu-id="e7b7e-146">Use una solicitud GetItem para obtener **BccRecipients**.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-146">Use a GetItem request to get **BccRecipients**.</span></span>
  
<span data-ttu-id="e7b7e-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e7b7e-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7b7e-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e7b7e-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7b7e-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7b7e-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7b7e-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e7b7e-150">Schema Name</span></span>  <br/> |<span data-ttu-id="e7b7e-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e7b7e-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7b7e-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e7b7e-152">Validation File</span></span>  <br/> |<span data-ttu-id="e7b7e-153">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e7b7e-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7b7e-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e7b7e-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="e7b7e-155">Falso</span><span class="sxs-lookup"><span data-stu-id="e7b7e-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7b7e-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7b7e-156">See also</span></span>



- [<span data-ttu-id="e7b7e-157">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e7b7e-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: CcRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CcRecipients
api_type:
- schema
ms.assetid: 5c20ec3a-0bee-4e67-b220-586ed0d601c9
description: El elemento CcRecipients representa una colección de los destinatarios que recibirán una copia del mensaje.
ms.openlocfilehash: 0afe19cfae49dbf48c685296a83ab1330b631d04
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763730"
---
# <a name="ccrecipients"></a><span data-ttu-id="4186d-103">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="4186d-103">CcRecipients</span></span>

<span data-ttu-id="4186d-104">El elemento **CcRecipients** representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4186d-104">The **CcRecipients** element represents a collection of recipients that will receive a copy of the message.</span></span> 
  
```xml
<CcRecipients>
   <Mailbox/>
</CcRecipients>
```

 <span data-ttu-id="4186d-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="4186d-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4186d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4186d-106">Attributes and elements</span></span>

<span data-ttu-id="4186d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4186d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4186d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4186d-108">Attributes</span></span>

<span data-ttu-id="4186d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4186d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4186d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4186d-110">Child elements</span></span>

|<span data-ttu-id="4186d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4186d-111">**Element**</span></span>|<span data-ttu-id="4186d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4186d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4186d-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="4186d-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="4186d-114">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="4186d-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4186d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4186d-115">Parent elements</span></span>

|<span data-ttu-id="4186d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4186d-116">**Element**</span></span>|<span data-ttu-id="4186d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4186d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4186d-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="4186d-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="4186d-119">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4186d-120">Message</span><span class="sxs-lookup"><span data-stu-id="4186d-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4186d-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="4186d-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="4186d-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="4186d-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4186d-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4186d-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4186d-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4186d-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="4186d-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="4186d-127">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4186d-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="4186d-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="4186d-129">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4186d-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="4186d-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="4186d-131">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="4186d-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="4186d-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="4186d-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="4186d-133">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="4186d-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="4186d-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="4186d-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="4186d-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="4186d-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="4186d-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="4186d-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="4186d-137">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4186d-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="4186d-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="4186d-139">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4186d-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4186d-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="4186d-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="4186d-141">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4186d-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="4186d-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="4186d-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="4186d-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="4186d-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4186d-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4186d-144">Remarks</span></span>

<span data-ttu-id="4186d-145">No se puede obtener **CcRecipients** mediante el uso de una solicitud de FindItem.</span><span class="sxs-lookup"><span data-stu-id="4186d-145">You cannot get **CcRecipients** by using a FindItem request.</span></span> <span data-ttu-id="4186d-146">Use una solicitud GetItem para obtener **CcRecipients**.</span><span class="sxs-lookup"><span data-stu-id="4186d-146">Use a GetItem request to get **CcRecipients**.</span></span>
  
<span data-ttu-id="4186d-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4186d-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4186d-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4186d-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4186d-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4186d-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4186d-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4186d-150">Schema Name</span></span>  <br/> |<span data-ttu-id="4186d-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4186d-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="4186d-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4186d-152">Validation File</span></span>  <br/> |<span data-ttu-id="4186d-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4186d-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4186d-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4186d-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="4186d-155">False</span><span class="sxs-lookup"><span data-stu-id="4186d-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4186d-156">Ver también</span><span class="sxs-lookup"><span data-stu-id="4186d-156">See also</span></span>



- [<span data-ttu-id="4186d-157">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4186d-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


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
description: El elemento CcRecipients representa una colección de destinatarios que recibirán una copia del mensaje.
ms.openlocfilehash: 57d0e2d3b2c44fbd7bb30696002b27e83d1e274e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462209"
---
# <a name="ccrecipients"></a><span data-ttu-id="8023a-103">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="8023a-103">CcRecipients</span></span>

<span data-ttu-id="8023a-104">El elemento **CcRecipients** representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8023a-104">The **CcRecipients** element represents a collection of recipients that will receive a copy of the message.</span></span> 
  
```xml
<CcRecipients>
   <Mailbox/>
</CcRecipients>
```

 <span data-ttu-id="8023a-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="8023a-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8023a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8023a-106">Attributes and elements</span></span>

<span data-ttu-id="8023a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8023a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8023a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8023a-108">Attributes</span></span>

<span data-ttu-id="8023a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8023a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8023a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8023a-110">Child elements</span></span>

|<span data-ttu-id="8023a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8023a-111">**Element**</span></span>|<span data-ttu-id="8023a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8023a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8023a-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="8023a-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="8023a-114">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="8023a-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8023a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8023a-115">Parent elements</span></span>

|<span data-ttu-id="8023a-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8023a-116">**Element**</span></span>|<span data-ttu-id="8023a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8023a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8023a-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="8023a-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="8023a-119">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8023a-120">Mensaje</span><span class="sxs-lookup"><span data-stu-id="8023a-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8023a-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="8023a-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="8023a-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="8023a-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8023a-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8023a-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8023a-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8023a-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="8023a-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="8023a-127">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8023a-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="8023a-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="8023a-129">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8023a-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="8023a-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="8023a-131">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8023a-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8023a-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="8023a-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="8023a-133">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8023a-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8023a-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="8023a-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="8023a-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8023a-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8023a-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="8023a-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="8023a-137">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8023a-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="8023a-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="8023a-139">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8023a-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8023a-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="8023a-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="8023a-141">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="8023a-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="8023a-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="8023a-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="8023a-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="8023a-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8023a-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8023a-144">Remarks</span></span>

<span data-ttu-id="8023a-145">No se puede obtener **CcRecipients** con una solicitud FindItem.</span><span class="sxs-lookup"><span data-stu-id="8023a-145">You cannot get **CcRecipients** by using a FindItem request.</span></span> <span data-ttu-id="8023a-146">Usa una solicitud GetItem para obtener **CcRecipients**.</span><span class="sxs-lookup"><span data-stu-id="8023a-146">Use a GetItem request to get **CcRecipients**.</span></span>
  
<span data-ttu-id="8023a-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8023a-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8023a-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8023a-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8023a-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="8023a-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8023a-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8023a-150">Schema Name</span></span>  <br/> |<span data-ttu-id="8023a-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8023a-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="8023a-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8023a-152">Validation File</span></span>  <br/> |<span data-ttu-id="8023a-153">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8023a-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8023a-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8023a-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="8023a-155">Falso</span><span class="sxs-lookup"><span data-stu-id="8023a-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8023a-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="8023a-156">See also</span></span>



- [<span data-ttu-id="8023a-157">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8023a-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


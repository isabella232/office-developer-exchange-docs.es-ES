---
title: ReplyTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyTo
api_type:
- schema
ms.assetid: 6b6ae792-e2c4-4aa0-95cb-b49b446f1e08
description: El elemento de origen identifica una matriz de direcciones a la que se deben enviar las respuestas.
ms.openlocfilehash: 0ceb4f5edb75bbfe52a7a7156da3c2a328bea346
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837115"
---
# <a name="replyto"></a><span data-ttu-id="973d2-103">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="973d2-103">ReplyTo</span></span>

<span data-ttu-id="973d2-104">El elemento de **origen** identifica una matriz de direcciones a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="973d2-104">The **ReplyTo** element identifies an array of addresses to which replies should be sent.</span></span> 
  
```xml
<ReplyTo>
   <Mailbox/>
</ReplyTo>
```

 <span data-ttu-id="973d2-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="973d2-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="973d2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="973d2-106">Attributes and elements</span></span>

<span data-ttu-id="973d2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="973d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="973d2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="973d2-108">Attributes</span></span>

<span data-ttu-id="973d2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="973d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="973d2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="973d2-110">Child elements</span></span>

|<span data-ttu-id="973d2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="973d2-111">**Element**</span></span>|<span data-ttu-id="973d2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="973d2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="973d2-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="973d2-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="973d2-114">Identifica un objeto habilitado para correo Active Directory directory servicio a la que se envía una respuesta.</span><span class="sxs-lookup"><span data-stu-id="973d2-114">Identifies a mail-enabled Active Directory directory service object to which a reply is sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="973d2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="973d2-115">Parent elements</span></span>

|<span data-ttu-id="973d2-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="973d2-116">**Element**</span></span>|<span data-ttu-id="973d2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="973d2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="973d2-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="973d2-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="973d2-119">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="973d2-120">Message</span><span class="sxs-lookup"><span data-stu-id="973d2-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="973d2-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="973d2-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="973d2-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="973d2-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="973d2-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="973d2-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="973d2-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="973d2-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="973d2-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="973d2-127">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="973d2-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="973d2-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="973d2-129">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="973d2-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="973d2-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="973d2-131">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="973d2-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="973d2-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="973d2-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="973d2-133">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="973d2-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="973d2-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="973d2-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="973d2-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="973d2-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="973d2-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="973d2-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="973d2-137">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="973d2-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="973d2-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="973d2-139">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="973d2-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="973d2-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="973d2-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="973d2-141">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="973d2-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="973d2-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="973d2-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="973d2-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="973d2-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="973d2-144">Notas</span><span class="sxs-lookup"><span data-stu-id="973d2-144">Remarks</span></span>

<span data-ttu-id="973d2-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="973d2-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="973d2-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="973d2-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="973d2-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="973d2-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="973d2-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="973d2-148">Schema Name</span></span>  <br/> |<span data-ttu-id="973d2-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="973d2-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="973d2-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="973d2-150">Validation File</span></span>  <br/> |<span data-ttu-id="973d2-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="973d2-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="973d2-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="973d2-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="973d2-153">False</span><span class="sxs-lookup"><span data-stu-id="973d2-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="973d2-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="973d2-154">See also</span></span>



- [<span data-ttu-id="973d2-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="973d2-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: Message
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 2400b33c-43b2-4fc2-b6fb-275a99e0e810
description: El elemento de mensaje representa un mensaje de correo electrónico de Microsoft Exchange.
ms.openlocfilehash: 388b944cfa16899cb2376320882f5087396d7b82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836474"
---
# <a name="message"></a><span data-ttu-id="5c8ae-103">Message</span><span class="sxs-lookup"><span data-stu-id="5c8ae-103">Message</span></span>

<span data-ttu-id="5c8ae-104">El elemento de **mensaje** representa un mensaje de correo electrónico de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-104">The **Message** element represents a Microsoft Exchange e-mail message.</span></span> 
  
```xml
<Message>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <Importance/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <ReminderMessageData/>
</Message>
```

 <span data-ttu-id="5c8ae-105">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="5c8ae-105">**MessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c8ae-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5c8ae-106">Attributes and elements</span></span>

<span data-ttu-id="5c8ae-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c8ae-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5c8ae-108">Attributes</span></span>

<span data-ttu-id="5c8ae-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c8ae-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5c8ae-110">Child elements</span></span>

|<span data-ttu-id="5c8ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c8ae-111">**Element**</span></span>|<span data-ttu-id="5c8ae-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c8ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c8ae-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="5c8ae-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="5c8ae-114">Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="5c8ae-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="5c8ae-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="5c8ae-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-118">Id</span><span class="sxs-lookup"><span data-stu-id="5c8ae-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="5c8ae-119">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="5c8ae-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="5c8ae-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="5c8ae-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-123">Subject</span><span class="sxs-lookup"><span data-stu-id="5c8ae-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="5c8ae-124">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="5c8ae-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-126">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="5c8ae-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="5c8ae-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-128">Body</span><span class="sxs-lookup"><span data-stu-id="5c8ae-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="5c8ae-129">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5c8ae-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5c8ae-131">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="5c8ae-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="5c8ae-133">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-134">Size</span><span class="sxs-lookup"><span data-stu-id="5c8ae-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="5c8ae-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="5c8ae-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-137">Categories</span><span class="sxs-lookup"><span data-stu-id="5c8ae-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5c8ae-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-139">Importancia</span><span class="sxs-lookup"><span data-stu-id="5c8ae-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="5c8ae-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="5c8ae-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="5c8ae-142">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="5c8ae-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="5c8ae-144">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="5c8ae-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="5c8ae-146">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="5c8ae-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="5c8ae-148">Indica si un usuario envía un elemento a él o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="5c8ae-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="5c8ae-150">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="5c8ae-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="5c8ae-152">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="5c8ae-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="5c8ae-154">Representa la colección de todos los encabezados de mensaje de Internet que están dentro de un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="5c8ae-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="5c8ae-156">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="5c8ae-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="5c8ae-158">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="5c8ae-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="5c8ae-160">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="5c8ae-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="5c8ae-162">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="5c8ae-163">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="5c8ae-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="5c8ae-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="5c8ae-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="5c8ae-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="5c8ae-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="5c8ae-169">Representa la cadena para mostrar que se usa para el contenido de la línea CC.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-169">Represents the display string that is used for the contents of the CC line.</span></span> <span data-ttu-id="5c8ae-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de CC.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-170">This is the concatenated string of all CC recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="5c8ae-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="5c8ae-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="5c8ae-173">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="5c8ae-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="5c8ae-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="5c8ae-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="5c8ae-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="5c8ae-178">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-179">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="5c8ae-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="5c8ae-180">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-181">Sender</span><span class="sxs-lookup"><span data-stu-id="5c8ae-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="5c8ae-182">Identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="5c8ae-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="5c8ae-184">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="5c8ae-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="5c8ae-186">Representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="5c8ae-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="5c8ae-188">Representa una colección de destinatarios para recibir una copia oculta (CCO) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="5c8ae-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="5c8ae-190">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="5c8ae-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="5c8ae-192">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="5c8ae-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="5c8ae-194">Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="5c8ae-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="5c8ae-196">Representa el identificador de conversación.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-197">From</span><span class="sxs-lookup"><span data-stu-id="5c8ae-197">From</span></span>](from.md) <br/> |<span data-ttu-id="5c8ae-198">Representa al destinatario de la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="5c8ae-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="5c8ae-200">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-201">Estáleído</span><span class="sxs-lookup"><span data-stu-id="5c8ae-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="5c8ae-202">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="5c8ae-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="5c8ae-204">Indica si se ha solicitado una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-205">Referencias</span><span class="sxs-lookup"><span data-stu-id="5c8ae-205">References</span></span>](references.md) <br/> |<span data-ttu-id="5c8ae-206">Representa el encabezado de Usenet que se usa para correlacionar las respuestas con sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="5c8ae-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="5c8ae-208">Identifica un conjunto de direcciones a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-209">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="5c8ae-209">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="5c8ae-210">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-210">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="5c8ae-211">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-211">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-212">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="5c8ae-212">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="5c8ae-213">Identifica al delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-213">Identifies the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-214">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="5c8ae-214">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="5c8ae-215">Identifica la entidad de seguridad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-215">Identifies the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-216">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="5c8ae-216">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="5c8ae-217">Contiene el nombre para mostrar del último usuario para modificar un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-217">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-218">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="5c8ae-218">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="5c8ae-219">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-219">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-220">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="5c8ae-220">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="5c8ae-221">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-221">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-222">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="5c8ae-222">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="5c8ae-223">Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-223">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-224">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="5c8ae-224">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="5c8ae-225">Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-225">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-226">ConversationId</span><span class="sxs-lookup"><span data-stu-id="5c8ae-226">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="5c8ae-227">Contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-227">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-228">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="5c8ae-228">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="5c8ae-229">Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-229">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-230">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="5c8ae-230">ReminderMessageData</span></span>](remindermessagedata.md) <br/> |<span data-ttu-id="5c8ae-231">Contiene los datos para un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-231">Contains the data for a reminder message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5c8ae-232">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5c8ae-232">Parent elements</span></span>

|<span data-ttu-id="5c8ae-233">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c8ae-233">**Element**</span></span>|<span data-ttu-id="5c8ae-234">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c8ae-234">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c8ae-235">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="5c8ae-235">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="5c8ae-236">Describe todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-236">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-237">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="5c8ae-237">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="5c8ae-238">Identifica los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5c8ae-238">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-239">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="5c8ae-239">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="5c8ae-240">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-240">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-241">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5c8ae-241">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="5c8ae-242">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-242">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-243">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="5c8ae-243">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="5c8ae-244">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-244">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-245">Items</span><span class="sxs-lookup"><span data-stu-id="5c8ae-245">Items</span></span>](items.md) <br/> |<span data-ttu-id="5c8ae-246">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-246">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-247">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="5c8ae-247">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="5c8ae-248">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="5c8ae-248">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-249">SetItemField</span><span class="sxs-lookup"><span data-stu-id="5c8ae-249">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="5c8ae-250">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5c8ae-250">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="5c8ae-251">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5c8ae-251">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="5c8ae-252">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-252">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c8ae-253">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5c8ae-253">Text value</span></span>

<span data-ttu-id="5c8ae-254">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-254">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c8ae-255">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c8ae-255">Remarks</span></span>

<span data-ttu-id="5c8ae-256">Otro elemento de **mensaje** , [mensaje (disponibilidad)](message-availability.md) se usa para las operaciones de disponibilidad para devolver los mensajes de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-256">Another **Message** element, [Message (Availability)](message-availability.md) is used by the Availability operations to return OOF messages.</span></span> 
  
<span data-ttu-id="5c8ae-257">Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de Exchange Web Services (EWS).</span><span class="sxs-lookup"><span data-stu-id="5c8ae-257">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="5c8ae-258">Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="5c8ae-258">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="5c8ae-259">Exchange 2010 no devuelve **el elemento de base** de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-259">Exchange 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="5c8ae-260">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c8ae-260">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c8ae-261">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5c8ae-261">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c8ae-262">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c8ae-262">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c8ae-263">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5c8ae-263">Schema Name</span></span>  <br/> |<span data-ttu-id="5c8ae-264">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5c8ae-264">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c8ae-265">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5c8ae-265">Validation File</span></span>  <br/> |<span data-ttu-id="5c8ae-266">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c8ae-266">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c8ae-267">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5c8ae-267">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c8ae-268">False</span><span class="sxs-lookup"><span data-stu-id="5c8ae-268">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c8ae-269">Ver también</span><span class="sxs-lookup"><span data-stu-id="5c8ae-269">See also</span></span>



- [<span data-ttu-id="5c8ae-270">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5c8ae-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


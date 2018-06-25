---
title: MeetingMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingMessage
api_type:
- schema
ms.assetid: c95956a8-7505-44b4-bea4-11d1f5182796
description: El elemento MeetingMessage representa una reunión en el almacén de Exchange.
ms.openlocfilehash: a2e87bc9800ee1dc66c1a3110df76745ac7c05b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836443"
---
# <a name="meetingmessage"></a><span data-ttu-id="a6781-103">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="a6781-103">MeetingMessage</span></span>

<span data-ttu-id="a6781-104">El elemento **MeetingMessage** representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6781-104">The **MeetingMessage** element represents a meeting in the Exchange store.</span></span> 
  
```xml
<MeetingMessage>
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
   <AssociatedCalendarItemId/>
   <IsDelegated/>
   <IsOutOfDate/>
   <HasBeenProcessed/>
   <ResponseType/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</MeetingMessage>
```

 <span data-ttu-id="a6781-105">**MeetingMessageType**</span><span class="sxs-lookup"><span data-stu-id="a6781-105">**MeetingMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6781-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a6781-106">Attributes and elements</span></span>

<span data-ttu-id="a6781-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a6781-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6781-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6781-108">Attributes</span></span>

<span data-ttu-id="a6781-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6781-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6781-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a6781-110">Child elements</span></span>

|<span data-ttu-id="a6781-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6781-111">**Element**</span></span>|<span data-ttu-id="a6781-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6781-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6781-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="a6781-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="a6781-114">Contiene la secuencia MIME nativa de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="a6781-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="a6781-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="a6781-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a6781-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6781-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="a6781-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6781-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a6781-118">Id</span><span class="sxs-lookup"><span data-stu-id="a6781-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="a6781-119">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a6781-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="a6781-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6781-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a6781-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="a6781-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="a6781-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="a6781-123">Subject</span><span class="sxs-lookup"><span data-stu-id="a6781-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="a6781-124">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6781-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="a6781-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6781-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="a6781-126">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="a6781-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="a6781-127">Contiene el estado de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-127">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="a6781-128">Body</span><span class="sxs-lookup"><span data-stu-id="a6781-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="a6781-129">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6781-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="a6781-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="a6781-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a6781-131">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6781-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a6781-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="a6781-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="a6781-133">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a6781-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="a6781-134">Size</span><span class="sxs-lookup"><span data-stu-id="a6781-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="a6781-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="a6781-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6781-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a6781-137">Categories</span><span class="sxs-lookup"><span data-stu-id="a6781-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a6781-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a6781-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="a6781-139">Importancia</span><span class="sxs-lookup"><span data-stu-id="a6781-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="a6781-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="a6781-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="a6781-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="a6781-142">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6781-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="a6781-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="a6781-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="a6781-144">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="a6781-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="a6781-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="a6781-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="a6781-146">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="a6781-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="a6781-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="a6781-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="a6781-148">Indica si un usuario envía un elemento a él o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="a6781-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="a6781-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="a6781-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="a6781-150">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a6781-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="a6781-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="a6781-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="a6781-152">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="a6781-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="a6781-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="a6781-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="a6781-154">Representa la colección de todos los encabezados de mensaje de Internet que están dentro de un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a6781-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a6781-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="a6781-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="a6781-156">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a6781-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="a6781-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="a6781-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="a6781-158">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a6781-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="a6781-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="a6781-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="a6781-160">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6781-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a6781-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="a6781-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="a6781-162">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="a6781-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="a6781-163">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="a6781-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="a6781-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="a6781-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="a6781-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6781-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a6781-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="a6781-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="a6781-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="a6781-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="a6781-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="a6781-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="a6781-169">Representa la cadena para mostrar que se usa para el contenido del cuadro Cc.</span><span class="sxs-lookup"><span data-stu-id="a6781-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="a6781-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="a6781-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="a6781-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="a6781-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="a6781-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="a6781-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="a6781-173">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="a6781-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="a6781-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="a6781-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="a6781-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="a6781-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="a6781-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6781-176">This property is read only.</span></span>  <br/> |
|[<span data-ttu-id="a6781-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a6781-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="a6781-178">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="a6781-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="a6781-179">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="a6781-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="a6781-180">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a6781-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a6781-181">Sender</span><span class="sxs-lookup"><span data-stu-id="a6781-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="a6781-182">Identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="a6781-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="a6781-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="a6781-184">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6781-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="a6781-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="a6781-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="a6781-186">Representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6781-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="a6781-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="a6781-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="a6781-188">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a6781-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="a6781-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="a6781-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="a6781-190">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="a6781-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="a6781-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="a6781-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="a6781-192">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="a6781-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="a6781-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="a6781-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="a6781-194">Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6781-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="a6781-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="a6781-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="a6781-196">Representa el identificador de conversación.</span><span class="sxs-lookup"><span data-stu-id="a6781-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="a6781-197">From</span><span class="sxs-lookup"><span data-stu-id="a6781-197">From</span></span>](from.md) <br/> |<span data-ttu-id="a6781-198">Representa al destinatario de la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6781-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="a6781-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="a6781-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="a6781-200">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="a6781-201">Estáleído</span><span class="sxs-lookup"><span data-stu-id="a6781-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="a6781-202">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6781-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="a6781-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="a6781-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="a6781-204">Indica si se ha solicitado una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a6781-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="a6781-205">Referencias</span><span class="sxs-lookup"><span data-stu-id="a6781-205">References</span></span>](references.md) <br/> |<span data-ttu-id="a6781-206">Representa el encabezado de Usenet que se usa para correlacionar las respuestas con sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="a6781-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="a6781-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="a6781-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="a6781-208">Identifica un conjunto de direcciones a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="a6781-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="a6781-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="a6781-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="a6781-210">Representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md).</span><span class="sxs-lookup"><span data-stu-id="a6781-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="a6781-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="a6781-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="a6781-212">Indica si una reunión se ha controlado por una cuenta con acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="a6781-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="a6781-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="a6781-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="a6781-214">Indica si un mensaje de reunión está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a6781-214">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="a6781-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="a6781-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="a6781-216">Indica si un mensaje de reunión item se han procesado.</span><span class="sxs-lookup"><span data-stu-id="a6781-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="a6781-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="a6781-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="a6781-218">Representa el tipo de destinatario respuesta recibida para una reunión.</span><span class="sxs-lookup"><span data-stu-id="a6781-218">Represents the type of recipient response received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="a6781-219">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="a6781-219">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="a6781-220">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a6781-220">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="a6781-221">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6781-221">This element is read-only.</span></span> <span data-ttu-id="a6781-222">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a6781-222">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="a6781-223">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="a6781-223">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="a6781-224">Contiene el nombre para mostrar del último usuario para modificar un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-224">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="a6781-225">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="a6781-225">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="a6781-226">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6781-226">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="a6781-227">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="a6781-227">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="a6781-228">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a6781-228">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="a6781-229">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="a6781-229">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="a6781-230">Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="a6781-230">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="a6781-231">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="a6781-231">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="a6781-232">Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="a6781-232">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="a6781-233">ConversationId</span><span class="sxs-lookup"><span data-stu-id="a6781-233">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="a6781-234">Contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="a6781-234">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="a6781-235">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="a6781-235">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="a6781-236">Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="a6781-236">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="a6781-237">UID</span><span class="sxs-lookup"><span data-stu-id="a6781-237">UID</span></span>](uid.md) <br/> |<span data-ttu-id="a6781-238">Identifica un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="a6781-238">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a6781-239">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="a6781-239">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="a6781-240">Se usa para identificar una instancia específica de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="a6781-240">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a6781-241">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="a6781-241">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="a6781-242">Indica la fecha y hora en que se ha creado una instancia de un objeto de iCalendar.</span><span class="sxs-lookup"><span data-stu-id="a6781-242">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6781-243">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a6781-243">Parent elements</span></span>

|<span data-ttu-id="a6781-244">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6781-244">**Element**</span></span>|<span data-ttu-id="a6781-245">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6781-245">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6781-246">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="a6781-246">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="a6781-247">Describe todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="a6781-247">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="a6781-248">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="a6781-248">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="a6781-249">Identifica los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a6781-249">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a6781-250">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="a6781-250">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="a6781-251">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a6781-251">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="a6781-252">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="a6781-252">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="a6781-253">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="a6781-253">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a6781-254">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="a6781-254">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="a6781-255">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="a6781-255">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a6781-256">Items</span><span class="sxs-lookup"><span data-stu-id="a6781-256">Items</span></span>](items.md) <br/> |<span data-ttu-id="a6781-257">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="a6781-257">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="a6781-258">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="a6781-258">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="a6781-259">Contiene una matriz de elementos que desea crear en la carpeta identificada por el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="a6781-259">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="a6781-260">SetItemField</span><span class="sxs-lookup"><span data-stu-id="a6781-260">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="a6781-261">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a6781-261">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a6781-262">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="a6781-262">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="a6781-263">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6781-263">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6781-264">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a6781-264">Text value</span></span>

<span data-ttu-id="a6781-265">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6781-265">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6781-266">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6781-266">Remarks</span></span>

<span data-ttu-id="a6781-267">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6781-267">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6781-268">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a6781-268">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6781-269">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6781-269">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6781-270">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a6781-270">Schema Name</span></span>  <br/> |<span data-ttu-id="a6781-271">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a6781-271">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6781-272">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a6781-272">Validation File</span></span>  <br/> |<span data-ttu-id="a6781-273">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6781-273">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6781-274">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a6781-274">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6781-275">False</span><span class="sxs-lookup"><span data-stu-id="a6781-275">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6781-276">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6781-276">See also</span></span>



- [<span data-ttu-id="a6781-277">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a6781-277">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


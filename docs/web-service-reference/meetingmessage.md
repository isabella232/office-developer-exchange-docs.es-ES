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
ms.openlocfilehash: fee615a1da117e5df03cd5ce8576bd66d7e89a4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468386"
---
# <a name="meetingmessage"></a><span data-ttu-id="5e567-103">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5e567-103">MeetingMessage</span></span>

<span data-ttu-id="5e567-104">El elemento **MeetingMessage** representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e567-104">The **MeetingMessage** element represents a meeting in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="5e567-105">**MeetingMessageType**</span><span class="sxs-lookup"><span data-stu-id="5e567-105">**MeetingMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e567-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5e567-106">Attributes and elements</span></span>

<span data-ttu-id="5e567-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5e567-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e567-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e567-108">Attributes</span></span>

<span data-ttu-id="5e567-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5e567-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5e567-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5e567-110">Child elements</span></span>

|<span data-ttu-id="5e567-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5e567-111">**Element**</span></span>|<span data-ttu-id="5e567-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e567-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e567-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="5e567-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="5e567-114">Contiene la secuencia MIME nativa de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="5e567-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="5e567-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="5e567-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="5e567-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e567-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="5e567-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e567-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5e567-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="5e567-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="5e567-119">Representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="5e567-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="5e567-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e567-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5e567-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="5e567-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="5e567-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="5e567-123">Asunto</span><span class="sxs-lookup"><span data-stu-id="5e567-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="5e567-124">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e567-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="5e567-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e567-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="5e567-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="5e567-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="5e567-127">Contiene el estado de la sensibilidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-127">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="5e567-128">Body</span><span class="sxs-lookup"><span data-stu-id="5e567-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="5e567-129">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5e567-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="5e567-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5e567-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5e567-131">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e567-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5e567-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="5e567-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="5e567-133">Representa la fecha y la hora en que se recibió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="5e567-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="5e567-134">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5e567-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="5e567-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="5e567-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e567-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="5e567-137">Categorías</span><span class="sxs-lookup"><span data-stu-id="5e567-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5e567-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="5e567-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="5e567-139">Importance</span><span class="sxs-lookup"><span data-stu-id="5e567-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="5e567-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="5e567-141">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="5e567-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="5e567-142">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="5e567-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="5e567-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="5e567-144">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="5e567-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="5e567-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="5e567-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="5e567-146">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="5e567-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="5e567-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="5e567-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="5e567-148">Indica si un usuario envió un elemento a ella o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="5e567-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="5e567-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="5e567-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="5e567-150">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="5e567-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="5e567-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="5e567-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="5e567-152">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="5e567-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="5e567-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="5e567-154">Representa la colección de todos los encabezados de mensajes de Internet que se encuentran dentro de un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="5e567-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5e567-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="5e567-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="5e567-156">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="5e567-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="5e567-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="5e567-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="5e567-158">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="5e567-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="5e567-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="5e567-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="5e567-160">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e567-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5e567-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="5e567-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="5e567-162">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="5e567-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="5e567-163">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="5e567-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="5e567-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="5e567-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="5e567-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e567-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5e567-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="5e567-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="5e567-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="5e567-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="5e567-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="5e567-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="5e567-169">Representa la cadena para mostrar que se usa para el contenido del cuadro CC.</span><span class="sxs-lookup"><span data-stu-id="5e567-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="5e567-170">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="5e567-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="5e567-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="5e567-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="5e567-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="5e567-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="5e567-173">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="5e567-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="5e567-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="5e567-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="5e567-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible.</span><span class="sxs-lookup"><span data-stu-id="5e567-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="5e567-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e567-176">This property is read only.</span></span>  <br/> |
|[<span data-ttu-id="5e567-177">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="5e567-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="5e567-178">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="5e567-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="5e567-179">Culture</span><span class="sxs-lookup"><span data-stu-id="5e567-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="5e567-180">Representa la referencia cultural de un elemento determinado en un buzón.</span><span class="sxs-lookup"><span data-stu-id="5e567-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5e567-181">Sender</span><span class="sxs-lookup"><span data-stu-id="5e567-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="5e567-182">Identifica al remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="5e567-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="5e567-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="5e567-184">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5e567-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="5e567-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="5e567-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="5e567-186">Representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5e567-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="5e567-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="5e567-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="5e567-188">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5e567-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="5e567-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="5e567-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="5e567-190">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="5e567-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="5e567-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="5e567-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="5e567-192">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="5e567-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="5e567-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="5e567-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="5e567-194">Contiene un identificador binario que representa el subproceso al que pertenece el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5e567-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="5e567-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="5e567-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="5e567-196">Representa el identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="5e567-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="5e567-197">From</span><span class="sxs-lookup"><span data-stu-id="5e567-197">From</span></span>](from.md) <br/> |<span data-ttu-id="5e567-198">Representa el destinatario del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5e567-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="5e567-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="5e567-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="5e567-200">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="5e567-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="5e567-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="5e567-202">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5e567-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="5e567-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="5e567-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="5e567-204">Indica si se solicita una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5e567-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="5e567-205">References</span><span class="sxs-lookup"><span data-stu-id="5e567-205">References</span></span>](references.md) <br/> |<span data-ttu-id="5e567-206">Representa el encabezado Usenet que se usa para correlacionar las respuestas con sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="5e567-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="5e567-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="5e567-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="5e567-208">Identifica un conjunto de direcciones a las que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="5e567-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="5e567-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="5e567-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="5e567-210">Representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md).</span><span class="sxs-lookup"><span data-stu-id="5e567-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="5e567-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="5e567-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="5e567-212">Indica si una reunión se controló mediante una cuenta con acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="5e567-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="5e567-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="5e567-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="5e567-214">Indica si un mensaje de reunión está desactualizado.</span><span class="sxs-lookup"><span data-stu-id="5e567-214">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="5e567-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="5e567-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="5e567-216">Indica si se ha procesado un elemento de mensaje de reunión.</span><span class="sxs-lookup"><span data-stu-id="5e567-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="5e567-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="5e567-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="5e567-218">Representa el tipo de respuesta de destinatarios que se ha recibido para una reunión.</span><span class="sxs-lookup"><span data-stu-id="5e567-218">Represents the type of recipient response received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="5e567-219">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="5e567-219">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="5e567-220">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="5e567-220">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="5e567-221">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5e567-221">This element is read-only.</span></span> <span data-ttu-id="5e567-222">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5e567-222">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="5e567-223">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="5e567-223">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="5e567-224">Contiene el nombre para mostrar del último usuario que modificó un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-224">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="5e567-225">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="5e567-225">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="5e567-226">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e567-226">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="5e567-227">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="5e567-227">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="5e567-228">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5e567-228">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="5e567-229">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="5e567-229">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="5e567-230">Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="5e567-230">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="5e567-231">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="5e567-231">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="5e567-232">Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="5e567-232">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="5e567-233">ConversationId</span><span class="sxs-lookup"><span data-stu-id="5e567-233">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="5e567-234">Contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="5e567-234">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="5e567-235">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="5e567-235">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="5e567-236">Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="5e567-236">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="5e567-237">EXCLUSIVO</span><span class="sxs-lookup"><span data-stu-id="5e567-237">UID</span></span>](uid.md) <br/> |<span data-ttu-id="5e567-238">Identifica un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="5e567-238">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5e567-239">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="5e567-239">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="5e567-240">Se usa para identificar una instancia específica de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="5e567-240">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5e567-241">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="5e567-241">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="5e567-242">Indica la fecha y la hora en que se creó una instancia de un objeto iCalendar.</span><span class="sxs-lookup"><span data-stu-id="5e567-242">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5e567-243">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5e567-243">Parent elements</span></span>

|<span data-ttu-id="5e567-244">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5e567-244">**Element**</span></span>|<span data-ttu-id="5e567-245">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e567-245">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e567-246">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="5e567-246">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="5e567-247">Describe todos los elementos de calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="5e567-247">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="5e567-248">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="5e567-248">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="5e567-249">Identifica los datos que se van a anexar a una sola propiedad de un elemento durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5e567-249">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="5e567-250">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="5e567-250">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="5e567-251">Identifica todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="5e567-251">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="5e567-252">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5e567-252">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="5e567-253">Identifica un solo elemento que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="5e567-253">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5e567-254">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5e567-254">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="5e567-255">Identifica un elemento único para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="5e567-255">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5e567-256">Items</span><span class="sxs-lookup"><span data-stu-id="5e567-256">Items</span></span>](items.md) <br/> |<span data-ttu-id="5e567-257">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="5e567-257">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="5e567-258">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="5e567-258">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="5e567-259">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="5e567-259">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="5e567-260">SetItemField</span><span class="sxs-lookup"><span data-stu-id="5e567-260">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="5e567-261">Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5e567-261">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="5e567-262">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="5e567-262">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="5e567-263">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e567-263">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5e567-264">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5e567-264">Text value</span></span>

<span data-ttu-id="5e567-265">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5e567-265">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e567-266">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e567-266">Remarks</span></span>

<span data-ttu-id="5e567-267">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e567-267">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e567-268">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5e567-268">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e567-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e567-269">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5e567-270">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5e567-270">Schema Name</span></span>  <br/> |<span data-ttu-id="5e567-271">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5e567-271">Types schema</span></span>  <br/> |
|<span data-ttu-id="5e567-272">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5e567-272">Validation File</span></span>  <br/> |<span data-ttu-id="5e567-273">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5e567-273">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5e567-274">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5e567-274">Can be Empty</span></span>  <br/> |<span data-ttu-id="5e567-275">Falso</span><span class="sxs-lookup"><span data-stu-id="5e567-275">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e567-276">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e567-276">See also</span></span>



- [<span data-ttu-id="5e567-277">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5e567-277">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: Mensaje
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
description: El elemento message representa un mensaje de correo electrónico de Microsoft Exchange.
ms.openlocfilehash: 510e97572e54f0ea0cb65fc7c75910e69cc0651f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467784"
---
# <a name="message"></a><span data-ttu-id="c392a-103">Mensaje</span><span class="sxs-lookup"><span data-stu-id="c392a-103">Message</span></span>

<span data-ttu-id="c392a-104">El elemento **Message** representa un mensaje de correo electrónico de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="c392a-104">The **Message** element represents a Microsoft Exchange e-mail message.</span></span> 
  
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

 <span data-ttu-id="c392a-105">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="c392a-105">**MessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c392a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c392a-106">Attributes and elements</span></span>

<span data-ttu-id="c392a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c392a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c392a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c392a-108">Attributes</span></span>

<span data-ttu-id="c392a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c392a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c392a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c392a-110">Child elements</span></span>

|<span data-ttu-id="c392a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c392a-111">**Element**</span></span>|<span data-ttu-id="c392a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c392a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c392a-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="c392a-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="c392a-114">Contiene la secuencia nativa de extensiones de correo de Internet multipropósito (MIME) de un objeto representado en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="c392a-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="c392a-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="c392a-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="c392a-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c392a-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="c392a-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c392a-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c392a-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="c392a-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="c392a-119">Representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="c392a-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="c392a-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c392a-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c392a-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="c392a-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="c392a-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="c392a-123">Asunto</span><span class="sxs-lookup"><span data-stu-id="c392a-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="c392a-124">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c392a-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="c392a-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c392a-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="c392a-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="c392a-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="c392a-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="c392a-128">Body</span><span class="sxs-lookup"><span data-stu-id="c392a-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="c392a-129">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c392a-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="c392a-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="c392a-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c392a-131">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c392a-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c392a-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="c392a-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="c392a-133">Representa la fecha y la hora en que se recibió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c392a-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="c392a-134">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c392a-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="c392a-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="c392a-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c392a-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c392a-137">Categorías</span><span class="sxs-lookup"><span data-stu-id="c392a-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c392a-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="c392a-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="c392a-139">Importance</span><span class="sxs-lookup"><span data-stu-id="c392a-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="c392a-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="c392a-141">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="c392a-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="c392a-142">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="c392a-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="c392a-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="c392a-144">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="c392a-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="c392a-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="c392a-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="c392a-146">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="c392a-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="c392a-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="c392a-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="c392a-148">Indica si un usuario envió un elemento a ella o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="c392a-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="c392a-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="c392a-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="c392a-150">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="c392a-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="c392a-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="c392a-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="c392a-152">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="c392a-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="c392a-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="c392a-154">Representa la colección de todos los encabezados de mensajes de Internet que se encuentran dentro de un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c392a-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c392a-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="c392a-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="c392a-156">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c392a-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="c392a-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="c392a-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="c392a-158">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="c392a-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="c392a-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="c392a-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="c392a-160">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c392a-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c392a-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="c392a-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="c392a-162">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="c392a-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="c392a-163">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="c392a-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="c392a-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="c392a-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="c392a-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c392a-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c392a-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="c392a-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="c392a-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="c392a-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="c392a-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="c392a-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="c392a-169">Representa la cadena para mostrar que se usa para el contenido de la línea CC.</span><span class="sxs-lookup"><span data-stu-id="c392a-169">Represents the display string that is used for the contents of the CC line.</span></span> <span data-ttu-id="c392a-170">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="c392a-170">This is the concatenated string of all CC recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="c392a-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="c392a-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="c392a-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="c392a-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="c392a-173">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="c392a-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="c392a-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="c392a-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="c392a-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible.</span><span class="sxs-lookup"><span data-stu-id="c392a-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="c392a-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c392a-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c392a-177">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="c392a-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="c392a-178">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="c392a-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="c392a-179">Culture</span><span class="sxs-lookup"><span data-stu-id="c392a-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="c392a-180">Representa la referencia cultural de un elemento determinado en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c392a-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c392a-181">Sender</span><span class="sxs-lookup"><span data-stu-id="c392a-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="c392a-182">Identifica al remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="c392a-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="c392a-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="c392a-184">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c392a-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="c392a-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="c392a-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="c392a-186">Representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c392a-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="c392a-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="c392a-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="c392a-188">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c392a-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c392a-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c392a-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="c392a-190">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="c392a-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="c392a-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c392a-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="c392a-192">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="c392a-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="c392a-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="c392a-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="c392a-194">Contiene un identificador binario que representa el subproceso al que pertenece el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c392a-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="c392a-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="c392a-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="c392a-196">Representa el identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="c392a-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="c392a-197">From</span><span class="sxs-lookup"><span data-stu-id="c392a-197">From</span></span>](from.md) <br/> |<span data-ttu-id="c392a-198">Representa el destinatario del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c392a-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="c392a-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="c392a-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="c392a-200">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="c392a-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="c392a-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="c392a-202">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c392a-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="c392a-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="c392a-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="c392a-204">Indica si se solicita una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c392a-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="c392a-205">References</span><span class="sxs-lookup"><span data-stu-id="c392a-205">References</span></span>](references.md) <br/> |<span data-ttu-id="c392a-206">Representa el encabezado Usenet que se usa para correlacionar las respuestas con sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="c392a-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="c392a-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="c392a-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="c392a-208">Identifica un conjunto de direcciones a las que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="c392a-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="c392a-209">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="c392a-209">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="c392a-210">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="c392a-210">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="c392a-211">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c392a-211">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c392a-212">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="c392a-212">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="c392a-213">Identifica el delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="c392a-213">Identifies the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="c392a-214">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="c392a-214">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="c392a-215">Identifica la entidad de identidad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="c392a-215">Identifies the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="c392a-216">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="c392a-216">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="c392a-217">Contiene el nombre para mostrar del último usuario que modificó un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-217">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="c392a-218">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="c392a-218">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="c392a-219">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="c392a-219">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="c392a-220">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="c392a-220">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="c392a-221">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c392a-221">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="c392a-222">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="c392a-222">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="c392a-223">Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="c392a-223">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="c392a-224">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="c392a-224">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="c392a-225">Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="c392a-225">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="c392a-226">ConversationId</span><span class="sxs-lookup"><span data-stu-id="c392a-226">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="c392a-227">Contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="c392a-227">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="c392a-228">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="c392a-228">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="c392a-229">Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="c392a-229">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="c392a-230">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="c392a-230">ReminderMessageData</span></span>](remindermessagedata.md) <br/> |<span data-ttu-id="c392a-231">Contiene los datos de un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="c392a-231">Contains the data for a reminder message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c392a-232">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c392a-232">Parent elements</span></span>

|<span data-ttu-id="c392a-233">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c392a-233">**Element**</span></span>|<span data-ttu-id="c392a-234">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c392a-234">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c392a-235">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="c392a-235">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="c392a-236">Describe todos los elementos de calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="c392a-236">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="c392a-237">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="c392a-237">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="c392a-238">Identifica los datos que se van a anexar a una sola propiedad de un elemento durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c392a-238">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c392a-239">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="c392a-239">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="c392a-240">Identifica todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="c392a-240">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="c392a-241">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c392a-241">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="c392a-242">Identifica un solo elemento que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="c392a-242">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c392a-243">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="c392a-243">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="c392a-244">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c392a-244">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="c392a-245">Items</span><span class="sxs-lookup"><span data-stu-id="c392a-245">Items</span></span>](items.md) <br/> |<span data-ttu-id="c392a-246">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="c392a-246">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="c392a-247">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c392a-247">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="c392a-248">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="c392a-248">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="c392a-249">SetItemField</span><span class="sxs-lookup"><span data-stu-id="c392a-249">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="c392a-250">Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c392a-250">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c392a-251">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c392a-251">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="c392a-252">Identifica un elemento único para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="c392a-252">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c392a-253">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c392a-253">Text value</span></span>

<span data-ttu-id="c392a-254">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c392a-254">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c392a-255">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c392a-255">Remarks</span></span>

<span data-ttu-id="c392a-256">Las operaciones de disponibilidad usan otro elemento de **mensaje** , [Message (disponibilidad)](message-availability.md) para devolver mensajes OOF.</span><span class="sxs-lookup"><span data-stu-id="c392a-256">Another **Message** element, [Message (Availability)](message-availability.md) is used by the Availability operations to return OOF messages.</span></span> 
  
<span data-ttu-id="c392a-257">Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no son fuertemente tipados por el esquema de servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="c392a-257">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="c392a-258">Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="c392a-258">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="c392a-259">Exchange 2010 no devuelve el elemento de **elemento** base en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="c392a-259">Exchange 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="c392a-260">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c392a-260">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c392a-261">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c392a-261">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c392a-262">Namespace</span><span class="sxs-lookup"><span data-stu-id="c392a-262">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c392a-263">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c392a-263">Schema Name</span></span>  <br/> |<span data-ttu-id="c392a-264">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c392a-264">Types schema</span></span>  <br/> |
|<span data-ttu-id="c392a-265">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c392a-265">Validation File</span></span>  <br/> |<span data-ttu-id="c392a-266">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c392a-266">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c392a-267">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c392a-267">Can be Empty</span></span>  <br/> |<span data-ttu-id="c392a-268">Falso</span><span class="sxs-lookup"><span data-stu-id="c392a-268">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c392a-269">Vea también</span><span class="sxs-lookup"><span data-stu-id="c392a-269">See also</span></span>



- [<span data-ttu-id="c392a-270">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c392a-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: PostReplyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostReplyItem
api_type:
- schema
ms.assetid: e5d93d63-0a3b-470f-9a94-2d57284c6745
description: El elemento PostReplyItem contiene una respuesta a un elemento post. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 4104e79449acc6e358b729cf2de769d28dac52bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461684"
---
# <a name="postreplyitem"></a><span data-ttu-id="33704-104">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="33704-104">PostReplyItem</span></span>

<span data-ttu-id="33704-105">El elemento **PostReplyItem** contiene una respuesta a un elemento post.</span><span class="sxs-lookup"><span data-stu-id="33704-105">The **PostReplyItem** element contains a reply to a post item.</span></span> <span data-ttu-id="33704-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="33704-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PostReplyItem>
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
   <NewBodyContent/>
</PostReplyItem>
```

 <span data-ttu-id="33704-107">**PostReplyItemType**</span><span class="sxs-lookup"><span data-stu-id="33704-107">**PostReplyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33704-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="33704-108">Attributes and elements</span></span>

<span data-ttu-id="33704-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="33704-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33704-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="33704-110">Attributes</span></span>

<span data-ttu-id="33704-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="33704-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33704-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="33704-112">Child elements</span></span>

|<span data-ttu-id="33704-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="33704-113">**Element**</span></span>|<span data-ttu-id="33704-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33704-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33704-115">MimeContent</span><span class="sxs-lookup"><span data-stu-id="33704-115">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="33704-116">Contiene la secuencia nativa de extensiones de correo de Internet multipropósito (MIME) de un objeto representado en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="33704-116">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="33704-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="33704-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="33704-118">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="33704-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="33704-119">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="33704-119">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="33704-120">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="33704-120">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="33704-121">Representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="33704-121">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="33704-122">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="33704-122">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="33704-123">ItemClass</span><span class="sxs-lookup"><span data-stu-id="33704-123">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="33704-124">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-124">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="33704-125">Asunto</span><span class="sxs-lookup"><span data-stu-id="33704-125">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="33704-126">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="33704-126">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="33704-127">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="33704-127">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="33704-128">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="33704-128">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="33704-129">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-129">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="33704-130">Body</span><span class="sxs-lookup"><span data-stu-id="33704-130">Body</span></span>](body.md) <br/> |<span data-ttu-id="33704-131">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="33704-131">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="33704-132">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="33704-132">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="33704-133">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="33704-133">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="33704-134">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="33704-134">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="33704-135">Representa la fecha y la hora en que se recibió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="33704-135">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="33704-136">Tamaño</span><span class="sxs-lookup"><span data-stu-id="33704-136">Size</span></span>](size.md) <br/> |<span data-ttu-id="33704-137">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-137">Represents the size in bytes of an item.</span></span> <span data-ttu-id="33704-138">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="33704-138">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="33704-139">Categorías</span><span class="sxs-lookup"><span data-stu-id="33704-139">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="33704-140">Representa una colección de cadenas que identifican las categorías a las que pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="33704-140">Represents a collection of strings that identify categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="33704-141">Importance</span><span class="sxs-lookup"><span data-stu-id="33704-141">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="33704-142">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-142">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="33704-143">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="33704-143">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="33704-144">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-144">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="33704-145">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="33704-145">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="33704-146">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="33704-146">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="33704-147">IsDraft</span><span class="sxs-lookup"><span data-stu-id="33704-147">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="33704-148">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="33704-148">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="33704-149">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="33704-149">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="33704-150">Indica si un usuario envió un elemento a ella o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="33704-150">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="33704-151">IsResend</span><span class="sxs-lookup"><span data-stu-id="33704-151">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="33704-152">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="33704-152">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="33704-153">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="33704-153">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="33704-154">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-154">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="33704-155">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="33704-155">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="33704-156">Representa la colección de todos los encabezados de mensajes de Internet que contiene un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="33704-156">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="33704-157">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="33704-157">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="33704-158">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="33704-158">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="33704-159">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="33704-159">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="33704-160">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="33704-160">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="33704-161">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="33704-161">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="33704-162">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="33704-162">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="33704-163">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="33704-163">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="33704-164">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="33704-164">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="33704-165">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="33704-165">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="33704-166">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="33704-166">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="33704-167">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="33704-167">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="33704-168">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="33704-168">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="33704-169">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="33704-169">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="33704-170">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="33704-170">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="33704-171">Representa la cadena para mostrar que se usa para el contenido de la línea CC.</span><span class="sxs-lookup"><span data-stu-id="33704-171">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="33704-172">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="33704-172">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="33704-173">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="33704-173">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="33704-174">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="33704-174">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="33704-175">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="33704-175">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="33704-176">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="33704-176">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="33704-177">Representa una propiedad que se establece en **true** si un elemento tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="33704-177">Represents a property that is set to **true** if an item has an attachment.</span></span> <span data-ttu-id="33704-178">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="33704-178">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="33704-179">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="33704-179">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="33704-180">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="33704-180">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="33704-181">Culture</span><span class="sxs-lookup"><span data-stu-id="33704-181">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="33704-182">Representa la referencia cultural de un elemento determinado en un buzón.</span><span class="sxs-lookup"><span data-stu-id="33704-182">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="33704-183">Sender</span><span class="sxs-lookup"><span data-stu-id="33704-183">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="33704-184">Identifica al remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-184">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="33704-185">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="33704-185">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="33704-186">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="33704-186">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="33704-187">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="33704-187">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="33704-188">Representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="33704-188">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="33704-189">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="33704-189">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="33704-190">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="33704-190">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="33704-191">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="33704-191">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="33704-192">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="33704-192">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="33704-193">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="33704-193">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="33704-194">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="33704-194">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="33704-195">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="33704-195">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="33704-196">Contiene un identificador binario que representa el subproceso al que pertenece el mensaje.</span><span class="sxs-lookup"><span data-stu-id="33704-196">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="33704-197">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="33704-197">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="33704-198">Representa el identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="33704-198">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="33704-199">From</span><span class="sxs-lookup"><span data-stu-id="33704-199">From</span></span>](from.md) <br/> |<span data-ttu-id="33704-200">Representa la dirección desde la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="33704-200">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="33704-201">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="33704-201">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="33704-202">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="33704-202">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="33704-203">IsRead</span><span class="sxs-lookup"><span data-stu-id="33704-203">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="33704-204">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="33704-204">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="33704-205">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="33704-205">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="33704-206">Indica si se solicita una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="33704-206">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="33704-207">References</span><span class="sxs-lookup"><span data-stu-id="33704-207">References</span></span>](references.md) <br/> |<span data-ttu-id="33704-208">Representa el encabezado Usenet que se usa para asociar respuestas a sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="33704-208">Represents the Usenet header that is used to associate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="33704-209">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="33704-209">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="33704-210">Identifica un conjunto de direcciones a las que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="33704-210">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="33704-211">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="33704-211">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="33704-212">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="33704-212">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="33704-213">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="33704-213">This element is read-only.</span></span> <span data-ttu-id="33704-214">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="33704-214">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="33704-215">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="33704-215">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="33704-216">Identifica el delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="33704-216">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="33704-217">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="33704-217">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="33704-218">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="33704-218">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="33704-219">Identifica la entidad de identidad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="33704-219">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="33704-220">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="33704-220">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="33704-221">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="33704-221">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="33704-222">Representa el nuevo contenido del cuerpo de un elemento post.</span><span class="sxs-lookup"><span data-stu-id="33704-222">Represents the new body content of a post item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="33704-223">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="33704-223">Parent elements</span></span>

|<span data-ttu-id="33704-224">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="33704-224">**Element**</span></span>|<span data-ttu-id="33704-225">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33704-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33704-226">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="33704-226">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="33704-227">Describe todos los elementos adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="33704-227">Describes all items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="33704-228">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="33704-228">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="33704-229">Describe todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="33704-229">Describes all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="33704-230">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="33704-230">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="33704-231">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="33704-231">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="33704-232">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="33704-232">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="33704-233">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="33704-233">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33704-234">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33704-234">Remarks</span></span>

<span data-ttu-id="33704-235">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="33704-235">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33704-236">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="33704-236">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33704-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="33704-237">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="33704-238">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="33704-238">Schema Name</span></span>  <br/> |<span data-ttu-id="33704-239">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="33704-239">Types schema</span></span>  <br/> |
|<span data-ttu-id="33704-240">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="33704-240">Validation File</span></span>  <br/> |<span data-ttu-id="33704-241">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="33704-241">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="33704-242">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="33704-242">Can be Empty</span></span>  <br/> |<span data-ttu-id="33704-243">Falso</span><span class="sxs-lookup"><span data-stu-id="33704-243">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33704-244">Vea también</span><span class="sxs-lookup"><span data-stu-id="33704-244">See also</span></span>



- [<span data-ttu-id="33704-245">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="33704-245">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


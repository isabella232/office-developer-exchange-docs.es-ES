---
title: MeetingResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingResponse
api_type:
- schema
ms.assetid: 9f798e79-dafd-4d4d-9967-95fd8e5c0502
description: El elemento MeetingResponse representa una respuesta a la reunión en el almacén de Exchange.
ms.openlocfilehash: c5f9f3ac2fcd12e9c95f663311c33cdd36783251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836446"
---
# <a name="meetingresponse"></a><span data-ttu-id="f4f6f-103">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="f4f6f-103">MeetingResponse</span></span>

<span data-ttu-id="f4f6f-104">El elemento **MeetingResponse** representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-104">The **MeetingResponse** element represents a meeting response in the Exchange store.</span></span> 
  
```xml
<MeetingResponse>
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
   <ReceivedBy/>
   <ReceivedRepresenting/>
</MeetingResponse>
```

 <span data-ttu-id="f4f6f-105">**MeetingResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f4f6f-105">**MeetingResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4f6f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f4f6f-106">Attributes and elements</span></span>

<span data-ttu-id="f4f6f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4f6f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4f6f-108">Attributes</span></span>

<span data-ttu-id="f4f6f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4f6f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4f6f-110">Child elements</span></span>

|<span data-ttu-id="f4f6f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4f6f-111">**Element**</span></span>|<span data-ttu-id="f4f6f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4f6f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4f6f-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="f4f6f-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="f4f6f-114">Contiene la secuencia MIME nativa de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="f4f6f-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f4f6f-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="f4f6f-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-118">Id</span><span class="sxs-lookup"><span data-stu-id="f4f6f-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f4f6f-119">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="f4f6f-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="f4f6f-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="f4f6f-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-123">Subject</span><span class="sxs-lookup"><span data-stu-id="f4f6f-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f4f6f-124">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="f4f6f-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-126">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="f4f6f-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="f4f6f-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-128">Body</span><span class="sxs-lookup"><span data-stu-id="f4f6f-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="f4f6f-129">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="f4f6f-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f4f6f-131">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="f4f6f-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="f4f6f-133">Representa los datos y la hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-133">Represents the data and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-134">Size</span><span class="sxs-lookup"><span data-stu-id="f4f6f-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="f4f6f-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="f4f6f-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-137">Categories</span><span class="sxs-lookup"><span data-stu-id="f4f6f-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f4f6f-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-139">Importancia</span><span class="sxs-lookup"><span data-stu-id="f4f6f-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="f4f6f-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="f4f6f-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="f4f6f-142">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="f4f6f-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="f4f6f-144">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="f4f6f-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="f4f6f-146">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="f4f6f-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="f4f6f-148">Indica si un usuario envía un elemento a él o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="f4f6f-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="f4f6f-150">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="f4f6f-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="f4f6f-152">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="f4f6f-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="f4f6f-154">Representa la colección de todos los encabezados de mensaje de Internet que están dentro de un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="f4f6f-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="f4f6f-156">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="f4f6f-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="f4f6f-158">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f4f6f-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f4f6f-160">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="f4f6f-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="f4f6f-162">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="f4f6f-163">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="f4f6f-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="f4f6f-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="f4f6f-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="f4f6f-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="f4f6f-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="f4f6f-169">Representa la cadena para mostrar que se usa para el contenido del cuadro Cc.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="f4f6f-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="f4f6f-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="f4f6f-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="f4f6f-173">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="f4f6f-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="f4f6f-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="f4f6f-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="f4f6f-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="f4f6f-178">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-179">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="f4f6f-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="f4f6f-180">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-181">Sender</span><span class="sxs-lookup"><span data-stu-id="f4f6f-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="f4f6f-182">Identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="f4f6f-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="f4f6f-184">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="f4f6f-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="f4f6f-186">Representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="f4f6f-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="f4f6f-188">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f4f6f-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="f4f6f-190">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f4f6f-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="f4f6f-192">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="f4f6f-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="f4f6f-194">Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="f4f6f-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="f4f6f-196">Representa el identificador de conversación.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-197">From</span><span class="sxs-lookup"><span data-stu-id="f4f6f-197">From</span></span>](from.md) <br/> |<span data-ttu-id="f4f6f-198">Representa al destinatario de la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="f4f6f-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="f4f6f-200">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-201">Estáleído</span><span class="sxs-lookup"><span data-stu-id="f4f6f-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="f4f6f-202">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="f4f6f-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="f4f6f-204">Indica si se ha solicitado una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-205">Referencias</span><span class="sxs-lookup"><span data-stu-id="f4f6f-205">References</span></span>](references.md) <br/> |<span data-ttu-id="f4f6f-206">Representa el encabezado de Usenet que se usa para correlacionar las respuestas con sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="f4f6f-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="f4f6f-208">Identifica un conjunto de direcciones a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="f4f6f-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="f4f6f-210">Representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md).</span><span class="sxs-lookup"><span data-stu-id="f4f6f-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="f4f6f-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="f4f6f-212">Indica si una reunión se ha controlado por una cuenta con acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="f4f6f-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="f4f6f-214">Indica si un mensaje de reunión está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-214">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="f4f6f-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="f4f6f-216">Indica si un mensaje de reunión item se han procesado.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="f4f6f-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="f4f6f-218">Representa el tipo de respuesta de destinatarios que se recibe de una reunión.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-218">Represents the type of recipient response that is received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-219">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f4f6f-219">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f4f6f-220">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-220">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="f4f6f-221">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-221">This element is read-only.</span></span> <span data-ttu-id="f4f6f-222">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f4f6f-222">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-223">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="f4f6f-223">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="f4f6f-224">Identifica al delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-224">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="f4f6f-225">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-225">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-226">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="f4f6f-226">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="f4f6f-227">Identifica la entidad de seguridad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-227">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="f4f6f-228">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-228">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-229">UID</span><span class="sxs-lookup"><span data-stu-id="f4f6f-229">UID</span></span>](uid.md) <br/> |<span data-ttu-id="f4f6f-230">Identifica un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-230">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-231">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f4f6f-231">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="f4f6f-232">Se usa para identificar una instancia específica de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-232">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-233">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="f4f6f-233">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="f4f6f-234">Indica la fecha y hora en que se ha creado una instancia de un objeto de iCalendar.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-234">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4f6f-235">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4f6f-235">Parent elements</span></span>

|<span data-ttu-id="f4f6f-236">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4f6f-236">**Element**</span></span>|<span data-ttu-id="f4f6f-237">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4f6f-237">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4f6f-238">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f4f6f-238">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="f4f6f-239">Identifica todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-239">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-240">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="f4f6f-240">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="f4f6f-241">Identifica los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f4f6f-241">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-242">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f4f6f-242">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="f4f6f-243">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-243">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-244">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f4f6f-244">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="f4f6f-245">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-245">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-246">Items</span><span class="sxs-lookup"><span data-stu-id="f4f6f-246">Items</span></span>](items.md) <br/> |<span data-ttu-id="f4f6f-247">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-247">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-248">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f4f6f-248">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="f4f6f-249">Contiene una matriz de elementos que desea crear.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-249">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-250">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="f4f6f-250">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="f4f6f-251">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-251">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-252">SetItemField</span><span class="sxs-lookup"><span data-stu-id="f4f6f-252">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="f4f6f-253">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f4f6f-253">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f4f6f-254">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f4f6f-254">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="f4f6f-255">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-255">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4f6f-256">Notas</span><span class="sxs-lookup"><span data-stu-id="f4f6f-256">Remarks</span></span>

<span data-ttu-id="f4f6f-257">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-257">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4f6f-258">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4f6f-258">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4f6f-259">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4f6f-259">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4f6f-260">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f4f6f-260">Schema Name</span></span>  <br/> |<span data-ttu-id="f4f6f-261">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f4f6f-261">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4f6f-262">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f4f6f-262">Validation File</span></span>  <br/> |<span data-ttu-id="f4f6f-263">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f4f6f-263">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4f6f-264">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f4f6f-264">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4f6f-265">False</span><span class="sxs-lookup"><span data-stu-id="f4f6f-265">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4f6f-266">Ver también</span><span class="sxs-lookup"><span data-stu-id="f4f6f-266">See also</span></span>



- [<span data-ttu-id="f4f6f-267">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f4f6f-267">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


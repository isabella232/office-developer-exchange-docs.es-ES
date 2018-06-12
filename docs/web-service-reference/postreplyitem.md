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
description: El elemento PostReplyItem contiene una respuesta a un elemento para exponer. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 70a0d6a7c670d0f16a55e66e7ef329331a04a5f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836868"
---
# <a name="postreplyitem"></a><span data-ttu-id="f161e-104">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="f161e-104">PostReplyItem</span></span>

<span data-ttu-id="f161e-105">El elemento **PostReplyItem** contiene una respuesta a un elemento para exponer.</span><span class="sxs-lookup"><span data-stu-id="f161e-105">The **PostReplyItem** element contains a reply to a post item.</span></span> <span data-ttu-id="f161e-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f161e-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
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

 <span data-ttu-id="f161e-107">**PostReplyItemType**</span><span class="sxs-lookup"><span data-stu-id="f161e-107">**PostReplyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f161e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f161e-108">Attributes and elements</span></span>

<span data-ttu-id="f161e-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f161e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f161e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f161e-110">Attributes</span></span>

<span data-ttu-id="f161e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f161e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f161e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f161e-112">Child elements</span></span>

|<span data-ttu-id="f161e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f161e-113">**Element**</span></span>|<span data-ttu-id="f161e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f161e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f161e-115">MimeContent</span><span class="sxs-lookup"><span data-stu-id="f161e-115">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="f161e-116">Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="f161e-116">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="f161e-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="f161e-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f161e-118">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f161e-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="f161e-119">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f161e-119">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f161e-120">Id</span><span class="sxs-lookup"><span data-stu-id="f161e-120">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f161e-121">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f161e-121">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="f161e-122">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f161e-122">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f161e-123">ItemClass</span><span class="sxs-lookup"><span data-stu-id="f161e-123">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="f161e-124">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f161e-124">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="f161e-125">Subject</span><span class="sxs-lookup"><span data-stu-id="f161e-125">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f161e-126">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f161e-126">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="f161e-127">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f161e-127">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="f161e-128">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="f161e-128">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="f161e-129">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f161e-129">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="f161e-130">Body</span><span class="sxs-lookup"><span data-stu-id="f161e-130">Body</span></span>](body.md) <br/> |<span data-ttu-id="f161e-131">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f161e-131">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="f161e-132">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="f161e-132">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f161e-133">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f161e-133">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f161e-134">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="f161e-134">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="f161e-135">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f161e-135">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="f161e-136">Size</span><span class="sxs-lookup"><span data-stu-id="f161e-136">Size</span></span>](size.md) <br/> |<span data-ttu-id="f161e-137">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f161e-137">Represents the size in bytes of an item.</span></span> <span data-ttu-id="f161e-138">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f161e-138">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f161e-139">Categories</span><span class="sxs-lookup"><span data-stu-id="f161e-139">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f161e-140">Representa una colección de cadenas que identifican categorías a las que pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f161e-140">Represents a collection of strings that identify categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="f161e-141">Importancia</span><span class="sxs-lookup"><span data-stu-id="f161e-141">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="f161e-142">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f161e-142">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="f161e-143">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="f161e-143">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="f161e-144">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f161e-144">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="f161e-145">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="f161e-145">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="f161e-146">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="f161e-146">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="f161e-147">IsDraft</span><span class="sxs-lookup"><span data-stu-id="f161e-147">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="f161e-148">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="f161e-148">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="f161e-149">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="f161e-149">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="f161e-150">Indica si un usuario envía un elemento a él o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="f161e-150">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="f161e-151">IsResend</span><span class="sxs-lookup"><span data-stu-id="f161e-151">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="f161e-152">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f161e-152">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="f161e-153">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="f161e-153">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="f161e-154">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="f161e-154">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="f161e-155">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="f161e-155">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="f161e-156">Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f161e-156">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f161e-157">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="f161e-157">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="f161e-158">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f161e-158">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="f161e-159">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="f161e-159">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="f161e-160">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f161e-160">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="f161e-161">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f161e-161">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f161e-162">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f161e-162">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f161e-163">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="f161e-163">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="f161e-164">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="f161e-164">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="f161e-165">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="f161e-165">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f161e-166">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="f161e-166">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="f161e-167">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f161e-167">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f161e-168">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="f161e-168">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="f161e-169">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="f161e-169">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f161e-170">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="f161e-170">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="f161e-171">Representa la cadena para mostrar que se usa para el contenido de la línea Cc.</span><span class="sxs-lookup"><span data-stu-id="f161e-171">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="f161e-172">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="f161e-172">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f161e-173">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="f161e-173">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="f161e-174">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="f161e-174">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="f161e-175">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f161e-175">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f161e-176">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="f161e-176">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="f161e-177">Representa una propiedad que se establece en **true** si un elemento tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f161e-177">Represents a property that is set to **true** if an item has an attachment.</span></span> <span data-ttu-id="f161e-178">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f161e-178">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f161e-179">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="f161e-179">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="f161e-180">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="f161e-180">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="f161e-181">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="f161e-181">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="f161e-182">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f161e-182">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f161e-183">Sender</span><span class="sxs-lookup"><span data-stu-id="f161e-183">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="f161e-184">Identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f161e-184">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="f161e-185">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="f161e-185">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="f161e-186">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f161e-186">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="f161e-187">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="f161e-187">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="f161e-188">Representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f161e-188">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="f161e-189">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="f161e-189">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="f161e-190">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f161e-190">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="f161e-191">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f161e-191">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="f161e-192">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="f161e-192">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="f161e-193">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f161e-193">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="f161e-194">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="f161e-194">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="f161e-195">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="f161e-195">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="f161e-196">Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f161e-196">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="f161e-197">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="f161e-197">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="f161e-198">Representa el identificador de conversación.</span><span class="sxs-lookup"><span data-stu-id="f161e-198">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="f161e-199">From</span><span class="sxs-lookup"><span data-stu-id="f161e-199">From</span></span>](from.md) <br/> |<span data-ttu-id="f161e-200">Representa la dirección desde la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f161e-200">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="f161e-201">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="f161e-201">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="f161e-202">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f161e-202">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="f161e-203">Estáleído</span><span class="sxs-lookup"><span data-stu-id="f161e-203">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="f161e-204">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f161e-204">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="f161e-205">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="f161e-205">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="f161e-206">Indica si se ha solicitado una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f161e-206">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="f161e-207">Referencias</span><span class="sxs-lookup"><span data-stu-id="f161e-207">References</span></span>](references.md) <br/> |<span data-ttu-id="f161e-208">Representa el encabezado de Usenet que se usa para asociar las respuestas a sus mensajes de originales.</span><span class="sxs-lookup"><span data-stu-id="f161e-208">Represents the Usenet header that is used to associate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="f161e-209">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="f161e-209">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="f161e-210">Identifica un conjunto de direcciones a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="f161e-210">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="f161e-211">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f161e-211">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f161e-212">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f161e-212">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="f161e-213">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f161e-213">This element is read-only.</span></span> <span data-ttu-id="f161e-214">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f161e-214">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f161e-215">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="f161e-215">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="f161e-216">Identifica al delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f161e-216">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="f161e-217">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f161e-217">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f161e-218">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="f161e-218">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="f161e-219">Identifica la entidad de seguridad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f161e-219">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="f161e-220">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f161e-220">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f161e-221">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="f161e-221">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="f161e-222">Representa el nuevo contenido del cuerpo de un elemento para exponer.</span><span class="sxs-lookup"><span data-stu-id="f161e-222">Represents the new body content of a post item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f161e-223">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f161e-223">Parent elements</span></span>

|<span data-ttu-id="f161e-224">**Element**</span><span class="sxs-lookup"><span data-stu-id="f161e-224">**Element**</span></span>|<span data-ttu-id="f161e-225">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f161e-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f161e-226">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f161e-226">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="f161e-227">Describe todos los elementos que están adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="f161e-227">Describes all items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f161e-228">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f161e-228">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="f161e-229">Describe todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f161e-229">Describes all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f161e-230">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f161e-230">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f161e-231">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f161e-231">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f161e-232">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f161e-232">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="f161e-233">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="f161e-233">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f161e-234">Notas</span><span class="sxs-lookup"><span data-stu-id="f161e-234">Remarks</span></span>

<span data-ttu-id="f161e-235">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f161e-235">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f161e-236">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f161e-236">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f161e-237">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f161e-237">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f161e-238">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f161e-238">Schema Name</span></span>  <br/> |<span data-ttu-id="f161e-239">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f161e-239">Types schema</span></span>  <br/> |
|<span data-ttu-id="f161e-240">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f161e-240">Validation File</span></span>  <br/> |<span data-ttu-id="f161e-241">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f161e-241">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f161e-242">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f161e-242">Can be Empty</span></span>  <br/> |<span data-ttu-id="f161e-243">False</span><span class="sxs-lookup"><span data-stu-id="f161e-243">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f161e-244">Ver también</span><span class="sxs-lookup"><span data-stu-id="f161e-244">See also</span></span>



- [<span data-ttu-id="f161e-245">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f161e-245">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


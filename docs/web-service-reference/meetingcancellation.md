---
title: MeetingCancellation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingCancellation
api_type:
- schema
ms.assetid: a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea
description: El elemento MeetingCancellation representa la cancelación de la reunión en el almacén de Exchange.
ms.openlocfilehash: b68135e2743c675bed92c54172369c2ef21f1a6d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836447"
---
# <a name="meetingcancellation"></a><span data-ttu-id="94ee0-103">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="94ee0-103">MeetingCancellation</span></span>

<span data-ttu-id="94ee0-104">El elemento **MeetingCancellation** representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="94ee0-104">The **MeetingCancellation** element represents a meeting cancellation in the Exchange store.</span></span> 
  
```xml
<MeetingCancellation>
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
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
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
</MeetingCancellation>
```

 <span data-ttu-id="94ee0-105">**MeetingCancellationMessageType**</span><span class="sxs-lookup"><span data-stu-id="94ee0-105">**MeetingCancellationMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94ee0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="94ee0-106">Attributes and elements</span></span>

<span data-ttu-id="94ee0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="94ee0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94ee0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="94ee0-108">Attributes</span></span>

<span data-ttu-id="94ee0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="94ee0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="94ee0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94ee0-110">Child elements</span></span>

|<span data-ttu-id="94ee0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="94ee0-111">**Element**</span></span>|<span data-ttu-id="94ee0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94ee0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94ee0-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="94ee0-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="94ee0-114">Contiene la secuencia MIME nativa de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="94ee0-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="94ee0-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="94ee0-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="94ee0-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="94ee0-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="94ee0-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-118">Id</span><span class="sxs-lookup"><span data-stu-id="94ee0-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="94ee0-119">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="94ee0-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="94ee0-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="94ee0-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="94ee0-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="94ee0-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-123">Subject</span><span class="sxs-lookup"><span data-stu-id="94ee0-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="94ee0-124">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="94ee0-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="94ee0-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="94ee0-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-126">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="94ee0-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="94ee0-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-128">Body</span><span class="sxs-lookup"><span data-stu-id="94ee0-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="94ee0-129">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="94ee0-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="94ee0-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="94ee0-131">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="94ee0-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="94ee0-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="94ee0-133">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="94ee0-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-134">Size</span><span class="sxs-lookup"><span data-stu-id="94ee0-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="94ee0-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="94ee0-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="94ee0-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-137">Categories</span><span class="sxs-lookup"><span data-stu-id="94ee0-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="94ee0-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="94ee0-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-139">Importancia</span><span class="sxs-lookup"><span data-stu-id="94ee0-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="94ee0-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="94ee0-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="94ee0-142">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="94ee0-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="94ee0-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="94ee0-144">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="94ee0-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="94ee0-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="94ee0-146">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="94ee0-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="94ee0-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="94ee0-148">Indica si un usuario envía un elemento a él o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="94ee0-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="94ee0-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="94ee0-150">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="94ee0-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="94ee0-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="94ee0-152">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="94ee0-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="94ee0-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="94ee0-154">Representa la colección de todos los encabezados de mensaje de Internet que están dentro de un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="94ee0-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="94ee0-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="94ee0-156">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="94ee0-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="94ee0-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="94ee0-158">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="94ee0-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="94ee0-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="94ee0-160">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="94ee0-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="94ee0-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="94ee0-162">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="94ee0-163">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="94ee0-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="94ee0-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="94ee0-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="94ee0-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="94ee0-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="94ee0-167">Representa el número de minutos antes de un evento que se muestre un aviso.</span><span class="sxs-lookup"><span data-stu-id="94ee0-167">Represents the number of minutes before an event that a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="94ee0-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="94ee0-169">Representa la cadena para mostrar que se usa para el contenido del cuadro Cc.</span><span class="sxs-lookup"><span data-stu-id="94ee0-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="94ee0-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="94ee0-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="94ee0-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="94ee0-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="94ee0-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="94ee0-173">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="94ee0-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="94ee0-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="94ee0-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="94ee0-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="94ee0-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="94ee0-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="94ee0-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="94ee0-178">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="94ee0-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-179">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="94ee0-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="94ee0-180">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="94ee0-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="94ee0-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="94ee0-182">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="94ee0-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="94ee0-183">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="94ee0-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="94ee0-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="94ee0-185">Contiene el nombre para mostrar del último usuario para modificar un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="94ee0-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="94ee0-187">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="94ee0-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="94ee0-189">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="94ee0-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="94ee0-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="94ee0-191">Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="94ee0-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="94ee0-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="94ee0-193">Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="94ee0-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="94ee0-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="94ee0-195">Contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="94ee0-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="94ee0-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="94ee0-197">Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="94ee0-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-198">Sender</span><span class="sxs-lookup"><span data-stu-id="94ee0-198">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="94ee0-199">Identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-199">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-200">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="94ee0-200">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="94ee0-201">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="94ee0-201">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-202">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="94ee0-202">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="94ee0-203">Representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="94ee0-203">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-204">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="94ee0-204">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="94ee0-205">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="94ee0-205">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-206">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="94ee0-206">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="94ee0-207">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="94ee0-207">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-208">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="94ee0-208">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="94ee0-209">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="94ee0-209">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-210">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="94ee0-210">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="94ee0-211">Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.</span><span class="sxs-lookup"><span data-stu-id="94ee0-211">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-212">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="94ee0-212">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="94ee0-213">Representa el identificador de conversación.</span><span class="sxs-lookup"><span data-stu-id="94ee0-213">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-214">From</span><span class="sxs-lookup"><span data-stu-id="94ee0-214">From</span></span>](from.md) <br/> |<span data-ttu-id="94ee0-215">Representa al destinatario de la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="94ee0-215">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-216">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="94ee0-216">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="94ee0-217">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="94ee0-217">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-218">Estáleído</span><span class="sxs-lookup"><span data-stu-id="94ee0-218">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="94ee0-219">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="94ee0-219">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-220">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="94ee0-220">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="94ee0-221">Indica si se ha solicitado una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="94ee0-221">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-222">Referencias</span><span class="sxs-lookup"><span data-stu-id="94ee0-222">References</span></span>](references.md) <br/> |<span data-ttu-id="94ee0-223">Representa el encabezado de Usenet que se usa para correlacionar las respuestas con sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="94ee0-223">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-224">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="94ee0-224">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="94ee0-225">Identifica un conjunto de direcciones a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="94ee0-225">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-226">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="94ee0-226">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="94ee0-227">Representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md).</span><span class="sxs-lookup"><span data-stu-id="94ee0-227">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="94ee0-228">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="94ee0-228">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="94ee0-229">Indica si una reunión se ha controlado por una cuenta con acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="94ee0-229">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-230">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="94ee0-230">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="94ee0-231">Indica si un mensaje de reunión está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="94ee0-231">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-232">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="94ee0-232">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="94ee0-233">Indica si un mensaje de reunión item se han procesado.</span><span class="sxs-lookup"><span data-stu-id="94ee0-233">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-234">ResponseType</span><span class="sxs-lookup"><span data-stu-id="94ee0-234">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="94ee0-235">Representa el tipo de destinatario respuesta recibida para una reunión.</span><span class="sxs-lookup"><span data-stu-id="94ee0-235">Represents the type of recipient response received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-236">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="94ee0-236">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="94ee0-237">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="94ee0-237">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="94ee0-238">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="94ee0-238">This element is read-only.</span></span> <span data-ttu-id="94ee0-239">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="94ee0-239">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="94ee0-240">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="94ee0-240">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="94ee0-241">Identifica al delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="94ee0-241">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="94ee0-242">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="94ee0-242">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-243">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="94ee0-243">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="94ee0-244">Identifica la entidad de seguridad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="94ee0-244">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="94ee0-245">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="94ee0-245">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-246">UID</span><span class="sxs-lookup"><span data-stu-id="94ee0-246">UID</span></span>](uid.md) <br/> |<span data-ttu-id="94ee0-247">Identifica un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="94ee0-247">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-248">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="94ee0-248">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="94ee0-249">Se usa para identificar una instancia específica de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="94ee0-249">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-250">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="94ee0-250">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="94ee0-251">Indica la fecha y hora en que se ha creado una instancia de un objeto de iCalendar.</span><span class="sxs-lookup"><span data-stu-id="94ee0-251">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="94ee0-252">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="94ee0-252">Parent elements</span></span>

|<span data-ttu-id="94ee0-253">**Element**</span><span class="sxs-lookup"><span data-stu-id="94ee0-253">**Element**</span></span>|<span data-ttu-id="94ee0-254">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94ee0-254">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94ee0-255">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="94ee0-255">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="94ee0-256">Identifica todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="94ee0-256">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-257">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="94ee0-257">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="94ee0-258">Identifica los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="94ee0-258">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="94ee0-259">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="94ee0-259">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="94ee0-260">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="94ee0-260">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-261">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="94ee0-261">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="94ee0-262">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="94ee0-262">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-263">Items</span><span class="sxs-lookup"><span data-stu-id="94ee0-263">Items</span></span>](items.md) <br/> |<span data-ttu-id="94ee0-264">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="94ee0-264">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-265">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="94ee0-265">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="94ee0-266">Contiene una matriz de elementos que desea crear.</span><span class="sxs-lookup"><span data-stu-id="94ee0-266">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-267">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="94ee0-267">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="94ee0-268">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="94ee0-268">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="94ee0-269">SetItemField</span><span class="sxs-lookup"><span data-stu-id="94ee0-269">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="94ee0-270">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="94ee0-270">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="94ee0-271">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="94ee0-271">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="94ee0-272">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="94ee0-272">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="94ee0-273">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="94ee0-273">Text value</span></span>

<span data-ttu-id="94ee0-274">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="94ee0-274">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94ee0-275">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94ee0-275">Remarks</span></span>

<span data-ttu-id="94ee0-276">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="94ee0-276">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94ee0-277">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="94ee0-277">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94ee0-278">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94ee0-278">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="94ee0-279">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="94ee0-279">Schema Name</span></span>  <br/> |<span data-ttu-id="94ee0-280">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="94ee0-280">Types schema</span></span>  <br/> |
|<span data-ttu-id="94ee0-281">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="94ee0-281">Validation File</span></span>  <br/> |<span data-ttu-id="94ee0-282">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="94ee0-282">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="94ee0-283">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="94ee0-283">Can be Empty</span></span>  <br/> |<span data-ttu-id="94ee0-284">False</span><span class="sxs-lookup"><span data-stu-id="94ee0-284">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94ee0-285">Ver también</span><span class="sxs-lookup"><span data-stu-id="94ee0-285">See also</span></span>



- [<span data-ttu-id="94ee0-286">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="94ee0-286">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


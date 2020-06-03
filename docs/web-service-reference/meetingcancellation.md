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
description: El elemento MeetingCancellation representa una cancelación de reunión en el almacén de Exchange.
ms.openlocfilehash: b0fca0a2dcbdf8685f7b9fb2197db1c3123d54b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467532"
---
# <a name="meetingcancellation"></a><span data-ttu-id="f238c-103">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="f238c-103">MeetingCancellation</span></span>

<span data-ttu-id="f238c-104">El elemento **MeetingCancellation** representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f238c-104">The **MeetingCancellation** element represents a meeting cancellation in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="f238c-105">**MeetingCancellationMessageType**</span><span class="sxs-lookup"><span data-stu-id="f238c-105">**MeetingCancellationMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f238c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f238c-106">Attributes and elements</span></span>

<span data-ttu-id="f238c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f238c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f238c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f238c-108">Attributes</span></span>

<span data-ttu-id="f238c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f238c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f238c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f238c-110">Child elements</span></span>

|<span data-ttu-id="f238c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f238c-111">**Element**</span></span>|<span data-ttu-id="f238c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f238c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f238c-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="f238c-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="f238c-114">Contiene la secuencia MIME nativa de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="f238c-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="f238c-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="f238c-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f238c-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f238c-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="f238c-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f238c-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f238c-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="f238c-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f238c-119">Representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="f238c-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="f238c-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f238c-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f238c-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="f238c-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="f238c-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-123">Asunto</span><span class="sxs-lookup"><span data-stu-id="f238c-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f238c-124">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f238c-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="f238c-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f238c-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="f238c-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="f238c-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="f238c-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-128">Body</span><span class="sxs-lookup"><span data-stu-id="f238c-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="f238c-129">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f238c-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="f238c-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="f238c-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f238c-131">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f238c-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f238c-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="f238c-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="f238c-133">Representa la fecha y la hora en que se recibió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f238c-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="f238c-134">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f238c-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="f238c-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="f238c-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f238c-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f238c-137">Categorías</span><span class="sxs-lookup"><span data-stu-id="f238c-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f238c-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="f238c-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="f238c-139">Importance</span><span class="sxs-lookup"><span data-stu-id="f238c-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="f238c-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-141">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="f238c-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="f238c-142">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="f238c-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="f238c-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="f238c-144">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="f238c-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="f238c-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="f238c-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="f238c-146">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="f238c-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="f238c-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="f238c-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="f238c-148">Indica si un usuario envió un elemento a ella o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="f238c-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="f238c-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="f238c-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="f238c-150">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="f238c-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="f238c-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="f238c-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="f238c-152">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="f238c-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="f238c-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="f238c-154">Representa la colección de todos los encabezados de mensajes de Internet que se encuentran dentro de un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f238c-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f238c-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="f238c-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="f238c-156">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f238c-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="f238c-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="f238c-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="f238c-158">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="f238c-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="f238c-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f238c-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f238c-160">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f238c-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f238c-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="f238c-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="f238c-162">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="f238c-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="f238c-163">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="f238c-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f238c-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="f238c-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="f238c-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f238c-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f238c-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="f238c-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="f238c-167">Representa el número de minutos antes de un evento que se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="f238c-167">Represents the number of minutes before an event that a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f238c-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="f238c-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="f238c-169">Representa la cadena para mostrar que se usa para el contenido del cuadro CC.</span><span class="sxs-lookup"><span data-stu-id="f238c-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="f238c-170">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="f238c-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f238c-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="f238c-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="f238c-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="f238c-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="f238c-173">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f238c-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f238c-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="f238c-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="f238c-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible.</span><span class="sxs-lookup"><span data-stu-id="f238c-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="f238c-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f238c-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f238c-177">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="f238c-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="f238c-178">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="f238c-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="f238c-179">Culture</span><span class="sxs-lookup"><span data-stu-id="f238c-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="f238c-180">Representa la referencia cultural de un elemento determinado en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f238c-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f238c-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f238c-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f238c-182">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="f238c-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="f238c-183">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f238c-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f238c-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="f238c-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="f238c-185">Contiene el nombre para mostrar del último usuario que modificó un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="f238c-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="f238c-187">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="f238c-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="f238c-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="f238c-189">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f238c-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="f238c-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f238c-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="f238c-191">Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="f238c-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f238c-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f238c-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="f238c-193">Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="f238c-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f238c-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="f238c-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="f238c-195">Contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="f238c-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="f238c-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="f238c-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="f238c-197">Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="f238c-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="f238c-198">Sender</span><span class="sxs-lookup"><span data-stu-id="f238c-198">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="f238c-199">Identifica al remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-199">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-200">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="f238c-200">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="f238c-201">Contiene un conjunto de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f238c-201">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="f238c-202">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="f238c-202">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="f238c-203">Representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f238c-203">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="f238c-204">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="f238c-204">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="f238c-205">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f238c-205">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="f238c-206">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f238c-206">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="f238c-207">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="f238c-207">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="f238c-208">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f238c-208">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="f238c-209">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="f238c-209">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="f238c-210">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="f238c-210">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="f238c-211">Contiene un identificador binario que representa el subproceso al que pertenece el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f238c-211">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="f238c-212">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="f238c-212">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="f238c-213">Representa el identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="f238c-213">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="f238c-214">From</span><span class="sxs-lookup"><span data-stu-id="f238c-214">From</span></span>](from.md) <br/> |<span data-ttu-id="f238c-215">Representa el destinatario del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f238c-215">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="f238c-216">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="f238c-216">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="f238c-217">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f238c-217">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-218">IsRead</span><span class="sxs-lookup"><span data-stu-id="f238c-218">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="f238c-219">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f238c-219">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="f238c-220">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="f238c-220">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="f238c-221">Indica si se solicita una respuesta a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f238c-221">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="f238c-222">References</span><span class="sxs-lookup"><span data-stu-id="f238c-222">References</span></span>](references.md) <br/> |<span data-ttu-id="f238c-223">Representa el encabezado Usenet que se usa para correlacionar las respuestas con sus mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="f238c-223">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="f238c-224">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="f238c-224">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="f238c-225">Identifica un conjunto de direcciones a las que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="f238c-225">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="f238c-226">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="f238c-226">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="f238c-227">Representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md).</span><span class="sxs-lookup"><span data-stu-id="f238c-227">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="f238c-228">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="f238c-228">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="f238c-229">Indica si una reunión se controló mediante una cuenta con acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="f238c-229">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="f238c-230">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="f238c-230">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="f238c-231">Indica si un mensaje de reunión está desactualizado.</span><span class="sxs-lookup"><span data-stu-id="f238c-231">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="f238c-232">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="f238c-232">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="f238c-233">Indica si se ha procesado un elemento de mensaje de reunión.</span><span class="sxs-lookup"><span data-stu-id="f238c-233">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="f238c-234">ResponseType</span><span class="sxs-lookup"><span data-stu-id="f238c-234">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="f238c-235">Representa el tipo de respuesta de destinatarios que se ha recibido para una reunión.</span><span class="sxs-lookup"><span data-stu-id="f238c-235">Represents the type of recipient response received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="f238c-236">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f238c-236">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f238c-237">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="f238c-237">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="f238c-238">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f238c-238">This element is read-only.</span></span> <span data-ttu-id="f238c-239">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f238c-239">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="f238c-240">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="f238c-240">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="f238c-241">Identifica el delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f238c-241">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="f238c-242">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f238c-242">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f238c-243">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="f238c-243">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="f238c-244">Identifica la entidad de identidad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f238c-244">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="f238c-245">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f238c-245">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f238c-246">EXCLUSIVO</span><span class="sxs-lookup"><span data-stu-id="f238c-246">UID</span></span>](uid.md) <br/> |<span data-ttu-id="f238c-247">Identifica un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="f238c-247">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-248">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f238c-248">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="f238c-249">Se usa para identificar una instancia específica de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="f238c-249">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-250">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="f238c-250">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="f238c-251">Indica la fecha y la hora en que se creó una instancia de un objeto iCalendar.</span><span class="sxs-lookup"><span data-stu-id="f238c-251">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f238c-252">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f238c-252">Parent elements</span></span>

|<span data-ttu-id="f238c-253">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f238c-253">**Element**</span></span>|<span data-ttu-id="f238c-254">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f238c-254">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f238c-255">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f238c-255">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="f238c-256">Identifica todos los elementos del calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="f238c-256">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f238c-257">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="f238c-257">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="f238c-258">Identifica los datos que se van a anexar a una sola propiedad de un elemento durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f238c-258">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f238c-259">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f238c-259">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="f238c-260">Identifica todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="f238c-260">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f238c-261">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f238c-261">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="f238c-262">Identifica un solo elemento que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="f238c-262">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f238c-263">Items</span><span class="sxs-lookup"><span data-stu-id="f238c-263">Items</span></span>](items.md) <br/> |<span data-ttu-id="f238c-264">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="f238c-264">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="f238c-265">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f238c-265">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="f238c-266">Contiene una matriz de elementos que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="f238c-266">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="f238c-267">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="f238c-267">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="f238c-268">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f238c-268">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="f238c-269">SetItemField</span><span class="sxs-lookup"><span data-stu-id="f238c-269">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="f238c-270">Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f238c-270">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f238c-271">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f238c-271">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="f238c-272">Identifica un elemento único para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="f238c-272">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f238c-273">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f238c-273">Text value</span></span>

<span data-ttu-id="f238c-274">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f238c-274">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f238c-275">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f238c-275">Remarks</span></span>

<span data-ttu-id="f238c-276">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f238c-276">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f238c-277">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f238c-277">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f238c-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="f238c-278">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f238c-279">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f238c-279">Schema Name</span></span>  <br/> |<span data-ttu-id="f238c-280">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f238c-280">Types schema</span></span>  <br/> |
|<span data-ttu-id="f238c-281">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f238c-281">Validation File</span></span>  <br/> |<span data-ttu-id="f238c-282">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f238c-282">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f238c-283">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f238c-283">Can be Empty</span></span>  <br/> |<span data-ttu-id="f238c-284">Falso</span><span class="sxs-lookup"><span data-stu-id="f238c-284">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f238c-285">Vea también</span><span class="sxs-lookup"><span data-stu-id="f238c-285">See also</span></span>



- [<span data-ttu-id="f238c-286">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f238c-286">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


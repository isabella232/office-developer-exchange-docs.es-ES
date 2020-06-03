---
title: PostItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostItem
api_type:
- schema
ms.assetid: 7727ed84-9591-4a1c-bb04-12129926499b
description: El elemento PostItem representa un elemento de exposición en el almacén de Exchange.
ms.openlocfilehash: 5fba1a9a6a3abc95ea2ce65cafa2b62bc7423f28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528870"
---
# <a name="postitem"></a><span data-ttu-id="fe6db-103">PostItem</span><span class="sxs-lookup"><span data-stu-id="fe6db-103">PostItem</span></span>

<span data-ttu-id="fe6db-104">El elemento **PostItem** representa un elemento de exposición en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe6db-104">The **PostItem** element represents a post item in the Exchange store.</span></span> 
  
```xml
<PostItem>
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
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <PostedTime/>
   <References/>
   <Sender/>
</PostItem>
```

 <span data-ttu-id="fe6db-105">**PostItemType**</span><span class="sxs-lookup"><span data-stu-id="fe6db-105">**PostItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe6db-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fe6db-106">Attributes and elements</span></span>

<span data-ttu-id="fe6db-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fe6db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe6db-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fe6db-108">Attributes</span></span>

<span data-ttu-id="fe6db-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fe6db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe6db-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fe6db-110">Child elements</span></span>

|<span data-ttu-id="fe6db-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fe6db-111">**Element**</span></span>|<span data-ttu-id="fe6db-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fe6db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe6db-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="fe6db-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="fe6db-114">Contiene la secuencia nativa de extensiones de correo de Internet multipropósito (MIME) de un objeto representado en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="fe6db-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="fe6db-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="fe6db-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe6db-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="fe6db-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe6db-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="fe6db-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="fe6db-119">Representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="fe6db-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="fe6db-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe6db-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="fe6db-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="fe6db-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-123">Asunto</span><span class="sxs-lookup"><span data-stu-id="fe6db-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="fe6db-124">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe6db-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="fe6db-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="fe6db-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="fe6db-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="fe6db-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-128">Body</span><span class="sxs-lookup"><span data-stu-id="fe6db-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="fe6db-129">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fe6db-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="fe6db-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fe6db-131">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe6db-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="fe6db-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="fe6db-133">Representa la fecha y la hora en que se recibió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fe6db-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-134">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fe6db-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="fe6db-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="fe6db-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe6db-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-137">Categorías</span><span class="sxs-lookup"><span data-stu-id="fe6db-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fe6db-138">Representa una colección de cadenas que identifican las categorías a las que pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="fe6db-138">Represents a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-139">Importance</span><span class="sxs-lookup"><span data-stu-id="fe6db-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="fe6db-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-141">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="fe6db-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="fe6db-142">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="fe6db-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="fe6db-144">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="fe6db-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="fe6db-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="fe6db-146">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="fe6db-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="fe6db-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="fe6db-148">Indica si un usuario envió un elemento a ella o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="fe6db-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="fe6db-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="fe6db-150">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="fe6db-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="fe6db-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="fe6db-152">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="fe6db-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="fe6db-154">Representa la colección de todos los encabezados de mensajes de Internet que contiene un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fe6db-154">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="fe6db-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="fe6db-156">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fe6db-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="fe6db-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="fe6db-158">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="fe6db-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="fe6db-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="fe6db-160">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe6db-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="fe6db-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="fe6db-162">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="fe6db-163">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="fe6db-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="fe6db-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="fe6db-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe6db-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="fe6db-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="fe6db-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="fe6db-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="fe6db-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="fe6db-169">Representa la cadena para mostrar que se usa para el contenido del cuadro CC.</span><span class="sxs-lookup"><span data-stu-id="fe6db-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="fe6db-170">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="fe6db-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="fe6db-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="fe6db-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="fe6db-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="fe6db-173">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="fe6db-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="fe6db-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="fe6db-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fe6db-175">Represents a property that is set to **true** if an item has at least one attachment.</span></span> <span data-ttu-id="fe6db-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe6db-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-177">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="fe6db-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="fe6db-178">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="fe6db-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-179">Culture</span><span class="sxs-lookup"><span data-stu-id="fe6db-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="fe6db-180">Representa la referencia cultural de un elemento determinado en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fe6db-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="fe6db-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="fe6db-182">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="fe6db-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="fe6db-183">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe6db-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="fe6db-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="fe6db-185">Contiene el nombre para mostrar del último usuario que modificó un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="fe6db-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="fe6db-187">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="fe6db-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="fe6db-189">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fe6db-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fe6db-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="fe6db-191">Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fe6db-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fe6db-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="fe6db-193">Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fe6db-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="fe6db-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="fe6db-195">Contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="fe6db-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="fe6db-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="fe6db-197">Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="fe6db-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-198">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="fe6db-198">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="fe6db-199">Contiene un identificador binario que representa el subproceso al que pertenece el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fe6db-199">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-200">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="fe6db-200">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="fe6db-201">Representa el identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="fe6db-201">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-202">From</span><span class="sxs-lookup"><span data-stu-id="fe6db-202">From</span></span>](from.md) <br/> |<span data-ttu-id="fe6db-203">Representa la dirección desde la que se envió el elemento de publicación.</span><span class="sxs-lookup"><span data-stu-id="fe6db-203">Represents the address from which the post item was sent.</span></span> <span data-ttu-id="fe6db-204">El elemento **from** solo se puede establecer en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="fe6db-204">The **From** element can only be set at creation time.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-205">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="fe6db-205">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="fe6db-206">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-206">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-207">IsRead</span><span class="sxs-lookup"><span data-stu-id="fe6db-207">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="fe6db-208">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fe6db-208">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-209">PostedTime</span><span class="sxs-lookup"><span data-stu-id="fe6db-209">PostedTime</span></span>](postedtime.md) <br/> |<span data-ttu-id="fe6db-210">Representa la hora en que se contabilizó un [elemento PostItem](postitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fe6db-210">Represents the time that a [PostItem](postitem.md) was posted.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-211">References</span><span class="sxs-lookup"><span data-stu-id="fe6db-211">References</span></span>](references.md) <br/> |<span data-ttu-id="fe6db-212">Representa el encabezado Usenet que se usa para asociar las respuestas con los mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="fe6db-212">Represents the Usenet header that is used to associate replies with the original messages.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-213">Sender</span><span class="sxs-lookup"><span data-stu-id="fe6db-213">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="fe6db-214">Identifica al remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-214">Identifies the sender of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fe6db-215">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fe6db-215">Parent elements</span></span>

|<span data-ttu-id="fe6db-216">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fe6db-216">**Element**</span></span>|<span data-ttu-id="fe6db-217">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fe6db-217">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe6db-218">SetItemField</span><span class="sxs-lookup"><span data-stu-id="fe6db-218">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="fe6db-219">Representa una actualización de una propiedad única de un elemento en una operación UpdateItem.</span><span class="sxs-lookup"><span data-stu-id="fe6db-219">Represents an update to a single property of an item in an UpdateItem operation.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-220">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="fe6db-220">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="fe6db-221">Identifica los datos que se van a anexar a una única propiedad de un elemento o carpeta durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fe6db-221">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fe6db-222">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="fe6db-222">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="fe6db-223">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe6db-223">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-224">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="fe6db-224">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="fe6db-225">Identifica un solo elemento que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="fe6db-225">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-226">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="fe6db-226">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="fe6db-227">Identifica un elemento único para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="fe6db-227">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-228">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="fe6db-228">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="fe6db-229">Se devuelve en respuestas [SyncFolderItems](syncfolderitems.md) cuando se ha leído un elemento.</span><span class="sxs-lookup"><span data-stu-id="fe6db-229">Returned in [SyncFolderItems](syncfolderitems.md) responses when an item has been read.</span></span> <span data-ttu-id="fe6db-230">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe6db-230">This property is read-only.</span></span> <span data-ttu-id="fe6db-231">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="fe6db-231">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-232">Items</span><span class="sxs-lookup"><span data-stu-id="fe6db-232">Items</span></span>](items.md) <br/> |<span data-ttu-id="fe6db-233">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="fe6db-233">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-234">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="fe6db-234">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="fe6db-235">Identifica todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="fe6db-235">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="fe6db-236">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="fe6db-236">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="fe6db-237">Describe todos los elementos de calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="fe6db-237">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe6db-238">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fe6db-238">Text value</span></span>

<span data-ttu-id="fe6db-239">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fe6db-239">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe6db-240">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe6db-240">Remarks</span></span>

<span data-ttu-id="fe6db-241">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe6db-241">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe6db-242">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fe6db-242">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe6db-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe6db-243">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe6db-244">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fe6db-244">Schema Name</span></span>  <br/> |<span data-ttu-id="fe6db-245">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fe6db-245">Types schema</span></span>  <br/> |
|<span data-ttu-id="fe6db-246">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fe6db-246">Validation File</span></span>  <br/> |<span data-ttu-id="fe6db-247">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fe6db-247">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe6db-248">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fe6db-248">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe6db-249">Falso</span><span class="sxs-lookup"><span data-stu-id="fe6db-249">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe6db-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe6db-250">See also</span></span>



- [<span data-ttu-id="fe6db-251">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fe6db-251">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


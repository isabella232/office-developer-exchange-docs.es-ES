---
title: Objeto postItem
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
description: El elemento PostItem representa un elemento para exponer en el almacén de Exchange.
ms.openlocfilehash: 3fb6d6cfe334999c93ca0238547dd5aee8150a5f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836866"
---
# <a name="postitem"></a><span data-ttu-id="f64ae-103">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="f64ae-103">PostItem</span></span>

<span data-ttu-id="f64ae-104">El elemento **PostItem** representa un elemento para exponer en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f64ae-104">The **PostItem** element represents a post item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="f64ae-105">**PostItemType**</span><span class="sxs-lookup"><span data-stu-id="f64ae-105">**PostItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f64ae-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f64ae-106">Attributes and elements</span></span>

<span data-ttu-id="f64ae-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f64ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f64ae-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f64ae-108">Attributes</span></span>

<span data-ttu-id="f64ae-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f64ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f64ae-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f64ae-110">Child elements</span></span>

|<span data-ttu-id="f64ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64ae-111">**Element**</span></span>|<span data-ttu-id="f64ae-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f64ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f64ae-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="f64ae-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="f64ae-114">Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="f64ae-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="f64ae-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f64ae-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f64ae-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="f64ae-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f64ae-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-118">Id</span><span class="sxs-lookup"><span data-stu-id="f64ae-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f64ae-119">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f64ae-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="f64ae-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f64ae-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="f64ae-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="f64ae-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-123">Subject</span><span class="sxs-lookup"><span data-stu-id="f64ae-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f64ae-124">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f64ae-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="f64ae-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f64ae-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-126">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="f64ae-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="f64ae-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-128">Body</span><span class="sxs-lookup"><span data-stu-id="f64ae-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="f64ae-129">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f64ae-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="f64ae-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f64ae-131">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f64ae-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="f64ae-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="f64ae-133">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f64ae-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-134">Size</span><span class="sxs-lookup"><span data-stu-id="f64ae-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="f64ae-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="f64ae-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f64ae-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-137">Categories</span><span class="sxs-lookup"><span data-stu-id="f64ae-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f64ae-138">Representa una colección de cadenas que identifican las categorías a la que pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f64ae-138">Represents a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-139">Importancia</span><span class="sxs-lookup"><span data-stu-id="f64ae-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="f64ae-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="f64ae-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="f64ae-142">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f64ae-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="f64ae-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="f64ae-144">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="f64ae-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="f64ae-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="f64ae-146">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="f64ae-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="f64ae-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="f64ae-148">Indica si un usuario envía un elemento a él o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="f64ae-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="f64ae-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="f64ae-150">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f64ae-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="f64ae-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="f64ae-152">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="f64ae-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="f64ae-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="f64ae-154">Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f64ae-154">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="f64ae-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="f64ae-156">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f64ae-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="f64ae-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="f64ae-158">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f64ae-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f64ae-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f64ae-160">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f64ae-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="f64ae-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="f64ae-162">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="f64ae-163">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="f64ae-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="f64ae-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="f64ae-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f64ae-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="f64ae-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="f64ae-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="f64ae-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="f64ae-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="f64ae-169">Representa la cadena para mostrar que se usa para el contenido del cuadro Cc.</span><span class="sxs-lookup"><span data-stu-id="f64ae-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="f64ae-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="f64ae-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="f64ae-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="f64ae-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="f64ae-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="f64ae-173">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f64ae-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="f64ae-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="f64ae-175">Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="f64ae-175">Represents a property that is set to **true** if an item has at least one attachment.</span></span> <span data-ttu-id="f64ae-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f64ae-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="f64ae-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="f64ae-178">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="f64ae-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-179">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="f64ae-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="f64ae-180">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f64ae-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f64ae-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f64ae-182">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f64ae-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="f64ae-183">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f64ae-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="f64ae-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="f64ae-185">Contiene el nombre para mostrar del último usuario para modificar un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="f64ae-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="f64ae-187">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="f64ae-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="f64ae-189">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f64ae-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f64ae-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="f64ae-191">Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="f64ae-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f64ae-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="f64ae-193">Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="f64ae-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="f64ae-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="f64ae-195">Contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="f64ae-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="f64ae-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="f64ae-197">Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="f64ae-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-198">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="f64ae-198">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="f64ae-199">Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f64ae-199">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-200">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="f64ae-200">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="f64ae-201">Representa el identificador de conversación.</span><span class="sxs-lookup"><span data-stu-id="f64ae-201">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-202">From</span><span class="sxs-lookup"><span data-stu-id="f64ae-202">From</span></span>](from.md) <br/> |<span data-ttu-id="f64ae-203">Representa la dirección desde la que se envió el elemento para exponer.</span><span class="sxs-lookup"><span data-stu-id="f64ae-203">Represents the address from which the post item was sent.</span></span> <span data-ttu-id="f64ae-204">El elemento **de** solo se puede establecer en tiempo de creación.</span><span class="sxs-lookup"><span data-stu-id="f64ae-204">The **From** element can only be set at creation time.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-205">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="f64ae-205">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="f64ae-206">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-206">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-207">Estáleído</span><span class="sxs-lookup"><span data-stu-id="f64ae-207">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="f64ae-208">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f64ae-208">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-209">PostedTime</span><span class="sxs-lookup"><span data-stu-id="f64ae-209">PostedTime</span></span>](postedtime.md) <br/> |<span data-ttu-id="f64ae-210">Representa el tiempo que se ha registrado un [objeto PostItem](postitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f64ae-210">Represents the time that a [PostItem](postitem.md) was posted.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-211">Referencias</span><span class="sxs-lookup"><span data-stu-id="f64ae-211">References</span></span>](references.md) <br/> |<span data-ttu-id="f64ae-212">Representa el encabezado de Usenet que se usa para asociar las respuestas a los mensajes originales.</span><span class="sxs-lookup"><span data-stu-id="f64ae-212">Represents the Usenet header that is used to associate replies with the original messages.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-213">Sender</span><span class="sxs-lookup"><span data-stu-id="f64ae-213">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="f64ae-214">Identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-214">Identifies the sender of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f64ae-215">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f64ae-215">Parent elements</span></span>

|<span data-ttu-id="f64ae-216">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64ae-216">**Element**</span></span>|<span data-ttu-id="f64ae-217">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f64ae-217">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f64ae-218">SetItemField</span><span class="sxs-lookup"><span data-stu-id="f64ae-218">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="f64ae-219">Representa una actualización para una única propiedad de un elemento en una operación UpdateItem.</span><span class="sxs-lookup"><span data-stu-id="f64ae-219">Represents an update to a single property of an item in an UpdateItem operation.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-220">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="f64ae-220">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="f64ae-221">Identifica los datos que se anexará a una propiedad única de una carpeta o elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f64ae-221">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f64ae-222">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="f64ae-222">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="f64ae-223">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f64ae-223">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-224">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f64ae-224">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="f64ae-225">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="f64ae-225">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-226">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f64ae-226">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="f64ae-227">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="f64ae-227">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-228">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="f64ae-228">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="f64ae-229">Devuelto en [SyncFolderItems](syncfolderitems.md) respuestas cuando se leyó un elemento.</span><span class="sxs-lookup"><span data-stu-id="f64ae-229">Returned in [SyncFolderItems](syncfolderitems.md) responses when an item has been read.</span></span> <span data-ttu-id="f64ae-230">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f64ae-230">This property is read-only.</span></span> <span data-ttu-id="f64ae-231">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f64ae-231">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-232">Items</span><span class="sxs-lookup"><span data-stu-id="f64ae-232">Items</span></span>](items.md) <br/> |<span data-ttu-id="f64ae-233">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="f64ae-233">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-234">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f64ae-234">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="f64ae-235">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f64ae-235">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f64ae-236">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f64ae-236">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="f64ae-237">Describe todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="f64ae-237">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f64ae-238">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f64ae-238">Text value</span></span>

<span data-ttu-id="f64ae-239">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f64ae-239">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f64ae-240">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f64ae-240">Remarks</span></span>

<span data-ttu-id="f64ae-241">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f64ae-241">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f64ae-242">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f64ae-242">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f64ae-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f64ae-243">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f64ae-244">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f64ae-244">Schema Name</span></span>  <br/> |<span data-ttu-id="f64ae-245">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f64ae-245">Types schema</span></span>  <br/> |
|<span data-ttu-id="f64ae-246">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f64ae-246">Validation File</span></span>  <br/> |<span data-ttu-id="f64ae-247">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f64ae-247">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f64ae-248">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f64ae-248">Can be Empty</span></span>  <br/> |<span data-ttu-id="f64ae-249">False</span><span class="sxs-lookup"><span data-stu-id="f64ae-249">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f64ae-250">Ver también</span><span class="sxs-lookup"><span data-stu-id="f64ae-250">See also</span></span>



- [<span data-ttu-id="f64ae-251">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f64ae-251">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


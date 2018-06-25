---
title: Elemento
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Item
api_type:
- schema
ms.assetid: 4dfe8f48-e7b4-444d-bdf9-a34e180f598b
description: El elemento representa un elemento genérico en el almacén de Exchange.
ms.openlocfilehash: 7af8e063c3bfd77bd87b80463c11c58d996626b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836143"
---
# <a name="item"></a><span data-ttu-id="d7945-103">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7945-103">Item</span></span>

<span data-ttu-id="d7945-104">**El elemento** representa un elemento genérico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7945-104">The **Item** element represents a generic item in the Exchange store.</span></span> 
  
```xml
<Item>
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
</Item>
```

 <span data-ttu-id="d7945-105">**ItemType**</span><span class="sxs-lookup"><span data-stu-id="d7945-105">**ItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7945-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d7945-106">Attributes and elements</span></span>

<span data-ttu-id="d7945-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d7945-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7945-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7945-108">Attributes</span></span>

<span data-ttu-id="d7945-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7945-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7945-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7945-110">Child elements</span></span>

|<span data-ttu-id="d7945-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7945-111">**Element**</span></span>|<span data-ttu-id="d7945-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7945-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7945-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="d7945-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="d7945-114">Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="d7945-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="d7945-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="d7945-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d7945-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7945-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="d7945-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7945-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d7945-118">Id</span><span class="sxs-lookup"><span data-stu-id="d7945-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="d7945-119">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7945-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="d7945-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7945-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d7945-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="d7945-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="d7945-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7945-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="d7945-123">Subject</span><span class="sxs-lookup"><span data-stu-id="d7945-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="d7945-124">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7945-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="d7945-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d7945-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="d7945-126">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="d7945-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="d7945-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7945-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="d7945-128">Body</span><span class="sxs-lookup"><span data-stu-id="d7945-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="d7945-129">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7945-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="d7945-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="d7945-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d7945-131">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7945-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d7945-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="d7945-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="d7945-133">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7945-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="d7945-134">Size</span><span class="sxs-lookup"><span data-stu-id="d7945-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="d7945-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7945-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="d7945-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7945-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d7945-137">Categories</span><span class="sxs-lookup"><span data-stu-id="d7945-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d7945-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7945-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="d7945-139">Importancia</span><span class="sxs-lookup"><span data-stu-id="d7945-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d7945-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7945-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="d7945-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="d7945-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="d7945-142">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7945-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="d7945-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="d7945-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="d7945-144">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="d7945-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="d7945-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="d7945-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="d7945-146">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="d7945-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="d7945-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="d7945-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="d7945-148">Indica si un usuario envía un elemento a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d7945-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="d7945-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="d7945-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="d7945-150">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d7945-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="d7945-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="d7945-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="d7945-152">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="d7945-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="d7945-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="d7945-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="d7945-154">Representa la colección de todos los encabezados de mensaje de Internet que están dentro de un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7945-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d7945-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="d7945-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="d7945-156">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7945-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="d7945-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="d7945-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="d7945-158">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7945-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="d7945-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d7945-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="d7945-160">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7945-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d7945-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="d7945-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="d7945-162">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="d7945-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="d7945-163">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="d7945-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d7945-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="d7945-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="d7945-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7945-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d7945-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="d7945-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="d7945-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="d7945-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d7945-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="d7945-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="d7945-169">Representa la cadena para mostrar que se usa para el contenido del cuadro Cc.</span><span class="sxs-lookup"><span data-stu-id="d7945-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="d7945-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="d7945-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d7945-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="d7945-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="d7945-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="d7945-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="d7945-173">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d7945-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d7945-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d7945-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d7945-175">Representa una propiedad que se establece en **true** si un elemento tiene datos adjuntos al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="d7945-175">Represents a property that is set to **true** if an item has attachments at least one visible attachment.</span></span> <span data-ttu-id="d7945-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7945-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d7945-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d7945-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="d7945-178">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="d7945-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="d7945-179">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="d7945-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="d7945-180">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7945-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d7945-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="d7945-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="d7945-182">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7945-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="d7945-183">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7945-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d7945-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="d7945-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="d7945-185">Contiene el nombre para mostrar del último usuario para modificar un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7945-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="d7945-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="d7945-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="d7945-187">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7945-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="d7945-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="d7945-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="d7945-189">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7945-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="d7945-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d7945-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="d7945-191">Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="d7945-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d7945-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d7945-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="d7945-193">Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="d7945-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d7945-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="d7945-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="d7945-195">Contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="d7945-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="d7945-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="d7945-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="d7945-197">Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="d7945-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7945-198">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d7945-198">Parent elements</span></span>

|<span data-ttu-id="d7945-199">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7945-199">**Element**</span></span>|<span data-ttu-id="d7945-200">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7945-200">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7945-201">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="d7945-201">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="d7945-202">Describe todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="d7945-202">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d7945-203">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="d7945-203">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="d7945-204">Identifica los datos que se anexará a una propiedad única de una carpeta de elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d7945-204">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d7945-205">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d7945-205">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="d7945-206">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="d7945-206">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d7945-207">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d7945-207">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="d7945-208">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="d7945-208">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d7945-209">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="d7945-209">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="d7945-210">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7945-210">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="d7945-211">Items</span><span class="sxs-lookup"><span data-stu-id="d7945-211">Items</span></span>](items.md) <br/> |<span data-ttu-id="d7945-212">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="d7945-212">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="d7945-213">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d7945-213">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="d7945-214">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="d7945-214">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="d7945-215">SetItemField</span><span class="sxs-lookup"><span data-stu-id="d7945-215">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="d7945-216">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d7945-216">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d7945-217">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d7945-217">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="d7945-218">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="d7945-218">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d7945-219">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d7945-219">Text value</span></span>

<span data-ttu-id="d7945-220">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7945-220">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7945-221">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7945-221">Remarks</span></span>

<span data-ttu-id="d7945-222">Es importante tener en cuenta que **ItemType** es el tipo base para la [tarea](task.md), [CalendarItem](calendaritem.md), [contacto](contact.md), [DistributionList](distributionlist.md)y [mensaje](message-ex15websvcsotherref.md).</span><span class="sxs-lookup"><span data-stu-id="d7945-222">It is important to note that **ItemType** is the base type for [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md), and [Message](message-ex15websvcsotherref.md).</span></span>
  
<span data-ttu-id="d7945-223">Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de Exchange Web Services (EWS).</span><span class="sxs-lookup"><span data-stu-id="d7945-223">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="d7945-224">Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="d7945-224">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="d7945-225">Microsoft Exchange Server 2010 no devuelve **el elemento de base** de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="d7945-225">Microsoft Exchange Server 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="d7945-226">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7945-226">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7945-227">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d7945-227">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7945-228">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d7945-228">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7945-229">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d7945-229">Schema Name</span></span>  <br/> |<span data-ttu-id="d7945-230">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d7945-230">Types schema</span></span>  <br/> |
|<span data-ttu-id="d7945-231">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d7945-231">Validation File</span></span>  <br/> |<span data-ttu-id="d7945-232">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d7945-232">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7945-233">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d7945-233">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7945-234">False</span><span class="sxs-lookup"><span data-stu-id="d7945-234">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7945-235">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7945-235">See also</span></span>



- [<span data-ttu-id="d7945-236">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d7945-236">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="d7945-237">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="d7945-237">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)


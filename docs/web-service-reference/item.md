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
description: El elemento Item representa un elemento genérico del almacén de Exchange.
ms.openlocfilehash: 72d8b1344bea3bcd105a0e293365b17f37193ac3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460319"
---
# <a name="item"></a><span data-ttu-id="53f5f-103">Elemento</span><span class="sxs-lookup"><span data-stu-id="53f5f-103">Item</span></span>

<span data-ttu-id="53f5f-104">El elemento **Item** representa un elemento genérico del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f5f-104">The **Item** element represents a generic item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="53f5f-105">**ItemType**</span><span class="sxs-lookup"><span data-stu-id="53f5f-105">**ItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53f5f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="53f5f-106">Attributes and elements</span></span>

<span data-ttu-id="53f5f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="53f5f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53f5f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="53f5f-108">Attributes</span></span>

<span data-ttu-id="53f5f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="53f5f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53f5f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53f5f-110">Child elements</span></span>

|<span data-ttu-id="53f5f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53f5f-111">**Element**</span></span>|<span data-ttu-id="53f5f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53f5f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53f5f-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="53f5f-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="53f5f-114">Contiene la secuencia nativa de extensiones de correo de Internet multipropósito (MIME) de un objeto representado en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="53f5f-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="53f5f-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="53f5f-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f5f-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="53f5f-117">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="53f5f-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="53f5f-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="53f5f-119">Representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="53f5f-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="53f5f-120">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="53f5f-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="53f5f-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="53f5f-122">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-123">Asunto</span><span class="sxs-lookup"><span data-stu-id="53f5f-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="53f5f-124">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="53f5f-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="53f5f-125">El asunto está limitado a 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="53f5f-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="53f5f-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="53f5f-127">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-128">Body</span><span class="sxs-lookup"><span data-stu-id="53f5f-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="53f5f-129">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="53f5f-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-130">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="53f5f-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="53f5f-131">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f5f-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="53f5f-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="53f5f-133">Representa la fecha y la hora en que se recibió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="53f5f-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-134">Tamaño</span><span class="sxs-lookup"><span data-stu-id="53f5f-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="53f5f-135">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="53f5f-136">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="53f5f-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-137">Categorías</span><span class="sxs-lookup"><span data-stu-id="53f5f-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="53f5f-138">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="53f5f-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-139">Importance</span><span class="sxs-lookup"><span data-stu-id="53f5f-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="53f5f-140">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-141">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="53f5f-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="53f5f-142">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="53f5f-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="53f5f-144">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="53f5f-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="53f5f-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="53f5f-146">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="53f5f-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="53f5f-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="53f5f-148">Indica si un usuario envió un elemento a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="53f5f-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="53f5f-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="53f5f-150">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="53f5f-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="53f5f-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="53f5f-152">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="53f5f-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="53f5f-154">Representa la colección de todos los encabezados de mensajes de Internet que se encuentran dentro de un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="53f5f-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="53f5f-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="53f5f-156">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="53f5f-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="53f5f-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="53f5f-158">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="53f5f-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="53f5f-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="53f5f-160">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f5f-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="53f5f-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="53f5f-162">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="53f5f-163">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="53f5f-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="53f5f-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="53f5f-165">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f5f-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="53f5f-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="53f5f-167">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="53f5f-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="53f5f-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="53f5f-169">Representa la cadena para mostrar que se usa para el contenido del cuadro CC.</span><span class="sxs-lookup"><span data-stu-id="53f5f-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="53f5f-170">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="53f5f-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="53f5f-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="53f5f-172">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="53f5f-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="53f5f-173">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="53f5f-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="53f5f-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="53f5f-175">Representa una propiedad que se establece en **true** si un elemento tiene datos adjuntos al menos un archivo de datos adjuntos visible.</span><span class="sxs-lookup"><span data-stu-id="53f5f-175">Represents a property that is set to **true** if an item has attachments at least one visible attachment.</span></span> <span data-ttu-id="53f5f-176">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="53f5f-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-177">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="53f5f-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="53f5f-178">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="53f5f-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-179">Culture</span><span class="sxs-lookup"><span data-stu-id="53f5f-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="53f5f-180">Representa la referencia cultural de un elemento determinado en un buzón.</span><span class="sxs-lookup"><span data-stu-id="53f5f-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="53f5f-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="53f5f-182">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="53f5f-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="53f5f-183">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="53f5f-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="53f5f-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="53f5f-185">Contiene el nombre para mostrar del último usuario que modificó un elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="53f5f-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="53f5f-187">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="53f5f-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="53f5f-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="53f5f-189">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="53f5f-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="53f5f-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="53f5f-191">Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="53f5f-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="53f5f-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="53f5f-193">Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="53f5f-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="53f5f-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="53f5f-195">Contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="53f5f-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="53f5f-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="53f5f-197">Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="53f5f-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53f5f-198">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="53f5f-198">Parent elements</span></span>

|<span data-ttu-id="53f5f-199">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53f5f-199">**Element**</span></span>|<span data-ttu-id="53f5f-200">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53f5f-200">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53f5f-201">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="53f5f-201">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="53f5f-202">Describe todos los elementos de calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="53f5f-202">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-203">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="53f5f-203">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="53f5f-204">Identifica los datos que se van a anexar a una sola propiedad de un elemento o carpeta durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="53f5f-204">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="53f5f-205">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="53f5f-205">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="53f5f-206">Identifica todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="53f5f-206">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-207">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="53f5f-207">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="53f5f-208">Identifica un solo elemento que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="53f5f-208">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-209">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="53f5f-209">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="53f5f-210">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f5f-210">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-211">Items</span><span class="sxs-lookup"><span data-stu-id="53f5f-211">Items</span></span>](items.md) <br/> |<span data-ttu-id="53f5f-212">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="53f5f-212">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-213">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="53f5f-213">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="53f5f-214">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="53f5f-214">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="53f5f-215">SetItemField</span><span class="sxs-lookup"><span data-stu-id="53f5f-215">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="53f5f-216">Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="53f5f-216">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="53f5f-217">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="53f5f-217">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="53f5f-218">Identifica un elemento único para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="53f5f-218">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="53f5f-219">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="53f5f-219">Text value</span></span>

<span data-ttu-id="53f5f-220">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53f5f-220">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53f5f-221">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53f5f-221">Remarks</span></span>

<span data-ttu-id="53f5f-222">Es importante tener en cuenta que **itemType** es el tipo base para [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md)y [Message](message-ex15websvcsotherref.md).</span><span class="sxs-lookup"><span data-stu-id="53f5f-222">It is important to note that **ItemType** is the base type for [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md), and [Message](message-ex15websvcsotherref.md).</span></span>
  
<span data-ttu-id="53f5f-223">Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no son fuertemente tipados por el esquema de servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="53f5f-223">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="53f5f-224">Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="53f5f-224">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="53f5f-225">Microsoft Exchange Server 2010 no devuelve el elemento de **elemento** base en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="53f5f-225">Microsoft Exchange Server 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="53f5f-226">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="53f5f-226">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53f5f-227">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="53f5f-227">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53f5f-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="53f5f-228">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53f5f-229">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="53f5f-229">Schema Name</span></span>  <br/> |<span data-ttu-id="53f5f-230">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="53f5f-230">Types schema</span></span>  <br/> |
|<span data-ttu-id="53f5f-231">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="53f5f-231">Validation File</span></span>  <br/> |<span data-ttu-id="53f5f-232">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="53f5f-232">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53f5f-233">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="53f5f-233">Can be Empty</span></span>  <br/> |<span data-ttu-id="53f5f-234">Falso</span><span class="sxs-lookup"><span data-stu-id="53f5f-234">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53f5f-235">Vea también</span><span class="sxs-lookup"><span data-stu-id="53f5f-235">See also</span></span>



- [<span data-ttu-id="53f5f-236">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="53f5f-236">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="53f5f-237">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="53f5f-237">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)


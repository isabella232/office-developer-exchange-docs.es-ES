---
title: Contacto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: El elemento Contact representa un elemento de contacto en el almacén de Exchange.
ms.openlocfilehash: b5b4af211815dbbd09449ca2f3c6b6b2dfba6f93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44445653"
---
# <a name="contact"></a><span data-ttu-id="8daf8-103">Contacto</span><span class="sxs-lookup"><span data-stu-id="8daf8-103">Contact</span></span>

<span data-ttu-id="8daf8-104">El elemento **Contact** representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8daf8-104">The **Contact** element represents a contact item in the Exchange store.</span></span> 
  
```XML
<Contact>
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
   <FileAs/>
   <FileAsMapping/>
   <DisplayName/>
   <GivenName/>
   <Initials/>
   <MiddleName/>
   <Nickname/>
   <CompleteName/>
   <CompanyName/>
   <EmailAddresses/>
   <PhysicalAddresses/>
   <PhoneNumbers/>
   <AssistantName/>
   <Birthday/>
   <BusinessHomePage/>
   <Children/>
   <Companies/>
   <ContactSource/>
   <Department/>
   <Generation/>
   <ImAddresses/>
   <JobTitle/>
   <Manager/>
   <Mileage/>
   <OfficeLocation/>
   <PostalAddressIndex/>
   <Profession/>
   <SpouseName/>
   <Surname/>
   <WeddingAnniversary/>
   <HasPicture/>
   <PhoneticFullName/>
   <PhoneticFirstName/>
   <PhoneticLastName/>
   <Alias/>
   <Notes/>
   <Photo/>
   <UserSMIMECertificate/>
   <MSExchangeCertificate/>
   <DirectoryId/>
   <ManagerMailbox/>
   <DirectReports/>
</Contact>
```

 <span data-ttu-id="8daf8-105">**ContactItemType**</span><span class="sxs-lookup"><span data-stu-id="8daf8-105">**ContactItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8daf8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8daf8-106">Attributes and elements</span></span>

<span data-ttu-id="8daf8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8daf8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8daf8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8daf8-108">Attributes</span></span>

<span data-ttu-id="8daf8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8daf8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8daf8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8daf8-110">Child elements</span></span>

|<span data-ttu-id="8daf8-111">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="8daf8-111">**Element name**</span></span>|<span data-ttu-id="8daf8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8daf8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8daf8-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="8daf8-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="8daf8-114">Contiene la secuencia nativa de extensiones de correo de Internet multipropósito (MIME) de un objeto representado en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="8daf8-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="8daf8-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="8daf8-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8daf8-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="8daf8-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="8daf8-118">Representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="8daf8-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="8daf8-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="8daf8-120">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-121">Asunto</span><span class="sxs-lookup"><span data-stu-id="8daf8-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="8daf8-122">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8daf8-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="8daf8-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="8daf8-124">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-124">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-125">Body</span><span class="sxs-lookup"><span data-stu-id="8daf8-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="8daf8-126">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8daf8-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-127">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="8daf8-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8daf8-128">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8daf8-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="8daf8-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="8daf8-130">Representa la fecha y la hora en que se recibió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8daf8-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-131">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8daf8-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="8daf8-132">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-132">Represents the size in bytes of an item.</span></span> <span data-ttu-id="8daf8-133">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8daf8-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-134">Categorías</span><span class="sxs-lookup"><span data-stu-id="8daf8-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8daf8-135">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="8daf8-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-136">Importance</span><span class="sxs-lookup"><span data-stu-id="8daf8-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="8daf8-137">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-138">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="8daf8-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="8daf8-139">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="8daf8-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="8daf8-141">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="8daf8-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="8daf8-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="8daf8-143">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="8daf8-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="8daf8-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="8daf8-145">Indica si un usuario ha enviado un elemento a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="8daf8-145">Indicates whether a user sent an item to himself or herself.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="8daf8-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="8daf8-147">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="8daf8-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="8daf8-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="8daf8-149">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="8daf8-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="8daf8-151">Representa la colección de todos los encabezados de mensajes de Internet que contiene un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8daf8-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="8daf8-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="8daf8-153">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8daf8-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="8daf8-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="8daf8-155">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="8daf8-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="8daf8-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="8daf8-157">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8daf8-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="8daf8-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="8daf8-159">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="8daf8-160">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="8daf8-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="8daf8-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="8daf8-162">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8daf8-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="8daf8-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="8daf8-164">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="8daf8-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="8daf8-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="8daf8-166">Representa la cadena para mostrar que se usa para el contenido de la línea CC.</span><span class="sxs-lookup"><span data-stu-id="8daf8-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="8daf8-167">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="8daf8-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="8daf8-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="8daf8-169">Representa la cadena para mostrar que se usa para el contenido de la línea para.</span><span class="sxs-lookup"><span data-stu-id="8daf8-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="8daf8-170">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="8daf8-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="8daf8-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="8daf8-172">Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible.</span><span class="sxs-lookup"><span data-stu-id="8daf8-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="8daf8-173">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8daf8-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-174">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="8daf8-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="8daf8-175">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="8daf8-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-176">Culture</span><span class="sxs-lookup"><span data-stu-id="8daf8-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="8daf8-177">Representa la referencia cultural de un elemento determinado en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8daf8-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="8daf8-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="8daf8-179">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="8daf8-179">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="8daf8-180">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8daf8-180">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="8daf8-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="8daf8-182">Contiene el nombre para mostrar del último usuario que modificó un elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="8daf8-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="8daf8-184">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="8daf8-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="8daf8-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="8daf8-186">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="8daf8-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="8daf8-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="8daf8-188">Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="8daf8-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="8daf8-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="8daf8-190">Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="8daf8-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="8daf8-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="8daf8-192">Contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="8daf8-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="8daf8-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="8daf8-194">Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="8daf8-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-195">FileAs</span><span class="sxs-lookup"><span data-stu-id="8daf8-195">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="8daf8-196">Representa cómo se archiva un contacto en la carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="8daf8-196">Represents how a contact is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-197">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="8daf8-197">FileAsMapping</span></span>](fileasmapping.md) <br/> |<span data-ttu-id="8daf8-198">Define cómo crear lo que se muestra para un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-198">Defines how to construct what is displayed for a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-199">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="8daf8-199">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="8daf8-200">Define el nombre para mostrar de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-200">Defines the display name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-201">GivenName</span><span class="sxs-lookup"><span data-stu-id="8daf8-201">GivenName</span></span>](givenname.md) <br/> |<span data-ttu-id="8daf8-202">Contiene el nombre especificado de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-202">Contains a contact's given name.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-203">Iniciales</span><span class="sxs-lookup"><span data-stu-id="8daf8-203">Initials</span></span>](initials.md) <br/> |<span data-ttu-id="8daf8-204">Representa las iniciales de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-204">Represents the initials of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-205">MiddleName</span><span class="sxs-lookup"><span data-stu-id="8daf8-205">MiddleName</span></span>](middlename.md) <br/> |<span data-ttu-id="8daf8-206">Representa el segundo nombre de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-206">Represents the middle name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-207">Llamamos</span><span class="sxs-lookup"><span data-stu-id="8daf8-207">Nickname</span></span>](nickname.md) <br/> |<span data-ttu-id="8daf8-208">Representa el alias de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-208">Represents the nickname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-209">CompleteName</span><span class="sxs-lookup"><span data-stu-id="8daf8-209">CompleteName</span></span>](completename.md) <br/> |<span data-ttu-id="8daf8-210">Representa el nombre completo de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-210">Represents the complete name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-211">CompanyName</span><span class="sxs-lookup"><span data-stu-id="8daf8-211">CompanyName</span></span>](companyname.md) <br/> |<span data-ttu-id="8daf8-212">Representa el nombre de la compañía que está asociado a un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-212">Represents the company name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-213">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="8daf8-213">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="8daf8-214">Representa una colección de direcciones de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-214">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-215">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="8daf8-215">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="8daf8-216">Contiene una colección de direcciones físicas que están asociadas a un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-216">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-217">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="8daf8-217">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="8daf8-218">Representa una colección de números de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-218">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-219">AssistantName</span><span class="sxs-lookup"><span data-stu-id="8daf8-219">AssistantName</span></span>](assistantname.md) <br/> |<span data-ttu-id="8daf8-220">Representa un asistente para un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-220">Represents an assistant to a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-221">Cumpleaños</span><span class="sxs-lookup"><span data-stu-id="8daf8-221">Birthday</span></span>](birthday.md) <br/> |<span data-ttu-id="8daf8-222">Representa la fecha de nacimiento de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-222">Represents the birth date of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-223">BusinessHomePage</span><span class="sxs-lookup"><span data-stu-id="8daf8-223">BusinessHomePage</span></span>](businesshomepage.md) <br/> |<span data-ttu-id="8daf8-224">Representa la Página principal (dirección web) del contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-224">Represents the Home page (Web address) for the contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-225">Niños</span><span class="sxs-lookup"><span data-stu-id="8daf8-225">Children</span></span>](children.md) <br/> |<span data-ttu-id="8daf8-226">Contiene los nombres de los elementos secundarios de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-226">Contains the names of a contact's children.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-227">Companies</span><span class="sxs-lookup"><span data-stu-id="8daf8-227">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="8daf8-228">Representa la colección de compañías que están asociadas a un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-228">Represents the collection of companies that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-229">ContactSource</span><span class="sxs-lookup"><span data-stu-id="8daf8-229">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="8daf8-230">Describe si el contacto se encuentra en el almacén de Exchange o en el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8daf8-230">Describes whether the contact is located in the Exchange store or the Active Directory directory service.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-231">Departamento</span><span class="sxs-lookup"><span data-stu-id="8daf8-231">Department</span></span>](department.md) <br/> |<span data-ttu-id="8daf8-232">Representa el Departamento del contacto en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="8daf8-232">Represents the contact's department at work.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-233">Generación</span><span class="sxs-lookup"><span data-stu-id="8daf8-233">Generation</span></span>](generation.md) <br/> |<span data-ttu-id="8daf8-234">Representa una abreviatura generacional que sigue el nombre completo de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-234">Represents a generational abbreviation that follows the full name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-235">Indirecciones</span><span class="sxs-lookup"><span data-stu-id="8daf8-235">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="8daf8-236">Representa una colección de direcciones de mensajería instantánea de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-236">Represents a collection of instant messaging addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-237">JobTitle</span><span class="sxs-lookup"><span data-stu-id="8daf8-237">JobTitle</span></span>](jobtitle.md) <br/> |<span data-ttu-id="8daf8-238">Representa el puesto de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-238">Represents the job title of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-239">Manager</span><span class="sxs-lookup"><span data-stu-id="8daf8-239">Manager</span></span>](manager.md) <br/> |<span data-ttu-id="8daf8-240">Representa el administrador de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-240">Represents a contact's manager.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-241">Mileage</span><span class="sxs-lookup"><span data-stu-id="8daf8-241">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="8daf8-242">Representa el kilometraje de un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-242">Represents mileage for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-243">OfficeLocation</span><span class="sxs-lookup"><span data-stu-id="8daf8-243">OfficeLocation</span></span>](officelocation.md) <br/> |<span data-ttu-id="8daf8-244">Representa la ubicación de la oficina de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-244">Represents the office location of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-245">PostalAddressIndex</span><span class="sxs-lookup"><span data-stu-id="8daf8-245">PostalAddressIndex</span></span>](postaladdressindex.md) <br/> |<span data-ttu-id="8daf8-246">Representa los tipos de presentación de direcciones físicas.</span><span class="sxs-lookup"><span data-stu-id="8daf8-246">Represents the display types for physical addresses.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-247">Profesión</span><span class="sxs-lookup"><span data-stu-id="8daf8-247">Profession</span></span>](profession.md) <br/> |<span data-ttu-id="8daf8-248">Representa la profesión de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-248">Represents the profession of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-249">SpouseName</span><span class="sxs-lookup"><span data-stu-id="8daf8-249">SpouseName</span></span>](spousename.md) <br/> |<span data-ttu-id="8daf8-250">Representa el nombre del cónyuge o pareja de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-250">Represents the name of a contact's spouse/partner.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-251">Apellido</span><span class="sxs-lookup"><span data-stu-id="8daf8-251">Surname</span></span>](surname.md) <br/> |<span data-ttu-id="8daf8-252">Representa el apellido de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-252">Represents the surname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-253">WeddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="8daf8-253">WeddingAnniversary</span></span>](weddinganniversary.md) <br/> |<span data-ttu-id="8daf8-254">Contiene el aniversario de boda de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-254">Contains the wedding anniversary of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-255">HasPicture</span><span class="sxs-lookup"><span data-stu-id="8daf8-255">HasPicture</span></span>](haspicture.md) <br/> |<span data-ttu-id="8daf8-256">Indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-256">Indicates whether the contact item has a file attachment that represents the contact's picture.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-257">PhoneticFullName</span><span class="sxs-lookup"><span data-stu-id="8daf8-257">PhoneticFullName</span></span>](phoneticfullname.md) <br/> |<span data-ttu-id="8daf8-258">Contiene el nombre completo de un contacto, incluidos el nombre y los apellidos, deletreados fonéticamente.</span><span class="sxs-lookup"><span data-stu-id="8daf8-258">Contains the full name of a contact, including the first and last name, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-259">PhoneticFirstName</span><span class="sxs-lookup"><span data-stu-id="8daf8-259">PhoneticFirstName</span></span>](phoneticfirstname.md) <br/> |<span data-ttu-id="8daf8-260">Contiene el nombre de un contacto, escrito en fonética.</span><span class="sxs-lookup"><span data-stu-id="8daf8-260">Contains the first name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-261">PhoneticLastName</span><span class="sxs-lookup"><span data-stu-id="8daf8-261">PhoneticLastName</span></span>](phoneticlastname.md) <br/> |<span data-ttu-id="8daf8-262">Contiene el apellido de un contacto, escrito en fonética.</span><span class="sxs-lookup"><span data-stu-id="8daf8-262">Contains the last name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-263">Alias</span><span class="sxs-lookup"><span data-stu-id="8daf8-263">Alias</span></span>](alias.md) <br/> |<span data-ttu-id="8daf8-264">Contiene el alias de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-264">Contains the email alias of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-265">Notas (contacto)</span><span class="sxs-lookup"><span data-stu-id="8daf8-265">Notes (Contact)</span></span>](notes-contact.md) <br/> |<span data-ttu-id="8daf8-266">Contiene información de contacto adicional.</span><span class="sxs-lookup"><span data-stu-id="8daf8-266">Contains supplementary contact information.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-267">Foto</span><span class="sxs-lookup"><span data-stu-id="8daf8-267">Photo</span></span>](photo.md) <br/> |<span data-ttu-id="8daf8-268">Contiene un valor que codifica la foto de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-268">Contains a value that encodes the photo of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-269">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="8daf8-269">UserSMIMECertificate</span></span>](usersmimecertificate.md) <br/> |<span data-ttu-id="8daf8-270">Contiene un valor que codifica el certificado SMIME de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-270">Contains a value that encodes the SMIME certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-271">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="8daf8-271">MSExchangeCertificate</span></span>](msexchangecertificate.md) <br/> |<span data-ttu-id="8daf8-272">Contiene un valor que codifica el certificado de Microsoft Exchange de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-272">Contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-273">DirectoryId</span><span class="sxs-lookup"><span data-stu-id="8daf8-273">DirectoryId</span></span>](directoryid.md) <br/> |<span data-ttu-id="8daf8-274">Contiene el identificador de directorio de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-274">Contains the directory ID of a contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-275">ManagerMailbox</span><span class="sxs-lookup"><span data-stu-id="8daf8-275">ManagerMailbox</span></span>](managermailbox.md) <br/> |<span data-ttu-id="8daf8-276">Contiene información SMTP que identifica el buzón de administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-276">Contains SMTP information that identifies the manager mailbox of the contact.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-277">DirectReports</span><span class="sxs-lookup"><span data-stu-id="8daf8-277">DirectReports</span></span>](directreports.md) <br/> |<span data-ttu-id="8daf8-278">Contiene información SMTP que identifica los subordinados directos de un contacto.</span><span class="sxs-lookup"><span data-stu-id="8daf8-278">Contains SMTP information that identifies the direct reports of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8daf8-279">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8daf8-279">Parent elements</span></span>

|<span data-ttu-id="8daf8-280">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="8daf8-280">**Element name**</span></span>|<span data-ttu-id="8daf8-281">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8daf8-281">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8daf8-282">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="8daf8-282">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="8daf8-283">Describe todos los elementos de calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="8daf8-283">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-284">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="8daf8-284">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="8daf8-285">Identifica los datos que se van a anexar a una única propiedad de un elemento o carpeta durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="8daf8-285">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="8daf8-286">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="8daf8-286">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="8daf8-287">Identifica todos los elementos que entran en conflicto con una hora de reunión</span><span class="sxs-lookup"><span data-stu-id="8daf8-287">Identifies all items that conflict with a meeting time</span></span>  <br/> |
|[<span data-ttu-id="8daf8-288">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="8daf8-288">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="8daf8-289">Identifica una única carpeta que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="8daf8-289">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-290">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="8daf8-290">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="8daf8-291">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8daf8-291">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-292">Items</span><span class="sxs-lookup"><span data-stu-id="8daf8-292">Items</span></span>](items.md) <br/> |<span data-ttu-id="8daf8-293">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="8daf8-293">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-294">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="8daf8-294">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="8daf8-295">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="8daf8-295">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-296">Resolución</span><span class="sxs-lookup"><span data-stu-id="8daf8-296">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="8daf8-297">Contiene una única entidad resuelta.</span><span class="sxs-lookup"><span data-stu-id="8daf8-297">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="8daf8-298">SetItemField</span><span class="sxs-lookup"><span data-stu-id="8daf8-298">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="8daf8-299">Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="8daf8-299">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="8daf8-300">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="8daf8-300">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="8daf8-301">Identifica un elemento único para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="8daf8-301">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8daf8-302">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8daf8-302">Text value</span></span>

<span data-ttu-id="8daf8-303">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8daf8-303">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8daf8-304">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8daf8-304">Remarks</span></span>

<span data-ttu-id="8daf8-305">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8daf8-305">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8daf8-306">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8daf8-306">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8daf8-307">Namespace</span><span class="sxs-lookup"><span data-stu-id="8daf8-307">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8daf8-308">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8daf8-308">Schema name</span></span>  <br/> |<span data-ttu-id="8daf8-309">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8daf8-309">Types schema</span></span>  <br/> |
|<span data-ttu-id="8daf8-310">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8daf8-310">Validation file</span></span>  <br/> |<span data-ttu-id="8daf8-311">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8daf8-311">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8daf8-312">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8daf8-312">Can be empty</span></span>  <br/> |<span data-ttu-id="8daf8-313">Falso</span><span class="sxs-lookup"><span data-stu-id="8daf8-313">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8daf8-314">Vea también</span><span class="sxs-lookup"><span data-stu-id="8daf8-314">See also</span></span>



- [<span data-ttu-id="8daf8-315">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8daf8-315">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="8daf8-316">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="8daf8-316">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="8daf8-317">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="8daf8-317">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="8daf8-318">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="8daf8-318">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)


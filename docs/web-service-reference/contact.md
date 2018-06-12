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
description: El elemento de contacto representa un elemento de contacto en el almacén de Exchange.
ms.openlocfilehash: 7b2e7c0197914c2a0a0ba3815dd05fca52a5f872
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763789"
---
# <a name="contact"></a><span data-ttu-id="689dc-103">Contacto</span><span class="sxs-lookup"><span data-stu-id="689dc-103">Contact</span></span>

<span data-ttu-id="689dc-104">El elemento **de contacto** representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="689dc-104">The **Contact** element represents a contact item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="689dc-105">**ContactItemType**</span><span class="sxs-lookup"><span data-stu-id="689dc-105">**ContactItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="689dc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="689dc-106">Attributes and elements</span></span>

<span data-ttu-id="689dc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="689dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="689dc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="689dc-108">Attributes</span></span>

<span data-ttu-id="689dc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="689dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="689dc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="689dc-110">Child elements</span></span>

|<span data-ttu-id="689dc-111">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="689dc-111">**Element name**</span></span>|<span data-ttu-id="689dc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="689dc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="689dc-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="689dc-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="689dc-114">Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="689dc-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="689dc-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="689dc-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="689dc-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="689dc-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="689dc-117">Id</span><span class="sxs-lookup"><span data-stu-id="689dc-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="689dc-118">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="689dc-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="689dc-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="689dc-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="689dc-120">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="689dc-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="689dc-121">Subject</span><span class="sxs-lookup"><span data-stu-id="689dc-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="689dc-122">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="689dc-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="689dc-123">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="689dc-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="689dc-124">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="689dc-124">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="689dc-125">Body</span><span class="sxs-lookup"><span data-stu-id="689dc-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="689dc-126">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="689dc-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="689dc-127">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="689dc-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="689dc-128">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="689dc-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="689dc-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="689dc-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="689dc-130">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="689dc-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="689dc-131">Size</span><span class="sxs-lookup"><span data-stu-id="689dc-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="689dc-132">Representa el tamaño en bytes de un elemento.</span><span class="sxs-lookup"><span data-stu-id="689dc-132">Represents the size in bytes of an item.</span></span> <span data-ttu-id="689dc-133">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="689dc-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="689dc-134">Categories</span><span class="sxs-lookup"><span data-stu-id="689dc-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="689dc-135">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="689dc-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="689dc-136">Importancia</span><span class="sxs-lookup"><span data-stu-id="689dc-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="689dc-137">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="689dc-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="689dc-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="689dc-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="689dc-139">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="689dc-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="689dc-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="689dc-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="689dc-141">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="689dc-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="689dc-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="689dc-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="689dc-143">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="689dc-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="689dc-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="689dc-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="689dc-145">Indica si un usuario envía un elemento a sí mismo o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="689dc-145">Indicates whether a user sent an item to himself or herself.</span></span>  <br/> |
|[<span data-ttu-id="689dc-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="689dc-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="689dc-147">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="689dc-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="689dc-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="689dc-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="689dc-149">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="689dc-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="689dc-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="689dc-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="689dc-151">Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="689dc-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="689dc-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="689dc-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="689dc-153">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="689dc-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="689dc-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="689dc-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="689dc-155">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="689dc-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="689dc-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="689dc-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="689dc-157">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="689dc-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="689dc-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="689dc-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="689dc-159">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="689dc-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="689dc-160">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="689dc-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="689dc-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="689dc-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="689dc-162">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="689dc-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="689dc-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="689dc-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="689dc-164">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="689dc-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="689dc-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="689dc-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="689dc-166">Representa la cadena para mostrar que se usa para el contenido de la línea Cc.</span><span class="sxs-lookup"><span data-stu-id="689dc-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="689dc-167">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="689dc-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="689dc-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="689dc-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="689dc-169">Representa la cadena para mostrar que se usa para el contenido de la línea para.</span><span class="sxs-lookup"><span data-stu-id="689dc-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="689dc-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="689dc-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="689dc-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="689dc-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="689dc-172">Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="689dc-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="689dc-173">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="689dc-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="689dc-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="689dc-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="689dc-175">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="689dc-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="689dc-176">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="689dc-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="689dc-177">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="689dc-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="689dc-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="689dc-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="689dc-179">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="689dc-179">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="689dc-180">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="689dc-180">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="689dc-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="689dc-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="689dc-182">Contiene el nombre para mostrar del último usuario para modificar un elemento.</span><span class="sxs-lookup"><span data-stu-id="689dc-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="689dc-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="689dc-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="689dc-184">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="689dc-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="689dc-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="689dc-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="689dc-186">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="689dc-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="689dc-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="689dc-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="689dc-188">Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="689dc-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="689dc-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="689dc-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="689dc-190">Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="689dc-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="689dc-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="689dc-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="689dc-192">Contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="689dc-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="689dc-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="689dc-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="689dc-194">Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="689dc-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="689dc-195">Archivar como</span><span class="sxs-lookup"><span data-stu-id="689dc-195">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="689dc-196">Representa cómo se archiva un contacto en la carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="689dc-196">Represents how a contact is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="689dc-197">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="689dc-197">FileAsMapping</span></span>](fileasmapping.md) <br/> |<span data-ttu-id="689dc-198">Define cómo se construye lo que se muestra para un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-198">Defines how to construct what is displayed for a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-199">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="689dc-199">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="689dc-200">Define el nombre para mostrar de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-200">Defines the display name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-201">GivenName</span><span class="sxs-lookup"><span data-stu-id="689dc-201">GivenName</span></span>](givenname.md) <br/> |<span data-ttu-id="689dc-202">Contiene el nombre de un contacto determinado.</span><span class="sxs-lookup"><span data-stu-id="689dc-202">Contains a contact's given name.</span></span>  <br/> |
|[<span data-ttu-id="689dc-203">Iniciales</span><span class="sxs-lookup"><span data-stu-id="689dc-203">Initials</span></span>](initials.md) <br/> |<span data-ttu-id="689dc-204">Representa las iniciales del contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-204">Represents the initials of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-205">MiddleName</span><span class="sxs-lookup"><span data-stu-id="689dc-205">MiddleName</span></span>](middlename.md) <br/> |<span data-ttu-id="689dc-206">Representa el segundo nombre de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-206">Represents the middle name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-207">Alias</span><span class="sxs-lookup"><span data-stu-id="689dc-207">Nickname</span></span>](nickname.md) <br/> |<span data-ttu-id="689dc-208">Representa el alias de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-208">Represents the nickname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-209">CompleteName</span><span class="sxs-lookup"><span data-stu-id="689dc-209">CompleteName</span></span>](completename.md) <br/> |<span data-ttu-id="689dc-210">Representa el nombre completo de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-210">Represents the complete name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-211">CompanyName</span><span class="sxs-lookup"><span data-stu-id="689dc-211">CompanyName</span></span>](companyname.md) <br/> |<span data-ttu-id="689dc-212">Representa el nombre de la empresa que está asociado con un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-212">Represents the company name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-213">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="689dc-213">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="689dc-214">Representa una colección de direcciones de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-214">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-215">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="689dc-215">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="689dc-216">Contiene una colección de direcciones físicas que están asociados con un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-216">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-217">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="689dc-217">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="689dc-218">Representa una colección de números de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-218">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-219">AssistantName</span><span class="sxs-lookup"><span data-stu-id="689dc-219">AssistantName</span></span>](assistantname.md) <br/> |<span data-ttu-id="689dc-220">Representa a un asistente a un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-220">Represents an assistant to a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-221">Cumpleaños</span><span class="sxs-lookup"><span data-stu-id="689dc-221">Birthday</span></span>](birthday.md) <br/> |<span data-ttu-id="689dc-222">Representa la fecha de nacimiento de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-222">Represents the birth date of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-223">BusinessHomePage</span><span class="sxs-lookup"><span data-stu-id="689dc-223">BusinessHomePage</span></span>](businesshomepage.md) <br/> |<span data-ttu-id="689dc-224">Representa la página principal (dirección Web) para el contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-224">Represents the Home page (Web address) for the contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-225">Niños</span><span class="sxs-lookup"><span data-stu-id="689dc-225">Children</span></span>](children.md) <br/> |<span data-ttu-id="689dc-226">Contiene los nombres de los elementos secundarios de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-226">Contains the names of a contact's children.</span></span>  <br/> |
|[<span data-ttu-id="689dc-227">Empresas</span><span class="sxs-lookup"><span data-stu-id="689dc-227">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="689dc-228">Representa la colección de las empresas que están asociados con un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-228">Represents the collection of companies that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-229">ContactSource</span><span class="sxs-lookup"><span data-stu-id="689dc-229">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="689dc-230">Describe si el contacto se encuentra en el almacén de Exchange o el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="689dc-230">Describes whether the contact is located in the Exchange store or the Active Directory directory service.</span></span>  <br/> |
|[<span data-ttu-id="689dc-231">Departamento</span><span class="sxs-lookup"><span data-stu-id="689dc-231">Department</span></span>](department.md) <br/> |<span data-ttu-id="689dc-232">Representa el departamento del contacto en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="689dc-232">Represents the contact's department at work.</span></span>  <br/> |
|[<span data-ttu-id="689dc-233">Generación</span><span class="sxs-lookup"><span data-stu-id="689dc-233">Generation</span></span>](generation.md) <br/> |<span data-ttu-id="689dc-234">Representa una abreviatura de generaciones que sigue el nombre completo de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-234">Represents a generational abbreviation that follows the full name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-235">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="689dc-235">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="689dc-236">Representa una colección de direcciones de mensajería instantáneas para un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-236">Represents a collection of instant messaging addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-237">JobTitle</span><span class="sxs-lookup"><span data-stu-id="689dc-237">JobTitle</span></span>](jobtitle.md) <br/> |<span data-ttu-id="689dc-238">Representa el título del trabajo de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-238">Represents the job title of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-239">Manager</span><span class="sxs-lookup"><span data-stu-id="689dc-239">Manager</span></span>](manager.md) <br/> |<span data-ttu-id="689dc-240">Representa el Administrador de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-240">Represents a contact's manager.</span></span>  <br/> |
|[<span data-ttu-id="689dc-241">Kilometraje</span><span class="sxs-lookup"><span data-stu-id="689dc-241">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="689dc-242">Representa mileage para un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-242">Represents mileage for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="689dc-243">OfficeLocation</span><span class="sxs-lookup"><span data-stu-id="689dc-243">OfficeLocation</span></span>](officelocation.md) <br/> |<span data-ttu-id="689dc-244">Representa la ubicación de la oficina de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-244">Represents the office location of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-245">PostalAddressIndex</span><span class="sxs-lookup"><span data-stu-id="689dc-245">PostalAddressIndex</span></span>](postaladdressindex.md) <br/> |<span data-ttu-id="689dc-246">Representa los tipos de presentación para direcciones físicas.</span><span class="sxs-lookup"><span data-stu-id="689dc-246">Represents the display types for physical addresses.</span></span>  <br/> |
|[<span data-ttu-id="689dc-247">Profession</span><span class="sxs-lookup"><span data-stu-id="689dc-247">Profession</span></span>](profession.md) <br/> |<span data-ttu-id="689dc-248">Representa el ámbito de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-248">Represents the profession of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-249">NombreCónyuge</span><span class="sxs-lookup"><span data-stu-id="689dc-249">SpouseName</span></span>](spousename.md) <br/> |<span data-ttu-id="689dc-250">Representa el nombre del cónyuge o pareja de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-250">Represents the name of a contact's spouse/partner.</span></span>  <br/> |
|[<span data-ttu-id="689dc-251">Apellido</span><span class="sxs-lookup"><span data-stu-id="689dc-251">Surname</span></span>](surname.md) <br/> |<span data-ttu-id="689dc-252">Representa el apellido de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-252">Represents the surname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-253">WeddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="689dc-253">WeddingAnniversary</span></span>](weddinganniversary.md) <br/> |<span data-ttu-id="689dc-254">Contiene el aniversario despedida de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-254">Contains the wedding anniversary of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-255">HasPicture</span><span class="sxs-lookup"><span data-stu-id="689dc-255">HasPicture</span></span>](haspicture.md) <br/> |<span data-ttu-id="689dc-256">Indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-256">Indicates whether the contact item has a file attachment that represents the contact's picture.</span></span>  <br/> |
|[<span data-ttu-id="689dc-257">PhoneticFullName</span><span class="sxs-lookup"><span data-stu-id="689dc-257">PhoneticFullName</span></span>](phoneticfullname.md) <br/> |<span data-ttu-id="689dc-258">Contiene el nombre completo de un contacto, incluido el nombre y el apellido, escrito fonéticamente.</span><span class="sxs-lookup"><span data-stu-id="689dc-258">Contains the full name of a contact, including the first and last name, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="689dc-259">PhoneticFirstName</span><span class="sxs-lookup"><span data-stu-id="689dc-259">PhoneticFirstName</span></span>](phoneticfirstname.md) <br/> |<span data-ttu-id="689dc-260">Contiene el nombre de un contacto, escrito fonéticamente.</span><span class="sxs-lookup"><span data-stu-id="689dc-260">Contains the first name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="689dc-261">PhoneticLastName</span><span class="sxs-lookup"><span data-stu-id="689dc-261">PhoneticLastName</span></span>](phoneticlastname.md) <br/> |<span data-ttu-id="689dc-262">Contiene el último nombre de un contacto, escrito fonéticamente.</span><span class="sxs-lookup"><span data-stu-id="689dc-262">Contains the last name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="689dc-263">Alias</span><span class="sxs-lookup"><span data-stu-id="689dc-263">Alias</span></span>](alias.md) <br/> |<span data-ttu-id="689dc-264">Contiene el alias de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-264">Contains the email alias of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-265">Notas (contacto)</span><span class="sxs-lookup"><span data-stu-id="689dc-265">Notes (Contact)</span></span>](notes-contact.md) <br/> |<span data-ttu-id="689dc-266">Contiene información de contacto adicional.</span><span class="sxs-lookup"><span data-stu-id="689dc-266">Contains supplementary contact information.</span></span>  <br/> |
|[<span data-ttu-id="689dc-267">Photo</span><span class="sxs-lookup"><span data-stu-id="689dc-267">Photo</span></span>](photo.md) <br/> |<span data-ttu-id="689dc-268">Contiene un valor que se codifica la foto de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-268">Contains a value that encodes the photo of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-269">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="689dc-269">UserSMIMECertificate</span></span>](usersmimecertificate.md) <br/> |<span data-ttu-id="689dc-270">Contiene un valor que se codifica el certificado SMIME de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-270">Contains a value that encodes the SMIME certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-271">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="689dc-271">MSExchangeCertificate</span></span>](msexchangecertificate.md) <br/> |<span data-ttu-id="689dc-272">Contiene un valor que se codifica el certificado de Microsoft Exchange de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-272">Contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-273">DirectoryId</span><span class="sxs-lookup"><span data-stu-id="689dc-273">DirectoryId</span></span>](directoryid.md) <br/> |<span data-ttu-id="689dc-274">Contiene el identificador de directorio de un contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-274">Contains the directory ID of a contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-275">ManagerMailbox</span><span class="sxs-lookup"><span data-stu-id="689dc-275">ManagerMailbox</span></span>](managermailbox.md) <br/> |<span data-ttu-id="689dc-276">Contiene información de SMTP que identifica el buzón de correo del administrador del contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-276">Contains SMTP information that identifies the manager mailbox of the contact.</span></span>  <br/> |
|[<span data-ttu-id="689dc-277">DirectReports</span><span class="sxs-lookup"><span data-stu-id="689dc-277">DirectReports</span></span>](directreports.md) <br/> |<span data-ttu-id="689dc-278">Contiene información de SMTP que identifica los informes directos del contacto.</span><span class="sxs-lookup"><span data-stu-id="689dc-278">Contains SMTP information that identifies the direct reports of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="689dc-279">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="689dc-279">Parent elements</span></span>

|<span data-ttu-id="689dc-280">**Nombre del elemento**</span><span class="sxs-lookup"><span data-stu-id="689dc-280">**Element name**</span></span>|<span data-ttu-id="689dc-281">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="689dc-281">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="689dc-282">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="689dc-282">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="689dc-283">Describe todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="689dc-283">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="689dc-284">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="689dc-284">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="689dc-285">Identifica los datos que se anexará a una propiedad única de una carpeta o elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="689dc-285">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="689dc-286">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="689dc-286">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="689dc-287">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión</span><span class="sxs-lookup"><span data-stu-id="689dc-287">Identifies all items that conflict with a meeting time</span></span>  <br/> |
|[<span data-ttu-id="689dc-288">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="689dc-288">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="689dc-289">Identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="689dc-289">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="689dc-290">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="689dc-290">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="689dc-291">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="689dc-291">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="689dc-292">Items</span><span class="sxs-lookup"><span data-stu-id="689dc-292">Items</span></span>](items.md) <br/> |<span data-ttu-id="689dc-293">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="689dc-293">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="689dc-294">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="689dc-294">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="689dc-295">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="689dc-295">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="689dc-296">Resoluci?n</span><span class="sxs-lookup"><span data-stu-id="689dc-296">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="689dc-297">Contiene una única entidad resuelta.</span><span class="sxs-lookup"><span data-stu-id="689dc-297">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="689dc-298">SetItemField</span><span class="sxs-lookup"><span data-stu-id="689dc-298">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="689dc-299">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="689dc-299">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="689dc-300">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="689dc-300">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="689dc-301">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="689dc-301">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="689dc-302">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="689dc-302">Text value</span></span>

<span data-ttu-id="689dc-303">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="689dc-303">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="689dc-304">Observaciones</span><span class="sxs-lookup"><span data-stu-id="689dc-304">Remarks</span></span>

<span data-ttu-id="689dc-305">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="689dc-305">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="689dc-306">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="689dc-306">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="689dc-307">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="689dc-307">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="689dc-308">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="689dc-308">Schema name</span></span>  <br/> |<span data-ttu-id="689dc-309">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="689dc-309">Types schema</span></span>  <br/> |
|<span data-ttu-id="689dc-310">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="689dc-310">Validation file</span></span>  <br/> |<span data-ttu-id="689dc-311">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="689dc-311">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="689dc-312">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="689dc-312">Can be empty</span></span>  <br/> |<span data-ttu-id="689dc-313">False</span><span class="sxs-lookup"><span data-stu-id="689dc-313">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="689dc-314">Ver también</span><span class="sxs-lookup"><span data-stu-id="689dc-314">See also</span></span>



- [<span data-ttu-id="689dc-315">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="689dc-315">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="689dc-316">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="689dc-316">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="689dc-317">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="689dc-317">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="689dc-318">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="689dc-318">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)


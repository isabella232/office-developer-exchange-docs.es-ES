---
title: DistributionList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistributionList
api_type:
- schema
ms.assetid: f65aea01-e870-44a2-8571-fa6c001341cc
description: El elemento DistributionList representa una lista de distribución.
ms.openlocfilehash: 5eb97bef349ca02848f65fa58370b9c81c6653d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457007"
---
# <a name="distributionlist"></a><span data-ttu-id="ed46a-103">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ed46a-103">DistributionList</span></span>

<span data-ttu-id="ed46a-104">El elemento **DistributionList** representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-104">The **DistributionList** element represents a distribution list.</span></span> 
  
```xml
<DistributionList>
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
   <DisplayName/>
   <FileAs/>
   <ContactSource/>
   <Members/>
</DistributionList>
```

 <span data-ttu-id="ed46a-105">**DistributionListType**</span><span class="sxs-lookup"><span data-stu-id="ed46a-105">**DistributionListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed46a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ed46a-106">Attributes and elements</span></span>

<span data-ttu-id="ed46a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ed46a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed46a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed46a-108">Attributes</span></span>

<span data-ttu-id="ed46a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ed46a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed46a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed46a-110">Child elements</span></span>

|<span data-ttu-id="ed46a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ed46a-111">**Element**</span></span>|<span data-ttu-id="ed46a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed46a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed46a-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="ed46a-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="ed46a-114">Contiene la secuencia MIME nativa de un objeto representado en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="ed46a-114">Contains the native MIME stream of an object represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="ed46a-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ed46a-116">Contiene el identificador único y la clave de cambio de un elemento de lista de distribución en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed46a-116">Contains the unique identifier and change key of a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="ed46a-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="ed46a-118">Representa el identificador de la carpeta principal que contiene el elemento de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-118">Represents the identifier of the parent folder that contains the distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="ed46a-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="ed46a-120">Representa la clase de mensaje de un elemento de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-120">Represents the message class of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-121">Asunto</span><span class="sxs-lookup"><span data-stu-id="ed46a-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="ed46a-122">Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed46a-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="ed46a-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="ed46a-124">Contiene el estado de la sensibilidad de un elemento de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-124">Contains the status for a distribution list item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-125">Body</span><span class="sxs-lookup"><span data-stu-id="ed46a-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="ed46a-126">Representa el contenido del cuerpo real de un elemento de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-126">Represents the actual body content of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-127">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="ed46a-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ed46a-128">Contiene los elementos o archivos adjuntos a un elemento de lista de distribución en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed46a-128">Contains the items or files that are attached to a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="ed46a-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="ed46a-130">Representa la fecha y la hora en que se recibió un elemento de lista de distribución en un buzón.</span><span class="sxs-lookup"><span data-stu-id="ed46a-130">Represents the date and time that a distribution list item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-131">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ed46a-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="ed46a-132">Representa el tamaño, en bytes, de un elemento de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-132">Represents the size, in bytes, of a distribution list item.</span></span> <span data-ttu-id="ed46a-133">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed46a-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-134">Categorías</span><span class="sxs-lookup"><span data-stu-id="ed46a-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ed46a-135">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento de lista de distribución en el buzón.</span><span class="sxs-lookup"><span data-stu-id="ed46a-135">Represents a collection of strings that identify to which categories a distribution list item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-136">Importance</span><span class="sxs-lookup"><span data-stu-id="ed46a-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="ed46a-137">Describe la importancia de un elemento de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-137">Describes the importance of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-138">Inreplyto</span><span class="sxs-lookup"><span data-stu-id="ed46a-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="ed46a-139">Representa el identificador del elemento al que se reenviará este elemento.</span><span class="sxs-lookup"><span data-stu-id="ed46a-139">Represents the identifier of the item which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="ed46a-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="ed46a-141">Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="ed46a-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="ed46a-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="ed46a-143">Representa si un elemento todavía no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="ed46a-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="ed46a-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="ed46a-145">Indica si un usuario envió un elemento a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="ed46a-145">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="ed46a-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="ed46a-147">Indica si el elemento se ha enviado previamente.</span><span class="sxs-lookup"><span data-stu-id="ed46a-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="ed46a-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="ed46a-149">Indica si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="ed46a-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="ed46a-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="ed46a-151">Representa la colección de todos los encabezados de mensajes de Internet contenidos en un elemento de un buzón.</span><span class="sxs-lookup"><span data-stu-id="ed46a-151">Represents the collection of all Internet message headers contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="ed46a-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="ed46a-153">Representa la fecha y la hora en que se envió un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="ed46a-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="ed46a-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="ed46a-155">Representa la fecha y la hora en que se creó un elemento determinado en el buzón.</span><span class="sxs-lookup"><span data-stu-id="ed46a-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="ed46a-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="ed46a-157">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed46a-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="ed46a-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="ed46a-159">Representa la fecha y la hora en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="ed46a-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="ed46a-160">El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="ed46a-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="ed46a-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="ed46a-162">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed46a-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="ed46a-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="ed46a-164">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="ed46a-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="ed46a-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="ed46a-166">Representa la cadena para mostrar que se usa para el contenido de la línea CC.</span><span class="sxs-lookup"><span data-stu-id="ed46a-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="ed46a-167">Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.</span><span class="sxs-lookup"><span data-stu-id="ed46a-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="ed46a-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="ed46a-169">Representa la cadena para mostrar que se usa para el contenido de la línea para.</span><span class="sxs-lookup"><span data-stu-id="ed46a-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="ed46a-170">Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="ed46a-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="ed46a-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="ed46a-172">Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible.</span><span class="sxs-lookup"><span data-stu-id="ed46a-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="ed46a-173">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed46a-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-174">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="ed46a-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="ed46a-175">Identifica las propiedades extendidas de un elemento de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-175">Identifies extended properties on a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-176">Culture</span><span class="sxs-lookup"><span data-stu-id="ed46a-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="ed46a-177">Representa la referencia cultural de un elemento de lista de distribución en un buzón.</span><span class="sxs-lookup"><span data-stu-id="ed46a-177">Represents the culture for a distribution list item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="ed46a-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="ed46a-179">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="ed46a-179">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="ed46a-180">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed46a-180">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="ed46a-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="ed46a-182">Contiene el nombre para mostrar del último usuario que modificó un elemento.</span><span class="sxs-lookup"><span data-stu-id="ed46a-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="ed46a-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="ed46a-184">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="ed46a-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="ed46a-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="ed46a-186">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ed46a-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="ed46a-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="ed46a-188">Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="ed46a-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="ed46a-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="ed46a-190">Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="ed46a-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="ed46a-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="ed46a-192">Contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="ed46a-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="ed46a-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="ed46a-194">Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="ed46a-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-195">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="ed46a-195">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="ed46a-196">Define el nombre para mostrar de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-196">Defines the display name of a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-197">FileAs</span><span class="sxs-lookup"><span data-stu-id="ed46a-197">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="ed46a-198">Representa cómo se archiva una lista de distribución en la carpeta contactos.</span><span class="sxs-lookup"><span data-stu-id="ed46a-198">Represents how a distribution list is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-199">ContactSource</span><span class="sxs-lookup"><span data-stu-id="ed46a-199">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="ed46a-200">Describe si el contacto se encuentra en el almacén de Exchange o en los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="ed46a-200">Describes whether the contact is located in the Exchange store or in Active Directory Domain Services (AD DS).</span></span>  <br/> |
|[<span data-ttu-id="ed46a-201">Miembros (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="ed46a-201">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="ed46a-202">Contiene una lista de miembros de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ed46a-202">Contains a list of members of the distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed46a-203">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ed46a-203">Parent elements</span></span>

|<span data-ttu-id="ed46a-204">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ed46a-204">**Element**</span></span>|<span data-ttu-id="ed46a-205">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed46a-205">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed46a-206">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="ed46a-206">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="ed46a-207">Describe todos los elementos de calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="ed46a-207">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-208">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="ed46a-208">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="ed46a-209">Identifica los datos que se van a anexar a una sola propiedad de una lista de distribución durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ed46a-209">Identifies data to append to a single property of a distribution list during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="ed46a-210">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="ed46a-210">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="ed46a-211">Identifica todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="ed46a-211">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-212">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="ed46a-212">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="ed46a-213">Identifica una lista de distribución única para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="ed46a-213">Identifies a single distribution list to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-214">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="ed46a-214">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="ed46a-215">Identifica una lista de distribución única para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="ed46a-215">Identifies a single distribution list to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-216">Items</span><span class="sxs-lookup"><span data-stu-id="ed46a-216">Items</span></span>](items.md) <br/> |<span data-ttu-id="ed46a-217">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="ed46a-217">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-218">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="ed46a-218">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="ed46a-219">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="ed46a-219">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="ed46a-220">SetItemField</span><span class="sxs-lookup"><span data-stu-id="ed46a-220">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="ed46a-221">Representa una actualización de una propiedad única de un elemento de lista de distribución en una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ed46a-221">Represents an update to a single property of a distribution list item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed46a-222">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ed46a-222">Text value</span></span>

<span data-ttu-id="ed46a-223">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed46a-223">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed46a-224">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed46a-224">Remarks</span></span>

<span data-ttu-id="ed46a-225">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed46a-225">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed46a-226">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ed46a-226">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed46a-227">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed46a-227">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ed46a-228">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ed46a-228">Schema Name</span></span>  <br/> |<span data-ttu-id="ed46a-229">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ed46a-229">Types schema</span></span>  <br/> |
|<span data-ttu-id="ed46a-230">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ed46a-230">Validation File</span></span>  <br/> |<span data-ttu-id="ed46a-231">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ed46a-231">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ed46a-232">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ed46a-232">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed46a-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ed46a-233">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed46a-234">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed46a-234">See also</span></span>

- [<span data-ttu-id="ed46a-235">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ed46a-235">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


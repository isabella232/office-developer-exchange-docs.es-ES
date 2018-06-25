---
title: Buz?n de correo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: El elemento de buzón de correo identifica un objeto de Active Directory habilitados para correo.
ms.openlocfilehash: e9fa21f3678249a9ac13d567b88beaf0177f989f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836258"
---
# <a name="mailbox"></a><span data-ttu-id="a9a67-103">Buz?n de correo</span><span class="sxs-lookup"><span data-stu-id="a9a67-103">Mailbox</span></span>

<span data-ttu-id="a9a67-104">El elemento de **buzón de correo** identifica un objeto de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-104">The **Mailbox** element identifies a mail-enabled Active Directory object.</span></span> 
  
```XML
<Mailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Mailbox>
```

<span data-ttu-id="a9a67-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="a9a67-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a9a67-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9a67-106">Attributes and elements</span></span>

<span data-ttu-id="a9a67-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9a67-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9a67-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9a67-108">Attributes</span></span>

<span data-ttu-id="a9a67-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9a67-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9a67-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9a67-110">Child elements</span></span>

|<span data-ttu-id="a9a67-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9a67-111">**Element**</span></span>|<span data-ttu-id="a9a67-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9a67-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9a67-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="a9a67-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="a9a67-114">Define el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-114">Defines the name of the mailbox user.</span></span> <span data-ttu-id="a9a67-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a9a67-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="a9a67-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="a9a67-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="a9a67-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a9a67-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="a9a67-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="a9a67-120">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="a9a67-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="a9a67-121">The default is SMTP.</span></span> <span data-ttu-id="a9a67-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a9a67-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="a9a67-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="a9a67-124">Define el tipo de buzón de correo de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-124">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="a9a67-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a9a67-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="a9a67-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a9a67-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a9a67-127">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder.</span></span> <span data-ttu-id="a9a67-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a9a67-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9a67-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9a67-129">Parent elements</span></span>

|<span data-ttu-id="a9a67-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9a67-130">**Element**</span></span>|<span data-ttu-id="a9a67-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9a67-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9a67-132">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="a9a67-132">ExpandDL</span></span>](expanddl.md) <br/> |<span data-ttu-id="a9a67-133">Define una solicitud para expandir una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="a9a67-133">Defines a request to expand a distribution list.</span></span> <br/> <br/> <span data-ttu-id="a9a67-134">La siguiente es la expresión de XPath para este elemento:` /ExpandDL `</span><span class="sxs-lookup"><span data-stu-id="a9a67-134">The following is the XPath expression to this element: ` /ExpandDL `</span></span> <br/> |
|[<span data-ttu-id="a9a67-135">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="a9a67-135">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="a9a67-136">Contiene una matriz de destinatarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a9a67-136">Contains an array of recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-137">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="a9a67-137">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="a9a67-138">Representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a9a67-138">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-139">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="a9a67-139">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="a9a67-140">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a9a67-140">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-141">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="a9a67-141">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="a9a67-142">Identifica una matriz de direcciones de correo electrónico a la que se deben enviar las respuestas.</span><span class="sxs-lookup"><span data-stu-id="a9a67-142">Identifies an array of e-mail addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-143">Sender</span><span class="sxs-lookup"><span data-stu-id="a9a67-143">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="a9a67-144">Identifica el remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a9a67-144">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-145">From</span><span class="sxs-lookup"><span data-stu-id="a9a67-145">From</span></span>](from.md) <br/> |<span data-ttu-id="a9a67-146">Representa al destinatario de la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a9a67-146">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-147">Organizer</span><span class="sxs-lookup"><span data-stu-id="a9a67-147">Organizer</span></span>](organizer.md) <br/> |<span data-ttu-id="a9a67-148">Representa el organizador de una reunión.</span><span class="sxs-lookup"><span data-stu-id="a9a67-148">Represents the organizer of a meeting.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-149">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a9a67-149">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> | <span data-ttu-id="a9a67-150">Identifica las carpetas predeterminadas de Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="a9a67-150">Identifies default Microsoft Exchange Server 2007 folders.</span></span>  <br/><br/>  <span data-ttu-id="a9a67-151">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a9a67-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[<span data-ttu-id="a9a67-152">Resoluci?n</span><span class="sxs-lookup"><span data-stu-id="a9a67-152">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="a9a67-153">Contiene una única entidad resuelta.</span><span class="sxs-lookup"><span data-stu-id="a9a67-153">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-154">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="a9a67-154">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="a9a67-155">Contiene una matriz de los buzones de correo que están contenidos en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="a9a67-155">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-156">Attendee</span><span class="sxs-lookup"><span data-stu-id="a9a67-156">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="a9a67-157">Representa los asistentes y los recursos para un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="a9a67-157">Represents attendees and resources for a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-158">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="a9a67-158">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="a9a67-159">Define una solicitud para agregar las carpetas administradas a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-159">Defines a request to add managed folders to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-160">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="a9a67-160">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="a9a67-161">Define una solicitud para agregar delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-161">Defines a request to add delegates to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-162">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="a9a67-162">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="a9a67-163">Define una solicitud para obtener información acerca de los delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-163">Defines a request to get information about delegates to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-164">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="a9a67-164">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="a9a67-165">Define una solicitud para quitar delegados de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-165">Defines a request to remove delegates from a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-166">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="a9a67-166">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="a9a67-167">Define una solicitud para actualizar los delegados en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a9a67-167">Defines a request to update delegates in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-168">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="a9a67-168">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="a9a67-169">Describe al delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="a9a67-169">Describes the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-170">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="a9a67-170">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="a9a67-171">Describe la entidad de seguridad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="a9a67-171">Describes the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="a9a67-172">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9a67-172">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a9a67-173">Representa a un miembro de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="a9a67-173">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9a67-174">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a9a67-174">Text value</span></span>

<span data-ttu-id="a9a67-175">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9a67-175">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9a67-176">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9a67-176">Remarks</span></span>

<span data-ttu-id="a9a67-177">Los elementos [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) y [ItemId](itemid.md) identifican una buzón de correo o lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="a9a67-177">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) and [ItemId](itemid.md) elements identify a mailbox or distribution list.</span></span> 

<span data-ttu-id="a9a67-178">El elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) identifica una buzón de correo o lista de distribución mediante la dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="a9a67-178">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element identifies a mailbox or distribution list by SMTP address.</span></span> 

<span data-ttu-id="a9a67-179">El elemento [ItemId](itemid.md) identifica un buzón de correo mediante un identificador de elemento, que está asociado a un buzón determinado.</span><span class="sxs-lookup"><span data-stu-id="a9a67-179">The [ItemId](itemid.md) element identifies a mailbox by an item identifier, which is associated with a particular mailbox.</span></span> 

<span data-ttu-id="a9a67-180">El elemento de [ItemId](itemid.md) no puede usarse para enviar un mensaje a una lista de distribución o un contacto en una carpeta pública de contactos.</span><span class="sxs-lookup"><span data-stu-id="a9a67-180">The [ItemId](itemid.md) element cannot be used for sending a message to a distribution list or a contact in a public contacts folder.</span></span> <span data-ttu-id="a9a67-181">Se producirá un error si se utiliza en una operación CreateItem, UpdateItem o SendItem cuando se realiza un intento para enviar un mensaje a una lista de distribución o un contacto en una carpeta pública de contactos.</span><span class="sxs-lookup"><span data-stu-id="a9a67-181">An error will be thrown if this is used in a CreateItem, UpdateItem, or SendItem operation when an attempt is made to send a message to a distribution list or contact in a contacts public folder.</span></span> <span data-ttu-id="a9a67-182">Use la operación de ExpandDL para obtener la dirección SMTP y, a continuación, envíe el mensaje mediante el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en lugar del elemento [ItemId](itemid.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a67-182">Use the ExpandDL operation to get the SMTP address and then send the message by using the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element instead of the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="a9a67-183">Otro elemento, [buzón de correo (disponibilidad)](mailbox-availability.md), proporciona información para las operaciones de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="a9a67-183">Another element, [Mailbox (Availability)](mailbox-availability.md), provides information for availability operations.</span></span> 
  
<span data-ttu-id="a9a67-184">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9a67-184">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9a67-185">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9a67-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9a67-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9a67-186">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9a67-187">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9a67-187">Schema Name</span></span>  <br/> |<span data-ttu-id="a9a67-188">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a9a67-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9a67-189">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9a67-189">Validation File</span></span>  <br/> |<span data-ttu-id="a9a67-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9a67-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9a67-191">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9a67-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9a67-192">False</span><span class="sxs-lookup"><span data-stu-id="a9a67-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9a67-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9a67-193">See also</span></span>

- [<span data-ttu-id="a9a67-194">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a9a67-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


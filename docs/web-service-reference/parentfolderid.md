---
title: ParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 258f4b1f-367e-4c7d-9c29-eb775a2398c7
description: El elemento ParentFolderId representa el identificador de la carpeta principal que contiene el elemento o carpeta.
ms.openlocfilehash: 3bad638aa21019472df8f487f1e065d2e725e750
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465754"
---
# <a name="parentfolderid"></a><span data-ttu-id="01e92-103">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="01e92-103">ParentFolderId</span></span>

<span data-ttu-id="01e92-104">El elemento **ParentFolderId** representa el identificador de la carpeta principal que contiene el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="01e92-104">The **ParentFolderId** element represents the identifier of the parent folder that contains the item or folder.</span></span> 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

<span data-ttu-id="01e92-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="01e92-105">**FolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="01e92-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="01e92-106">Attributes and elements</span></span>

<span data-ttu-id="01e92-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="01e92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01e92-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="01e92-108">Attributes</span></span>

|<span data-ttu-id="01e92-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="01e92-109">**Attribute**</span></span>|<span data-ttu-id="01e92-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01e92-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01e92-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="01e92-111">**Id**</span></span> <br/> |<span data-ttu-id="01e92-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="01e92-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="01e92-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01e92-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="01e92-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="01e92-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="01e92-115">Contiene una cadena que identifica una versión de una carpeta identificada por el atributo **ID** .</span><span class="sxs-lookup"><span data-stu-id="01e92-115">Contains a string that identifies a version of a folder that is identified by the **Id** attribute.</span></span> <span data-ttu-id="01e92-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="01e92-116">This attribute is optional.</span></span> <span data-ttu-id="01e92-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="01e92-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="01e92-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="01e92-118">Child elements</span></span>

<span data-ttu-id="01e92-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="01e92-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01e92-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="01e92-120">Parent elements</span></span>

|<span data-ttu-id="01e92-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="01e92-121">**Element**</span></span>|<span data-ttu-id="01e92-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01e92-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01e92-123">Hubiera</span><span class="sxs-lookup"><span data-stu-id="01e92-123">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="01e92-124">Representa una carpeta de calendario en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-124">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="01e92-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="01e92-126">Representa un elemento de calendario en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-126">Represents a calendar item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-127">Contacto</span><span class="sxs-lookup"><span data-stu-id="01e92-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="01e92-128">Representa un elemento de contacto en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-128">Represents a contact item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-129">Hubiera</span><span class="sxs-lookup"><span data-stu-id="01e92-129">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="01e92-130">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-130">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="01e92-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="01e92-132">Representa un evento en el que se copia un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="01e92-132">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="01e92-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="01e92-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="01e92-134">Representa un evento en el que se crea un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="01e92-134">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="01e92-135">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="01e92-135">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="01e92-136">Representa un evento en el que se elimina un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="01e92-136">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="01e92-137">DistributionList</span><span class="sxs-lookup"><span data-stu-id="01e92-137">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="01e92-138">Representa una lista de distribución privada en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-138">Represents a private distribution list in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-139">Folder</span><span class="sxs-lookup"><span data-stu-id="01e92-139">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="01e92-140">Representa una carpeta en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-140">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="01e92-141">Item</span></span>](item.md) <br/> |<span data-ttu-id="01e92-142">Representa un elemento de Exchange genérico.</span><span class="sxs-lookup"><span data-stu-id="01e92-142">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="01e92-143">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="01e92-143">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="01e92-144">Representa un solo elemento que se va a cargar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-144">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-145">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="01e92-145">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="01e92-146">Representa una cancelación de reunión en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-146">Represents a meeting cancellation in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-147">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="01e92-147">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="01e92-148">Representa un mensaje de reunión en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-148">Represents a meeting message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-149">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="01e92-149">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="01e92-150">Representa una convocatoria de reunión en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-150">Represents a meeting request in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-151">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="01e92-151">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="01e92-152">Representa una respuesta a una reunión en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-152">Represents a meeting response in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-153">Mensaje</span><span class="sxs-lookup"><span data-stu-id="01e92-153">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="01e92-154">Representa un mensaje de correo electrónico en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-154">Represents an e-mail message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-155">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="01e92-155">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="01e92-156">Representa un evento en el que se modifica un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="01e92-156">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="01e92-157">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="01e92-157">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="01e92-158">Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="01e92-158">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="01e92-159">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="01e92-159">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="01e92-160">Representa un evento desencadenado por un nuevo elemento de correo en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-160">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-161">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="01e92-161">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="01e92-162">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="01e92-162">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="01e92-163">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="01e92-163">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="01e92-164">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="01e92-164">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="01e92-165">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="01e92-165">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="01e92-166">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="01e92-166">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="01e92-167">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="01e92-167">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="01e92-168">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="01e92-168">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="01e92-169">Tarea</span><span class="sxs-lookup"><span data-stu-id="01e92-169">Task</span></span>](task.md) <br/> |<span data-ttu-id="01e92-170">Representa un elemento de tarea en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-170">Represents a task item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-171">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="01e92-171">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="01e92-172">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="01e92-172">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="01e92-173">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="01e92-173">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="01e92-174">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="01e92-174">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="01e92-175">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="01e92-175">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="01e92-176">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="01e92-176">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="01e92-177">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="01e92-177">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="01e92-178">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="01e92-178">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="01e92-179">Hubiera</span><span class="sxs-lookup"><span data-stu-id="01e92-179">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="01e92-180">Representa una carpeta de tareas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-180">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="01e92-181">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="01e92-181">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="01e92-182">Representa una carpeta de búsqueda en un buzón.</span><span class="sxs-lookup"><span data-stu-id="01e92-182">Represents a search folder in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01e92-183">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01e92-183">Remarks</span></span>

<span data-ttu-id="01e92-184">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="01e92-184">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01e92-185">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="01e92-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01e92-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="01e92-186">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01e92-187">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="01e92-187">Schema Name</span></span>  <br/> |<span data-ttu-id="01e92-188">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="01e92-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="01e92-189">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="01e92-189">Validation File</span></span>  <br/> |<span data-ttu-id="01e92-190">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="01e92-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01e92-191">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="01e92-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="01e92-192">Falso</span><span class="sxs-lookup"><span data-stu-id="01e92-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01e92-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="01e92-193">See also</span></span>

- [<span data-ttu-id="01e92-194">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="01e92-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


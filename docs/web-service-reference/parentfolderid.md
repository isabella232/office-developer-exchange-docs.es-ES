---
title: Id
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
description: El elemento ID representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.
ms.openlocfilehash: 3f60e8adb62fbf464a58af4169fbcd83910877cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836687"
---
# <a name="parentfolderid"></a><span data-ttu-id="a59a5-103">Id</span><span class="sxs-lookup"><span data-stu-id="a59a5-103">ParentFolderId</span></span>

<span data-ttu-id="a59a5-104">El elemento **ID** representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a59a5-104">The **ParentFolderId** element represents the identifier of the parent folder that contains the item or folder.</span></span> 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

<span data-ttu-id="a59a5-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="a59a5-105">**FolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a59a5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a59a5-106">Attributes and elements</span></span>

<span data-ttu-id="a59a5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a59a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a59a5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a59a5-108">Attributes</span></span>

|<span data-ttu-id="a59a5-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a59a5-109">**Attribute**</span></span>|<span data-ttu-id="a59a5-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a59a5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a59a5-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="a59a5-111">**Id**</span></span> <br/> |<span data-ttu-id="a59a5-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a59a5-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="a59a5-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="a59a5-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="a59a5-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="a59a5-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="a59a5-115">Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo **Id** .</span><span class="sxs-lookup"><span data-stu-id="a59a5-115">Contains a string that identifies a version of a folder that is identified by the **Id** attribute.</span></span> <span data-ttu-id="a59a5-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="a59a5-116">This attribute is optional.</span></span> <span data-ttu-id="a59a5-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a59a5-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a59a5-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a59a5-118">Child elements</span></span>

<span data-ttu-id="a59a5-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a59a5-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a59a5-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a59a5-120">Parent elements</span></span>

|<span data-ttu-id="a59a5-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="a59a5-121">**Element**</span></span>|<span data-ttu-id="a59a5-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a59a5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a59a5-123">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="a59a5-123">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="a59a5-124">Representa una carpeta del calendario en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-124">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a59a5-126">Representa un elemento de calendario en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-126">Represents a calendar item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-127">Contact</span><span class="sxs-lookup"><span data-stu-id="a59a5-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="a59a5-128">Representa un elemento de contacto en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-128">Represents a contact item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-129">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="a59a5-129">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="a59a5-130">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-130">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="a59a5-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="a59a5-132">Representa un evento en el que se copia un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="a59a5-132">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="a59a5-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="a59a5-134">Representa un evento en el que se crea una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="a59a5-134">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-135">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="a59a5-135">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="a59a5-136">Representa un evento en el que se elimina un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="a59a5-136">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-137">DistributionList</span><span class="sxs-lookup"><span data-stu-id="a59a5-137">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="a59a5-138">Representa una lista de distribución privada en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-138">Represents a private distribution list in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-139">Folder</span><span class="sxs-lookup"><span data-stu-id="a59a5-139">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="a59a5-140">Representa una carpeta en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-140">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-141">Item</span><span class="sxs-lookup"><span data-stu-id="a59a5-141">Item</span></span>](item.md) <br/> |<span data-ttu-id="a59a5-142">Representa un elemento genérico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a59a5-142">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-143">Elemento (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="a59a5-143">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="a59a5-144">Representa un solo elemento va a cargar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-144">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-145">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="a59a5-145">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="a59a5-146">Representa la cancelación de la reunión en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-146">Represents a meeting cancellation in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-147">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="a59a5-147">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="a59a5-148">Representa un mensaje de reunión en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-148">Represents a meeting message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-149">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a59a5-149">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a59a5-150">Representa una convocatoria de reunión en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-150">Represents a meeting request in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-151">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="a59a5-151">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="a59a5-152">Representa una respuesta a la reunión en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-152">Represents a meeting response in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-153">Message</span><span class="sxs-lookup"><span data-stu-id="a59a5-153">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a59a5-154">Representa un mensaje de correo electrónico en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-154">Represents an e-mail message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-155">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="a59a5-155">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="a59a5-156">Representa un evento en el que se modifica una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="a59a5-156">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-157">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="a59a5-157">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="a59a5-158">Representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="a59a5-158">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-159">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="a59a5-159">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="a59a5-160">Representa un evento que se desencadena por un nuevo elemento de correo en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-160">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-161">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-161">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="a59a5-162">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="a59a5-162">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-163">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-163">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="a59a5-164">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="a59a5-164">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-165">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-165">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="a59a5-166">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="a59a5-166">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-167">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-167">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="a59a5-168">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a59a5-168">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-169">Tarea</span><span class="sxs-lookup"><span data-stu-id="a59a5-169">Task</span></span>](task.md) <br/> |<span data-ttu-id="a59a5-170">Representa un elemento de tarea en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-170">Represents a task item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-171">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-171">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="a59a5-172">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a59a5-172">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-173">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-173">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="a59a5-174">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a59a5-174">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-175">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-175">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="a59a5-176">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="a59a5-176">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-177">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="a59a5-177">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="a59a5-178">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="a59a5-178">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-179">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="a59a5-179">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="a59a5-180">Representa una carpeta de tareas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-180">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a59a5-181">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a59a5-181">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="a59a5-182">Representa una carpeta de búsqueda en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59a5-182">Represents a search folder in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a59a5-183">Notas</span><span class="sxs-lookup"><span data-stu-id="a59a5-183">Remarks</span></span>

<span data-ttu-id="a59a5-184">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a59a5-184">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a59a5-185">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a59a5-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a59a5-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a59a5-186">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a59a5-187">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a59a5-187">Schema Name</span></span>  <br/> |<span data-ttu-id="a59a5-188">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a59a5-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="a59a5-189">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a59a5-189">Validation File</span></span>  <br/> |<span data-ttu-id="a59a5-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a59a5-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a59a5-191">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a59a5-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="a59a5-192">False</span><span class="sxs-lookup"><span data-stu-id="a59a5-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a59a5-193">Ver también</span><span class="sxs-lookup"><span data-stu-id="a59a5-193">See also</span></span>

- [<span data-ttu-id="a59a5-194">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a59a5-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


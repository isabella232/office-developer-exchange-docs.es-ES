---
title: Operación CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: La operación CreateItem crea elementos en el almacén de Exchange.
ms.openlocfilehash: f6aaa9ed8e8257f19780492d6137fb015c1b6136
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458869"
---
# <a name="createitem-operation"></a><span data-ttu-id="e8fc5-103">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-103">CreateItem operation</span></span>

<span data-ttu-id="e8fc5-104">La operación CreateItem crea elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-104">The CreateItem operation creates items in the Exchange store.</span></span>
  
## <a name="using-the-createitem-operation"></a><span data-ttu-id="e8fc5-105">Uso de la operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-105">Using the CreateItem Operation</span></span>

<span data-ttu-id="e8fc5-106">Puede usar la operación CreateItem para crear lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e8fc5-106">You can use the CreateItem operation to create the following:</span></span>
  
- <span data-ttu-id="e8fc5-107">Elementos de calendario</span><span class="sxs-lookup"><span data-stu-id="e8fc5-107">Calendar items</span></span>
    
- <span data-ttu-id="e8fc5-108">Mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-108">E-mail messages</span></span>
    
- <span data-ttu-id="e8fc5-109">Convocatorias de reunión</span><span class="sxs-lookup"><span data-stu-id="e8fc5-109">Meeting requests</span></span>
    
- <span data-ttu-id="e8fc5-110">Tareas</span><span class="sxs-lookup"><span data-stu-id="e8fc5-110">Tasks</span></span>
    
- <span data-ttu-id="e8fc5-111">Contactos</span><span class="sxs-lookup"><span data-stu-id="e8fc5-111">Contacts</span></span>
    
<span data-ttu-id="e8fc5-112">Para obtener más información, vea [operación CreateItem (elemento de calendario)](createitem-operation-calendar-item.md), [operación CreateItem (mensaje de correo electrónico)](createitem-operation-email-message.md), [operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md), [operación CreateItem (tarea)](createitem-operation-task.md)y [operación CreateItem (contacto)](createitem-operation-contact.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc5-112">For more information, see [CreateItem operation (calendar item)](createitem-operation-calendar-item.md), [CreateItem operation (email message)](createitem-operation-email-message.md), [CreateItem operation (meeting request)](createitem-operation-meeting-request.md), [CreateItem operation (task)](createitem-operation-task.md), and [CreateItem operation (contact)](createitem-operation-contact.md).</span></span>
  
<span data-ttu-id="e8fc5-113">La operación CreateItem admite el uso de objetos Response.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-113">The CreateItem operation supports the use of response objects.</span></span> <span data-ttu-id="e8fc5-114">Los objetos de respuesta admiten la aceptación y el rechazo de las reuniones y el tratamiento de los botones de voto incluidos en un mensaje de correo electrónico estándar.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-114">Response objects support the acceptance and rejection of meetings and the handling of voting buttons that are included in a standard e-mail message.</span></span> <span data-ttu-id="e8fc5-115">En la siguiente tabla se enumeran los objetos de respuesta que se controlan en la operación CreateItem.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-115">The following table lists the response objects that are handled in the CreateItem operation.</span></span>
  
|<span data-ttu-id="e8fc5-116">**Response (objeto)**</span><span class="sxs-lookup"><span data-stu-id="e8fc5-116">**Response object**</span></span>|<span data-ttu-id="e8fc5-117">**Action**</span><span class="sxs-lookup"><span data-stu-id="e8fc5-117">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8fc5-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-118">AcceptItem</span></span>  <br/> |<span data-ttu-id="e8fc5-119">Aceptar una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-119">Accept a meeting request.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-120">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-120">CancelCalendarItem</span></span>  <br/> |<span data-ttu-id="e8fc5-121">Cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-121">Cancel a meeting.</span></span> <span data-ttu-id="e8fc5-122">Esto difiere de la eliminación de todos los asistentes porque también elimina la reunión del organizador.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-122">This differs from deleting all attendees because it deletes the meeting for the organizer also.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-123">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-123">DeclineItem</span></span>  <br/> |<span data-ttu-id="e8fc5-124">Rechazar una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-124">Decline a meeting request.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-125">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-125">ForwardItem</span></span>  <br/> |<span data-ttu-id="e8fc5-126">Envíe una convocatoria de reunión a otra persona como convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-126">Send a meeting request to another person as a meeting request.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-127">RemoveItem</span></span>  <br/> |<span data-ttu-id="e8fc5-128">Quitar una reunión cancelada del calendario.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-128">Remove a canceled meeting from the calendar.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-129">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-129">ReplyAllToItem</span></span>  <br/> |<span data-ttu-id="e8fc5-130">Envíe un mensaje que incluya el cuerpo de la convocatoria de reunión original a todos los asistentes a la reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-130">Send a message that includes the body of the original meeting request to all attendees of the meeting.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-131">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-131">ReplyToItem</span></span>  <br/> |<span data-ttu-id="e8fc5-132">Envíe un mensaje que incluya el cuerpo de la convocatoria de reunión original al remitente de la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-132">Send a message that includes the body of the original meeting request to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-133">SendReadReceipt</span><span class="sxs-lookup"><span data-stu-id="e8fc5-133">SendReadReceipt</span></span>  <br/> |<span data-ttu-id="e8fc5-134">Enviar una confirmación de lectura al remitente de la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-134">Send a read receipt to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-135">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="e8fc5-135">TentativelyAcceptItem</span></span>  <br/> |<span data-ttu-id="e8fc5-136">Acepta provisionalmente una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-136">Tentatively accept a meeting request.</span></span>  <br/> |
   
<span data-ttu-id="e8fc5-137">La operación CreateItem también admite objetos de reunión adicionales.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-137">The CreateItem operation also supports additional meeting objects.</span></span> <span data-ttu-id="e8fc5-138">En la tabla siguiente se enumeran los objetos adicionales que admite la operación CreateItem.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-138">The following table lists additional objects that the CreateItem operation supports.</span></span>
  
|<span data-ttu-id="e8fc5-139">**Objeto de reunión**</span><span class="sxs-lookup"><span data-stu-id="e8fc5-139">**Meeting object**</span></span>|<span data-ttu-id="e8fc5-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8fc5-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8fc5-141">Mensaje de reunión</span><span class="sxs-lookup"><span data-stu-id="e8fc5-141">Meeting Message</span></span>  <br/> |<span data-ttu-id="e8fc5-142">Representa un mensaje de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-142">Represents a meeting message in the Exchange store.</span></span> <span data-ttu-id="e8fc5-143">Se trata del objeto base de los otros objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-143">This is the base object for the other meeting objects.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-144">Convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="e8fc5-144">Meeting Request</span></span>  <br/> |<span data-ttu-id="e8fc5-145">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-145">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-146">Respuesta a la reunión</span><span class="sxs-lookup"><span data-stu-id="e8fc5-146">Meeting Response</span></span>  <br/> |<span data-ttu-id="e8fc5-147">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-147">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="e8fc5-148">Cancelación de reunión</span><span class="sxs-lookup"><span data-stu-id="e8fc5-148">Meeting Cancellation</span></span>  <br/> |<span data-ttu-id="e8fc5-149">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8fc5-149">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8fc5-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8fc5-150">See also</span></span>



[<span data-ttu-id="e8fc5-151">Operación CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="e8fc5-151">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)
  
[<span data-ttu-id="e8fc5-152">Operación CreateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="e8fc5-152">CreateItem operation (contact)</span></span>](createitem-operation-contact.md)
  
[<span data-ttu-id="e8fc5-153">Operación CreateItem (mensaje de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="e8fc5-153">CreateItem operation (email message)</span></span>](createitem-operation-email-message.md)
  
[<span data-ttu-id="e8fc5-154">Operación CreateItem (convocatoria de reunión)</span><span class="sxs-lookup"><span data-stu-id="e8fc5-154">CreateItem operation (meeting request)</span></span>](createitem-operation-meeting-request.md)
  
[<span data-ttu-id="e8fc5-155">Operación CreateItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="e8fc5-155">CreateItem operation (task)</span></span>](createitem-operation-task.md)
  
 <span data-ttu-id="e8fc5-156">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="e8fc5-156">**CreateItemType**</span></span>


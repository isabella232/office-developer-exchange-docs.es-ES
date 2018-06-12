---
title: CreateItem Operation
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
ms.openlocfilehash: 7e1808c685cdbaa1e8867aa7425b2cc52218d001
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763955"
---
# <a name="createitem-operation"></a><span data-ttu-id="3af26-103">CreateItem Operation</span><span class="sxs-lookup"><span data-stu-id="3af26-103">CreateItem operation</span></span>

<span data-ttu-id="3af26-104">La operación CreateItem crea elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3af26-104">The CreateItem operation creates items in the Exchange store.</span></span>
  
## <a name="using-the-createitem-operation"></a><span data-ttu-id="3af26-105">Mediante la operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="3af26-105">Using the CreateItem Operation</span></span>

<span data-ttu-id="3af26-106">Puede usar la operación CreateItem para crear lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3af26-106">You can use the CreateItem operation to create the following:</span></span>
  
- <span data-ttu-id="3af26-107">Elementos de calendario</span><span class="sxs-lookup"><span data-stu-id="3af26-107">Calendar items</span></span>
    
- <span data-ttu-id="3af26-108">Mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3af26-108">E-mail messages</span></span>
    
- <span data-ttu-id="3af26-109">Convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="3af26-109">Meeting requests</span></span>
    
- <span data-ttu-id="3af26-110">Tareas</span><span class="sxs-lookup"><span data-stu-id="3af26-110">Tasks</span></span>
    
- <span data-ttu-id="3af26-111">Contacts</span><span class="sxs-lookup"><span data-stu-id="3af26-111">Contacts</span></span>
    
<span data-ttu-id="3af26-112">Para obtener más información, vea [operación CreateItem (elemento de calendario)](createitem-operation-calendar-item.md), [operación CreateItem (mensaje de correo electrónico)](createitem-operation-email-message.md), [operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md), [operación CreateItem (tarea)](createitem-operation-task.md)y [operación CreateItem (contacto) ](createitem-operation-contact.md).</span><span class="sxs-lookup"><span data-stu-id="3af26-112">For more information, see [CreateItem operation (calendar item)](createitem-operation-calendar-item.md), [CreateItem operation (email message)](createitem-operation-email-message.md), [CreateItem operation (meeting request)](createitem-operation-meeting-request.md), [CreateItem operation (task)](createitem-operation-task.md), and [CreateItem operation (contact)](createitem-operation-contact.md).</span></span>
  
<span data-ttu-id="3af26-113">La operación CreateItem admite el uso de objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="3af26-113">The CreateItem operation supports the use of response objects.</span></span> <span data-ttu-id="3af26-114">Objetos de respuesta admiten la aceptación y rechazo de las reuniones y el control de botones de voto que se incluyen en un mensaje de correo electrónico estándar.</span><span class="sxs-lookup"><span data-stu-id="3af26-114">Response objects support the acceptance and rejection of meetings and the handling of voting buttons that are included in a standard e-mail message.</span></span> <span data-ttu-id="3af26-115">En la siguiente tabla se enumera los objetos de respuesta que se administran en la operación CreateItem.</span><span class="sxs-lookup"><span data-stu-id="3af26-115">The following table lists the response objects that are handled in the CreateItem operation.</span></span>
  
|<span data-ttu-id="3af26-116">**Objeto de respuesta**</span><span class="sxs-lookup"><span data-stu-id="3af26-116">**Response object**</span></span>|<span data-ttu-id="3af26-117">**Acción**</span><span class="sxs-lookup"><span data-stu-id="3af26-117">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3af26-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="3af26-118">AcceptItem</span></span>  <br/> |<span data-ttu-id="3af26-119">Aceptar una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-119">Accept a meeting request.</span></span>  <br/> |
|<span data-ttu-id="3af26-120">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="3af26-120">CancelCalendarItem</span></span>  <br/> |<span data-ttu-id="3af26-121">Cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-121">Cancel a meeting.</span></span> <span data-ttu-id="3af26-122">Esto difiere de la eliminación de todos los asistentes debido a que elimina la reunión para el Organizador también.</span><span class="sxs-lookup"><span data-stu-id="3af26-122">This differs from deleting all attendees because it deletes the meeting for the organizer also.</span></span>  <br/> |
|<span data-ttu-id="3af26-123">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="3af26-123">DeclineItem</span></span>  <br/> |<span data-ttu-id="3af26-124">Rechazar una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-124">Decline a meeting request.</span></span>  <br/> |
|<span data-ttu-id="3af26-125">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="3af26-125">ForwardItem</span></span>  <br/> |<span data-ttu-id="3af26-126">Enviar una convocatoria de reunión a otra persona como una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-126">Send a meeting request to another person as a meeting request.</span></span>  <br/> |
|<span data-ttu-id="3af26-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="3af26-127">RemoveItem</span></span>  <br/> |<span data-ttu-id="3af26-128">Quitar una reunión cancelada del calendario.</span><span class="sxs-lookup"><span data-stu-id="3af26-128">Remove a canceled meeting from the calendar.</span></span>  <br/> |
|<span data-ttu-id="3af26-129">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="3af26-129">ReplyAllToItem</span></span>  <br/> |<span data-ttu-id="3af26-130">Enviar un mensaje que incluye el cuerpo de la convocatoria de reunión original a todos los asistentes a la reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-130">Send a message that includes the body of the original meeting request to all attendees of the meeting.</span></span>  <br/> |
|<span data-ttu-id="3af26-131">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="3af26-131">ReplyToItem</span></span>  <br/> |<span data-ttu-id="3af26-132">Enviar un mensaje que incluye el cuerpo de la convocatoria de reunión original al remitente de la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-132">Send a message that includes the body of the original meeting request to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="3af26-133">SendReadReceipt</span><span class="sxs-lookup"><span data-stu-id="3af26-133">SendReadReceipt</span></span>  <br/> |<span data-ttu-id="3af26-134">Enviar una confirmación de lectura para el remitente de la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-134">Send a read receipt to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="3af26-135">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="3af26-135">TentativelyAcceptItem</span></span>  <br/> |<span data-ttu-id="3af26-136">Aceptar provisionalmente una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-136">Tentatively accept a meeting request.</span></span>  <br/> |
   
<span data-ttu-id="3af26-137">La operación CreateItem también es compatible con objetos adicionales de la reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-137">The CreateItem operation also supports additional meeting objects.</span></span> <span data-ttu-id="3af26-138">En la siguiente tabla se enumera los objetos adicionales que admite la operación CreateItem.</span><span class="sxs-lookup"><span data-stu-id="3af26-138">The following table lists additional objects that the CreateItem operation supports.</span></span>
  
|<span data-ttu-id="3af26-139">**Objeto de la reunión**</span><span class="sxs-lookup"><span data-stu-id="3af26-139">**Meeting object**</span></span>|<span data-ttu-id="3af26-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3af26-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3af26-141">Mensaje de la reunión</span><span class="sxs-lookup"><span data-stu-id="3af26-141">Meeting Message</span></span>  <br/> |<span data-ttu-id="3af26-142">Representa un mensaje de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3af26-142">Represents a meeting message in the Exchange store.</span></span> <span data-ttu-id="3af26-143">Éste es el objeto base para los demás objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="3af26-143">This is the base object for the other meeting objects.</span></span>  <br/> |
|<span data-ttu-id="3af26-144">Convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="3af26-144">Meeting Request</span></span>  <br/> |<span data-ttu-id="3af26-145">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3af26-145">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="3af26-146">Respuesta a la reunión</span><span class="sxs-lookup"><span data-stu-id="3af26-146">Meeting Response</span></span>  <br/> |<span data-ttu-id="3af26-147">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3af26-147">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="3af26-148">Cancelación de reunión</span><span class="sxs-lookup"><span data-stu-id="3af26-148">Meeting Cancellation</span></span>  <br/> |<span data-ttu-id="3af26-149">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3af26-149">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3af26-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="3af26-150">See also</span></span>



[<span data-ttu-id="3af26-151">Operación CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="3af26-151">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)
  
[<span data-ttu-id="3af26-152">Operación CreateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="3af26-152">CreateItem operation (contact)</span></span>](createitem-operation-contact.md)
  
[<span data-ttu-id="3af26-153">Operación CreateItem (mensaje de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="3af26-153">CreateItem operation (email message)</span></span>](createitem-operation-email-message.md)
  
[<span data-ttu-id="3af26-154">Operación CreateItem (convocatoria de reunión)</span><span class="sxs-lookup"><span data-stu-id="3af26-154">CreateItem operation (meeting request)</span></span>](createitem-operation-meeting-request.md)
  
[<span data-ttu-id="3af26-155">Operación CreateItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="3af26-155">CreateItem operation (task)</span></span>](createitem-operation-task.md)
  
 <span data-ttu-id="3af26-156">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="3af26-156">**CreateItemType**</span></span>


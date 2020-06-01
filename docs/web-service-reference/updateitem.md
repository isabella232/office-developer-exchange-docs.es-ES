---
title: UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: El elemento UpdateItem define una solicitud para actualizar un elemento en un buzón.
ms.openlocfilehash: 43821db58457ffce22be918a7ba6427f57230010
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466573"
---
# <a name="updateitem"></a><span data-ttu-id="13c24-103">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="13c24-103">UpdateItem</span></span>

<span data-ttu-id="13c24-104">El elemento **UpdateItem** define una solicitud para actualizar un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="13c24-104">The **UpdateItem** element defines a request to update an item in a mailbox.</span></span> 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 <span data-ttu-id="13c24-105">**UpdateItemType**</span><span class="sxs-lookup"><span data-stu-id="13c24-105">**UpdateItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13c24-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="13c24-106">Attributes and elements</span></span>

<span data-ttu-id="13c24-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="13c24-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13c24-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="13c24-108">Attributes</span></span>

|<span data-ttu-id="13c24-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="13c24-109">**Attribute**</span></span>|<span data-ttu-id="13c24-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13c24-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13c24-111">**ConflictResolution**</span><span class="sxs-lookup"><span data-stu-id="13c24-111">**ConflictResolution**</span></span> <br/> |<span data-ttu-id="13c24-112">Identifica el tipo de resolución de conflictos que se va a probar durante una actualización.</span><span class="sxs-lookup"><span data-stu-id="13c24-112">Identifies the type of conflict resolution to try during an update.</span></span> <span data-ttu-id="13c24-113">El valor predeterminado es autoresolve.</span><span class="sxs-lookup"><span data-stu-id="13c24-113">The default value is AutoResolve.</span></span>  <br/> |
|<span data-ttu-id="13c24-114">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="13c24-114">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="13c24-115">Describe cómo se controlará el elemento después de que se actualice.</span><span class="sxs-lookup"><span data-stu-id="13c24-115">Describes how the item will be handled after it is updated.</span></span> <span data-ttu-id="13c24-116">El atributo **MessageDisposition** es necesario para los elementos de mensaje, incluidos los mensajes de reunión, como cancelaciones de reunión, convocatorias de reunión y respuestas a la reunión.</span><span class="sxs-lookup"><span data-stu-id="13c24-116">The **MessageDisposition** attribute is required for message items, including meeting messages such as meeting cancellations, meeting requests, and meeting responses.</span></span>  <br/> |
|<span data-ttu-id="13c24-117">**SendMeetingInvitationsOrCancellations**</span><span class="sxs-lookup"><span data-stu-id="13c24-117">**SendMeetingInvitationsOrCancellations**</span></span> <br/> |<span data-ttu-id="13c24-118">Describe cómo se comunican las actualizaciones de reunión después de que se actualice un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="13c24-118">Describes how meeting updates are communicated after a calendar item is updated.</span></span> <span data-ttu-id="13c24-119">Este atributo es necesario para los elementos de calendario y las ocurrencias de elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="13c24-119">This attribute is required for calendar items and calendar item occurrences.</span></span>  <br/> |
|<span data-ttu-id="13c24-120">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="13c24-120">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="13c24-121">Indica si se deben suprimir las confirmaciones de lectura del elemento actualizado.</span><span class="sxs-lookup"><span data-stu-id="13c24-121">Indicates whether read receipts for the updated item should be suppressed.</span></span> <span data-ttu-id="13c24-122">Un valor de texto de **true** indica que las confirmaciones de lectura deben suprimirse.</span><span class="sxs-lookup"><span data-stu-id="13c24-122">A text value of **true** indicates that read receipts should be suppressed.</span></span> <span data-ttu-id="13c24-123">Un valor de **false** indica que las confirmaciones de lectura se enviarán al remitente.</span><span class="sxs-lookup"><span data-stu-id="13c24-123">A value of **false** indicates that the read receipts will be sent to the sender.</span></span> <span data-ttu-id="13c24-124">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="13c24-124">This attribute is optional.</span></span>  <br/> <span data-ttu-id="13c24-125">Este atributo se introdujo en Exchange Server 2013 SP1.</span><span class="sxs-lookup"><span data-stu-id="13c24-125">This attribute was introduced in Exchange Server 2013 SP1.</span></span>  <br/> |
   
#### <a name="conflictresolution-attribute"></a><span data-ttu-id="13c24-126">Atributo ConflictResolution</span><span class="sxs-lookup"><span data-stu-id="13c24-126">ConflictResolution Attribute</span></span>

|<span data-ttu-id="13c24-127">**Valor**</span><span class="sxs-lookup"><span data-stu-id="13c24-127">**Value**</span></span>|<span data-ttu-id="13c24-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13c24-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13c24-129">NeverOverwrite</span><span class="sxs-lookup"><span data-stu-id="13c24-129">NeverOverwrite</span></span>  <br/> |<span data-ttu-id="13c24-130">Si hay un conflicto, se produce un error en la operación de actualización y se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="13c24-130">If there is a conflict, the update operation fails and an error is returned.</span></span>  <br/> |
|<span data-ttu-id="13c24-131">Autoresolve</span><span class="sxs-lookup"><span data-stu-id="13c24-131">AutoResolve</span></span>  <br/> |<span data-ttu-id="13c24-132">La operación de actualización resuelve automáticamente cualquier conflicto.</span><span class="sxs-lookup"><span data-stu-id="13c24-132">The update operation automatically resolves any conflict.</span></span>  <br/> |
|<span data-ttu-id="13c24-133">AlwaysOverwrite</span><span class="sxs-lookup"><span data-stu-id="13c24-133">AlwaysOverwrite</span></span>  <br/> |<span data-ttu-id="13c24-134">Si hay un conflicto, la operación de actualización sobrescribirá la información.</span><span class="sxs-lookup"><span data-stu-id="13c24-134">If there is a conflict, the update operation will overwrite information.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="13c24-135">Atributo MessageDisposition</span><span class="sxs-lookup"><span data-stu-id="13c24-135">MessageDisposition Attribute</span></span>

|<span data-ttu-id="13c24-136">**Valor**</span><span class="sxs-lookup"><span data-stu-id="13c24-136">**Value**</span></span>|<span data-ttu-id="13c24-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13c24-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13c24-138">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="13c24-138">SaveOnly</span></span>  <br/> |<span data-ttu-id="13c24-139">El elemento se actualiza y se guarda de nuevo en su carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="13c24-139">The item is updated and saved back to its current folder.</span></span>  <br/> |
|<span data-ttu-id="13c24-140">SendOnly</span><span class="sxs-lookup"><span data-stu-id="13c24-140">SendOnly</span></span>  <br/> |<span data-ttu-id="13c24-141">El elemento se actualiza y se envía, pero no se guarda ninguna copia.</span><span class="sxs-lookup"><span data-stu-id="13c24-141">The item is updated and sent but no copy is saved.</span></span>  <br/> |
|<span data-ttu-id="13c24-142">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="13c24-142">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="13c24-143">El elemento se actualiza y se guarda una copia en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="13c24-143">The item is updated and a copy is saved in the folder identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a><span data-ttu-id="13c24-144">Atributo SendMeetingInvitationsOrCancellations</span><span class="sxs-lookup"><span data-stu-id="13c24-144">SendMeetingInvitationsOrCancellations Attribute</span></span>

|<span data-ttu-id="13c24-145">**Valor**</span><span class="sxs-lookup"><span data-stu-id="13c24-145">**Value**</span></span>|<span data-ttu-id="13c24-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13c24-146">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13c24-147">SendToNone</span><span class="sxs-lookup"><span data-stu-id="13c24-147">SendToNone</span></span>  <br/> |<span data-ttu-id="13c24-148">El elemento de calendario se actualiza pero no se envían actualizaciones a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="13c24-148">The calendar item is updated but updates are not sent to attendees.</span></span>  <br/> |
|<span data-ttu-id="13c24-149">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="13c24-149">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="13c24-150">El elemento de calendario se actualiza y la actualización de la reunión se envía a todos los asistentes, pero no se guarda en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="13c24-150">The calendar item is updated and the meeting update is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="13c24-151">SendOnlyToChanged</span><span class="sxs-lookup"><span data-stu-id="13c24-151">SendOnlyToChanged</span></span>  <br/> |<span data-ttu-id="13c24-152">El elemento de calendario se actualiza y la actualización de la reunión se envía sólo a los asistentes afectados por el cambio en la reunión.</span><span class="sxs-lookup"><span data-stu-id="13c24-152">The calendar item is updated and the meeting update is sent only to attendees that are affected by the change in the meeting.</span></span>  <br/> |
|<span data-ttu-id="13c24-153">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="13c24-153">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="13c24-154">El elemento de calendario se actualiza, la actualización de la reunión se envía a todos los asistentes y se guarda una copia en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="13c24-154">The calendar item is updated, the meeting update is sent to all attendees, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="13c24-155">SendToChangedAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="13c24-155">SendToChangedAndSaveCopy</span></span>  <br/> |<span data-ttu-id="13c24-156">El elemento de calendario se actualiza, la actualización de la reunión se envía a todos los asistentes afectados por el cambio en la reunión y se guarda una copia en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="13c24-156">The calendar item is updated, the meeting update is sent to all attendees that are affected by the change in the meeting, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13c24-157">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13c24-157">Child elements</span></span>

|<span data-ttu-id="13c24-158">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13c24-158">**Element**</span></span>|<span data-ttu-id="13c24-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13c24-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13c24-160">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="13c24-160">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="13c24-161">Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="13c24-161">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="13c24-162">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="13c24-162">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="13c24-163">Contiene una matriz de elementos [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se aplican a los elementos.</span><span class="sxs-lookup"><span data-stu-id="13c24-163">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13c24-164">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13c24-164">Parent elements</span></span>

<span data-ttu-id="13c24-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="13c24-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13c24-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13c24-166">Remarks</span></span>

<span data-ttu-id="13c24-167">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="13c24-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13c24-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13c24-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13c24-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="13c24-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="13c24-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="13c24-170">Schema Name</span></span>  <br/> |<span data-ttu-id="13c24-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="13c24-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="13c24-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="13c24-172">Validation File</span></span>  <br/> |<span data-ttu-id="13c24-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="13c24-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="13c24-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="13c24-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="13c24-175">Falso</span><span class="sxs-lookup"><span data-stu-id="13c24-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13c24-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="13c24-176">See also</span></span>



[<span data-ttu-id="13c24-177">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="13c24-177">UpdateItem operation</span></span>](updateitem-operation.md)


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
description: El elemento UpdateItem define una solicitud para actualizar un elemento en un buzón de correo.
ms.openlocfilehash: 7b9b5f1dcffb95eb127572cb91f92d961c05a77e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19840845"
---
# <a name="updateitem"></a><span data-ttu-id="1d4fd-103">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="1d4fd-103">UpdateItem</span></span>

<span data-ttu-id="1d4fd-104">El elemento **UpdateItem** define una solicitud para actualizar un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-104">The **UpdateItem** element defines a request to update an item in a mailbox.</span></span> 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 <span data-ttu-id="1d4fd-105">**UpdateItemType**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-105">**UpdateItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d4fd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d4fd-106">Attributes and elements</span></span>

<span data-ttu-id="1d4fd-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d4fd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d4fd-108">Attributes</span></span>

|<span data-ttu-id="1d4fd-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-109">**Attribute**</span></span>|<span data-ttu-id="1d4fd-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d4fd-111">**ConflictResolution**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-111">**ConflictResolution**</span></span> <br/> |<span data-ttu-id="1d4fd-112">Identifica el tipo de resolución de conflictos para probar durante una actualización.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-112">Identifies the type of conflict resolution to try during an update.</span></span> <span data-ttu-id="1d4fd-113">El valor predeterminado es resolver automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-113">The default value is AutoResolve.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-114">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-114">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="1d4fd-115">Describe cómo se controlarán el elemento después de que se actualice.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-115">Describes how the item will be handled after it is updated.</span></span> <span data-ttu-id="1d4fd-116">El atributo **MessageDisposition** es obligatorio para los elementos de mensaje, incluidos los mensajes de reunión como cancelaciones de reunión, convocatorias de reunión y respuestas a la reunión.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-116">The **MessageDisposition** attribute is required for message items, including meeting messages such as meeting cancellations, meeting requests, and meeting responses.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-117">**SendMeetingInvitationsOrCancellations**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-117">**SendMeetingInvitationsOrCancellations**</span></span> <br/> |<span data-ttu-id="1d4fd-118">Describe cómo se comunican las actualizaciones de la reunión después de actualiza un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-118">Describes how meeting updates are communicated after a calendar item is updated.</span></span> <span data-ttu-id="1d4fd-119">Este atributo es necesario para los elementos de calendario y las apariciones del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-119">This attribute is required for calendar items and calendar item occurrences.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-120">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-120">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="1d4fd-121">Indica si se deben suprimir confirmaciones de lectura para el elemento actualizado.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-121">Indicates whether read receipts for the updated item should be suppressed.</span></span> <span data-ttu-id="1d4fd-122">Un valor de texto de **true** indica que se deben suprimir confirmaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-122">A text value of **true** indicates that read receipts should be suppressed.</span></span> <span data-ttu-id="1d4fd-123">Un valor de **false** indica que se enviarán las confirmaciones de lectura al remitente.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-123">A value of **false** indicates that the read receipts will be sent to the sender.</span></span> <span data-ttu-id="1d4fd-124">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-124">This attribute is optional.</span></span>  <br/> <span data-ttu-id="1d4fd-125">Este atributo se introdujo en Exchange Server 2013 SP1.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-125">This attribute was introduced in Exchange Server 2013 SP1.</span></span>  <br/> |
   
#### <a name="conflictresolution-attribute"></a><span data-ttu-id="1d4fd-126">Atributo ConflictResolution</span><span class="sxs-lookup"><span data-stu-id="1d4fd-126">ConflictResolution Attribute</span></span>

|<span data-ttu-id="1d4fd-127">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-127">**Value**</span></span>|<span data-ttu-id="1d4fd-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d4fd-129">NeverOverwrite</span><span class="sxs-lookup"><span data-stu-id="1d4fd-129">NeverOverwrite</span></span>  <br/> |<span data-ttu-id="1d4fd-130">Si hay un conflicto, se produce un error en la operación de actualización y se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-130">If there is a conflict, the update operation fails and an error is returned.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-131">Resolver automáticamente</span><span class="sxs-lookup"><span data-stu-id="1d4fd-131">AutoResolve</span></span>  <br/> |<span data-ttu-id="1d4fd-132">La operación de actualización resuelve automáticamente cualquier conflicto.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-132">The update operation automatically resolves any conflict.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-133">AlwaysOverwrite</span><span class="sxs-lookup"><span data-stu-id="1d4fd-133">AlwaysOverwrite</span></span>  <br/> |<span data-ttu-id="1d4fd-134">Si hay un conflicto, la operación de actualización sobrescribirá información.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-134">If there is a conflict, the update operation will overwrite information.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="1d4fd-135">Atributo MessageDisposition</span><span class="sxs-lookup"><span data-stu-id="1d4fd-135">MessageDisposition Attribute</span></span>

|<span data-ttu-id="1d4fd-136">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-136">**Value**</span></span>|<span data-ttu-id="1d4fd-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d4fd-138">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="1d4fd-138">SaveOnly</span></span>  <br/> |<span data-ttu-id="1d4fd-139">El elemento se actualiza y se vuelve a guardar en su carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-139">The item is updated and saved back to its current folder.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-140">SendOnly</span><span class="sxs-lookup"><span data-stu-id="1d4fd-140">SendOnly</span></span>  <br/> |<span data-ttu-id="1d4fd-141">El elemento se actualiza y se envía, pero ninguna copia se guarda.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-141">The item is updated and sent but no copy is saved.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-142">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="1d4fd-142">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="1d4fd-143">El elemento se actualiza y se guarda una copia en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4fd-143">The item is updated and a copy is saved in the folder identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a><span data-ttu-id="1d4fd-144">Atributo SendMeetingInvitationsOrCancellations</span><span class="sxs-lookup"><span data-stu-id="1d4fd-144">SendMeetingInvitationsOrCancellations Attribute</span></span>

|<span data-ttu-id="1d4fd-145">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-145">**Value**</span></span>|<span data-ttu-id="1d4fd-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-146">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d4fd-147">SendToNone</span><span class="sxs-lookup"><span data-stu-id="1d4fd-147">SendToNone</span></span>  <br/> |<span data-ttu-id="1d4fd-148">El elemento de calendario se actualiza pero no se envían las actualizaciones a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-148">The calendar item is updated but updates are not sent to attendees.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-149">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="1d4fd-149">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="1d4fd-150">El elemento de calendario se actualiza y se envía a todos los asistentes de la actualización de la reunión pero no se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-150">The calendar item is updated and the meeting update is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-151">SendOnlyToChanged</span><span class="sxs-lookup"><span data-stu-id="1d4fd-151">SendOnlyToChanged</span></span>  <br/> |<span data-ttu-id="1d4fd-152">Se actualiza el elemento de calendario y la actualización de la reunión sólo se envía a los asistentes que se ven afectados por el cambio en la reunión.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-152">The calendar item is updated and the meeting update is sent only to attendees that are affected by the change in the meeting.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-153">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="1d4fd-153">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="1d4fd-154">Se actualiza el elemento de calendario, la actualización de la reunión se envía a todos los asistentes y se guarda una copia en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-154">The calendar item is updated, the meeting update is sent to all attendees, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="1d4fd-155">SendToChangedAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="1d4fd-155">SendToChangedAndSaveCopy</span></span>  <br/> |<span data-ttu-id="1d4fd-156">Se actualiza el elemento de calendario, la actualización de la reunión se envía a todos los asistentes que se ven afectados por el cambio de la reunión y se guarda una copia en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-156">The calendar item is updated, the meeting update is sent to all attendees that are affected by the change in the meeting, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d4fd-157">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d4fd-157">Child elements</span></span>

|<span data-ttu-id="1d4fd-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-158">**Element**</span></span>|<span data-ttu-id="1d4fd-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4fd-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d4fd-160">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="1d4fd-160">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="1d4fd-161">Identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-161">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1d4fd-162">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="1d4fd-162">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="1d4fd-163">Contiene una matriz de elementos de [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se debe aplicar a los elementos.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-163">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d4fd-164">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d4fd-164">Parent elements</span></span>

<span data-ttu-id="1d4fd-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d4fd-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d4fd-166">Remarks</span></span>

<span data-ttu-id="1d4fd-167">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d4fd-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d4fd-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d4fd-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d4fd-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d4fd-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1d4fd-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d4fd-170">Schema Name</span></span>  <br/> |<span data-ttu-id="1d4fd-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1d4fd-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1d4fd-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d4fd-172">Validation File</span></span>  <br/> |<span data-ttu-id="1d4fd-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1d4fd-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d4fd-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d4fd-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d4fd-175">False</span><span class="sxs-lookup"><span data-stu-id="1d4fd-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d4fd-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d4fd-176">See also</span></span>



[<span data-ttu-id="1d4fd-177">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="1d4fd-177">UpdateItem operation</span></span>](updateitem-operation.md)


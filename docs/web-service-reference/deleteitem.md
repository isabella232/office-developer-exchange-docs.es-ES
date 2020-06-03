---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: El elemento DeleteItem define una solicitud para eliminar un elemento de un buzón de correo en el almacén de Exchange.
ms.openlocfilehash: ed13ee32b487f49740aed80e8705257d3e2e6938
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529206"
---
# <a name="deleteitem"></a><span data-ttu-id="3f6b1-103">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="3f6b1-103">DeleteItem</span></span>

<span data-ttu-id="3f6b1-104">El elemento **DeleteItem** define una solicitud para eliminar un elemento de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-104">The **DeleteItem** element defines a request to delete an item from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 <span data-ttu-id="3f6b1-105">**DeleteItemType**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-105">**DeleteItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f6b1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3f6b1-106">Attributes and elements</span></span>

<span data-ttu-id="3f6b1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f6b1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f6b1-108">Attributes</span></span>

|<span data-ttu-id="3f6b1-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-109">**Attribute**</span></span>|<span data-ttu-id="3f6b1-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f6b1-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="3f6b1-112">Describe cómo se elimina un elemento.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-112">Describes how an item is deleted.</span></span> <span data-ttu-id="3f6b1-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-114">**SendMeetingCancellations**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-114">**SendMeetingCancellations**</span></span> <br/> |<span data-ttu-id="3f6b1-115">Describe si la eliminación de un elemento de calendario se comunica a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-115">Describes whether a calendar item deletion is communicated to attendees.</span></span> <span data-ttu-id="3f6b1-116">Este atributo es necesario cuando se eliminan elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-116">This attribute is required when calendar items are deleted.</span></span> <span data-ttu-id="3f6b1-117">Este atributo es opcional si se eliminan elementos que no son de calendario.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-117">This attribute is optional if non-calendar items are deleted.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-118">**AffectedTaskOccurrences**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-118">**AffectedTaskOccurrences**</span></span> <br/> |<span data-ttu-id="3f6b1-119">Describe si una [operación DeleteItem](deleteitem-operation.md)elimina una instancia de tarea o un patrón de tareas.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-119">Describes whether a task instance or a task master is deleted by a [DeleteItem operation](deleteitem-operation.md).</span></span> <span data-ttu-id="3f6b1-120">Este atributo es necesario cuando se eliminan tareas.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-120">This attribute is required when tasks are deleted.</span></span> <span data-ttu-id="3f6b1-121">Este atributo es opcional cuando se eliminan elementos que no son de tarea.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-121">This attribute is optional when non-task items are deleted.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-122">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-122">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="3f6b1-123">Indica si se suprimen las confirmaciones de lectura del elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-123">Indicates whether read receipts for the deleted item are suppressed.</span></span> <span data-ttu-id="3f6b1-124">Un valor de texto de **true**, indica que se suprimen las confirmaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-124">A text value of **true**, indicates that the read receipts are suppressed.</span></span> <span data-ttu-id="3f6b1-125">Un valor de **false** indica que las confirmaciones de lectura se envían al remitente.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-125">A value of **false** indicates that the read receipts are sent to the sender.</span></span> <span data-ttu-id="3f6b1-126">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-126">This attribute is optional.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="3f6b1-127">Atributo DeleteType</span><span class="sxs-lookup"><span data-stu-id="3f6b1-127">DeleteType attribute</span></span>

|<span data-ttu-id="3f6b1-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-128">**Value**</span></span>|<span data-ttu-id="3f6b1-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f6b1-130">HardDelete</span><span class="sxs-lookup"><span data-stu-id="3f6b1-130">HardDelete</span></span>  <br/> |<span data-ttu-id="3f6b1-131">Un elemento se elimina de forma permanente de la tienda.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-131">An item is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-132">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="3f6b1-132">SoftDelete</span></span>  <br/> |<span data-ttu-id="3f6b1-133">Si el contenedor está habilitado, se mueve un elemento al contenedor.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-133">An item is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-134">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="3f6b1-134">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="3f6b1-135">Se mueve un elemento a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-135">An item is moved to the Deleted Items folder.</span></span>  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a><span data-ttu-id="3f6b1-136">Atributo SendMeetingCancellations</span><span class="sxs-lookup"><span data-stu-id="3f6b1-136">SendMeetingCancellations attribute</span></span>

|<span data-ttu-id="3f6b1-137">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-137">**Value**</span></span>|<span data-ttu-id="3f6b1-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f6b1-139">SendToNone</span><span class="sxs-lookup"><span data-stu-id="3f6b1-139">SendToNone</span></span>  <br/> |<span data-ttu-id="3f6b1-140">Se elimina un elemento de calendario sin enviar un mensaje de cancelación.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-140">A calendar item is deleted without sending a cancellation message.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-141">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="3f6b1-141">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="3f6b1-142">Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-142">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-143">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="3f6b1-143">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="3f6b1-144">Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-144">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span> <span data-ttu-id="3f6b1-145">Se guarda una copia del mensaje de cancelación en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-145">A copy of the cancellation message is saved in the Sent Items folder.</span></span>  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a><span data-ttu-id="3f6b1-146">Atributo AffectedTaskOccurrences</span><span class="sxs-lookup"><span data-stu-id="3f6b1-146">AffectedTaskOccurrences attribute</span></span>

|<span data-ttu-id="3f6b1-147">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-147">**Value**</span></span>|<span data-ttu-id="3f6b1-148">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-148">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f6b1-149">AllOccurrences</span><span class="sxs-lookup"><span data-stu-id="3f6b1-149">AllOccurrences</span></span>  <br/> |<span data-ttu-id="3f6b1-150">Una solicitud de eliminación de elemento elimina la tarea maestra y, por tanto, todas las tareas periódicas que están asociadas a la tarea maestra.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-150">A delete item request deletes the master task, and therefore all recurring tasks that are associated with the master task.</span></span>  <br/> |
|<span data-ttu-id="3f6b1-151">SpecifiedOccurrenceOnly</span><span class="sxs-lookup"><span data-stu-id="3f6b1-151">SpecifiedOccurrenceOnly</span></span>  <br/> |<span data-ttu-id="3f6b1-152">Una solicitud de eliminación de elementos elimina solo las ocurrencias específicas de una tarea.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-152">A delete item request deletes only specific occurrences of a task.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3f6b1-153">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f6b1-153">Child elements</span></span>

|<span data-ttu-id="3f6b1-154">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-154">**Element**</span></span>|<span data-ttu-id="3f6b1-155">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f6b1-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f6b1-156">ItemIds</span><span class="sxs-lookup"><span data-stu-id="3f6b1-156">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="3f6b1-157">Contiene una matriz de elementos, elementos de ocurrencia y elementos maestros periódicos para eliminarlos de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-157">Contains an array of items, occurrence items, and recurring master items to delete from a mailbox in the Exchange store.</span></span> <span data-ttu-id="3f6b1-158">La [operación DeleteItem](deleteitem-operation.md) puede realizarse en cualquier tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-158">The [DeleteItem operation](deleteitem-operation.md) can be performed on any item type.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f6b1-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3f6b1-159">Parent elements</span></span>

<span data-ttu-id="3f6b1-160">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f6b1-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f6b1-161">Remarks</span></span>

<span data-ttu-id="3f6b1-162">Las opciones **MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que cuando se completa una llamada de servicio Web, la base de datos movió el elemento a la carpeta elementos eliminados o quitó permanentemente el elemento de la base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-162">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="3f6b1-163">Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-163">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="3f6b1-164">La opción **SoftDelete** funciona de forma diferente para las distintas versiones de Exchange de destino.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-164">The **SoftDelete** option works differently for different target versions of Exchange.</span></span> <span data-ttu-id="3f6b1-165">**SoftDelete** para Exchange 2007 establece un bit en el elemento que indica a la base de datos de Exchange que el elemento se moverá a la carpeta del contenedor a una hora indeterminada en el futuro.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-165">**SoftDelete** for Exchange 2007 sets a bit on the item that indicates to the Exchange database that the item will be moved to the dumpster folder at an indeterminate time in the future.</span></span> <span data-ttu-id="3f6b1-166">**SoftDelete** para Exchange 2010 inmediatamente mueve el elemento al contenedor.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-166">**SoftDelete** for Exchange 2010 immediately moves the item to the dumpster.</span></span> <span data-ttu-id="3f6b1-167">**SoftDelete** no es una opción para la eliminación de carpetas.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-167">**SoftDelete** is not an option for folder deletion.</span></span> <span data-ttu-id="3f6b1-168">**SoftDelete** búsquedas transversales de elementos y carpetas no devolverán ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-168">**SoftDelete** traversal searches for items and folders will not return any results.</span></span> 
  
<span data-ttu-id="3f6b1-169">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f6b1-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f6b1-170">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3f6b1-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f6b1-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f6b1-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3f6b1-172">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3f6b1-172">Schema Name</span></span>  <br/> |<span data-ttu-id="3f6b1-173">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3f6b1-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3f6b1-174">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3f6b1-174">Validation File</span></span>  <br/> |<span data-ttu-id="3f6b1-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3f6b1-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3f6b1-176">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3f6b1-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f6b1-177">Falso</span><span class="sxs-lookup"><span data-stu-id="3f6b1-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f6b1-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f6b1-178">See also</span></span>

- [<span data-ttu-id="3f6b1-179">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="3f6b1-179">DeleteItemResponse</span></span>](deleteitemresponse.md)  
- [<span data-ttu-id="3f6b1-180">Operación DeleteItem</span><span class="sxs-lookup"><span data-stu-id="3f6b1-180">DeleteItem operation</span></span>](deleteitem-operation.md)


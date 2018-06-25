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
description: El elemento DeleteItem define una solicitud para eliminar un elemento de un buzón en el almacén de Exchange.
ms.openlocfilehash: de64787750c88c8a47bb69daddc0a1d2ebe8bde9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764106"
---
# <a name="deleteitem"></a><span data-ttu-id="1fa77-103">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="1fa77-103">DeleteItem</span></span>

<span data-ttu-id="1fa77-104">El elemento **DeleteItem** define una solicitud para eliminar un elemento de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1fa77-104">The **DeleteItem** element defines a request to delete an item from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 <span data-ttu-id="1fa77-105">**DeleteItemType**</span><span class="sxs-lookup"><span data-stu-id="1fa77-105">**DeleteItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1fa77-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1fa77-106">Attributes and elements</span></span>

<span data-ttu-id="1fa77-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1fa77-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1fa77-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1fa77-108">Attributes</span></span>

|<span data-ttu-id="1fa77-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1fa77-109">**Attribute**</span></span>|<span data-ttu-id="1fa77-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fa77-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fa77-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="1fa77-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="1fa77-112">Describe cómo se elimina un elemento.</span><span class="sxs-lookup"><span data-stu-id="1fa77-112">Describes how an item is deleted.</span></span> <span data-ttu-id="1fa77-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="1fa77-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="1fa77-114">**SendMeetingCancellations**</span><span class="sxs-lookup"><span data-stu-id="1fa77-114">**SendMeetingCancellations**</span></span> <br/> |<span data-ttu-id="1fa77-115">Describe si una eliminación del elemento de calendario se comunica a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="1fa77-115">Describes whether a calendar item deletion is communicated to attendees.</span></span> <span data-ttu-id="1fa77-116">Este atributo es necesario cuando se eliminan los elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="1fa77-116">This attribute is required when calendar items are deleted.</span></span> <span data-ttu-id="1fa77-117">Este atributo es opcional si los elementos de calendario no se eliminan.</span><span class="sxs-lookup"><span data-stu-id="1fa77-117">This attribute is optional if non-calendar items are deleted.</span></span>  <br/> |
|<span data-ttu-id="1fa77-118">**AffectedTaskOccurrences**</span><span class="sxs-lookup"><span data-stu-id="1fa77-118">**AffectedTaskOccurrences**</span></span> <br/> |<span data-ttu-id="1fa77-119">Describe si se elimina una instancia de la tarea o un patrón de tarea por una [operación DeleteItem](deleteitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="1fa77-119">Describes whether a task instance or a task master is deleted by a [DeleteItem operation](deleteitem-operation.md).</span></span> <span data-ttu-id="1fa77-120">Este atributo es necesario cuando se eliminan las tareas.</span><span class="sxs-lookup"><span data-stu-id="1fa77-120">This attribute is required when tasks are deleted.</span></span> <span data-ttu-id="1fa77-121">Este atributo es opcional cuando se eliminan los elementos de tarea que no sean.</span><span class="sxs-lookup"><span data-stu-id="1fa77-121">This attribute is optional when non-task items are deleted.</span></span>  <br/> |
|<span data-ttu-id="1fa77-122">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="1fa77-122">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="1fa77-123">Indica si se suprimen las confirmaciones de lectura para el elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="1fa77-123">Indicates whether read receipts for the deleted item are suppressed.</span></span> <span data-ttu-id="1fa77-124">Un valor de texto **es true**, indica que se suprimen las confirmaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="1fa77-124">A text value of **true**, indicates that the read receipts are suppressed.</span></span> <span data-ttu-id="1fa77-125">Un valor de **false** indica que se envían las confirmaciones de lectura al remitente.</span><span class="sxs-lookup"><span data-stu-id="1fa77-125">A value of **false** indicates that the read receipts are sent to the sender.</span></span> <span data-ttu-id="1fa77-126">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="1fa77-126">This attribute is optional.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="1fa77-127">Atributo DeleteType</span><span class="sxs-lookup"><span data-stu-id="1fa77-127">DeleteType attribute</span></span>

|<span data-ttu-id="1fa77-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1fa77-128">**Value**</span></span>|<span data-ttu-id="1fa77-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fa77-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fa77-130">HardDelete</span><span class="sxs-lookup"><span data-stu-id="1fa77-130">HardDelete</span></span>  <br/> |<span data-ttu-id="1fa77-131">Un elemento se quitará permanentemente el almacén.</span><span class="sxs-lookup"><span data-stu-id="1fa77-131">An item is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="1fa77-132">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="1fa77-132">SoftDelete</span></span>  <br/> |<span data-ttu-id="1fa77-133">Un elemento se mueve al volcado de archivos si el volcado de archivos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1fa77-133">An item is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="1fa77-134">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="1fa77-134">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="1fa77-135">Un elemento se mueve a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="1fa77-135">An item is moved to the Deleted Items folder.</span></span>  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a><span data-ttu-id="1fa77-136">Atributo SendMeetingCancellations</span><span class="sxs-lookup"><span data-stu-id="1fa77-136">SendMeetingCancellations attribute</span></span>

|<span data-ttu-id="1fa77-137">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1fa77-137">**Value**</span></span>|<span data-ttu-id="1fa77-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fa77-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fa77-139">SendToNone</span><span class="sxs-lookup"><span data-stu-id="1fa77-139">SendToNone</span></span>  <br/> |<span data-ttu-id="1fa77-140">Se elimina un elemento de calendario sin enviar un mensaje de cancelación.</span><span class="sxs-lookup"><span data-stu-id="1fa77-140">A calendar item is deleted without sending a cancellation message.</span></span>  <br/> |
|<span data-ttu-id="1fa77-141">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="1fa77-141">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="1fa77-142">Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="1fa77-142">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span>  <br/> |
|<span data-ttu-id="1fa77-143">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="1fa77-143">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="1fa77-144">Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="1fa77-144">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span> <span data-ttu-id="1fa77-145">En la carpeta Elementos enviados, se guarda una copia del mensaje de cancelación.</span><span class="sxs-lookup"><span data-stu-id="1fa77-145">A copy of the cancellation message is saved in the Sent Items folder.</span></span>  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a><span data-ttu-id="1fa77-146">Atributo AffectedTaskOccurrences</span><span class="sxs-lookup"><span data-stu-id="1fa77-146">AffectedTaskOccurrences attribute</span></span>

|<span data-ttu-id="1fa77-147">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1fa77-147">**Value**</span></span>|<span data-ttu-id="1fa77-148">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fa77-148">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fa77-149">AllOccurrences</span><span class="sxs-lookup"><span data-stu-id="1fa77-149">AllOccurrences</span></span>  <br/> |<span data-ttu-id="1fa77-150">Una solicitud de elemento delete Elimina la tarea principal y, por lo tanto, todas las tareas repetitivas que están asociados con la tarea principal.</span><span class="sxs-lookup"><span data-stu-id="1fa77-150">A delete item request deletes the master task, and therefore all recurring tasks that are associated with the master task.</span></span>  <br/> |
|<span data-ttu-id="1fa77-151">SpecifiedOccurrenceOnly</span><span class="sxs-lookup"><span data-stu-id="1fa77-151">SpecifiedOccurrenceOnly</span></span>  <br/> |<span data-ttu-id="1fa77-152">Una solicitud de elemento delete elimina sólo las apariciones específicas de una tarea.</span><span class="sxs-lookup"><span data-stu-id="1fa77-152">A delete item request deletes only specific occurrences of a task.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1fa77-153">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1fa77-153">Child elements</span></span>

|<span data-ttu-id="1fa77-154">**Element**</span><span class="sxs-lookup"><span data-stu-id="1fa77-154">**Element**</span></span>|<span data-ttu-id="1fa77-155">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fa77-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1fa77-156">ItemId</span><span class="sxs-lookup"><span data-stu-id="1fa77-156">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="1fa77-157">Contiene una matriz de elementos, elementos de repetición y periódica maestra para eliminar de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1fa77-157">Contains an array of items, occurrence items, and recurring master items to delete from a mailbox in the Exchange store.</span></span> <span data-ttu-id="1fa77-158">La [operación DeleteItem](deleteitem-operation.md) puede realizarse en cualquier tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="1fa77-158">The [DeleteItem operation](deleteitem-operation.md) can be performed on any item type.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1fa77-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1fa77-159">Parent elements</span></span>

<span data-ttu-id="1fa77-160">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1fa77-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1fa77-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1fa77-161">Remarks</span></span>

<span data-ttu-id="1fa77-162">Las opciones **MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que el tiempo de una llamada al servicio Web completa, la base de datos ha movido el elemento a la carpeta Elementos eliminados o quita permanentemente el elemento de la base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1fa77-162">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="1fa77-163">Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="1fa77-163">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="1fa77-164">La opción **SoftDelete** funciona de manera diferente para las versiones de destino diferente de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1fa77-164">The **SoftDelete** option works differently for different target versions of Exchange.</span></span> <span data-ttu-id="1fa77-165">**SoftDelete** para Exchange 2007 establece un bit en el elemento que se indica a la base de datos de Exchange que se moverá el elemento para el volcado de archivos carpeta en un momento indeterminado en el futuro.</span><span class="sxs-lookup"><span data-stu-id="1fa77-165">**SoftDelete** for Exchange 2007 sets a bit on the item that indicates to the Exchange database that the item will be moved to the dumpster folder at an indeterminate time in the future.</span></span> <span data-ttu-id="1fa77-166">**SoftDelete** para Exchange 2010 mueve inmediatamente el elemento para el volcado de archivos.</span><span class="sxs-lookup"><span data-stu-id="1fa77-166">**SoftDelete** for Exchange 2010 immediately moves the item to the dumpster.</span></span> <span data-ttu-id="1fa77-167">**SoftDelete** no es una opción de eliminación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1fa77-167">**SoftDelete** is not an option for folder deletion.</span></span> <span data-ttu-id="1fa77-168">**SoftDelete** búsquedas de recorrido de elementos y carpetas no devolverá ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="1fa77-168">**SoftDelete** traversal searches for items and folders will not return any results.</span></span> 
  
<span data-ttu-id="1fa77-169">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1fa77-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1fa77-170">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1fa77-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fa77-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1fa77-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1fa77-172">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1fa77-172">Schema Name</span></span>  <br/> |<span data-ttu-id="1fa77-173">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1fa77-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1fa77-174">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1fa77-174">Validation File</span></span>  <br/> |<span data-ttu-id="1fa77-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1fa77-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1fa77-176">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1fa77-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="1fa77-177">False</span><span class="sxs-lookup"><span data-stu-id="1fa77-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1fa77-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fa77-178">See also</span></span>

- [<span data-ttu-id="1fa77-179">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="1fa77-179">DeleteItemResponse</span></span>](deleteitemresponse.md)  
- [<span data-ttu-id="1fa77-180">Operación DeleteItem</span><span class="sxs-lookup"><span data-stu-id="1fa77-180">DeleteItem operation</span></span>](deleteitem-operation.md)


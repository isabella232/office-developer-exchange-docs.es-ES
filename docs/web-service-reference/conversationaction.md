---
title: ConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: El elemento ConversationAction contiene una sola acción que se aplicará a una única conversación.
ms.openlocfilehash: cb7d874f787b105d5185749dfaf1e940d2411d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529255"
---
# <a name="conversationaction"></a><span data-ttu-id="8e721-103">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="8e721-103">ConversationAction</span></span>

<span data-ttu-id="8e721-104">El elemento **ConversationAction** contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-104">The **ConversationAction** element contains a single action to be applied to a single conversation.</span></span> 
  
[<span data-ttu-id="8e721-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="8e721-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="8e721-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="8e721-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="8e721-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="8e721-107">ConversationAction</span></span>](conversationaction.md)
  
```XML
<ConversationAction>
   <Action/>
   <ConversationId/>
   <ContextFolderId/>
   <ConversationLastSyncTime/>
   <ProcessRightAway/>
   <DestinationFolderId/>
   <Categories/>
   <EnableAlwaysDelete/>
   <IsRead/>
   <DeleteType/>
</ConversationAction>
```

 <span data-ttu-id="8e721-108">**ConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="8e721-108">**ConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e721-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8e721-109">Attributes and elements</span></span>

<span data-ttu-id="8e721-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8e721-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e721-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e721-111">Attributes</span></span>

<span data-ttu-id="8e721-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8e721-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e721-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8e721-113">Child elements</span></span>

|<span data-ttu-id="8e721-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e721-114">**Element**</span></span>|<span data-ttu-id="8e721-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e721-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e721-116">Acción (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="8e721-116">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md) <br/> |<span data-ttu-id="8e721-117">Contiene la acción que se realizará en la conversación especificada por el elemento [ConversationId](conversationid.md) .</span><span class="sxs-lookup"><span data-stu-id="8e721-117">Contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> <span data-ttu-id="8e721-118">Este elemento debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8e721-118">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="8e721-119">ConversationId</span><span class="sxs-lookup"><span data-stu-id="8e721-119">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="8e721-120">Contiene el identificador de la conversación que tendrá la acción especificada por el elemento [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) aplicado a los elementos de la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-120">Contains the identifier of the conversation that will have the action specified by the [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) element applied to items in the conversation.</span></span> <span data-ttu-id="8e721-121">Este elemento debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8e721-121">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="8e721-122">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="8e721-122">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="8e721-123">Indica la carpeta que está destinada a las acciones que usan carpetas.</span><span class="sxs-lookup"><span data-stu-id="8e721-123">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="8e721-124">Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de la conversación de una carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="8e721-124">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="8e721-125">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="8e721-125">ConversationLastSyncTime</span></span>](conversationlastsynctime.md) <br/> |<span data-ttu-id="8e721-126">Contiene la fecha y la hora en que una conversación se sincronizó por última vez.</span><span class="sxs-lookup"><span data-stu-id="8e721-126">Contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="8e721-127">Este elemento debe estar presente cuando se intenta eliminar todos los elementos de una conversación que se recibieron hasta la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="8e721-127">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span>  <br/> |
|[<span data-ttu-id="8e721-128">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="8e721-128">ProcessRightAway</span></span>](processrightaway.md) <br/> |<span data-ttu-id="8e721-129">Indica si la respuesta se envía en cuanto la acción comienza a procesarse en el servidor o si la respuesta se envía una vez completada la acción.</span><span class="sxs-lookup"><span data-stu-id="8e721-129">Indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="8e721-130">Este elemento debe estar presente para que la respuesta se envíe asincrónica a la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="8e721-130">This element must be present for the response to be sent asynchronous to the requested action.</span></span>  <br/> |
|[<span data-ttu-id="8e721-131">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="8e721-131">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="8e721-132">Indica la carpeta de destino para las acciones de copiar y mover.</span><span class="sxs-lookup"><span data-stu-id="8e721-132">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="8e721-133">Categorías</span><span class="sxs-lookup"><span data-stu-id="8e721-133">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8e721-134">Contiene una colección de cadenas que identifican las categorías a las que pertenecen los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-134">Contains a collection of strings that identify the categories to which items in a conversation belong.</span></span>  <br/> |
|[<span data-ttu-id="8e721-135">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="8e721-135">EnableAlwaysDelete</span></span>](enablealwaysdelete.md) <br/> |<span data-ttu-id="8e721-136">Especifica una marca que permite la eliminación para todos los elementos nuevos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-136">Specifies a flag that enables deletion for all new items in a conversation.</span></span>  <br/> |
|[<span data-ttu-id="8e721-137">IsRead</span><span class="sxs-lookup"><span data-stu-id="8e721-137">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="8e721-138">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8e721-138">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="8e721-139">DeleteType</span><span class="sxs-lookup"><span data-stu-id="8e721-139">DeleteType</span></span>](deletetype.md) <br/> |<span data-ttu-id="8e721-140">Indica cómo se eliminan los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-140">Indicates how items in a conversation are deleted.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8e721-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8e721-141">Parent elements</span></span>

|<span data-ttu-id="8e721-142">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e721-142">**Element**</span></span>|<span data-ttu-id="8e721-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e721-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e721-144">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="8e721-144">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="8e721-145">Contiene una colección de conversaciones y las acciones que se aplican a ellas.</span><span class="sxs-lookup"><span data-stu-id="8e721-145">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8e721-146">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8e721-146">Text value</span></span>

<span data-ttu-id="8e721-147">**Valores de texto del elemento ConversationAction**</span><span class="sxs-lookup"><span data-stu-id="8e721-147">**ConversationAction element text values**</span></span>

|<span data-ttu-id="8e721-148">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8e721-148">**Value**</span></span>|<span data-ttu-id="8e721-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e721-149">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e721-150">AlwaysCategorize</span><span class="sxs-lookup"><span data-stu-id="8e721-150">AlwaysCategorize</span></span>  <br/> |<span data-ttu-id="8e721-151">Clasificar siempre la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-151">Always categorize the conversation.</span></span>  <br/> |
|<span data-ttu-id="8e721-152">AlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="8e721-152">AlwaysDelete</span></span>  <br/> |<span data-ttu-id="8e721-153">Elimine siempre la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-153">Always delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="8e721-154">AlwaysMove</span><span class="sxs-lookup"><span data-stu-id="8e721-154">AlwaysMove</span></span>  <br/> |<span data-ttu-id="8e721-155">Mueva siempre la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-155">Always move the conversation.</span></span>  <br/> |
|<span data-ttu-id="8e721-156">Eliminar</span><span class="sxs-lookup"><span data-stu-id="8e721-156">Delete</span></span>  <br/> |<span data-ttu-id="8e721-157">Elimine la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-157">Delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="8e721-158">Mover</span><span class="sxs-lookup"><span data-stu-id="8e721-158">Move</span></span>  <br/> |<span data-ttu-id="8e721-159">Mover la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-159">Move the conversation.</span></span>  <br/> |
|<span data-ttu-id="8e721-160">Copiar</span><span class="sxs-lookup"><span data-stu-id="8e721-160">Copy</span></span>  <br/> |<span data-ttu-id="8e721-161">Copiar la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-161">Copy the conversation.</span></span>  <br/> |
|<span data-ttu-id="8e721-162">SetReadState</span><span class="sxs-lookup"><span data-stu-id="8e721-162">SetReadState</span></span>  <br/> |<span data-ttu-id="8e721-163">Establezca el estado de lectura de la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-163">Set the read state of the conversation.</span></span>  <br/> |
|<span data-ttu-id="8e721-164">SetRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8e721-164">SetRetentionPolicy</span></span>  <br/> |<span data-ttu-id="8e721-165">Establezca la Directiva de retención para la conversación.</span><span class="sxs-lookup"><span data-stu-id="8e721-165">Set the retention policy for the conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e721-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e721-166">Remarks</span></span>

<span data-ttu-id="8e721-167">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8e721-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e721-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8e721-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e721-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e721-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8e721-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8e721-170">Schema Name</span></span>  <br/> |<span data-ttu-id="8e721-171">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8e721-171">Types schema</span></span>  <br/> |
|<span data-ttu-id="8e721-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8e721-172">Validation File</span></span>  <br/> |<span data-ttu-id="8e721-173">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8e721-173">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8e721-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8e721-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="8e721-175">Falso</span><span class="sxs-lookup"><span data-stu-id="8e721-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e721-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e721-176">See also</span></span>



[<span data-ttu-id="8e721-177">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="8e721-177">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="8e721-178">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8e721-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


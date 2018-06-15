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
description: El elemento ConversationAction contiene una sola acción que se aplicará a una conversación único.
ms.openlocfilehash: 45cd6df3aba94062bd5aa0ddf9367e8cf118dc6b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763869"
---
# <a name="conversationaction"></a><span data-ttu-id="9f3c5-103">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="9f3c5-103">ConversationAction</span></span>

<span data-ttu-id="9f3c5-104">El elemento **ConversationAction** contiene una sola acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-104">The **ConversationAction** element contains a single action to be applied to a single conversation.</span></span> 
  
[<span data-ttu-id="9f3c5-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="9f3c5-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="9f3c5-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="9f3c5-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="9f3c5-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="9f3c5-107">ConversationAction</span></span>](conversationaction.md)
  
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

 <span data-ttu-id="9f3c5-108">**ConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-108">**ConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9f3c5-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9f3c5-109">Attributes and elements</span></span>

<span data-ttu-id="9f3c5-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9f3c5-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f3c5-111">Attributes</span></span>

<span data-ttu-id="9f3c5-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9f3c5-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9f3c5-113">Child elements</span></span>

|<span data-ttu-id="9f3c5-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-114">**Element**</span></span>|<span data-ttu-id="9f3c5-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f3c5-116">Acción (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="9f3c5-116">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md) <br/> |<span data-ttu-id="9f3c5-117">Contiene la acción para llevar a cabo en la conversación especificada por el elemento [ConversationId](conversationid.md) .</span><span class="sxs-lookup"><span data-stu-id="9f3c5-117">Contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> <span data-ttu-id="9f3c5-118">Este elemento debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-118">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-119">ConversationId</span><span class="sxs-lookup"><span data-stu-id="9f3c5-119">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="9f3c5-120">Contiene el identificador de la conversación que se va a tener la acción especificada por el elemento de [acción (ConversationActionTypeType)](action-conversationactiontypetype.md) aplicado a los elementos de la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-120">Contains the identifier of the conversation that will have the action specified by the [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) element applied to items in the conversation.</span></span> <span data-ttu-id="9f3c5-121">Este elemento debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-121">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-122">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="9f3c5-122">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="9f3c5-123">Indica la carpeta que está destinada a las acciones que utilizan carpetas.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-123">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="9f3c5-124">Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de una conversación en una carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-124">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-125">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="9f3c5-125">ConversationLastSyncTime</span></span>](conversationlastsynctime.md) <br/> |<span data-ttu-id="9f3c5-126">Contiene la fecha y hora en que se sincronizaron por última vez una conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-126">Contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="9f3c5-127">Este elemento debe estar presente al intentar eliminar todos los elementos de una conversación que se han recibido hasta el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-127">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-128">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="9f3c5-128">ProcessRightAway</span></span>](processrightaway.md) <br/> |<span data-ttu-id="9f3c5-129">Indica si la respuesta se envía tan pronto como la acción inicia el procesamiento en el servidor o si la respuesta se ha enviado una vez completada la acción.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-129">Indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="9f3c5-130">Este elemento debe estar presente para la respuesta que se envíen asincrónica a la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-130">This element must be present for the response to be sent asynchronous to the requested action.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-131">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="9f3c5-131">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="9f3c5-132">Indica la carpeta de destino para copiar y mover las acciones.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-132">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-133">Categories</span><span class="sxs-lookup"><span data-stu-id="9f3c5-133">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9f3c5-134">Contiene una colección de cadenas que identifican las categorías a la que pertenecen los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-134">Contains a collection of strings that identify the categories to which items in a conversation belong.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-135">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="9f3c5-135">EnableAlwaysDelete</span></span>](enablealwaysdelete.md) <br/> |<span data-ttu-id="9f3c5-136">Especifica una marca que habilita la eliminación de todos los elementos nuevos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-136">Specifies a flag that enables deletion for all new items in a conversation.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-137">Estáleído</span><span class="sxs-lookup"><span data-stu-id="9f3c5-137">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="9f3c5-138">Indica si se ha leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-138">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="9f3c5-139">DeleteType</span><span class="sxs-lookup"><span data-stu-id="9f3c5-139">DeleteType</span></span>](deletetype.md) <br/> |<span data-ttu-id="9f3c5-140">Indica cómo se eliminan los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-140">Indicates how items in a conversation are deleted.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9f3c5-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9f3c5-141">Parent elements</span></span>

|<span data-ttu-id="9f3c5-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-142">**Element**</span></span>|<span data-ttu-id="9f3c5-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f3c5-144">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="9f3c5-144">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="9f3c5-145">Contiene una colección de las conversaciones y las acciones que se debe aplicar a ellos.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-145">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9f3c5-146">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9f3c5-146">Text value</span></span>

<span data-ttu-id="9f3c5-147">**Valores de texto de elemento ConversationAction**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-147">**ConversationAction element text values**</span></span>

|<span data-ttu-id="9f3c5-148">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-148">**Value**</span></span>|<span data-ttu-id="9f3c5-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f3c5-149">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f3c5-150">AlwaysCategorize</span><span class="sxs-lookup"><span data-stu-id="9f3c5-150">AlwaysCategorize</span></span>  <br/> |<span data-ttu-id="9f3c5-151">Clasificar siempre la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-151">Always categorize the conversation.</span></span>  <br/> |
|<span data-ttu-id="9f3c5-152">AlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="9f3c5-152">AlwaysDelete</span></span>  <br/> |<span data-ttu-id="9f3c5-153">Eliminar siempre la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-153">Always delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="9f3c5-154">AlwaysMove</span><span class="sxs-lookup"><span data-stu-id="9f3c5-154">AlwaysMove</span></span>  <br/> |<span data-ttu-id="9f3c5-155">Mover siempre la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-155">Always move the conversation.</span></span>  <br/> |
|<span data-ttu-id="9f3c5-156">Eliminar</span><span class="sxs-lookup"><span data-stu-id="9f3c5-156">Delete</span></span>  <br/> |<span data-ttu-id="9f3c5-157">Eliminación de la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-157">Delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="9f3c5-158">Mover</span><span class="sxs-lookup"><span data-stu-id="9f3c5-158">Move</span></span>  <br/> |<span data-ttu-id="9f3c5-159">Mover la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-159">Move the conversation.</span></span>  <br/> |
|<span data-ttu-id="9f3c5-160">Copiar</span><span class="sxs-lookup"><span data-stu-id="9f3c5-160">Copy</span></span>  <br/> |<span data-ttu-id="9f3c5-161">Copie la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-161">Copy the conversation.</span></span>  <br/> |
|<span data-ttu-id="9f3c5-162">SetReadState</span><span class="sxs-lookup"><span data-stu-id="9f3c5-162">SetReadState</span></span>  <br/> |<span data-ttu-id="9f3c5-163">Establecer el estado de la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-163">Set the read state of the conversation.</span></span>  <br/> |
|<span data-ttu-id="9f3c5-164">SetRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9f3c5-164">SetRetentionPolicy</span></span>  <br/> |<span data-ttu-id="9f3c5-165">Establecer la directiva de retención para la conversación.</span><span class="sxs-lookup"><span data-stu-id="9f3c5-165">Set the retention policy for the conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f3c5-166">Notas</span><span class="sxs-lookup"><span data-stu-id="9f3c5-166">Remarks</span></span>

<span data-ttu-id="9f3c5-167">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9f3c5-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9f3c5-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9f3c5-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f3c5-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f3c5-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9f3c5-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9f3c5-170">Schema Name</span></span>  <br/> |<span data-ttu-id="9f3c5-171">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9f3c5-171">Types schema</span></span>  <br/> |
|<span data-ttu-id="9f3c5-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9f3c5-172">Validation File</span></span>  <br/> |<span data-ttu-id="9f3c5-173">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9f3c5-173">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9f3c5-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9f3c5-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="9f3c5-175">False</span><span class="sxs-lookup"><span data-stu-id="9f3c5-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f3c5-176">Ver también</span><span class="sxs-lookup"><span data-stu-id="9f3c5-176">See also</span></span>



[<span data-ttu-id="9f3c5-177">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="9f3c5-177">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="9f3c5-178">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9f3c5-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: El elemento FindConversation define una solicitud para buscar conversaciones en un buzón.
ms.openlocfilehash: 98d692132ed9375d981c95d24600b0e2c4b1d8c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462650"
---
# <a name="findconversation"></a><span data-ttu-id="56cc3-103">FindConversation</span><span class="sxs-lookup"><span data-stu-id="56cc3-103">FindConversation</span></span>

<span data-ttu-id="56cc3-104">El elemento **FindConversation** define una solicitud para buscar conversaciones en un buzón.</span><span class="sxs-lookup"><span data-stu-id="56cc3-104">The **FindConversation** element defines a request to find conversations in a mailbox.</span></span> 
  
[<span data-ttu-id="56cc3-105">FindConversation</span><span class="sxs-lookup"><span data-stu-id="56cc3-105">FindConversation</span></span>](findconversation.md)
  
```XML
<FindConversation Traversal="" ViewFilter="">
   <IndexedPageItemView/>
   <SeekToConditionPageItemView/>
   <SortOrder/>
   <ParentFolderId/>
   <MailboxScope/>
   <QueryString/>
   <ConversationShape/>
</FindConversation>
```

 <span data-ttu-id="56cc3-106">**FindConversationType**</span><span class="sxs-lookup"><span data-stu-id="56cc3-106">**FindConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56cc3-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="56cc3-107">Attributes and elements</span></span>

<span data-ttu-id="56cc3-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="56cc3-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56cc3-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="56cc3-109">Attributes</span></span>

****

|<span data-ttu-id="56cc3-110">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="56cc3-110">**Attribute**</span></span>|<span data-ttu-id="56cc3-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56cc3-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56cc3-112">Transversal</span><span class="sxs-lookup"><span data-stu-id="56cc3-112">Traversal</span></span>  <br/> |<span data-ttu-id="56cc3-113">Identifica los tipos de recorrido subárbol.</span><span class="sxs-lookup"><span data-stu-id="56cc3-113">Identifies the types of sub-tree traversal.</span></span> <span data-ttu-id="56cc3-114">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="56cc3-114">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="56cc3-115">ViewFilter</span><span class="sxs-lookup"><span data-stu-id="56cc3-115">ViewFilter</span></span>  <br/> |<span data-ttu-id="56cc3-116">Identifica los filtros de la vista de tipos.</span><span class="sxs-lookup"><span data-stu-id="56cc3-116">Identifies the types view filters.</span></span> <span data-ttu-id="56cc3-117">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="56cc3-117">This attribute is optional.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="56cc3-118">Valores de atributo de recorrido</span><span class="sxs-lookup"><span data-stu-id="56cc3-118">Traversal attribute values</span></span>

****

|<span data-ttu-id="56cc3-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="56cc3-119">**Value**</span></span>|<span data-ttu-id="56cc3-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56cc3-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56cc3-121">Profunda</span><span class="sxs-lookup"><span data-stu-id="56cc3-121">Shallow</span></span>  <br/> |<span data-ttu-id="56cc3-122">Indica un recorrido superficial.</span><span class="sxs-lookup"><span data-stu-id="56cc3-122">Indicates a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="56cc3-123">Gran</span><span class="sxs-lookup"><span data-stu-id="56cc3-123">Deep</span></span>  <br/> |<span data-ttu-id="56cc3-124">Indica un recorrido profundo.</span><span class="sxs-lookup"><span data-stu-id="56cc3-124">Indicates a deep traversal.</span></span>  <br/> |
   
#### <a name="viewfilter-attribute-values"></a><span data-ttu-id="56cc3-125">Valores del atributo ViewFilter</span><span class="sxs-lookup"><span data-stu-id="56cc3-125">ViewFilter attribute values</span></span>

****

|<span data-ttu-id="56cc3-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="56cc3-126">**Value**</span></span>|<span data-ttu-id="56cc3-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56cc3-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56cc3-128">Todo</span><span class="sxs-lookup"><span data-stu-id="56cc3-128">All</span></span>  <br/> |<span data-ttu-id="56cc3-129">Buscar todas las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="56cc3-129">Find all conversations.</span></span>  <br/> |
|<span data-ttu-id="56cc3-130">Marcado</span><span class="sxs-lookup"><span data-stu-id="56cc3-130">Flagged</span></span>  <br/> |<span data-ttu-id="56cc3-131">Buscar conversaciones marcadas.</span><span class="sxs-lookup"><span data-stu-id="56cc3-131">Find flagged conversations.</span></span>  <br/> |
|<span data-ttu-id="56cc3-132">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="56cc3-132">HasAttachment</span></span>  <br/> |<span data-ttu-id="56cc3-133">Buscar conversaciones con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="56cc3-133">Find conversations with attachments.</span></span>  <br/> |
|<span data-ttu-id="56cc3-134">ToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="56cc3-134">ToOrCcMe</span></span>  <br/> |<span data-ttu-id="56cc3-135">Buscar conversaciones dirigidas o CC a mí.</span><span class="sxs-lookup"><span data-stu-id="56cc3-135">Find conversations addressed or cc'd to me.</span></span>  <br/> |
|<span data-ttu-id="56cc3-136">No leídos</span><span class="sxs-lookup"><span data-stu-id="56cc3-136">Unread</span></span>  <br/> |<span data-ttu-id="56cc3-137">Buscar conversaciones no leídas.</span><span class="sxs-lookup"><span data-stu-id="56cc3-137">Find unread conversations.</span></span>  <br/> |
|<span data-ttu-id="56cc3-138">TaskActive</span><span class="sxs-lookup"><span data-stu-id="56cc3-138">TaskActive</span></span>  <br/> |<span data-ttu-id="56cc3-139">Buscar las tareas activas.</span><span class="sxs-lookup"><span data-stu-id="56cc3-139">Find active tasks.</span></span>  <br/> |
|<span data-ttu-id="56cc3-140">TaskOverdue</span><span class="sxs-lookup"><span data-stu-id="56cc3-140">TaskOverdue</span></span>  <br/> |<span data-ttu-id="56cc3-141">Buscar tareas vencidas.</span><span class="sxs-lookup"><span data-stu-id="56cc3-141">Find overdue tasks.</span></span>  <br/> |
|<span data-ttu-id="56cc3-142">TaskCompleted</span><span class="sxs-lookup"><span data-stu-id="56cc3-142">TaskCompleted</span></span>  <br/> |<span data-ttu-id="56cc3-143">Buscar las tareas completadas.</span><span class="sxs-lookup"><span data-stu-id="56cc3-143">Find completed tasks.</span></span>  <br/> |
|<span data-ttu-id="56cc3-144">Confuso</span><span class="sxs-lookup"><span data-stu-id="56cc3-144">NoClutter</span></span>  <br/> |<span data-ttu-id="56cc3-145">Únicamente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="56cc3-145">For internal use only.</span></span>  <br/> |
|<span data-ttu-id="56cc3-146">Otros correos</span><span class="sxs-lookup"><span data-stu-id="56cc3-146">Clutter</span></span>  <br/> |<span data-ttu-id="56cc3-147">Únicamente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="56cc3-147">For internal use only.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="56cc3-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56cc3-148">Child elements</span></span>

|<span data-ttu-id="56cc3-149">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="56cc3-149">**Element**</span></span>|<span data-ttu-id="56cc3-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56cc3-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56cc3-151">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="56cc3-151">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="56cc3-152">Describe cómo se devuelve la información de conversación paginada.</span><span class="sxs-lookup"><span data-stu-id="56cc3-152">Describes how paged conversation information is returned.</span></span>  <br/> |
|[<span data-ttu-id="56cc3-153">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="56cc3-153">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="56cc3-154">Especifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda de **FindItem** o **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="56cc3-154">Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span>  <br/> |
|[<span data-ttu-id="56cc3-155">SortOrder</span><span class="sxs-lookup"><span data-stu-id="56cc3-155">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="56cc3-156">Define cómo se ordenan los elementos en una solicitud de [operación FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="56cc3-156">Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request.</span></span> <span data-ttu-id="56cc3-157">La propiedad **Conversation: LastDeliveryTime** es la única propiedad que se admite para ordenar cuando se usa la operación **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="56cc3-157">The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.</span></span>  <br/> |
|[<span data-ttu-id="56cc3-158">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="56cc3-158">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="56cc3-159">Identifica la carpeta en la que buscar conversaciones.</span><span class="sxs-lookup"><span data-stu-id="56cc3-159">Identifies the folder to search for conversations.</span></span>  <br/> |
|[<span data-ttu-id="56cc3-160">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="56cc3-160">MailboxScope</span></span>](mailboxscope.md) <br/> |<span data-ttu-id="56cc3-161">Especifica si la búsqueda o recuperación de una conversación debe abarcar el buzón principal, el buzón de archivo o bien el buzón principal y el de archivo.</span><span class="sxs-lookup"><span data-stu-id="56cc3-161">Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="56cc3-162">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="56cc3-162">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="56cc3-163">Especifica una cadena de consulta de buzón basada en la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="56cc3-163">Specifies a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
|[<span data-ttu-id="56cc3-164">ConversationShape</span><span class="sxs-lookup"><span data-stu-id="56cc3-164">ConversationShape</span></span>](conversationshape.md) <br/> |<span data-ttu-id="56cc3-165">Identifica el conjunto de propiedades que se va a devolver en una respuesta de [operación FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="56cc3-165">Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="56cc3-166">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="56cc3-166">Parent elements</span></span>

<span data-ttu-id="56cc3-167">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="56cc3-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56cc3-168">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56cc3-168">Remarks</span></span>

<span data-ttu-id="56cc3-169">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="56cc3-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56cc3-170">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="56cc3-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56cc3-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="56cc3-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="56cc3-172">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="56cc3-172">Schema Name</span></span>  <br/> |<span data-ttu-id="56cc3-173">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="56cc3-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="56cc3-174">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="56cc3-174">Validation File</span></span>  <br/> |<span data-ttu-id="56cc3-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="56cc3-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="56cc3-176">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="56cc3-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="56cc3-177">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc3-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56cc3-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="56cc3-178">See also</span></span>



[<span data-ttu-id="56cc3-179">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="56cc3-179">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="56cc3-180">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="56cc3-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="56cc3-181">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="56cc3-181">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)


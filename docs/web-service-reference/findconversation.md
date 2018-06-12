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
description: El elemento FindConversation define una solicitud para buscar las conversaciones en un buzón de correo.
ms.openlocfilehash: 990e15f468f836d51977329c524acb439014da95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764613"
---
# <a name="findconversation"></a><span data-ttu-id="bdb6a-103">FindConversation</span><span class="sxs-lookup"><span data-stu-id="bdb6a-103">FindConversation</span></span>

<span data-ttu-id="bdb6a-104">El elemento **FindConversation** define una solicitud para buscar las conversaciones en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-104">The **FindConversation** element defines a request to find conversations in a mailbox.</span></span> 
  
[<span data-ttu-id="bdb6a-105">FindConversation</span><span class="sxs-lookup"><span data-stu-id="bdb6a-105">FindConversation</span></span>](findconversation.md)
  
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

 <span data-ttu-id="bdb6a-106">**FindConversationType**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-106">**FindConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bdb6a-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bdb6a-107">Attributes and elements</span></span>

<span data-ttu-id="bdb6a-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdb6a-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="bdb6a-109">Attributes</span></span>

****

|<span data-ttu-id="bdb6a-110">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-110">**Attribute**</span></span>|<span data-ttu-id="bdb6a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bdb6a-112">Cruce seguro del</span><span class="sxs-lookup"><span data-stu-id="bdb6a-112">Traversal</span></span>  <br/> |<span data-ttu-id="bdb6a-113">Identifica los tipos de cruce del subárbol.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-113">Identifies the types of sub-tree traversal.</span></span> <span data-ttu-id="bdb6a-114">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-114">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-115">DinámicaFiltrar</span><span class="sxs-lookup"><span data-stu-id="bdb6a-115">ViewFilter</span></span>  <br/> |<span data-ttu-id="bdb6a-116">Identifica los filtros de vista de tipos.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-116">Identifies the types view filters.</span></span> <span data-ttu-id="bdb6a-117">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-117">This attribute is optional.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="bdb6a-118">Valores de atributo recorrido</span><span class="sxs-lookup"><span data-stu-id="bdb6a-118">Traversal attribute values</span></span>

****

|<span data-ttu-id="bdb6a-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-119">**Value**</span></span>|<span data-ttu-id="bdb6a-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bdb6a-121">Superficial</span><span class="sxs-lookup"><span data-stu-id="bdb6a-121">Shallow</span></span>  <br/> |<span data-ttu-id="bdb6a-122">Indica un recorrido superficial.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-122">Indicates a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-123">Profunda</span><span class="sxs-lookup"><span data-stu-id="bdb6a-123">Deep</span></span>  <br/> |<span data-ttu-id="bdb6a-124">Indica un recorrido profundo.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-124">Indicates a deep traversal.</span></span>  <br/> |
   
#### <a name="viewfilter-attribute-values"></a><span data-ttu-id="bdb6a-125">Valores de atributo de dinámicaFiltrar</span><span class="sxs-lookup"><span data-stu-id="bdb6a-125">ViewFilter attribute values</span></span>

****

|<span data-ttu-id="bdb6a-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-126">**Value**</span></span>|<span data-ttu-id="bdb6a-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bdb6a-128">Todos</span><span class="sxs-lookup"><span data-stu-id="bdb6a-128">All</span></span>  <br/> |<span data-ttu-id="bdb6a-129">Buscar todas las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-129">Find all conversations.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-130">Marca</span><span class="sxs-lookup"><span data-stu-id="bdb6a-130">Flagged</span></span>  <br/> |<span data-ttu-id="bdb6a-131">Buscar conversaciones marcas.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-131">Find flagged conversations.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-132">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="bdb6a-132">HasAttachment</span></span>  <br/> |<span data-ttu-id="bdb6a-133">Buscar conversaciones con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-133">Find conversations with attachments.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-134">ToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="bdb6a-134">ToOrCcMe</span></span>  <br/> |<span data-ttu-id="bdb6a-135">Buscar conversaciones dirigidas o cc sería a mí.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-135">Find conversations addressed or cc'd to me.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-136">Unread</span><span class="sxs-lookup"><span data-stu-id="bdb6a-136">Unread</span></span>  <br/> |<span data-ttu-id="bdb6a-137">Buscar conversaciones no leídas.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-137">Find unread conversations.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-138">TaskActive</span><span class="sxs-lookup"><span data-stu-id="bdb6a-138">TaskActive</span></span>  <br/> |<span data-ttu-id="bdb6a-139">Aquí encontrará las tareas activas.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-139">Find active tasks.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-140">TaskOverdue</span><span class="sxs-lookup"><span data-stu-id="bdb6a-140">TaskOverdue</span></span>  <br/> |<span data-ttu-id="bdb6a-141">Aquí encontrará las tareas vencidas.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-141">Find overdue tasks.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-142">TaskCompleted</span><span class="sxs-lookup"><span data-stu-id="bdb6a-142">TaskCompleted</span></span>  <br/> |<span data-ttu-id="bdb6a-143">Aquí encontrará las tareas completadas.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-143">Find completed tasks.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-144">NoClutter</span><span class="sxs-lookup"><span data-stu-id="bdb6a-144">NoClutter</span></span>  <br/> |<span data-ttu-id="bdb6a-145">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-145">For internal use only.</span></span>  <br/> |
|<span data-ttu-id="bdb6a-146">Desorden</span><span class="sxs-lookup"><span data-stu-id="bdb6a-146">Clutter</span></span>  <br/> |<span data-ttu-id="bdb6a-147">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-147">For internal use only.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bdb6a-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bdb6a-148">Child elements</span></span>

|<span data-ttu-id="bdb6a-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-149">**Element**</span></span>|<span data-ttu-id="bdb6a-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdb6a-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdb6a-151">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="bdb6a-151">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="bdb6a-152">Describe cómo paginada conversación se devuelve información.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-152">Describes how paged conversation information is returned.</span></span>  <br/> |
|[<span data-ttu-id="bdb6a-153">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="bdb6a-153">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="bdb6a-154">Especifica la condición que se usa para identificar el final de una búsqueda, el índice de inicio de una búsqueda, las entradas máximas para devolver y las instrucciones de búsqueda para una búsqueda **FindItem** o **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="bdb6a-154">Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span>  <br/> |
|[<span data-ttu-id="bdb6a-155">SortOrder</span><span class="sxs-lookup"><span data-stu-id="bdb6a-155">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="bdb6a-156">Define cómo se ordenan los elementos en una solicitud de [operación FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bdb6a-156">Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request.</span></span> <span data-ttu-id="bdb6a-157">La propiedad de **Conversación: LastDeliveryTime** es la única propiedad que se admite para la ordenación cuando se usa la operación **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="bdb6a-157">The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.</span></span>  <br/> |
|[<span data-ttu-id="bdb6a-158">ID (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="bdb6a-158">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="bdb6a-159">Identifica la carpeta de búsqueda para las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-159">Identifies the folder to search for conversations.</span></span>  <br/> |
|[<span data-ttu-id="bdb6a-160">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="bdb6a-160">MailboxScope</span></span>](mailboxscope.md) <br/> |<span data-ttu-id="bdb6a-161">Especifica si debe abarcar el buzón principal, buzón de archivo o ambos la principal y archivar el buzón de correo, una búsqueda u obtención de una conversación.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-161">Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bdb6a-162">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="bdb6a-162">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="bdb6a-163">Especifica una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="bdb6a-163">Specifies a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
|[<span data-ttu-id="bdb6a-164">ConversationShape</span><span class="sxs-lookup"><span data-stu-id="bdb6a-164">ConversationShape</span></span>](conversationshape.md) <br/> |<span data-ttu-id="bdb6a-165">Identifica la propiedad establecida para devolver en una respuesta de la [operación de FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bdb6a-165">Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdb6a-166">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bdb6a-166">Parent elements</span></span>

<span data-ttu-id="bdb6a-167">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bdb6a-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdb6a-168">Remarks</span></span>

<span data-ttu-id="bdb6a-169">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="bdb6a-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdb6a-170">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bdb6a-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdb6a-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bdb6a-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bdb6a-172">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bdb6a-172">Schema Name</span></span>  <br/> |<span data-ttu-id="bdb6a-173">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bdb6a-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bdb6a-174">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bdb6a-174">Validation File</span></span>  <br/> |<span data-ttu-id="bdb6a-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bdb6a-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bdb6a-176">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bdb6a-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="bdb6a-177">False</span><span class="sxs-lookup"><span data-stu-id="bdb6a-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdb6a-178">Ver también</span><span class="sxs-lookup"><span data-stu-id="bdb6a-178">See also</span></span>



[<span data-ttu-id="bdb6a-179">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="bdb6a-179">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="bdb6a-180">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="bdb6a-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="bdb6a-181">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="bdb6a-181">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)


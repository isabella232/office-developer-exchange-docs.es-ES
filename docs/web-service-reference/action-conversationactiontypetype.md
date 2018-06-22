---
title: Acción (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: El elemento de acción contiene la acción para llevar a cabo en la conversación especificada por el elemento ConversationId.
ms.openlocfilehash: b468eeaf0c2509bfa53cbd83f497f0bae20a7f68
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763381"
---
# <a name="action-conversationactiontypetype"></a><span data-ttu-id="dce61-103">Acción (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="dce61-103">Action (ConversationActionTypeType)</span></span>

<span data-ttu-id="dce61-104">El elemento de **acción** contiene la acción para llevar a cabo en la conversación especificada por el elemento [ConversationId](conversationid.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-104">The **Action** element contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> 
  
- [<span data-ttu-id="dce61-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="dce61-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
- [<span data-ttu-id="dce61-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="dce61-106">ConversationActions</span></span>](conversationactions.md)
  
- [<span data-ttu-id="dce61-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="dce61-107">ConversationAction</span></span>](conversationaction.md)
  
- [<span data-ttu-id="dce61-108">Acción (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="dce61-108">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 <span data-ttu-id="dce61-109">**ConversationActionTypeType**</span><span class="sxs-lookup"><span data-stu-id="dce61-109">**ConversationActionTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dce61-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dce61-110">Attributes and elements</span></span>

<span data-ttu-id="dce61-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dce61-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dce61-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="dce61-112">Attributes</span></span>

<span data-ttu-id="dce61-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dce61-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dce61-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dce61-114">Child elements</span></span>

<span data-ttu-id="dce61-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dce61-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dce61-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dce61-116">Parent elements</span></span>

|<span data-ttu-id="dce61-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="dce61-117">**Element**</span></span>|<span data-ttu-id="dce61-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dce61-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dce61-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="dce61-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="dce61-120">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="dce61-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dce61-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="dce61-121">Text value</span></span>

<span data-ttu-id="dce61-122">El valor de texto del elemento **Action** indica la acción que se realizará en una conversación.</span><span class="sxs-lookup"><span data-stu-id="dce61-122">The text value of the **Action** element indicates which action will be performed on a conversation.</span></span> <span data-ttu-id="dce61-123">Los siguientes son los valores de texto posibles y las acciones correspondientes:</span><span class="sxs-lookup"><span data-stu-id="dce61-123">The following are the possible text values and the corresponding actions:</span></span> 
  
- <span data-ttu-id="dce61-124">**AlwaysCategorize** - los elementos actuales y los elementos nuevos en la conversación se establecerá automáticamente con las categorías identificadas en el elemento de [categorías](categories-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-124">**AlwaysCategorize** - The current items and new items in the conversation will automatically be set with the categories identified in the [Categories](categories-ex15websvcsotherref.md) element.</span></span> 
    
- <span data-ttu-id="dce61-125">**AlwaysDelete** - los elementos actuales y los elementos nuevos en la conversación se eliminarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="dce61-125">**AlwaysDelete** - The current items and new items in the conversation will automatically be deleted.</span></span> <span data-ttu-id="dce61-126">El modo de eliminación está establecido por el elemento [DeleteType](deletetype.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-126">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="dce61-127">**AlwaysMove** - los elementos actuales y los elementos nuevos en la conversación se moverán automáticamente a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-127">**AlwaysMove** - The current items and new items in the conversation will automatically be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> 
    
- <span data-ttu-id="dce61-128">**Eliminar** - los elementos de la conversación actuales se eliminará.</span><span class="sxs-lookup"><span data-stu-id="dce61-128">**Delete** - The current items in the conversation will be deleted.</span></span> <span data-ttu-id="dce61-129">No se eliminarán los elementos subsiguientes de la conversación.</span><span class="sxs-lookup"><span data-stu-id="dce61-129">Subsequent items in the conversation will not be deleted.</span></span> <span data-ttu-id="dce61-130">El modo de eliminación está establecido por el elemento [DeleteType](deletetype.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-130">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="dce61-131">**Mover** - los elementos actualmente en la conversación se moverán a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-131">**Move** - The current items in the conversation will be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="dce61-132">No se moverán los elementos subsiguientes de la conversación.</span><span class="sxs-lookup"><span data-stu-id="dce61-132">Subsequent items in the conversation will not be moved.</span></span> 
    
- <span data-ttu-id="dce61-133">**Copia** : los elementos de la conversación actuales se copiarán a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-133">**Copy** - The current items in the conversation will be copied to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="dce61-134">No se copiarán los elementos subsiguientes de la conversación.</span><span class="sxs-lookup"><span data-stu-id="dce61-134">Subsequent items in the conversation will not be copied.</span></span> 
    
- <span data-ttu-id="dce61-135">**SetReadState** - los elementos de la conversación actuales tendrán a su estado de lectura a establecer.</span><span class="sxs-lookup"><span data-stu-id="dce61-135">**SetReadState** - The current items in the conversation will have their read state set.</span></span> <span data-ttu-id="dce61-136">El estado de lectura está establecido por el elemento [estáleído](isread.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-136">The read state is set by the [IsRead](isread.md) element.</span></span> 
    
- <span data-ttu-id="dce61-137">**Marca** - los elementos de la conversación actuales tendrá una marca establecida como definidas por el elemento de [marca](flag.md) .</span><span class="sxs-lookup"><span data-stu-id="dce61-137">**Flag** - The current items in the conversation will have a flag set as defined by the [Flag](flag.md) element.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dce61-138">Notas</span><span class="sxs-lookup"><span data-stu-id="dce61-138">Remarks</span></span>

<span data-ttu-id="dce61-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dce61-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dce61-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dce61-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dce61-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dce61-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dce61-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dce61-142">Schema Name</span></span>  <br/> |<span data-ttu-id="dce61-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dce61-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="dce61-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dce61-144">Validation File</span></span>  <br/> |<span data-ttu-id="dce61-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dce61-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dce61-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dce61-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="dce61-147">False</span><span class="sxs-lookup"><span data-stu-id="dce61-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dce61-148">Ver también</span><span class="sxs-lookup"><span data-stu-id="dce61-148">See also</span></span>

- [<span data-ttu-id="dce61-149">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="dce61-149">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="dce61-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dce61-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


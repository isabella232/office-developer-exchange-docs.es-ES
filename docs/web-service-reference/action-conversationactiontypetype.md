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
description: El elemento Action contiene la acción que se realizará en la conversación especificada por el elemento ConversationId.
ms.openlocfilehash: f97b04b98cdc29bee9aff5fa1fc6f37400b8314c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527547"
---
# <a name="action-conversationactiontypetype"></a><span data-ttu-id="aea93-103">Acción (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="aea93-103">Action (ConversationActionTypeType)</span></span>

<span data-ttu-id="aea93-104">El elemento **Action** contiene la acción que se realizará en la conversación especificada por el elemento [ConversationId](conversationid.md) .</span><span class="sxs-lookup"><span data-stu-id="aea93-104">The **Action** element contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> 
  
- [<span data-ttu-id="aea93-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="aea93-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
- [<span data-ttu-id="aea93-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="aea93-106">ConversationActions</span></span>](conversationactions.md)
  
- [<span data-ttu-id="aea93-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="aea93-107">ConversationAction</span></span>](conversationaction.md)
  
- [<span data-ttu-id="aea93-108">Acción (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="aea93-108">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 <span data-ttu-id="aea93-109">**ConversationActionTypeType**</span><span class="sxs-lookup"><span data-stu-id="aea93-109">**ConversationActionTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aea93-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aea93-110">Attributes and elements</span></span>

<span data-ttu-id="aea93-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aea93-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aea93-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="aea93-112">Attributes</span></span>

<span data-ttu-id="aea93-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aea93-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aea93-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aea93-114">Child elements</span></span>

<span data-ttu-id="aea93-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aea93-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aea93-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aea93-116">Parent elements</span></span>

|<span data-ttu-id="aea93-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aea93-117">**Element**</span></span>|<span data-ttu-id="aea93-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aea93-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aea93-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="aea93-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="aea93-120">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="aea93-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aea93-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aea93-121">Text value</span></span>

<span data-ttu-id="aea93-122">El valor de texto del elemento **Action** indica la acción que se realizará en una conversación.</span><span class="sxs-lookup"><span data-stu-id="aea93-122">The text value of the **Action** element indicates which action will be performed on a conversation.</span></span> <span data-ttu-id="aea93-123">A continuación se muestran los valores de texto posibles y las acciones correspondientes:</span><span class="sxs-lookup"><span data-stu-id="aea93-123">The following are the possible text values and the corresponding actions:</span></span> 
  
- <span data-ttu-id="aea93-124">**AlwaysCategorize** : los elementos actuales y los nuevos elementos de la conversación se establecerán automáticamente con las categorías identificadas en el elemento [Categories](categories-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="aea93-124">**AlwaysCategorize** - The current items and new items in the conversation will automatically be set with the categories identified in the [Categories](categories-ex15websvcsotherref.md) element.</span></span> 
    
- <span data-ttu-id="aea93-125">**AlwaysDelete** : los elementos actuales y los nuevos elementos de la conversación se eliminarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="aea93-125">**AlwaysDelete** - The current items and new items in the conversation will automatically be deleted.</span></span> <span data-ttu-id="aea93-126">El elemento [DeleteType](deletetype.md) establece el modo de eliminación.</span><span class="sxs-lookup"><span data-stu-id="aea93-126">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="aea93-127">**AlwaysMove** : los elementos actuales y los nuevos elementos de la conversación se moverán automáticamente a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="aea93-127">**AlwaysMove** - The current items and new items in the conversation will automatically be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> 
    
- <span data-ttu-id="aea93-128">**Eliminar** : se eliminarán los elementos actuales de la conversación.</span><span class="sxs-lookup"><span data-stu-id="aea93-128">**Delete** - The current items in the conversation will be deleted.</span></span> <span data-ttu-id="aea93-129">Los siguientes elementos de la conversación no se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="aea93-129">Subsequent items in the conversation will not be deleted.</span></span> <span data-ttu-id="aea93-130">El elemento [DeleteType](deletetype.md) establece el modo de eliminación.</span><span class="sxs-lookup"><span data-stu-id="aea93-130">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="aea93-131">**Move** : los elementos actuales de la conversación se moverán a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="aea93-131">**Move** - The current items in the conversation will be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="aea93-132">Los siguientes elementos de la conversación no se moverán.</span><span class="sxs-lookup"><span data-stu-id="aea93-132">Subsequent items in the conversation will not be moved.</span></span> 
    
- <span data-ttu-id="aea93-133">**Copy** : los elementos actuales de la conversación se copiarán en la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="aea93-133">**Copy** - The current items in the conversation will be copied to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="aea93-134">No se copiarán los siguientes elementos de la conversación.</span><span class="sxs-lookup"><span data-stu-id="aea93-134">Subsequent items in the conversation will not be copied.</span></span> 
    
- <span data-ttu-id="aea93-135">**SetReadState** : los elementos actuales de la conversación tendrán establecido el estado de lectura.</span><span class="sxs-lookup"><span data-stu-id="aea93-135">**SetReadState** - The current items in the conversation will have their read state set.</span></span> <span data-ttu-id="aea93-136">El estado de lectura se establece mediante el elemento [IsRead](isread.md) .</span><span class="sxs-lookup"><span data-stu-id="aea93-136">The read state is set by the [IsRead](isread.md) element.</span></span> 
    
- <span data-ttu-id="aea93-137">**Marca** : los elementos actuales de la conversación tendrán un indicador establecido como definido por el elemento [Flag](flag.md) .</span><span class="sxs-lookup"><span data-stu-id="aea93-137">**Flag** - The current items in the conversation will have a flag set as defined by the [Flag](flag.md) element.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aea93-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aea93-138">Remarks</span></span>

<span data-ttu-id="aea93-139">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="aea93-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aea93-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aea93-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aea93-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="aea93-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aea93-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aea93-142">Schema Name</span></span>  <br/> |<span data-ttu-id="aea93-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="aea93-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="aea93-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aea93-144">Validation File</span></span>  <br/> |<span data-ttu-id="aea93-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="aea93-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aea93-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aea93-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="aea93-147">Falso</span><span class="sxs-lookup"><span data-stu-id="aea93-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aea93-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="aea93-148">See also</span></span>

- [<span data-ttu-id="aea93-149">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="aea93-149">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="aea93-150">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aea93-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


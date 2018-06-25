---
title: DeleteType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteType
api_type:
- schema
ms.assetid: 6e3136cd-9cb4-493a-aa85-9678f719002d
description: El elemento DeleteType indica cómo se eliminan los elementos en una conversación.
ms.openlocfilehash: abaa0c3d8b7001b2f42a38d1c82475edba32d2c5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764104"
---
# <a name="deletetype"></a><span data-ttu-id="0eca9-103">DeleteType</span><span class="sxs-lookup"><span data-stu-id="0eca9-103">DeleteType</span></span>

<span data-ttu-id="0eca9-104">El elemento **DeleteType** indica cómo se eliminan los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="0eca9-104">The **DeleteType** element indicates how items in a conversation are deleted.</span></span> 
  
- [<span data-ttu-id="0eca9-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="0eca9-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="0eca9-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="0eca9-106">ConversationActions</span></span>](conversationactions.md)  
- [<span data-ttu-id="0eca9-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="0eca9-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="0eca9-108">DeleteType</span><span class="sxs-lookup"><span data-stu-id="0eca9-108">DeleteType</span></span>](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 <span data-ttu-id="0eca9-109">**DisposalType**</span><span class="sxs-lookup"><span data-stu-id="0eca9-109">**DisposalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0eca9-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0eca9-110">Attributes and elements</span></span>

<span data-ttu-id="0eca9-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0eca9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0eca9-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="0eca9-112">Attributes</span></span>

<span data-ttu-id="0eca9-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0eca9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0eca9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0eca9-114">Child elements</span></span>

<span data-ttu-id="0eca9-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0eca9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0eca9-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0eca9-116">Parent elements</span></span>

|<span data-ttu-id="0eca9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0eca9-117">**Element**</span></span>|<span data-ttu-id="0eca9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0eca9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0eca9-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="0eca9-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="0eca9-120">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="0eca9-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0eca9-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0eca9-121">Text value</span></span>

<span data-ttu-id="0eca9-122">El valor de texto del elemento **DeleteType** indica cómo se eliminan los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="0eca9-122">The text value of the **DeleteType** element indicates how items in a conversation are deleted.</span></span> <span data-ttu-id="0eca9-123">Los siguientes son los valores de texto posibles:</span><span class="sxs-lookup"><span data-stu-id="0eca9-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="0eca9-124">HardDelete - indica que los elementos en una conversación se quitan permanentemente de la base de datos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0eca9-124">HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.</span></span>
    
- <span data-ttu-id="0eca9-125">MoveToDeleteItems - indica que se mueven los elementos en una conversación a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="0eca9-125">MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.</span></span>
    
- <span data-ttu-id="0eca9-126">SoftDelete - indica que se mueven los elementos en una conversación para el volcado de archivos si el volcado de archivos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0eca9-126">SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0eca9-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0eca9-127">Remarks</span></span>

<span data-ttu-id="0eca9-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0eca9-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0eca9-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0eca9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0eca9-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0eca9-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0eca9-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0eca9-131">Schema Name</span></span>  <br/> |<span data-ttu-id="0eca9-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0eca9-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="0eca9-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0eca9-133">Validation File</span></span>  <br/> |<span data-ttu-id="0eca9-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0eca9-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0eca9-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0eca9-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="0eca9-136">False</span><span class="sxs-lookup"><span data-stu-id="0eca9-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0eca9-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0eca9-137">See also</span></span>

- [<span data-ttu-id="0eca9-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="0eca9-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="0eca9-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0eca9-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


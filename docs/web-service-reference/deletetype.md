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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764104"
---
# <a name="deletetype"></a><span data-ttu-id="30f35-103">DeleteType</span><span class="sxs-lookup"><span data-stu-id="30f35-103">DeleteType</span></span>

<span data-ttu-id="30f35-104">El elemento **DeleteType** indica cómo se eliminan los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="30f35-104">The **DeleteType** element indicates how items in a conversation are deleted.</span></span> 
  
- [<span data-ttu-id="30f35-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="30f35-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="30f35-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="30f35-106">ConversationActions</span></span>](conversationactions.md)  
- [<span data-ttu-id="30f35-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="30f35-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="30f35-108">DeleteType</span><span class="sxs-lookup"><span data-stu-id="30f35-108">DeleteType</span></span>](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 <span data-ttu-id="30f35-109">**DisposalType**</span><span class="sxs-lookup"><span data-stu-id="30f35-109">**DisposalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30f35-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="30f35-110">Attributes and elements</span></span>

<span data-ttu-id="30f35-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="30f35-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30f35-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="30f35-112">Attributes</span></span>

<span data-ttu-id="30f35-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30f35-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30f35-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="30f35-114">Child elements</span></span>

<span data-ttu-id="30f35-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30f35-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="30f35-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="30f35-116">Parent elements</span></span>

|<span data-ttu-id="30f35-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="30f35-117">**Element**</span></span>|<span data-ttu-id="30f35-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30f35-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30f35-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="30f35-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="30f35-120">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="30f35-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="30f35-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="30f35-121">Text value</span></span>

<span data-ttu-id="30f35-122">El valor de texto del elemento **DeleteType** indica cómo se eliminan los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="30f35-122">The text value of the **DeleteType** element indicates how items in a conversation are deleted.</span></span> <span data-ttu-id="30f35-123">Los siguientes son los valores de texto posibles:</span><span class="sxs-lookup"><span data-stu-id="30f35-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="30f35-124">HardDelete - indica que los elementos en una conversación se quitan permanentemente de la base de datos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="30f35-124">HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.</span></span>
    
- <span data-ttu-id="30f35-125">MoveToDeleteItems - indica que se mueven los elementos en una conversación a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="30f35-125">MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.</span></span>
    
- <span data-ttu-id="30f35-126">SoftDelete - indica que se mueven los elementos en una conversación para el volcado de archivos si el volcado de archivos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="30f35-126">SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30f35-127">Notas</span><span class="sxs-lookup"><span data-stu-id="30f35-127">Remarks</span></span>

<span data-ttu-id="30f35-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="30f35-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30f35-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="30f35-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30f35-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30f35-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30f35-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="30f35-131">Schema Name</span></span>  <br/> |<span data-ttu-id="30f35-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="30f35-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="30f35-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="30f35-133">Validation File</span></span>  <br/> |<span data-ttu-id="30f35-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30f35-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="30f35-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="30f35-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="30f35-136">False</span><span class="sxs-lookup"><span data-stu-id="30f35-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30f35-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="30f35-137">See also</span></span>

- [<span data-ttu-id="30f35-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="30f35-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="30f35-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="30f35-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


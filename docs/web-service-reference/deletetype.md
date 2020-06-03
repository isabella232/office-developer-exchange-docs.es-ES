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
description: El elemento DeleteType indica cómo se eliminan los elementos de una conversación.
ms.openlocfilehash: 199f7afc29fe866865509d2fb90d24944113d5c0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44442636"
---
# <a name="deletetype"></a><span data-ttu-id="c1605-103">DeleteType</span><span class="sxs-lookup"><span data-stu-id="c1605-103">DeleteType</span></span>

<span data-ttu-id="c1605-104">El elemento **DeleteType** indica cómo se eliminan los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="c1605-104">The **DeleteType** element indicates how items in a conversation are deleted.</span></span> 
  
- [<span data-ttu-id="c1605-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1605-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="c1605-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="c1605-106">ConversationActions</span></span>](conversationactions.md)  
- [<span data-ttu-id="c1605-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1605-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="c1605-108">DeleteType</span><span class="sxs-lookup"><span data-stu-id="c1605-108">DeleteType</span></span>](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 <span data-ttu-id="c1605-109">**DisposalType**</span><span class="sxs-lookup"><span data-stu-id="c1605-109">**DisposalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1605-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1605-110">Attributes and elements</span></span>

<span data-ttu-id="c1605-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1605-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1605-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1605-112">Attributes</span></span>

<span data-ttu-id="c1605-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1605-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1605-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1605-114">Child elements</span></span>

<span data-ttu-id="c1605-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1605-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1605-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1605-116">Parent elements</span></span>

|<span data-ttu-id="c1605-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1605-117">**Element**</span></span>|<span data-ttu-id="c1605-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1605-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1605-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1605-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="c1605-120">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="c1605-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1605-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c1605-121">Text value</span></span>

<span data-ttu-id="c1605-122">El valor de texto del elemento **DeleteType** indica cómo se eliminan los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="c1605-122">The text value of the **DeleteType** element indicates how items in a conversation are deleted.</span></span> <span data-ttu-id="c1605-123">A continuación se muestran los valores de texto posibles:</span><span class="sxs-lookup"><span data-stu-id="c1605-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="c1605-124">HardDelete: indica que los elementos de una conversación se quitan permanentemente de la base de datos de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="c1605-124">HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.</span></span>
    
- <span data-ttu-id="c1605-125">MoveToDeleteItems: indica que los elementos de una conversación se mueven a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="c1605-125">MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.</span></span>
    
- <span data-ttu-id="c1605-126">SoftDelete: indica que los elementos de una conversación se mueven al contenedor si el contenedor está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c1605-126">SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1605-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1605-127">Remarks</span></span>

<span data-ttu-id="c1605-128">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c1605-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1605-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1605-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1605-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1605-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1605-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1605-131">Schema Name</span></span>  <br/> |<span data-ttu-id="c1605-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c1605-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1605-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1605-133">Validation File</span></span>  <br/> |<span data-ttu-id="c1605-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c1605-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1605-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1605-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1605-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c1605-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1605-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1605-137">See also</span></span>

- [<span data-ttu-id="c1605-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1605-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="c1605-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1605-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


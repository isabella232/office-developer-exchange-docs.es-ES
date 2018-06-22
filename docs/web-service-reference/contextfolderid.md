---
title: ContextFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContextFolderId
api_type:
- schema
ms.assetid: 48de92aa-e124-42b5-89bc-cdce5e93d78b
description: El elemento ContextFolderId indica la carpeta que está destinada a las acciones que utilizan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de una conversación en una carpeta de destino.
ms.openlocfilehash: bd863d0395b9b9d7b437833acfb656fec4580985
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763858"
---
# <a name="contextfolderid"></a><span data-ttu-id="21491-104">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="21491-104">ContextFolderId</span></span>

<span data-ttu-id="21491-105">El elemento **ContextFolderId** indica la carpeta que está destinada a las acciones que utilizan carpetas.</span><span class="sxs-lookup"><span data-stu-id="21491-105">The **ContextFolderId** element indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="21491-106">Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de una conversación en una carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="21491-106">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span> 
  
[<span data-ttu-id="21491-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="21491-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="21491-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="21491-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="21491-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="21491-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="21491-110">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="21491-110">ContextFolderId</span></span>](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

 <span data-ttu-id="21491-111">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="21491-111">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21491-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="21491-112">Attributes and elements</span></span>

<span data-ttu-id="21491-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="21491-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21491-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="21491-114">Attributes</span></span>

<span data-ttu-id="21491-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="21491-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21491-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="21491-116">Child elements</span></span>

|<span data-ttu-id="21491-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="21491-117">**Element**</span></span>|<span data-ttu-id="21491-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21491-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21491-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="21491-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="21491-120">Contiene el identificador y cambiar la clave de la carpeta de contexto.</span><span class="sxs-lookup"><span data-stu-id="21491-120">Contains the identifier and change key of the context folder.</span></span>  <br/> |
|[<span data-ttu-id="21491-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="21491-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="21491-122">Identifica las carpetas que se pueden hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="21491-122">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21491-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="21491-123">Parent elements</span></span>

|<span data-ttu-id="21491-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="21491-124">**Element**</span></span>|<span data-ttu-id="21491-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21491-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21491-126">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="21491-126">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="21491-127">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="21491-127">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21491-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="21491-128">Text value</span></span>

<span data-ttu-id="21491-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="21491-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21491-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21491-130">Remarks</span></span>

<span data-ttu-id="21491-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="21491-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21491-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="21491-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21491-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21491-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21491-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="21491-134">Schema Name</span></span>  <br/> |<span data-ttu-id="21491-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="21491-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="21491-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="21491-136">Validation File</span></span>  <br/> |<span data-ttu-id="21491-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21491-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21491-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="21491-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="21491-139">False</span><span class="sxs-lookup"><span data-stu-id="21491-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21491-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="21491-140">See also</span></span>



[<span data-ttu-id="21491-141">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="21491-141">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


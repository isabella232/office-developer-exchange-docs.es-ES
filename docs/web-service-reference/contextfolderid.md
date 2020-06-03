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
description: El elemento ContextFolderId indica la carpeta que está destinada a las acciones que usan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de la conversación de una carpeta de destino.
ms.openlocfilehash: 60f1eaf3b45eee83632c7da6f453a1d09f54d9fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529262"
---
# <a name="contextfolderid"></a><span data-ttu-id="cf432-104">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="cf432-104">ContextFolderId</span></span>

<span data-ttu-id="cf432-105">El elemento **ContextFolderId** indica la carpeta que está destinada a las acciones que usan carpetas.</span><span class="sxs-lookup"><span data-stu-id="cf432-105">The **ContextFolderId** element indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="cf432-106">Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de la conversación de una carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="cf432-106">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span> 
  
- [<span data-ttu-id="cf432-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="cf432-107">ApplyConversationAction</span></span>](applyconversationaction.md) 
- [<span data-ttu-id="cf432-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="cf432-108">ConversationActions</span></span>](conversationactions.md)
- [<span data-ttu-id="cf432-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="cf432-109">ConversationAction</span></span>](conversationaction.md)
- [<span data-ttu-id="cf432-110">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="cf432-110">ContextFolderId</span></span>](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

```XML
<ContextFolderId>
   <DistinguishedFolderId/>
</ContextFolderId>
```


<span data-ttu-id="cf432-111">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="cf432-111">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cf432-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cf432-112">Attributes and elements</span></span>

<span data-ttu-id="cf432-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cf432-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf432-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf432-114">Attributes</span></span>

<span data-ttu-id="cf432-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cf432-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf432-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf432-116">Child elements</span></span>

|<span data-ttu-id="cf432-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf432-117">**Element**</span></span>|<span data-ttu-id="cf432-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf432-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf432-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="cf432-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="cf432-120">Contiene el identificador y la clave de cambio de la carpeta de contexto.</span><span class="sxs-lookup"><span data-stu-id="cf432-120">Contains the identifier and change key of the context folder.</span></span>  <br/> |
|[<span data-ttu-id="cf432-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="cf432-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="cf432-122">Identifica las carpetas a las que se puede hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="cf432-122">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf432-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cf432-123">Parent elements</span></span>

|<span data-ttu-id="cf432-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf432-124">**Element**</span></span>|<span data-ttu-id="cf432-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf432-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf432-126">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="cf432-126">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="cf432-127">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="cf432-127">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cf432-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cf432-128">Text value</span></span>

<span data-ttu-id="cf432-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cf432-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf432-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf432-130">Remarks</span></span>

<span data-ttu-id="cf432-131">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cf432-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf432-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cf432-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf432-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf432-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cf432-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cf432-134">Schema Name</span></span>  <br/> |<span data-ttu-id="cf432-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cf432-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="cf432-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cf432-136">Validation File</span></span>  <br/> |<span data-ttu-id="cf432-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cf432-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cf432-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cf432-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf432-139">Falso</span><span class="sxs-lookup"><span data-stu-id="cf432-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf432-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf432-140">See also</span></span>

- [<span data-ttu-id="cf432-141">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="cf432-141">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


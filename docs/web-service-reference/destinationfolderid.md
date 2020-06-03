---
title: DestinationFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DestinationFolderId
api_type:
- schema
ms.assetid: 77d2d222-320b-4aab-88e4-934ef177f55c
description: El elemento DestinationFolderId indica la carpeta de destino para las acciones de copiar y mover.
ms.openlocfilehash: dbfd25084dbd4ea9d5f4ddf98b256d02e71139d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526917"
---
# <a name="destinationfolderid"></a><span data-ttu-id="b1213-103">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="b1213-103">DestinationFolderId</span></span>

<span data-ttu-id="b1213-104">El elemento **DestinationFolderId** indica la carpeta de destino para las acciones de copiar y mover.</span><span class="sxs-lookup"><span data-stu-id="b1213-104">The **DestinationFolderId** element indicates the destination folder for copy and move actions.</span></span> 
  
- [<span data-ttu-id="b1213-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="b1213-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="b1213-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="b1213-106">ConversationActions</span></span>](conversationactions.md) 
- [<span data-ttu-id="b1213-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="b1213-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="b1213-108">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="b1213-108">DestinationFolderId</span></span>](destinationfolderid.md)
  
```XML
<DestinationFolderId>
   <FolderId/>
</DestinationFolderId>
```

```XML
<DestinationFolderId>
   <DistinguishedFolderId/>
</DestinationFolderId>
```

<span data-ttu-id="b1213-109">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="b1213-109">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b1213-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1213-110">Attributes and elements</span></span>

<span data-ttu-id="b1213-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1213-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1213-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1213-112">Attributes</span></span>

<span data-ttu-id="b1213-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1213-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1213-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1213-114">Child elements</span></span>

|<span data-ttu-id="b1213-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b1213-115">**Element**</span></span>|<span data-ttu-id="b1213-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1213-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1213-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="b1213-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="b1213-118">Contiene el identificador y la clave de cambio de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="b1213-118">Contains the identifier and change key of the destination folder.</span></span>  <br/> |
|[<span data-ttu-id="b1213-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="b1213-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="b1213-120">Identifica las carpetas a las que se puede hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="b1213-120">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1213-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1213-121">Parent elements</span></span>

|<span data-ttu-id="b1213-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b1213-122">**Element**</span></span>|<span data-ttu-id="b1213-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1213-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1213-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="b1213-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="b1213-125">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="b1213-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b1213-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b1213-126">Text value</span></span>

<span data-ttu-id="b1213-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b1213-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1213-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1213-128">Remarks</span></span>

<span data-ttu-id="b1213-129">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b1213-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1213-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b1213-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1213-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1213-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b1213-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b1213-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b1213-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b1213-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="b1213-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b1213-134">Validation File</span></span>  <br/> |<span data-ttu-id="b1213-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b1213-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b1213-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1213-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1213-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b1213-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1213-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1213-138">See also</span></span>

- [<span data-ttu-id="b1213-139">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="b1213-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


---
title: GlobalParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f5fcbcb-05ed-462a-99cf-a6b112a4aef6
description: El elemento GlobalParentFolderIds especifica los identificadores de las carpetas primarias globales.
ms.openlocfilehash: 11c520fa0f4a1ed6d6c9d694b407e39cd036b9cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459100"
---
# <a name="globalparentfolderids"></a><span data-ttu-id="aa7a4-103">GlobalParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="aa7a4-103">GlobalParentFolderIds</span></span>

<span data-ttu-id="aa7a4-104">El elemento **GlobalParentFolderIds** especifica los identificadores de las carpetas primarias globales.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-104">The **GlobalParentFolderIds** element specifies the identifiers of the global parent folders.</span></span> 
  
```XML
<GlobalParentFolderIds>
    <FolderId/>
    <DistinguishedFolderId/>
</GlobalParentFolderIds>
```

 <span data-ttu-id="aa7a4-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa7a4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aa7a4-106">Attributes and elements</span></span>

<span data-ttu-id="aa7a4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa7a4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa7a4-108">Attributes</span></span>

<span data-ttu-id="aa7a4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa7a4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa7a4-110">Child elements</span></span>

|<span data-ttu-id="aa7a4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-111">**Element**</span></span>|<span data-ttu-id="aa7a4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa7a4-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="aa7a4-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="aa7a4-114">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="aa7a4-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="aa7a4-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="aa7a4-116">Identifica las carpetas a las que se puede hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-116">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa7a4-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aa7a4-117">Parent elements</span></span>

|<span data-ttu-id="aa7a4-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-118">**Element**</span></span>|<span data-ttu-id="aa7a4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa7a4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa7a4-120">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="aa7a4-120">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="aa7a4-121">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-121">Represents a single conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa7a4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa7a4-122">Remarks</span></span>

<span data-ttu-id="aa7a4-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="aa7a4-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa7a4-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa7a4-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aa7a4-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa7a4-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa7a4-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa7a4-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aa7a4-127">Schema Name</span></span>  <br/> |<span data-ttu-id="aa7a4-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="aa7a4-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="aa7a4-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aa7a4-129">Validation File</span></span>  <br/> |<span data-ttu-id="aa7a4-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="aa7a4-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa7a4-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aa7a4-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="aa7a4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa7a4-132">See also</span></span>



- [<span data-ttu-id="aa7a4-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa7a4-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


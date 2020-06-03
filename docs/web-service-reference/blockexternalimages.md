---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: El elemento BlockExternalImages especifica si las imágenes externas están bloqueadas en cuerpos de texto HTML.
ms.openlocfilehash: 73342316024ebe476a0e35f14157befc80edcf83
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527407"
---
# <a name="blockexternalimages"></a><span data-ttu-id="6d45b-103">BlockExternalImages</span><span class="sxs-lookup"><span data-stu-id="6d45b-103">BlockExternalImages</span></span>

<span data-ttu-id="6d45b-104">El elemento **BlockExternalImages** especifica si las imágenes externas están bloqueadas en cuerpos de texto HTML.</span><span class="sxs-lookup"><span data-stu-id="6d45b-104">The **BlockExternalImages** element specifies whether external images are blocked in HTML text bodies.</span></span> 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 <span data-ttu-id="6d45b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d45b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d45b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6d45b-106">Attributes and elements</span></span>

<span data-ttu-id="6d45b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6d45b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d45b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d45b-108">Attributes</span></span>

<span data-ttu-id="6d45b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d45b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d45b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d45b-110">Child elements</span></span>

<span data-ttu-id="6d45b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d45b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d45b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6d45b-112">Parent elements</span></span>

|<span data-ttu-id="6d45b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6d45b-113">**Element**</span></span>|<span data-ttu-id="6d45b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d45b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d45b-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6d45b-115">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="6d45b-116">Identifica las propiedades de carpeta que se incluirán en la respuesta GetFolder, FindFolder o SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="6d45b-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span>  <br/> |
|[<span data-ttu-id="6d45b-117">ItemShape</span><span class="sxs-lookup"><span data-stu-id="6d45b-117">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="6d45b-118">Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="6d45b-118">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6d45b-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6d45b-119">Text value</span></span>

<span data-ttu-id="6d45b-120">Un valor de texto de **true** para el elemento **BlockExternalImages** indica que las imágenes externas están bloqueadas en cuerpos HTML.</span><span class="sxs-lookup"><span data-stu-id="6d45b-120">A text value of **true** for **BlockExternalImages** element indicates that external images are blocked in HTML bodies.</span></span> <span data-ttu-id="6d45b-121">Un valor de **false** indica que se permiten las imágenes externas.</span><span class="sxs-lookup"><span data-stu-id="6d45b-121">A value of **false** indicates that external images are allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6d45b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d45b-122">Remarks</span></span>

<span data-ttu-id="6d45b-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d45b-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6d45b-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d45b-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d45b-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6d45b-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d45b-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d45b-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6d45b-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6d45b-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6d45b-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="6d45b-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="6d45b-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6d45b-129">Validation File</span></span>  <br/> |<span data-ttu-id="6d45b-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6d45b-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="6d45b-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6d45b-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6d45b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d45b-132">See also</span></span>



- [<span data-ttu-id="6d45b-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6d45b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


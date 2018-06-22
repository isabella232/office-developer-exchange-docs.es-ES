---
title: CopyToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyToFolder
api_type:
- schema
ms.assetid: 6fd8a6b8-d813-43ff-991b-0e9e782fe00e
description: El elemento CopyToFolder especifica el identificador de la carpeta de ese correo electrónico se pueden copiar elementos a.
ms.openlocfilehash: b641c23b7aed11ae85157e2ed01cfa9d61d07e0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763902"
---
# <a name="copytofolder"></a><span data-ttu-id="a780d-103">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="a780d-103">CopyToFolder</span></span>

<span data-ttu-id="a780d-104">El elemento **CopyToFolder** especifica el identificador de la carpeta de ese correo electrónico se pueden copiar elementos a.</span><span class="sxs-lookup"><span data-stu-id="a780d-104">The **CopyToFolder** element specifies the identifier of the folder that email items can be copied to.</span></span> 
  
```XML
<CopyToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</CopyToFolder>
```

 <span data-ttu-id="a780d-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="a780d-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a780d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a780d-106">Attributes and elements</span></span>

<span data-ttu-id="a780d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a780d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a780d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a780d-108">Attributes</span></span>

<span data-ttu-id="a780d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a780d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a780d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a780d-110">Child elements</span></span>

|<span data-ttu-id="a780d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a780d-111">**Element**</span></span>|<span data-ttu-id="a780d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a780d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a780d-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="a780d-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a780d-114">Contiene el identificador de una carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a780d-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="a780d-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a780d-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="a780d-116">Identifica una carpeta de destino con nombre para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a780d-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a780d-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a780d-117">Parent elements</span></span>

|<span data-ttu-id="a780d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a780d-118">**Element**</span></span>|<span data-ttu-id="a780d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a780d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a780d-120">Acciones</span><span class="sxs-lookup"><span data-stu-id="a780d-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="a780d-121">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="a780d-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a780d-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a780d-122">Text value</span></span>

<span data-ttu-id="a780d-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a780d-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a780d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a780d-124">Remarks</span></span>

<span data-ttu-id="a780d-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a780d-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a780d-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a780d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a780d-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a780d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a780d-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a780d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a780d-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a780d-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a780d-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a780d-130">Validation File</span></span>  <br/> |<span data-ttu-id="a780d-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a780d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a780d-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a780d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a780d-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="a780d-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a780d-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="a780d-134">See also</span></span>



[<span data-ttu-id="a780d-135">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="a780d-135">MoveToFolder</span></span>](movetofolder.md)


- [<span data-ttu-id="a780d-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a780d-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


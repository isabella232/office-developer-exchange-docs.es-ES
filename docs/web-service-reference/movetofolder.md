---
title: MoveToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveToFolder
api_type:
- schema
ms.assetid: 991673b9-b627-4848-bfba-59a187b8575f
description: El elemento MoveToFolder especifica el identificador de la carpeta a la que se pueden mover los elementos de correo electrónico.
ms.openlocfilehash: 058f008b348d49c932bf334dd3379f02d06154e9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836494"
---
# <a name="movetofolder"></a><span data-ttu-id="e0fa4-103">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="e0fa4-103">MoveToFolder</span></span>

<span data-ttu-id="e0fa4-104">El elemento **MoveToFolder** especifica el identificador de la carpeta a la que se pueden mover los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-104">The **MoveToFolder** element specifies the identifier of the folder to which email items can be moved.</span></span> 
  
```XML
<MoveToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</MoveToFolder>
```

 <span data-ttu-id="e0fa4-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="e0fa4-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0fa4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0fa4-106">Attributes and elements</span></span>

<span data-ttu-id="e0fa4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0fa4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0fa4-108">Attributes</span></span>

<span data-ttu-id="e0fa4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0fa4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0fa4-110">Child elements</span></span>

|<span data-ttu-id="e0fa4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0fa4-111">**Element**</span></span>|<span data-ttu-id="e0fa4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0fa4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0fa4-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="e0fa4-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="e0fa4-114">Contiene el identificador de una carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="e0fa4-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="e0fa4-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="e0fa4-116">Identifica una carpeta de destino con nombre para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0fa4-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0fa4-117">Parent elements</span></span>

|<span data-ttu-id="e0fa4-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0fa4-118">**Element**</span></span>|<span data-ttu-id="e0fa4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0fa4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0fa4-120">Acciones</span><span class="sxs-lookup"><span data-stu-id="e0fa4-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="e0fa4-121">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones..</span><span class="sxs-lookup"><span data-stu-id="e0fa4-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled..</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e0fa4-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e0fa4-122">Text value</span></span>

<span data-ttu-id="e0fa4-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0fa4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0fa4-124">Remarks</span></span>

<span data-ttu-id="e0fa4-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0fa4-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0fa4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0fa4-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e0fa4-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0fa4-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0fa4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e0fa4-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0fa4-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0fa4-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0fa4-130">Validation File</span></span>  <br/> |<span data-ttu-id="e0fa4-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0fa4-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0fa4-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0fa4-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0fa4-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e0fa4-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0fa4-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="e0fa4-134">See also</span></span>



[<span data-ttu-id="e0fa4-135">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="e0fa4-135">CopyToFolder</span></span>](copytofolder.md)


- [<span data-ttu-id="e0fa4-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e0fa4-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


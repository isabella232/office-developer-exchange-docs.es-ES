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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836494"
---
# <a name="movetofolder"></a><span data-ttu-id="83481-103">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="83481-103">MoveToFolder</span></span>

<span data-ttu-id="83481-104">El elemento **MoveToFolder** especifica el identificador de la carpeta a la que se pueden mover los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="83481-104">The **MoveToFolder** element specifies the identifier of the folder to which email items can be moved.</span></span> 
  
```XML
<MoveToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</MoveToFolder>
```

 <span data-ttu-id="83481-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="83481-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83481-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="83481-106">Attributes and elements</span></span>

<span data-ttu-id="83481-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="83481-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83481-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="83481-108">Attributes</span></span>

<span data-ttu-id="83481-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83481-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83481-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83481-110">Child elements</span></span>

|<span data-ttu-id="83481-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="83481-111">**Element**</span></span>|<span data-ttu-id="83481-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83481-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83481-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="83481-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="83481-114">Contiene el identificador de una carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="83481-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="83481-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="83481-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="83481-116">Identifica una carpeta de destino con nombre para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="83481-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83481-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="83481-117">Parent elements</span></span>

|<span data-ttu-id="83481-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="83481-118">**Element**</span></span>|<span data-ttu-id="83481-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83481-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83481-120">Acciones</span><span class="sxs-lookup"><span data-stu-id="83481-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="83481-121">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones..</span><span class="sxs-lookup"><span data-stu-id="83481-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled..</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83481-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="83481-122">Text value</span></span>

<span data-ttu-id="83481-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83481-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83481-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83481-124">Remarks</span></span>

<span data-ttu-id="83481-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="83481-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83481-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="83481-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83481-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83481-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="83481-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="83481-128">Schema Name</span></span>  <br/> |<span data-ttu-id="83481-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="83481-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="83481-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="83481-130">Validation File</span></span>  <br/> |<span data-ttu-id="83481-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="83481-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="83481-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="83481-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="83481-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="83481-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83481-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="83481-134">See also</span></span>



[<span data-ttu-id="83481-135">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="83481-135">CopyToFolder</span></span>](copytofolder.md)


- [<span data-ttu-id="83481-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="83481-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


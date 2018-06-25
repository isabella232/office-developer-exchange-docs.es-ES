---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: El elemento ToFolderId representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta.
ms.openlocfilehash: a48309f0b7f5c9bf667fc2eb653a0502832bc996
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840686"
---
# <a name="tofolderid"></a><span data-ttu-id="d081e-103">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="d081e-103">ToFolderId</span></span>

<span data-ttu-id="d081e-104">El elemento **ToFolderId** representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d081e-104">The **ToFolderId** element represents the destination folder for a copied or moved item or folder.</span></span> 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

 <span data-ttu-id="d081e-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="d081e-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d081e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d081e-106">Attributes and elements</span></span>

<span data-ttu-id="d081e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d081e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d081e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d081e-108">Attributes</span></span>

<span data-ttu-id="d081e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d081e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d081e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d081e-110">Child elements</span></span>

|<span data-ttu-id="d081e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d081e-111">**Element**</span></span>|<span data-ttu-id="d081e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d081e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d081e-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="d081e-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="d081e-114">Contiene el identificador de una carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d081e-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="d081e-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="d081e-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="d081e-116">Identifica una carpeta de destino con nombre para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d081e-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d081e-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d081e-117">Parent elements</span></span>

|<span data-ttu-id="d081e-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d081e-118">**Element**</span></span>|<span data-ttu-id="d081e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d081e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d081e-120">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="d081e-120">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="d081e-121">Define una solicitud para mover una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d081e-121">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="d081e-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="d081e-122">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveFolder` <br/> |
|[<span data-ttu-id="d081e-123">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d081e-123">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="d081e-124">Define una solicitud para copiar una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d081e-124">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="d081e-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="d081e-125">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyFolder` <br/> |
|[<span data-ttu-id="d081e-126">MoveItem</span><span class="sxs-lookup"><span data-stu-id="d081e-126">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="d081e-127">Define una solicitud para mover un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d081e-127">Defines a request to move an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="d081e-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="d081e-128">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="d081e-129">CopyItem</span><span class="sxs-lookup"><span data-stu-id="d081e-129">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="d081e-130">Define una solicitud para copiar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d081e-130">Defines a request to copy an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="d081e-131">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="d081e-131">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d081e-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d081e-132">Remarks</span></span>

<span data-ttu-id="d081e-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d081e-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d081e-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d081e-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d081e-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d081e-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d081e-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d081e-136">Schema Name</span></span>  <br/> |<span data-ttu-id="d081e-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d081e-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d081e-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d081e-138">Validation File</span></span>  <br/> |<span data-ttu-id="d081e-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d081e-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d081e-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d081e-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="d081e-141">False</span><span class="sxs-lookup"><span data-stu-id="d081e-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d081e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d081e-142">See also</span></span>



[<span data-ttu-id="d081e-143">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="d081e-143">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="d081e-144">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d081e-144">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="d081e-145">Operación MoveItem</span><span class="sxs-lookup"><span data-stu-id="d081e-145">MoveItem operation</span></span>](moveitem-operation.md)
  
[<span data-ttu-id="d081e-146">Operación CopyItem</span><span class="sxs-lookup"><span data-stu-id="d081e-146">CopyItem operation</span></span>](copyitem-operation.md)


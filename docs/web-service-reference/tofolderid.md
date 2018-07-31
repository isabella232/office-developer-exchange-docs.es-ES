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
ms.openlocfilehash: 9d2fd6c177711cfe3a5d3415320440259e2f5289
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353661"
---
# <a name="tofolderid"></a><span data-ttu-id="93625-103">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="93625-103">ToFolderId</span></span>

<span data-ttu-id="93625-104">El elemento **ToFolderId** representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="93625-104">The **ToFolderId** element represents the destination folder for a copied or moved item or folder.</span></span> 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

```xml
<ToFolderId>
   <DistinguishedFolderId/>
</ToFolderId>
```

<span data-ttu-id="93625-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="93625-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="93625-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="93625-106">Attributes and elements</span></span>

<span data-ttu-id="93625-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="93625-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93625-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="93625-108">Attributes</span></span>

<span data-ttu-id="93625-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="93625-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93625-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="93625-110">Child elements</span></span>

|<span data-ttu-id="93625-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="93625-111">**Element**</span></span>|<span data-ttu-id="93625-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="93625-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93625-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="93625-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="93625-114">Contiene el identificador de una carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="93625-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="93625-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="93625-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="93625-116">Identifica una carpeta de destino con nombre para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="93625-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="93625-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="93625-117">Parent elements</span></span>

|<span data-ttu-id="93625-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="93625-118">**Element**</span></span>|<span data-ttu-id="93625-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="93625-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93625-120">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="93625-120">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="93625-121">Define una solicitud para mover una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="93625-121">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="93625-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="93625-122">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveFolder` <br/> |
|[<span data-ttu-id="93625-123">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="93625-123">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="93625-124">Define una solicitud para copiar una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="93625-124">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="93625-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="93625-125">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyFolder` <br/> |
|[<span data-ttu-id="93625-126">MoveItem</span><span class="sxs-lookup"><span data-stu-id="93625-126">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="93625-127">Define una solicitud para mover un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="93625-127">Defines a request to move an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="93625-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="93625-128">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="93625-129">CopyItem</span><span class="sxs-lookup"><span data-stu-id="93625-129">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="93625-130">Define una solicitud para copiar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="93625-130">Defines a request to copy an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="93625-131">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="93625-131">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93625-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93625-132">Remarks</span></span>

<span data-ttu-id="93625-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="93625-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93625-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="93625-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93625-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93625-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="93625-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="93625-136">Schema Name</span></span>  <br/> |<span data-ttu-id="93625-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="93625-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="93625-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="93625-138">Validation File</span></span>  <br/> |<span data-ttu-id="93625-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="93625-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="93625-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="93625-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="93625-141">False</span><span class="sxs-lookup"><span data-stu-id="93625-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93625-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="93625-142">See also</span></span>

- [<span data-ttu-id="93625-143">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="93625-143">MoveFolder operation</span></span>](movefolder-operation.md)  
- [<span data-ttu-id="93625-144">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="93625-144">CopyFolder operation</span></span>](copyfolder-operation.md) 
- [<span data-ttu-id="93625-145">Operación MoveItem</span><span class="sxs-lookup"><span data-stu-id="93625-145">MoveItem operation</span></span>](moveitem-operation.md) 
- [<span data-ttu-id="93625-146">Operación CopyItem</span><span class="sxs-lookup"><span data-stu-id="93625-146">CopyItem operation</span></span>](copyitem-operation.md)


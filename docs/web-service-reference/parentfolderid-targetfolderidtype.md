---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: El elemento ID identifica la carpeta en que se crea una nueva carpeta o la carpeta que se va a buscar la operación FindConversation.
ms.openlocfilehash: 8e80b9b342274a8b2004838ebd16f8425a2d3fa3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353829"
---
# <a name="parentfolderid-targetfolderidtype"></a><span data-ttu-id="38de5-103">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="38de5-103">ParentFolderId (TargetFolderIdType)</span></span>

<span data-ttu-id="38de5-104">El elemento **ID** identifica la carpeta en que se crea una nueva carpeta o la carpeta que se va a buscar la [operación FindConversation](findconversation-operation.md).</span><span class="sxs-lookup"><span data-stu-id="38de5-104">The **ParentFolderId** element identifies the folder in which a new folder is created or the folder to search for the [FindConversation operation](findconversation-operation.md).</span></span>
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

```xml
<ParentFolderId>
   <FolderId/> 
</ParentFolderId>
```

<span data-ttu-id="38de5-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="38de5-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="38de5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="38de5-106">Attributes and elements</span></span>

<span data-ttu-id="38de5-107">El elemento **ID** contiene dos elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="38de5-107">The **ParentFolderId** element contains two child elements.</span></span> <span data-ttu-id="38de5-108">Los elementos secundarios son mutuamente excluyentes en el esquema.</span><span class="sxs-lookup"><span data-stu-id="38de5-108">The child elements are mutually exclusive in the schema.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="38de5-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="38de5-109">Attributes</span></span>

<span data-ttu-id="38de5-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38de5-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38de5-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38de5-111">Child elements</span></span>

|<span data-ttu-id="38de5-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="38de5-112">**Element**</span></span>|<span data-ttu-id="38de5-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38de5-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38de5-114">FolderId</span><span class="sxs-lookup"><span data-stu-id="38de5-114">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="38de5-115">Contiene el identificador requerido y la clave de cambio opcional de una carpeta en la que se crea una nueva carpeta o la carpeta que se va a buscar la [operación FindConversation](findconversation-operation.md).</span><span class="sxs-lookup"><span data-stu-id="38de5-115">Contains the required identifier and the optional change key of a folder in which a new folder is created or the folder that is searched for the [FindConversation operation](findconversation-operation.md).</span></span> <span data-ttu-id="38de5-116">Uso de este elemento excluye el uso del elemento [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="38de5-116">Using this element excludes the use of the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="38de5-117">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="38de5-117">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="38de5-118">Identifica las carpetas predeterminadas de Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="38de5-118">Identifies default Microsoft Exchange Server 2007 folders.</span></span> <span data-ttu-id="38de5-119">Uso de este elemento excluye el uso del elemento [FolderId](folderid.md) .</span><span class="sxs-lookup"><span data-stu-id="38de5-119">Using this element excludes the use of the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="38de5-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="38de5-120">Parent elements</span></span>

|<span data-ttu-id="38de5-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="38de5-121">**Element**</span></span>|<span data-ttu-id="38de5-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38de5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38de5-123">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="38de5-123">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="38de5-124">Define una solicitud para crear una carpeta en la base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="38de5-124">Defines a request to create a folder in the Exchange database.</span></span>  <br/> <span data-ttu-id="38de5-125">La siguiente es la expresión de XPath para este elemento:`/CreateFolder`</span><span class="sxs-lookup"><span data-stu-id="38de5-125">The following is the XPath expression to this element:  `/CreateFolder`</span></span> <br/> |
|[<span data-ttu-id="38de5-126">FindConversation</span><span class="sxs-lookup"><span data-stu-id="38de5-126">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="38de5-127">Define una solicitud para buscar las conversaciones en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="38de5-127">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="38de5-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="38de5-128">Text value</span></span>

<span data-ttu-id="38de5-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38de5-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38de5-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38de5-130">Remarks</span></span>

<span data-ttu-id="38de5-131">Los dos elementos secundarios se usan para definir la carpeta que contendrá la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="38de5-131">The two child elements are used to define the folder that will contain the new folder.</span></span> <span data-ttu-id="38de5-132">Debe seleccionar el [FolderId](folderid.md) o el elemento [DistinguishedFolderId](distinguishedfolderid.md) para identificar la carpeta principal de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="38de5-132">You must select either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element to identify the parent folder of the new folder.</span></span> <span data-ttu-id="38de5-133">No puede utilizar ambos elementos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="38de5-133">You cannot use both elements at the same time.</span></span> <span data-ttu-id="38de5-134">Este elemento es necesario crear carpetas.</span><span class="sxs-lookup"><span data-stu-id="38de5-134">This element is required to create folders.</span></span> 
  
<span data-ttu-id="38de5-135">El elemento [ID](parentfolderid.md) describe la ubicación de los elementos y las carpetas existentes.</span><span class="sxs-lookup"><span data-stu-id="38de5-135">The [ParentFolderId](parentfolderid.md) element describes the location of existing items and folders.</span></span> 
  
<span data-ttu-id="38de5-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="38de5-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38de5-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="38de5-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38de5-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38de5-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="38de5-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="38de5-139">Schema Name</span></span>  <br/> |<span data-ttu-id="38de5-140">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="38de5-140">Message schema</span></span>  <br/> |
|<span data-ttu-id="38de5-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="38de5-141">Validation File</span></span>  <br/> |<span data-ttu-id="38de5-142">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="38de5-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="38de5-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="38de5-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="38de5-144">False</span><span class="sxs-lookup"><span data-stu-id="38de5-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38de5-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="38de5-145">See also</span></span>

- [<span data-ttu-id="38de5-146">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="38de5-146">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="38de5-147">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="38de5-147">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="38de5-148">Creación de carpetas (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="38de5-148">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)


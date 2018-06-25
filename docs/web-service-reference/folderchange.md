---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: El elemento FolderChange representa una colección de los cambios que se debe realizar en una sola carpeta.
ms.openlocfilehash: 3f8b42ff4ac88eaef53d1d4ec1d61212bc14b8c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764679"
---
# <a name="folderchange"></a><span data-ttu-id="87a25-103">FolderChange</span><span class="sxs-lookup"><span data-stu-id="87a25-103">FolderChange</span></span>

<span data-ttu-id="87a25-104">El elemento **FolderChange** representa una colección de los cambios que se debe realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="87a25-104">The **FolderChange** element represents a collection of changes to be performed on a single folder.</span></span> 
  
[<span data-ttu-id="87a25-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="87a25-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="87a25-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="87a25-106">FolderChanges</span></span>](folderchanges.md)
  
[<span data-ttu-id="87a25-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="87a25-107">FolderChange</span></span>](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

 <span data-ttu-id="87a25-108">**FolderChangeType**</span><span class="sxs-lookup"><span data-stu-id="87a25-108">**FolderChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87a25-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="87a25-109">Attributes and elements</span></span>

<span data-ttu-id="87a25-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="87a25-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87a25-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="87a25-111">Attributes</span></span>

<span data-ttu-id="87a25-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="87a25-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87a25-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="87a25-113">Child elements</span></span>

|<span data-ttu-id="87a25-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="87a25-114">**Element**</span></span>|<span data-ttu-id="87a25-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87a25-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87a25-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="87a25-116">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="87a25-117">Contiene el identificador y cambiar la clave de una carpeta que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="87a25-117">Contains the identifier and change key of a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="87a25-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="87a25-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="87a25-119">Identifica las carpetas de MicrosoftExchange Server 2007 que se pueden hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="87a25-119">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
|[<span data-ttu-id="87a25-120">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="87a25-120">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="87a25-121">Define el tipo de actualización que se lleva a cabo en una carpeta que se identifica con el elemento el [FolderId](folderid.md) o [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="87a25-121">Defines the type of update that is performed on a folder that is identified by either the [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="87a25-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="87a25-122">Parent elements</span></span>

|<span data-ttu-id="87a25-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="87a25-123">**Element**</span></span>|<span data-ttu-id="87a25-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87a25-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87a25-125">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="87a25-125">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="87a25-126">Representa una colección de cambios para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="87a25-126">Represents a collection of changes for a folder.</span></span>  <br/> <span data-ttu-id="87a25-127">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="87a25-127">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87a25-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87a25-128">Remarks</span></span>

<span data-ttu-id="87a25-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="87a25-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87a25-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="87a25-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87a25-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="87a25-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="87a25-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="87a25-132">Schema name</span></span>  <br/> |<span data-ttu-id="87a25-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="87a25-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="87a25-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="87a25-134">Validation file</span></span>  <br/> |<span data-ttu-id="87a25-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="87a25-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="87a25-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="87a25-136">Can be empty</span></span>  <br/> |<span data-ttu-id="87a25-137">False</span><span class="sxs-lookup"><span data-stu-id="87a25-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87a25-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="87a25-138">See also</span></span>



[<span data-ttu-id="87a25-139">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="87a25-139">UpdateFolder operation</span></span>](updatefolder-operation.md)


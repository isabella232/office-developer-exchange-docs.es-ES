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
ms.openlocfilehash: f25defa9974f7b5dd0c683c7657983741890d45d
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354333"
---
# <a name="folderchange"></a><span data-ttu-id="318f2-103">FolderChange</span><span class="sxs-lookup"><span data-stu-id="318f2-103">FolderChange</span></span>

<span data-ttu-id="318f2-104">El elemento **FolderChange** representa una colección de los cambios que se debe realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="318f2-104">The **FolderChange** element represents a collection of changes to be performed on a single folder.</span></span> 
  
- [<span data-ttu-id="318f2-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="318f2-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="318f2-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="318f2-106">FolderChanges</span></span>](folderchanges.md) 
- [<span data-ttu-id="318f2-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="318f2-107">FolderChange</span></span>](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

```xml
<FolderChange>
   <DistinguishedFolderId/>
   <Updates/>
</FolderChange>
```

<span data-ttu-id="318f2-108">**FolderChangeType**</span><span class="sxs-lookup"><span data-stu-id="318f2-108">**FolderChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="318f2-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="318f2-109">Attributes and elements</span></span>

<span data-ttu-id="318f2-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="318f2-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="318f2-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="318f2-111">Attributes</span></span>

<span data-ttu-id="318f2-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="318f2-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="318f2-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="318f2-113">Child elements</span></span>

|<span data-ttu-id="318f2-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="318f2-114">**Element**</span></span>|<span data-ttu-id="318f2-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="318f2-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="318f2-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="318f2-116">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="318f2-117">Contiene el identificador y cambiar la clave de una carpeta que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="318f2-117">Contains the identifier and change key of a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="318f2-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="318f2-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="318f2-119">Identifica las carpetas de MicrosoftExchange Server 2007 que se pueden hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="318f2-119">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
|[<span data-ttu-id="318f2-120">Updates (Carpeta)</span><span class="sxs-lookup"><span data-stu-id="318f2-120">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="318f2-121">Define el tipo de actualización que se lleva a cabo en una carpeta que se identifica con el elemento el [FolderId](folderid.md) o [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="318f2-121">Defines the type of update that is performed on a folder that is identified by either the [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="318f2-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="318f2-122">Parent elements</span></span>

|<span data-ttu-id="318f2-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="318f2-123">**Element**</span></span>|<span data-ttu-id="318f2-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="318f2-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="318f2-125">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="318f2-125">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="318f2-126">Representa una colección de cambios para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="318f2-126">Represents a collection of changes for a folder.</span></span>  <br/> <span data-ttu-id="318f2-127">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="318f2-127">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="318f2-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="318f2-128">Remarks</span></span>

<span data-ttu-id="318f2-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="318f2-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="318f2-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="318f2-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="318f2-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="318f2-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="318f2-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="318f2-132">Schema name</span></span>  <br/> |<span data-ttu-id="318f2-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="318f2-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="318f2-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="318f2-134">Validation file</span></span>  <br/> |<span data-ttu-id="318f2-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="318f2-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="318f2-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="318f2-136">Can be empty</span></span>  <br/> |<span data-ttu-id="318f2-137">False</span><span class="sxs-lookup"><span data-stu-id="318f2-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="318f2-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="318f2-138">See also</span></span>

- [<span data-ttu-id="318f2-139">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="318f2-139">UpdateFolder operation</span></span>](updatefolder-operation.md)


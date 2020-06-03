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
description: El elemento FolderChange representa una colección de cambios que se van a realizar en una sola carpeta.
ms.openlocfilehash: e4a025bef100fdd478be545b6448b15886e47c60
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530242"
---
# <a name="folderchange"></a><span data-ttu-id="9d634-103">FolderChange</span><span class="sxs-lookup"><span data-stu-id="9d634-103">FolderChange</span></span>

<span data-ttu-id="9d634-104">El elemento **FolderChange** representa una colección de cambios que se van a realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d634-104">The **FolderChange** element represents a collection of changes to be performed on a single folder.</span></span> 
  
- [<span data-ttu-id="9d634-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="9d634-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="9d634-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="9d634-106">FolderChanges</span></span>](folderchanges.md) 
- [<span data-ttu-id="9d634-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="9d634-107">FolderChange</span></span>](folderchange.md)
  
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

<span data-ttu-id="9d634-108">**FolderChangeType**</span><span class="sxs-lookup"><span data-stu-id="9d634-108">**FolderChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9d634-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9d634-109">Attributes and elements</span></span>

<span data-ttu-id="9d634-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9d634-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d634-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d634-111">Attributes</span></span>

<span data-ttu-id="9d634-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9d634-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d634-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d634-113">Child elements</span></span>

|<span data-ttu-id="9d634-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d634-114">**Element**</span></span>|<span data-ttu-id="9d634-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d634-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d634-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="9d634-116">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="9d634-117">Contiene el identificador y la clave de cambio de una carpeta que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="9d634-117">Contains the identifier and change key of a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="9d634-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="9d634-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="9d634-119">Identifica las carpetas de MicrosoftExchange Server 2007 a las que se puede hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="9d634-119">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
|[<span data-ttu-id="9d634-120">Updates (carpeta)</span><span class="sxs-lookup"><span data-stu-id="9d634-120">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="9d634-121">Define el tipo de actualización que se realiza en una carpeta identificada por el elemento [FolderId](folderid.md) o [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="9d634-121">Defines the type of update that is performed on a folder that is identified by either the [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d634-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9d634-122">Parent elements</span></span>

|<span data-ttu-id="9d634-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d634-123">**Element**</span></span>|<span data-ttu-id="9d634-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d634-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d634-125">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="9d634-125">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="9d634-126">Representa una colección de cambios para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d634-126">Represents a collection of changes for a folder.</span></span>  <br/> <span data-ttu-id="9d634-127">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="9d634-127">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d634-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d634-128">Remarks</span></span>

<span data-ttu-id="9d634-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9d634-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d634-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9d634-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d634-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d634-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d634-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9d634-132">Schema name</span></span>  <br/> |<span data-ttu-id="9d634-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9d634-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="9d634-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9d634-134">Validation file</span></span>  <br/> |<span data-ttu-id="9d634-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9d634-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d634-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9d634-136">Can be empty</span></span>  <br/> |<span data-ttu-id="9d634-137">Falso</span><span class="sxs-lookup"><span data-stu-id="9d634-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d634-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d634-138">See also</span></span>

- [<span data-ttu-id="9d634-139">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="9d634-139">UpdateFolder operation</span></span>](updatefolder-operation.md)


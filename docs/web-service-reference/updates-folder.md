---
title: Actualizaciones (carpeta)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: El elemento de actualizaciones contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de la carpeta.
ms.openlocfilehash: 31f25b1e88fb8756f189a6d75259dd4fc198582f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840867"
---
# <a name="updates-folder"></a><span data-ttu-id="bfe93-103">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="bfe93-103">Updates (Folder)</span></span>

<span data-ttu-id="bfe93-104">El elemento de **actualizaciones** contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="bfe93-104">The **Updates** element contains a set of elements that define append, set, and delete changes to folder properties.</span></span> 
  
- [<span data-ttu-id="bfe93-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="bfe93-105">UpdateFolder</span></span>](updatefolder.md)
  
- [<span data-ttu-id="bfe93-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="bfe93-106">FolderChanges</span></span>](folderchanges.md)
  
- [<span data-ttu-id="bfe93-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="bfe93-107">FolderChange</span></span>](folderchange.md)
  
- [<span data-ttu-id="bfe93-108">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="bfe93-108">Updates (Folder)</span></span>](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

<span data-ttu-id="bfe93-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="bfe93-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bfe93-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bfe93-110">Attributes and elements</span></span>

<span data-ttu-id="bfe93-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bfe93-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfe93-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="bfe93-112">Attributes</span></span>

<span data-ttu-id="bfe93-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bfe93-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bfe93-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bfe93-114">Child elements</span></span>

|<span data-ttu-id="bfe93-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfe93-115">**Element**</span></span>|<span data-ttu-id="bfe93-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bfe93-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfe93-117">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="bfe93-117">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="bfe93-118">Representa los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="bfe93-118">Represents data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bfe93-119">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="bfe93-119">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="bfe93-120">Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="bfe93-120">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bfe93-121">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="bfe93-121">DeleteFolderField</span></span>](deletefolderfield.md) <br/> |<span data-ttu-id="bfe93-122">Representa una operación para eliminar una propiedad determinada de una carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="bfe93-122">Represents an operation to delete a given property from a folder during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bfe93-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bfe93-123">Parent elements</span></span>

|<span data-ttu-id="bfe93-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfe93-124">**Element**</span></span>|<span data-ttu-id="bfe93-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bfe93-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfe93-126">FolderChange</span><span class="sxs-lookup"><span data-stu-id="bfe93-126">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="bfe93-127">Representa una colección de los cambios que se debe realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="bfe93-127">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="bfe93-128">La siguiente es la expresión de XPath para este elemento:`/UpdateFolder/FolderChanges/FolderChange[i]`</span><span class="sxs-lookup"><span data-stu-id="bfe93-128">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfe93-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bfe93-129">Remarks</span></span>

<span data-ttu-id="bfe93-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="bfe93-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bfe93-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bfe93-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfe93-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bfe93-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bfe93-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bfe93-133">Schema Name</span></span>  <br/> |<span data-ttu-id="bfe93-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bfe93-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="bfe93-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bfe93-135">Validation File</span></span>  <br/> |<span data-ttu-id="bfe93-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bfe93-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bfe93-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bfe93-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="bfe93-138">False</span><span class="sxs-lookup"><span data-stu-id="bfe93-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfe93-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfe93-139">See also</span></span>

- [<span data-ttu-id="bfe93-140">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="bfe93-140">UpdateFolder operation</span></span>](updatefolder-operation.md)
- [<span data-ttu-id="bfe93-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="bfe93-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


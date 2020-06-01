---
title: Updates (carpeta)
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
description: El elemento updates contiene un conjunto de elementos que definen los cambios en las propiedades de la carpeta append, Set y DELETE.
ms.openlocfilehash: 3282171dfc188a9d4735a19a97e80fe0e2f79b89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457182"
---
# <a name="updates-folder"></a><span data-ttu-id="9d198-103">Updates (carpeta)</span><span class="sxs-lookup"><span data-stu-id="9d198-103">Updates (Folder)</span></span>

<span data-ttu-id="9d198-104">El elemento **updates** contiene un conjunto de elementos que definen los cambios en las propiedades de la carpeta append, Set y DELETE.</span><span class="sxs-lookup"><span data-stu-id="9d198-104">The **Updates** element contains a set of elements that define append, set, and delete changes to folder properties.</span></span> 
  
- [<span data-ttu-id="9d198-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="9d198-105">UpdateFolder</span></span>](updatefolder.md)
  
- [<span data-ttu-id="9d198-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="9d198-106">FolderChanges</span></span>](folderchanges.md)
  
- [<span data-ttu-id="9d198-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="9d198-107">FolderChange</span></span>](folderchange.md)
  
- [<span data-ttu-id="9d198-108">Updates (carpeta)</span><span class="sxs-lookup"><span data-stu-id="9d198-108">Updates (Folder)</span></span>](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

<span data-ttu-id="9d198-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="9d198-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9d198-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9d198-110">Attributes and elements</span></span>

<span data-ttu-id="9d198-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9d198-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d198-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d198-112">Attributes</span></span>

<span data-ttu-id="9d198-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9d198-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d198-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d198-114">Child elements</span></span>

|<span data-ttu-id="9d198-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d198-115">**Element**</span></span>|<span data-ttu-id="9d198-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d198-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d198-117">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="9d198-117">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="9d198-118">Representa los datos que se van a anexar a una propiedad de carpeta durante una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="9d198-118">Represents data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="9d198-119">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="9d198-119">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="9d198-120">Representa una actualización de una propiedad única de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="9d198-120">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="9d198-121">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="9d198-121">DeleteFolderField</span></span>](deletefolderfield.md) <br/> |<span data-ttu-id="9d198-122">Representa una operación para eliminar una propiedad determinada de una carpeta durante una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="9d198-122">Represents an operation to delete a given property from a folder during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d198-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9d198-123">Parent elements</span></span>

|<span data-ttu-id="9d198-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d198-124">**Element**</span></span>|<span data-ttu-id="9d198-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d198-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d198-126">FolderChange</span><span class="sxs-lookup"><span data-stu-id="9d198-126">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="9d198-127">Representa una colección de cambios que se van a realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d198-127">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="9d198-128">La siguiente es la expresión XPath a este elemento:`/UpdateFolder/FolderChanges/FolderChange[i]`</span><span class="sxs-lookup"><span data-stu-id="9d198-128">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d198-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d198-129">Remarks</span></span>

<span data-ttu-id="9d198-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9d198-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d198-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9d198-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d198-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d198-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d198-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9d198-133">Schema Name</span></span>  <br/> |<span data-ttu-id="9d198-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9d198-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="9d198-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9d198-135">Validation File</span></span>  <br/> |<span data-ttu-id="9d198-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9d198-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d198-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9d198-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d198-138">Falso</span><span class="sxs-lookup"><span data-stu-id="9d198-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d198-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d198-139">See also</span></span>

- [<span data-ttu-id="9d198-140">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="9d198-140">UpdateFolder operation</span></span>](updatefolder-operation.md)
- [<span data-ttu-id="9d198-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9d198-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


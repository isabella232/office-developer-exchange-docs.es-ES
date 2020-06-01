---
title: DeleteFolderField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderField
api_type:
- schema
ms.assetid: f9c2187b-4c60-4358-b4b4-ede50eadae48
description: El elemento DeleteFolderField representa una operación para eliminar una propiedad determinada de una carpeta durante una llamada de UpdateFolder.
ms.openlocfilehash: a0b48b667c8c8afbd5729d5deb84359a6a6ccc25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462160"
---
# <a name="deletefolderfield"></a><span data-ttu-id="29a7a-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="29a7a-103">DeleteFolderField</span></span>

<span data-ttu-id="29a7a-104">El elemento **DeleteFolderField** representa una operación para eliminar una propiedad determinada de una carpeta durante una llamada de UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="29a7a-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="29a7a-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="29a7a-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="29a7a-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="29a7a-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="29a7a-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="29a7a-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="29a7a-108">Updates (carpeta)</span><span class="sxs-lookup"><span data-stu-id="29a7a-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="29a7a-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="29a7a-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
```xml
<DeleteFolderField>
   <FieldURI/>
</DeleteFolderField>
```

```xml
<DeleteFolderField>
   <ExtendedFieldURI/>
</DeleteFolderField>
```

```xml
<DeleteFolderField>
   <IndexedFieldURI/>
</DeleteFolderField>
```

<span data-ttu-id="29a7a-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="29a7a-110">**DeleteFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="29a7a-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="29a7a-111">Attributes and elements</span></span>

<span data-ttu-id="29a7a-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="29a7a-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29a7a-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="29a7a-113">Attributes</span></span>

<span data-ttu-id="29a7a-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="29a7a-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29a7a-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="29a7a-115">Child elements</span></span>

|<span data-ttu-id="29a7a-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="29a7a-116">**Element**</span></span>|<span data-ttu-id="29a7a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="29a7a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29a7a-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="29a7a-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="29a7a-119">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="29a7a-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="29a7a-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="29a7a-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="29a7a-121">Identifica los miembros individuales de una propiedad Dictionary.</span><span class="sxs-lookup"><span data-stu-id="29a7a-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="29a7a-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="29a7a-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="29a7a-123">Identifica las propiedades de MAPI extendida.</span><span class="sxs-lookup"><span data-stu-id="29a7a-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="29a7a-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="29a7a-124">Parent elements</span></span>

|<span data-ttu-id="29a7a-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="29a7a-125">**Element**</span></span>|<span data-ttu-id="29a7a-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="29a7a-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29a7a-127">Updates (carpeta)</span><span class="sxs-lookup"><span data-stu-id="29a7a-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="29a7a-128">Contiene un conjunto de elementos que definen los cambios de anexar, establecer y eliminar en las propiedades de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="29a7a-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="29a7a-129">La siguiente es la expresión XPath a este elemento:`/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="29a7a-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29a7a-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29a7a-130">Remarks</span></span>

<span data-ttu-id="29a7a-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="29a7a-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29a7a-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="29a7a-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29a7a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="29a7a-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29a7a-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="29a7a-134">Schema Name</span></span>  <br/> |<span data-ttu-id="29a7a-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="29a7a-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="29a7a-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="29a7a-136">Validation File</span></span>  <br/> |<span data-ttu-id="29a7a-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="29a7a-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="29a7a-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="29a7a-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="29a7a-139">Falso</span><span class="sxs-lookup"><span data-stu-id="29a7a-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29a7a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="29a7a-140">See also</span></span>

- [<span data-ttu-id="29a7a-141">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="29a7a-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


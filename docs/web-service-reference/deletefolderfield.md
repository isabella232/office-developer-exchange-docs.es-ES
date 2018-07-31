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
description: El elemento DeleteFolderField representa una operación para eliminar una propiedad determinada de una carpeta durante una llamada UpdateFolder.
ms.openlocfilehash: 60d4a5c19d89c109913e83fea99c2f7910566c72
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354095"
---
# <a name="deletefolderfield"></a><span data-ttu-id="9f5ab-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="9f5ab-103">DeleteFolderField</span></span>

<span data-ttu-id="9f5ab-104">El elemento **DeleteFolderField** representa una operación para eliminar una propiedad determinada de una carpeta durante una llamada UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="9f5ab-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="9f5ab-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="9f5ab-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="9f5ab-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="9f5ab-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="9f5ab-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="9f5ab-108">Updates (Carpeta)</span><span class="sxs-lookup"><span data-stu-id="9f5ab-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="9f5ab-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="9f5ab-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
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

<span data-ttu-id="9f5ab-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-110">**DeleteFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9f5ab-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9f5ab-111">Attributes and elements</span></span>

<span data-ttu-id="9f5ab-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9f5ab-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f5ab-113">Attributes</span></span>

<span data-ttu-id="9f5ab-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9f5ab-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9f5ab-115">Child elements</span></span>

|<span data-ttu-id="9f5ab-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-116">**Element**</span></span>|<span data-ttu-id="9f5ab-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f5ab-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="9f5ab-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="9f5ab-119">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="9f5ab-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9f5ab-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="9f5ab-121">Identifica a los miembros individuales de una propiedad de diccionario.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="9f5ab-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9f5ab-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="9f5ab-123">Identifica las propiedades extendidas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9f5ab-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9f5ab-124">Parent elements</span></span>

|<span data-ttu-id="9f5ab-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-125">**Element**</span></span>|<span data-ttu-id="9f5ab-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f5ab-127">Updates (Carpeta)</span><span class="sxs-lookup"><span data-stu-id="9f5ab-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="9f5ab-128">Contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="9f5ab-129">La siguiente es la expresión de XPath para este elemento:`/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="9f5ab-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f5ab-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f5ab-130">Remarks</span></span>

<span data-ttu-id="9f5ab-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9f5ab-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9f5ab-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f5ab-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f5ab-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9f5ab-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9f5ab-134">Schema Name</span></span>  <br/> |<span data-ttu-id="9f5ab-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9f5ab-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="9f5ab-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9f5ab-136">Validation File</span></span>  <br/> |<span data-ttu-id="9f5ab-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9f5ab-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9f5ab-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9f5ab-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="9f5ab-139">False</span><span class="sxs-lookup"><span data-stu-id="9f5ab-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f5ab-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f5ab-140">See also</span></span>

- [<span data-ttu-id="9f5ab-141">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="9f5ab-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


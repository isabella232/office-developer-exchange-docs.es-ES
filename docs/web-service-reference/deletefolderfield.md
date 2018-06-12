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
ms.openlocfilehash: d0a5fb18c5f3445982a6417007ad6af9b1b365af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764092"
---
# <a name="deletefolderfield"></a><span data-ttu-id="f80cd-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="f80cd-103">DeleteFolderField</span></span>

<span data-ttu-id="f80cd-104">El elemento **DeleteFolderField** representa una operación para eliminar una propiedad determinada de una carpeta durante una llamada UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="f80cd-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="f80cd-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="f80cd-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="f80cd-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="f80cd-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="f80cd-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="f80cd-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="f80cd-108">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="f80cd-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="f80cd-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="f80cd-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
```xml
<DeleteFolderField>
   <FieldURI/>
</DeleteFolderField>
```

 <span data-ttu-id="f80cd-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="f80cd-110">**DeleteFolderFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f80cd-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f80cd-111">Attributes and elements</span></span>

<span data-ttu-id="f80cd-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f80cd-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f80cd-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="f80cd-113">Attributes</span></span>

<span data-ttu-id="f80cd-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f80cd-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f80cd-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f80cd-115">Child elements</span></span>

|<span data-ttu-id="f80cd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f80cd-116">**Element**</span></span>|<span data-ttu-id="f80cd-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f80cd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f80cd-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="f80cd-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="f80cd-119">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="f80cd-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="f80cd-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f80cd-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="f80cd-121">Identifica a los miembros individuales de una propiedad de diccionario.</span><span class="sxs-lookup"><span data-stu-id="f80cd-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="f80cd-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f80cd-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="f80cd-123">Identifica las propiedades extendidas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f80cd-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f80cd-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f80cd-124">Parent elements</span></span>

|<span data-ttu-id="f80cd-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f80cd-125">**Element**</span></span>|<span data-ttu-id="f80cd-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f80cd-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f80cd-127">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="f80cd-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="f80cd-128">Contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f80cd-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="f80cd-129">La siguiente es la expresión de XPath para este elemento:`/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="f80cd-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f80cd-130">Notas</span><span class="sxs-lookup"><span data-stu-id="f80cd-130">Remarks</span></span>

<span data-ttu-id="f80cd-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f80cd-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f80cd-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f80cd-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f80cd-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f80cd-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f80cd-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f80cd-134">Schema Name</span></span>  <br/> |<span data-ttu-id="f80cd-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f80cd-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="f80cd-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f80cd-136">Validation File</span></span>  <br/> |<span data-ttu-id="f80cd-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f80cd-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f80cd-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f80cd-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="f80cd-139">False</span><span class="sxs-lookup"><span data-stu-id="f80cd-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f80cd-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="f80cd-140">See also</span></span>

- [<span data-ttu-id="f80cd-141">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="f80cd-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


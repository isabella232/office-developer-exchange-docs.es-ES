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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764092"
---
# <a name="deletefolderfield"></a><span data-ttu-id="539a6-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="539a6-103">DeleteFolderField</span></span>

<span data-ttu-id="539a6-104">El elemento **DeleteFolderField** representa una operación para eliminar una propiedad determinada de una carpeta durante una llamada UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="539a6-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="539a6-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="539a6-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="539a6-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="539a6-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="539a6-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="539a6-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="539a6-108">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="539a6-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="539a6-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="539a6-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
```xml
<DeleteFolderField>
   <FieldURI/>
</DeleteFolderField>
```

 <span data-ttu-id="539a6-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="539a6-110">**DeleteFolderFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="539a6-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="539a6-111">Attributes and elements</span></span>

<span data-ttu-id="539a6-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="539a6-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="539a6-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="539a6-113">Attributes</span></span>

<span data-ttu-id="539a6-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="539a6-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="539a6-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="539a6-115">Child elements</span></span>

|<span data-ttu-id="539a6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="539a6-116">**Element**</span></span>|<span data-ttu-id="539a6-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="539a6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="539a6-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="539a6-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="539a6-119">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="539a6-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="539a6-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="539a6-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="539a6-121">Identifica a los miembros individuales de una propiedad de diccionario.</span><span class="sxs-lookup"><span data-stu-id="539a6-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="539a6-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="539a6-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="539a6-123">Identifica las propiedades extendidas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="539a6-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="539a6-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="539a6-124">Parent elements</span></span>

|<span data-ttu-id="539a6-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="539a6-125">**Element**</span></span>|<span data-ttu-id="539a6-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="539a6-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="539a6-127">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="539a6-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="539a6-128">Contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="539a6-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="539a6-129">La siguiente es la expresión de XPath para este elemento:`/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="539a6-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="539a6-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="539a6-130">Remarks</span></span>

<span data-ttu-id="539a6-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="539a6-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="539a6-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="539a6-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="539a6-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="539a6-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="539a6-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="539a6-134">Schema Name</span></span>  <br/> |<span data-ttu-id="539a6-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="539a6-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="539a6-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="539a6-136">Validation File</span></span>  <br/> |<span data-ttu-id="539a6-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="539a6-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="539a6-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="539a6-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="539a6-139">False</span><span class="sxs-lookup"><span data-stu-id="539a6-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="539a6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="539a6-140">See also</span></span>

- [<span data-ttu-id="539a6-141">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="539a6-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


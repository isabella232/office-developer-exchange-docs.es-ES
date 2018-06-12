---
title: SetFolderField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetFolderField
api_type:
- schema
ms.assetid: 8c69db7b-54b5-4ae2-abca-4d6e0937a790
description: El elemento SetFolderField representa una actualización que establece el valor de una propiedad única en una carpeta en una operación UpdateFolder.
ms.openlocfilehash: 1919c335197c83999875a17397e9c9d4405d1e3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837407"
---
# <a name="setfolderfield"></a><span data-ttu-id="e06fe-103">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="e06fe-103">SetFolderField</span></span>

<span data-ttu-id="e06fe-104">El elemento **SetFolderField** representa una actualización que establece el valor de una propiedad única en una carpeta en una operación UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="e06fe-104">The **SetFolderField** element represents an update that sets the value for a single property on a folder in an UpdateFolder operation.</span></span> 
  
```xml
<SetFolderField>
   <FieldURI/>
   <Folder/>
</SetFolderField>
```

 <span data-ttu-id="e06fe-105">**SetFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="e06fe-105">**SetFolderFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e06fe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e06fe-106">Attributes and elements</span></span>

<span data-ttu-id="e06fe-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e06fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e06fe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e06fe-108">Attributes</span></span>

<span data-ttu-id="e06fe-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e06fe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e06fe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e06fe-110">Child elements</span></span>

|<span data-ttu-id="e06fe-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e06fe-111">**Element**</span></span>|<span data-ttu-id="e06fe-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e06fe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e06fe-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e06fe-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="e06fe-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="e06fe-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="e06fe-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e06fe-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="e06fe-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="e06fe-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="e06fe-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e06fe-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="e06fe-118">Identifica las propiedades extendidas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e06fe-118">Identifies extended MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="e06fe-119">Folder</span><span class="sxs-lookup"><span data-stu-id="e06fe-119">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="e06fe-120">Identifica una carpeta que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="e06fe-120">Identifies a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="e06fe-121">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="e06fe-121">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="e06fe-122">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="e06fe-122">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="e06fe-123">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="e06fe-123">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="e06fe-124">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e06fe-124">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e06fe-125">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="e06fe-125">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="e06fe-126">Representa una carpeta de búsqueda que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e06fe-126">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e06fe-127">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="e06fe-127">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="e06fe-128">Representa una carpeta de tareas que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e06fe-128">Represents a Tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e06fe-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e06fe-129">Parent elements</span></span>

|<span data-ttu-id="e06fe-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="e06fe-130">**Element**</span></span>|<span data-ttu-id="e06fe-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e06fe-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e06fe-132">Actualizaciones (carpeta)</span><span class="sxs-lookup"><span data-stu-id="e06fe-132">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="e06fe-133">Contiene un conjunto de elementos que define append, establecer y eliminar los cambios realizados en las propiedades de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e06fe-133">Contains a set of elements that defines append, set, and delete changes to folder properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e06fe-134">Notas</span><span class="sxs-lookup"><span data-stu-id="e06fe-134">Remarks</span></span>

<span data-ttu-id="e06fe-135">Si la propiedad existe, el valor de la propiedad se establece en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e06fe-135">If the property exists, the property value is set to the specified value.</span></span> <span data-ttu-id="e06fe-136">Si la propiedad no existe, se crea la propiedad con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e06fe-136">If the property does not exist, the property is created with the specified value.</span></span>
  
<span data-ttu-id="e06fe-137">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e06fe-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e06fe-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e06fe-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e06fe-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e06fe-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e06fe-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e06fe-140">Schema Name</span></span>  <br/> |<span data-ttu-id="e06fe-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e06fe-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="e06fe-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e06fe-142">Validation File</span></span>  <br/> |<span data-ttu-id="e06fe-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e06fe-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e06fe-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e06fe-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="e06fe-145">False</span><span class="sxs-lookup"><span data-stu-id="e06fe-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e06fe-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="e06fe-146">See also</span></span>



[<span data-ttu-id="e06fe-147">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="e06fe-147">UpdateFolder operation</span></span>](updatefolder-operation.md)


- [<span data-ttu-id="e06fe-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e06fe-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


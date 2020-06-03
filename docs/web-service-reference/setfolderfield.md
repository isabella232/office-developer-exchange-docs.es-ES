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
description: El elemento SetFolderField representa una actualización que establece el valor de una propiedad única en una carpeta de una operación de UpdateFolder.
ms.openlocfilehash: ab75a3862801b9a7b3369d9a4116c653b461781c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530320"
---
# <a name="setfolderfield"></a><span data-ttu-id="dce25-103">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="dce25-103">SetFolderField</span></span>

<span data-ttu-id="dce25-104">El elemento **SetFolderField** representa una actualización que establece el valor de una propiedad única en una carpeta de una operación de UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="dce25-104">The **SetFolderField** element represents an update that sets the value for a single property on a folder in an UpdateFolder operation.</span></span> 

```xml
<SetFolderField>
   <FieldURI/>
   <Folder/>
</SetFolderField>
```
  
```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <SearchFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <TasksFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <SearchFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <Folder/> 
</SetFolderField>
```

```xml
<SetFolderField>
    <IndexedFieldURI/> 
    <TasksFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <SearchFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <TasksFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <Folder/>
</SetFolderField>
```

```xml
<SetFolderField>
    <FieldURI/> 
    <ContactsFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <ContactsFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <ContactsFolder/> 
</SetFolderField>
```


<span data-ttu-id="dce25-105">**SetFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="dce25-105">**SetFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dce25-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dce25-106">Attributes and elements</span></span>

<span data-ttu-id="dce25-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dce25-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dce25-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dce25-108">Attributes</span></span>

<span data-ttu-id="dce25-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dce25-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dce25-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dce25-110">Child elements</span></span>

|<span data-ttu-id="dce25-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dce25-111">**Element**</span></span>|<span data-ttu-id="dce25-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dce25-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dce25-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="dce25-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="dce25-114">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="dce25-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="dce25-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="dce25-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="dce25-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="dce25-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="dce25-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="dce25-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="dce25-118">Identifica las propiedades de MAPI extendida.</span><span class="sxs-lookup"><span data-stu-id="dce25-118">Identifies extended MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="dce25-119">Folder</span><span class="sxs-lookup"><span data-stu-id="dce25-119">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="dce25-120">Identifica una carpeta que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="dce25-120">Identifies a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="dce25-121">Hubiera</span><span class="sxs-lookup"><span data-stu-id="dce25-121">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="dce25-122">Representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="dce25-122">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="dce25-123">Hubiera</span><span class="sxs-lookup"><span data-stu-id="dce25-123">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="dce25-124">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="dce25-124">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="dce25-125">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="dce25-125">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="dce25-126">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="dce25-126">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="dce25-127">Hubiera</span><span class="sxs-lookup"><span data-stu-id="dce25-127">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="dce25-128">Representa una carpeta de tareas contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="dce25-128">Represents a Tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dce25-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dce25-129">Parent elements</span></span>

|<span data-ttu-id="dce25-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dce25-130">**Element**</span></span>|<span data-ttu-id="dce25-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dce25-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dce25-132">Updates (carpeta)</span><span class="sxs-lookup"><span data-stu-id="dce25-132">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="dce25-133">Contiene un conjunto de elementos que define los cambios de anexar, establecer y eliminar en las propiedades de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="dce25-133">Contains a set of elements that defines append, set, and delete changes to folder properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dce25-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dce25-134">Remarks</span></span>

<span data-ttu-id="dce25-135">Si la propiedad existe, el valor de la propiedad se establece en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="dce25-135">If the property exists, the property value is set to the specified value.</span></span> <span data-ttu-id="dce25-136">Si la propiedad no existe, la propiedad se crea con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="dce25-136">If the property does not exist, the property is created with the specified value.</span></span>
  
<span data-ttu-id="dce25-137">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="dce25-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dce25-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dce25-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dce25-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="dce25-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dce25-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dce25-140">Schema Name</span></span>  <br/> |<span data-ttu-id="dce25-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dce25-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="dce25-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dce25-142">Validation File</span></span>  <br/> |<span data-ttu-id="dce25-143">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="dce25-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dce25-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dce25-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="dce25-145">Falso</span><span class="sxs-lookup"><span data-stu-id="dce25-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dce25-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="dce25-146">See also</span></span>

- [<span data-ttu-id="dce25-147">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="dce25-147">UpdateFolder operation</span></span>](updatefolder-operation.md)
- [<span data-ttu-id="dce25-148">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dce25-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


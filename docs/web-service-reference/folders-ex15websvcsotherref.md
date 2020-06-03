---
title: Carpetas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: El elemento folders contiene una matriz de carpetas que se usan en las operaciones de carpeta.
ms.openlocfilehash: b087be0501f04390b80458458e7e7ccc24bf27bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530982"
---
# <a name="folders"></a><span data-ttu-id="2c883-103">Folders</span><span class="sxs-lookup"><span data-stu-id="2c883-103">Folders</span></span>

<span data-ttu-id="2c883-104">El elemento **folders** contiene una matriz de carpetas que se usan en las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c883-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

```xml
<Folders>
   <ContactsFolder/> 
</Folders>
```

```xml
<Folders>
   <TasksFolder/>
</Folders>
```

```xml
<Folders>
   <CalendarFolder/>
</Folders>
```

```xml
<Folders>
   <SearchFolder/> 
</Folders>
```

<span data-ttu-id="2c883-105">**ArrayOfFoldersType** o **NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="2c883-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2c883-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2c883-106">Attributes and elements</span></span>

<span data-ttu-id="2c883-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2c883-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c883-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2c883-108">Attributes</span></span>

<span data-ttu-id="2c883-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2c883-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c883-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c883-110">Child elements</span></span>

|<span data-ttu-id="2c883-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2c883-111">**Element**</span></span>|<span data-ttu-id="2c883-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c883-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c883-113">Folder</span><span class="sxs-lookup"><span data-stu-id="2c883-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="2c883-114">Identifica una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="2c883-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="2c883-115">Hubiera</span><span class="sxs-lookup"><span data-stu-id="2c883-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="2c883-116">Representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="2c883-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="2c883-117">Hubiera</span><span class="sxs-lookup"><span data-stu-id="2c883-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="2c883-118">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2c883-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2c883-119">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="2c883-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="2c883-120">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2c883-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2c883-121">Hubiera</span><span class="sxs-lookup"><span data-stu-id="2c883-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="2c883-122">Representa una carpeta de tareas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2c883-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c883-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2c883-123">Parent elements</span></span>

|<span data-ttu-id="2c883-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2c883-124">**Element**</span></span>|<span data-ttu-id="2c883-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c883-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c883-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c883-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="2c883-127">Contiene el estado y el resultado de una sola solicitud de [operación CopyFolder](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c883-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2c883-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="2c883-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="2c883-129">Define una solicitud para crear una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2c883-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2c883-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c883-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="2c883-131">Contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c883-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2c883-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c883-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="2c883-133">Contiene el estado y el resultado de una sola solicitud de [operación CreateManagedFolder](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c883-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2c883-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c883-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="2c883-135">Contiene el estado y el resultado de una solicitud de la [operación GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c883-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2c883-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c883-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="2c883-137">Contiene el estado y el resultado de una solicitud de [operación MoveFolder](movefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c883-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2c883-138">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="2c883-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="2c883-139">Identifica la carpeta en la que se crea una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c883-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="2c883-140">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="2c883-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="2c883-141">Contiene los resultados de la búsqueda en una única carpeta raíz durante una [operación FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="2c883-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="2c883-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c883-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="2c883-143">Contiene el estado y el resultado de una sola solicitud de [operación UpdateFolder](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c883-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c883-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c883-144">Remarks</span></span>

<span data-ttu-id="2c883-145">Este elemento es un elemento secundario necesario del elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c883-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="2c883-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2c883-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c883-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2c883-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c883-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c883-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c883-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2c883-149">Schema Name</span></span>  <br/> |<span data-ttu-id="2c883-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2c883-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c883-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2c883-151">Validation File</span></span>  <br/> |<span data-ttu-id="2c883-152">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2c883-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c883-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2c883-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c883-154">Falso</span><span class="sxs-lookup"><span data-stu-id="2c883-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c883-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c883-155">See also</span></span>

- [<span data-ttu-id="2c883-156">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="2c883-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)


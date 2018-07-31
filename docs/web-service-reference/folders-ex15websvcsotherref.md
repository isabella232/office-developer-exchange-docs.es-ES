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
description: El elemento de las carpetas contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.
ms.openlocfilehash: 34372f2480825c7a9977eeae8e730c201307f36b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353591"
---
# <a name="folders"></a><span data-ttu-id="1276f-103">Carpetas</span><span class="sxs-lookup"><span data-stu-id="1276f-103">Folders</span></span>

<span data-ttu-id="1276f-104">El elemento de **las carpetas** contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1276f-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
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

<span data-ttu-id="1276f-105">**ArrayOfFoldersType** o **NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="1276f-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1276f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1276f-106">Attributes and elements</span></span>

<span data-ttu-id="1276f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1276f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1276f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1276f-108">Attributes</span></span>

<span data-ttu-id="1276f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1276f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1276f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1276f-110">Child elements</span></span>

|<span data-ttu-id="1276f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1276f-111">**Element**</span></span>|<span data-ttu-id="1276f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1276f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1276f-113">Folder</span><span class="sxs-lookup"><span data-stu-id="1276f-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="1276f-114">Identifica una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="1276f-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="1276f-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="1276f-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="1276f-116">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="1276f-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="1276f-117">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="1276f-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="1276f-118">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1276f-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="1276f-119">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="1276f-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="1276f-120">Representa una carpeta de búsqueda incluida en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1276f-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="1276f-121">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="1276f-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="1276f-122">Representa una carpeta de tareas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1276f-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1276f-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1276f-123">Parent elements</span></span>

|<span data-ttu-id="1276f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1276f-124">**Element**</span></span>|<span data-ttu-id="1276f-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1276f-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1276f-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1276f-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="1276f-127">Contiene el estado y el resultado de una única solicitud de [operación CopyFolder](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1276f-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1276f-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1276f-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="1276f-129">Define una solicitud para crear una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1276f-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1276f-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1276f-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="1276f-131">Contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1276f-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1276f-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1276f-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="1276f-133">Contiene el estado y el resultado de una única solicitud de [operación CreateManagedFolder](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1276f-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1276f-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1276f-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="1276f-135">Contiene el estado y el resultado de una solicitud de [operación GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1276f-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1276f-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1276f-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="1276f-137">Contiene el estado y el resultado de una solicitud de [operación MoveFolder](movefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1276f-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1276f-138">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="1276f-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="1276f-139">Identifica la carpeta donde se crea una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1276f-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="1276f-140">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="1276f-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="1276f-141">Contiene los resultados de búsqueda de una sola carpeta raíz durante una [operación de FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="1276f-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1276f-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1276f-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="1276f-143">Contiene el estado y el resultado de una única solicitud de [operación UpdateFolder](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1276f-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1276f-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1276f-144">Remarks</span></span>

<span data-ttu-id="1276f-145">Este elemento es un elemento secundario necesario del elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="1276f-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="1276f-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1276f-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1276f-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1276f-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1276f-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1276f-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1276f-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1276f-149">Schema Name</span></span>  <br/> |<span data-ttu-id="1276f-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1276f-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="1276f-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1276f-151">Validation File</span></span>  <br/> |<span data-ttu-id="1276f-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1276f-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1276f-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1276f-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="1276f-154">False</span><span class="sxs-lookup"><span data-stu-id="1276f-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1276f-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="1276f-155">See also</span></span>

- [<span data-ttu-id="1276f-156">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="1276f-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)


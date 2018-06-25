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
ms.openlocfilehash: e1b9e337f633dbf6fda159c28725d3fb8dcd55a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764686"
---
# <a name="folders"></a><span data-ttu-id="99ea1-103">Carpetas</span><span class="sxs-lookup"><span data-stu-id="99ea1-103">Folders</span></span>

<span data-ttu-id="99ea1-104">El elemento de **las carpetas** contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="99ea1-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

 <span data-ttu-id="99ea1-105">**ArrayOfFoldersType** o **NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="99ea1-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99ea1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="99ea1-106">Attributes and elements</span></span>

<span data-ttu-id="99ea1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="99ea1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99ea1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="99ea1-108">Attributes</span></span>

<span data-ttu-id="99ea1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99ea1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99ea1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99ea1-110">Child elements</span></span>

|<span data-ttu-id="99ea1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="99ea1-111">**Element**</span></span>|<span data-ttu-id="99ea1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99ea1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99ea1-113">Folder</span><span class="sxs-lookup"><span data-stu-id="99ea1-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="99ea1-114">Identifica una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="99ea1-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="99ea1-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="99ea1-116">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="99ea1-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-117">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="99ea1-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="99ea1-118">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="99ea1-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-119">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="99ea1-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="99ea1-120">Representa una carpeta de búsqueda incluida en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="99ea1-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-121">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="99ea1-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="99ea1-122">Representa una carpeta de tareas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="99ea1-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99ea1-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="99ea1-123">Parent elements</span></span>

|<span data-ttu-id="99ea1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="99ea1-124">**Element**</span></span>|<span data-ttu-id="99ea1-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99ea1-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99ea1-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ea1-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="99ea1-127">Contiene el estado y el resultado de una única solicitud de [operación CopyFolder](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="99ea1-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="99ea1-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="99ea1-129">Define una solicitud para crear una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="99ea1-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ea1-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="99ea1-131">Contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="99ea1-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ea1-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="99ea1-133">Contiene el estado y el resultado de una única solicitud de [operación CreateManagedFolder](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="99ea1-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ea1-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="99ea1-135">Contiene el estado y el resultado de una solicitud de [operación GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="99ea1-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ea1-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="99ea1-137">Contiene el estado y el resultado de una solicitud de [operación MoveFolder](movefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="99ea1-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-138">ID (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="99ea1-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="99ea1-139">Identifica la carpeta donde se crea una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="99ea1-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="99ea1-140">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="99ea1-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="99ea1-141">Contiene los resultados de búsqueda de una sola carpeta raíz durante una [operación de FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="99ea1-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="99ea1-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ea1-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="99ea1-143">Contiene el estado y el resultado de una única solicitud de [operación UpdateFolder](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="99ea1-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99ea1-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99ea1-144">Remarks</span></span>

<span data-ttu-id="99ea1-145">Este elemento es un elemento secundario necesario del elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="99ea1-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="99ea1-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="99ea1-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99ea1-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="99ea1-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99ea1-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99ea1-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99ea1-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="99ea1-149">Schema Name</span></span>  <br/> |<span data-ttu-id="99ea1-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="99ea1-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="99ea1-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="99ea1-151">Validation File</span></span>  <br/> |<span data-ttu-id="99ea1-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="99ea1-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="99ea1-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="99ea1-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="99ea1-154">False</span><span class="sxs-lookup"><span data-stu-id="99ea1-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99ea1-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="99ea1-155">See also</span></span>



[<span data-ttu-id="99ea1-156">ID (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="99ea1-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)


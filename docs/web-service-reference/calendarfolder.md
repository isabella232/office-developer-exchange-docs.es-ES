---
title: CalendarFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarFolder
api_type:
- schema
ms.assetid: 48687a78-e757-4c04-9641-bf4302c6b565
description: El elemento CalendarFolder representa una carpeta que principalmente contiene los elementos del calendario.
ms.openlocfilehash: 7dc90706eb45eb4617a68b9fdcf37669921af966
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763699"
---
# <a name="calendarfolder"></a><span data-ttu-id="fc410-103">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="fc410-103">CalendarFolder</span></span>

<span data-ttu-id="fc410-104">El elemento **CalendarFolder** representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="fc410-104">The **CalendarFolder** element represents a folder that primarily contains calendar items.</span></span> 
  
```xml
<CalendarFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <EffectiveRights/>
   <SharingEffectiveRights/>
   <PermissionSet/>
</CalendarFolder>
```

 <span data-ttu-id="fc410-105">**CalendarFolderType**</span><span class="sxs-lookup"><span data-stu-id="fc410-105">**CalendarFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc410-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fc410-106">Attributes and elements</span></span>

<span data-ttu-id="fc410-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fc410-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc410-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc410-108">Attributes</span></span>

<span data-ttu-id="fc410-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fc410-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc410-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc410-110">Child elements</span></span>

|<span data-ttu-id="fc410-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc410-111">**Element**</span></span>|<span data-ttu-id="fc410-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc410-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc410-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="fc410-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="fc410-114">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc410-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="fc410-115">Id</span><span class="sxs-lookup"><span data-stu-id="fc410-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="fc410-116">Representa el identificador de la carpeta primaria que contiene la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc410-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="fc410-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="fc410-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="fc410-118">Representa la clase de carpeta para una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="fc410-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="fc410-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="fc410-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="fc410-120">Contiene el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc410-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="fc410-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="fc410-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="fc410-122">Representa el recuento total de elementos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="fc410-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="fc410-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="fc410-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="fc410-124">Representa el número de carpetas secundarias contenidas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc410-124">Represents the number of child folders that are contained within a folder.</span></span> <span data-ttu-id="fc410-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fc410-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fc410-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="fc410-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="fc410-127">Identifica las propiedades extendidas en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="fc410-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="fc410-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="fc410-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="fc410-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="fc410-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="fc410-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="fc410-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="fc410-131">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc410-131">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="fc410-132">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fc410-132">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fc410-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="fc410-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>](sharingeffectiverights-calendarpermissionreadaccesstype.md) <br/> |<span data-ttu-id="fc410-134">Indica los permisos que tiene el usuario para los datos del calendario que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="fc410-134">Indicates the permissions that the user has for the calendar data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="fc410-135">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="fc410-135">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="fc410-136">Contiene todos los permisos configurados para una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="fc410-136">Contains all the configured permissions for a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fc410-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fc410-137">Parent elements</span></span>

|<span data-ttu-id="fc410-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc410-138">**Element**</span></span>|<span data-ttu-id="fc410-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc410-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc410-140">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="fc410-140">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="fc410-141">Especifica los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fc410-141">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fc410-142">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="fc410-142">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="fc410-143">Identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="fc410-143">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fc410-144">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="fc410-144">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="fc410-145">Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fc410-145">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fc410-146">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="fc410-146">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="fc410-147">Identifica una sola carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="fc410-147">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fc410-148">Carpetas</span><span class="sxs-lookup"><span data-stu-id="fc410-148">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fc410-149">Contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc410-149">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc410-150">Notas</span><span class="sxs-lookup"><span data-stu-id="fc410-150">Remarks</span></span>

<span data-ttu-id="fc410-151">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc410-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc410-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fc410-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc410-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc410-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fc410-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fc410-154">Schema Name</span></span>  <br/> |<span data-ttu-id="fc410-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fc410-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="fc410-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fc410-156">Validation File</span></span>  <br/> |<span data-ttu-id="fc410-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fc410-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fc410-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fc410-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="fc410-159">False</span><span class="sxs-lookup"><span data-stu-id="fc410-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc410-160">Ver también</span><span class="sxs-lookup"><span data-stu-id="fc410-160">See also</span></span>



- [<span data-ttu-id="fc410-161">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fc410-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


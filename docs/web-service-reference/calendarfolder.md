---
title: Hubiera
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
description: El elemento hubiera representa una carpeta que contiene principalmente elementos de calendario.
ms.openlocfilehash: dcd0ab9d7dea1152766997de0618b3dcceed5567
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461495"
---
# <a name="calendarfolder"></a><span data-ttu-id="b9545-103">Hubiera</span><span class="sxs-lookup"><span data-stu-id="b9545-103">CalendarFolder</span></span>

<span data-ttu-id="b9545-104">El elemento **hubiera** representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="b9545-104">The **CalendarFolder** element represents a folder that primarily contains calendar items.</span></span> 
  
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

 <span data-ttu-id="b9545-105">**CalendarFolderType**</span><span class="sxs-lookup"><span data-stu-id="b9545-105">**CalendarFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9545-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b9545-106">Attributes and elements</span></span>

<span data-ttu-id="b9545-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b9545-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9545-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9545-108">Attributes</span></span>

<span data-ttu-id="b9545-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b9545-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9545-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b9545-110">Child elements</span></span>

|<span data-ttu-id="b9545-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b9545-111">**Element**</span></span>|<span data-ttu-id="b9545-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9545-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9545-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="b9545-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="b9545-114">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9545-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="b9545-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="b9545-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="b9545-116">Representa el identificador de la carpeta principal que contiene la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9545-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="b9545-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="b9545-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="b9545-118">Representa la clase de carpeta de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="b9545-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="b9545-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="b9545-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="b9545-120">Contiene el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9545-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="b9545-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="b9545-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="b9545-122">Representa el número total de elementos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="b9545-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="b9545-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="b9545-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="b9545-124">Representa el número de carpetas secundarias incluidas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9545-124">Represents the number of child folders that are contained within a folder.</span></span> <span data-ttu-id="b9545-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b9545-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b9545-126">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="b9545-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="b9545-127">Identifica las propiedades extendidas de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="b9545-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="b9545-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="b9545-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="b9545-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="b9545-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="b9545-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="b9545-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="b9545-131">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9545-131">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="b9545-132">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b9545-132">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b9545-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="b9545-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>](sharingeffectiverights-calendarpermissionreadaccesstype.md) <br/> |<span data-ttu-id="b9545-134">Indica los permisos que tiene el usuario para los datos de calendario que se están compartiendo.</span><span class="sxs-lookup"><span data-stu-id="b9545-134">Indicates the permissions that the user has for the calendar data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="b9545-135">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="b9545-135">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="b9545-136">Contiene todos los permisos configurados para una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="b9545-136">Contains all the configured permissions for a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b9545-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b9545-137">Parent elements</span></span>

|<span data-ttu-id="b9545-138">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b9545-138">**Element**</span></span>|<span data-ttu-id="b9545-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9545-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9545-140">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="b9545-140">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="b9545-141">Especifica los datos que se van a anexar a una propiedad de carpeta durante una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="b9545-141">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b9545-142">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="b9545-142">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="b9545-143">Identifica una única carpeta que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="b9545-143">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b9545-144">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="b9545-144">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="b9545-145">Representa una actualización de una propiedad única de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="b9545-145">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b9545-146">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="b9545-146">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="b9545-147">Identifica una única carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="b9545-147">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b9545-148">Folders</span><span class="sxs-lookup"><span data-stu-id="b9545-148">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b9545-149">Contiene una matriz de carpetas que se usan en las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9545-149">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9545-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9545-150">Remarks</span></span>

<span data-ttu-id="b9545-151">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b9545-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9545-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b9545-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9545-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9545-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9545-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b9545-154">Schema Name</span></span>  <br/> |<span data-ttu-id="b9545-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b9545-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9545-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b9545-156">Validation File</span></span>  <br/> |<span data-ttu-id="b9545-157">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b9545-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9545-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b9545-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9545-159">Falso</span><span class="sxs-lookup"><span data-stu-id="b9545-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9545-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9545-160">See also</span></span>



- [<span data-ttu-id="b9545-161">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b9545-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


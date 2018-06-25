---
title: ContactsFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsFolder
api_type:
- schema
ms.assetid: 6c299de8-2087-4aeb-8e66-2bc7586509a6
description: El elemento ContactsFolder representa una carpeta de contactos que se encuentra en un buzón de correo.
ms.openlocfilehash: 01302f00d84cfff9713e3b188b7799c537fc0629
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763797"
---
# <a name="contactsfolder"></a><span data-ttu-id="215f0-103">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="215f0-103">ContactsFolder</span></span>

<span data-ttu-id="215f0-104">El elemento **ContactsFolder** representa una carpeta de contactos que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="215f0-104">The **ContactsFolder** element represents a contacts folder that is contained in a mailbox.</span></span> 
  
```xml
<ContactsFolder>
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
</ContactsFolder>
```

 <span data-ttu-id="215f0-105">**ContactsFolderType**</span><span class="sxs-lookup"><span data-stu-id="215f0-105">**ContactsFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="215f0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="215f0-106">Attributes and elements</span></span>

<span data-ttu-id="215f0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="215f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="215f0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="215f0-108">Attributes</span></span>

<span data-ttu-id="215f0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="215f0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="215f0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="215f0-110">Child elements</span></span>

|<span data-ttu-id="215f0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="215f0-111">**Element**</span></span>|<span data-ttu-id="215f0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="215f0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="215f0-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="215f0-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="215f0-114">Contiene el identificador y cambiar la clave de una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="215f0-114">Contains the identifier and change key of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="215f0-115">Id</span><span class="sxs-lookup"><span data-stu-id="215f0-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="215f0-116">Representa el identificador de la carpeta primaria que contiene la carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="215f0-116">Represents the identifier of the parent folder that contains the contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="215f0-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="215f0-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="215f0-118">Representa la clase de carpeta para una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="215f0-118">Represents the folder class for a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="215f0-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="215f0-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="215f0-120">Contiene el nombre para mostrar de una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="215f0-120">Contains the display name of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="215f0-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="215f0-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="215f0-122">Representa el número total de elementos dentro de una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="215f0-122">Represents the total count of items within a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="215f0-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="215f0-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="215f0-124">Representa el número de carpetas secundarias contenidas en una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="215f0-124">Represents the number of child folders that are contained within a contacts folder.</span></span> <span data-ttu-id="215f0-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="215f0-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="215f0-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="215f0-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="215f0-127">Identifica las propiedades extendidas en las carpetas de contactos.</span><span class="sxs-lookup"><span data-stu-id="215f0-127">Identifies extended properties on contacts folders.</span></span>  <br/> |
|[<span data-ttu-id="215f0-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="215f0-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="215f0-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="215f0-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="215f0-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="215f0-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="215f0-131">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="215f0-131">Contains the client's rights based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="215f0-132">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="215f0-132">SharingEffectiveRights (PermissionReadAccessType)</span></span>](sharingeffectiverights-permissionreadaccesstype.md) <br/> |<span data-ttu-id="215f0-133">Indica los permisos que tiene el usuario para los datos de contacto que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="215f0-133">Indicates the permissions that the user has for the contact data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="215f0-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="215f0-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="215f0-135">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="215f0-135">Contains all the configured permissions for a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="215f0-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="215f0-136">Parent elements</span></span>

|<span data-ttu-id="215f0-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="215f0-137">**Element**</span></span>|<span data-ttu-id="215f0-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="215f0-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="215f0-139">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="215f0-139">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="215f0-140">Especifica los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="215f0-140">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="215f0-141">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="215f0-141">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="215f0-142">Identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="215f0-142">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="215f0-143">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="215f0-143">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="215f0-144">Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="215f0-144">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="215f0-145">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="215f0-145">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="215f0-146">Identifica una sola carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="215f0-146">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="215f0-147">Carpetas</span><span class="sxs-lookup"><span data-stu-id="215f0-147">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="215f0-148">Contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="215f0-148">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="215f0-149">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="215f0-149">Text value</span></span>

<span data-ttu-id="215f0-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="215f0-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="215f0-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="215f0-151">Remarks</span></span>

<span data-ttu-id="215f0-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="215f0-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="215f0-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="215f0-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="215f0-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="215f0-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="215f0-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="215f0-155">Schema Name</span></span>  <br/> |<span data-ttu-id="215f0-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="215f0-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="215f0-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="215f0-157">Validation File</span></span>  <br/> |<span data-ttu-id="215f0-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="215f0-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="215f0-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="215f0-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="215f0-160">False</span><span class="sxs-lookup"><span data-stu-id="215f0-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="215f0-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="215f0-161">See also</span></span>



- [<span data-ttu-id="215f0-162">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="215f0-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


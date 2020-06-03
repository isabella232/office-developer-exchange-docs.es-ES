---
title: Hubiera
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
description: El elemento hubiera representa una carpeta de contactos que está contenida en un buzón.
ms.openlocfilehash: 997b4f603198e6d05a011c4ef6bac7fe4dfbfe52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529437"
---
# <a name="contactsfolder"></a><span data-ttu-id="afcc8-103">Hubiera</span><span class="sxs-lookup"><span data-stu-id="afcc8-103">ContactsFolder</span></span>

<span data-ttu-id="afcc8-104">El elemento **hubiera** representa una carpeta de contactos que está contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="afcc8-104">The **ContactsFolder** element represents a contacts folder that is contained in a mailbox.</span></span> 
  
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

 <span data-ttu-id="afcc8-105">**ContactsFolderType**</span><span class="sxs-lookup"><span data-stu-id="afcc8-105">**ContactsFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afcc8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="afcc8-106">Attributes and elements</span></span>

<span data-ttu-id="afcc8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="afcc8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afcc8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="afcc8-108">Attributes</span></span>

<span data-ttu-id="afcc8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="afcc8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afcc8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="afcc8-110">Child elements</span></span>

|<span data-ttu-id="afcc8-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afcc8-111">**Element**</span></span>|<span data-ttu-id="afcc8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afcc8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afcc8-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="afcc8-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="afcc8-114">Contiene el identificador y la clave de cambio de una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="afcc8-114">Contains the identifier and change key of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="afcc8-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="afcc8-116">Representa el identificador de la carpeta principal que contiene la carpeta contactos.</span><span class="sxs-lookup"><span data-stu-id="afcc8-116">Represents the identifier of the parent folder that contains the contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="afcc8-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="afcc8-118">Representa la clase de carpeta de una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="afcc8-118">Represents the folder class for a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="afcc8-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="afcc8-120">Contiene el nombre para mostrar de una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="afcc8-120">Contains the display name of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="afcc8-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="afcc8-122">Representa el número total de elementos dentro de una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="afcc8-122">Represents the total count of items within a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="afcc8-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="afcc8-124">Representa el número de carpetas secundarias que contiene una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="afcc8-124">Represents the number of child folders that are contained within a contacts folder.</span></span> <span data-ttu-id="afcc8-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="afcc8-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-126">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="afcc8-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="afcc8-127">Identifica las propiedades extendidas de las carpetas de contactos.</span><span class="sxs-lookup"><span data-stu-id="afcc8-127">Identifies extended properties on contacts folders.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="afcc8-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="afcc8-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="afcc8-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="afcc8-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="afcc8-131">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="afcc8-131">Contains the client's rights based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-132">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="afcc8-132">SharingEffectiveRights (PermissionReadAccessType)</span></span>](sharingeffectiverights-permissionreadaccesstype.md) <br/> |<span data-ttu-id="afcc8-133">Indica los permisos que tiene el usuario para los datos de contacto que se están compartiendo.</span><span class="sxs-lookup"><span data-stu-id="afcc8-133">Indicates the permissions that the user has for the contact data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="afcc8-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="afcc8-135">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="afcc8-135">Contains all the configured permissions for a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afcc8-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="afcc8-136">Parent elements</span></span>

|<span data-ttu-id="afcc8-137">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afcc8-137">**Element**</span></span>|<span data-ttu-id="afcc8-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afcc8-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afcc8-139">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="afcc8-139">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="afcc8-140">Especifica los datos que se van a anexar a una propiedad de carpeta durante una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="afcc8-140">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="afcc8-141">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="afcc8-141">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="afcc8-142">Identifica una única carpeta que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="afcc8-142">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-143">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="afcc8-143">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="afcc8-144">Representa una actualización de una propiedad única de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="afcc8-144">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="afcc8-145">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="afcc8-145">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="afcc8-146">Identifica una única carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="afcc8-146">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="afcc8-147">Folders</span><span class="sxs-lookup"><span data-stu-id="afcc8-147">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="afcc8-148">Contiene una matriz de carpetas que se usan en las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="afcc8-148">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="afcc8-149">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="afcc8-149">Text value</span></span>

<span data-ttu-id="afcc8-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afcc8-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afcc8-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="afcc8-151">Remarks</span></span>

<span data-ttu-id="afcc8-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="afcc8-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afcc8-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="afcc8-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afcc8-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="afcc8-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="afcc8-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="afcc8-155">Schema Name</span></span>  <br/> |<span data-ttu-id="afcc8-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="afcc8-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="afcc8-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="afcc8-157">Validation File</span></span>  <br/> |<span data-ttu-id="afcc8-158">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="afcc8-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="afcc8-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="afcc8-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="afcc8-160">Falso</span><span class="sxs-lookup"><span data-stu-id="afcc8-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afcc8-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="afcc8-161">See also</span></span>



- [<span data-ttu-id="afcc8-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="afcc8-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


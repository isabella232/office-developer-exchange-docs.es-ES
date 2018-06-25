---
title: Carpeta
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folder
api_type:
- schema
ms.assetid: 812948d8-c7db-45ce-bb3a-77233a53a974
description: El elemento de carpeta define una carpeta para crear, obtener, buscar, sincronizar o actualizar.
ms.openlocfilehash: ecfea52d2105599372a22b78778ac0d0d066bc60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764680"
---
# <a name="folder"></a><span data-ttu-id="2bda8-103">Carpeta</span><span class="sxs-lookup"><span data-stu-id="2bda8-103">Folder</span></span>

<span data-ttu-id="2bda8-104">El elemento de **carpeta** define una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="2bda8-104">The **Folder** element defines a folder to create, get, find, synchronize, or update.</span></span> 
  
```xml
<Folder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <PermissionSet/>
      <EffectiveRights/>
</Folder>
```

 <span data-ttu-id="2bda8-105">**FolderType**</span><span class="sxs-lookup"><span data-stu-id="2bda8-105">**FolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2bda8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2bda8-106">Attributes and elements</span></span>

<span data-ttu-id="2bda8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2bda8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2bda8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2bda8-108">Attributes</span></span>

<span data-ttu-id="2bda8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2bda8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2bda8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2bda8-110">Child elements</span></span>

|<span data-ttu-id="2bda8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2bda8-111">**Element**</span></span>|<span data-ttu-id="2bda8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2bda8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2bda8-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="2bda8-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="2bda8-114">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2bda8-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-115">Id</span><span class="sxs-lookup"><span data-stu-id="2bda8-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="2bda8-116">Representa el identificador de la carpeta primaria que contiene la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2bda8-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="2bda8-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="2bda8-118">Representa la clase de carpeta para una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="2bda8-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="2bda8-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="2bda8-120">Contiene el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2bda8-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="2bda8-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="2bda8-122">Representa el recuento total de elementos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="2bda8-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="2bda8-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="2bda8-124">Representa el número de carpetas secundarias contenidas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2bda8-124">Represents the number of child folders that are contained within a folder.</span></span> <span data-ttu-id="2bda8-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2bda8-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="2bda8-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="2bda8-127">Identifica las propiedades extendidas en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="2bda8-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="2bda8-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="2bda8-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="2bda8-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="2bda8-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="2bda8-131">Representa el recuento de elementos no leídos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="2bda8-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-132">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="2bda8-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="2bda8-133">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2bda8-133">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="2bda8-134">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2bda8-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="2bda8-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="2bda8-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="2bda8-136">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2bda8-136">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="2bda8-137">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2bda8-137">This element is read-only.</span></span> <span data-ttu-id="2bda8-138">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="2bda8-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2bda8-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2bda8-139">Parent elements</span></span>

|<span data-ttu-id="2bda8-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="2bda8-140">**Element**</span></span>|<span data-ttu-id="2bda8-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2bda8-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2bda8-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="2bda8-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="2bda8-143">Especifica los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="2bda8-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="2bda8-144">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="2bda8-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="2bda8-145">Identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="2bda8-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="2bda8-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="2bda8-147">Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="2bda8-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="2bda8-148">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="2bda8-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="2bda8-149">Identifica una sola carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="2bda8-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="2bda8-150">Carpetas</span><span class="sxs-lookup"><span data-stu-id="2bda8-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2bda8-151">Contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2bda8-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bda8-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bda8-152">Remarks</span></span>

<span data-ttu-id="2bda8-153">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2bda8-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2bda8-154">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2bda8-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2bda8-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2bda8-155">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2bda8-156">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2bda8-156">Schema Name</span></span>  <br/> |<span data-ttu-id="2bda8-157">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2bda8-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="2bda8-158">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2bda8-158">Validation File</span></span>  <br/> |<span data-ttu-id="2bda8-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2bda8-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2bda8-160">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2bda8-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="2bda8-161">False</span><span class="sxs-lookup"><span data-stu-id="2bda8-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2bda8-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bda8-162">See also</span></span>



[<span data-ttu-id="2bda8-163">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="2bda8-163">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="2bda8-164">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2bda8-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


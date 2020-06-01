---
title: Hubiera
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TasksFolder
api_type:
- schema
ms.assetid: 5a9a4612-8064-4986-b467-c44f268c64df
description: El elemento hubiera representa una carpeta tareas que está contenida en un buzón.
ms.openlocfilehash: 522fe485482bd8159927f9925b7a5582ba2e1c22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465341"
---
# <a name="tasksfolder"></a><span data-ttu-id="de812-103">Hubiera</span><span class="sxs-lookup"><span data-stu-id="de812-103">TasksFolder</span></span>

<span data-ttu-id="de812-104">El elemento **hubiera** representa una carpeta tareas que está contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="de812-104">The **TasksFolder** element represents a Tasks folder that is contained in a mailbox.</span></span> 
  
```xml
<TasksFolder>
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
</TasksFolder>
```

<span data-ttu-id="de812-105">**TasksFolderType**</span><span class="sxs-lookup"><span data-stu-id="de812-105">**TasksFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="de812-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de812-106">Attributes and elements</span></span>

<span data-ttu-id="de812-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de812-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de812-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="de812-108">Attributes</span></span>

<span data-ttu-id="de812-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="de812-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de812-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de812-110">Child elements</span></span>

|<span data-ttu-id="de812-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de812-111">**Element**</span></span>|<span data-ttu-id="de812-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de812-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de812-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="de812-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="de812-114">Contiene el identificador y la clave de cambio de una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="de812-114">Contains the identifier and change key of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="de812-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="de812-116">Representa el identificador de la carpeta principal que contiene la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="de812-116">Represents the identifier of the parent folder that contains the Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="de812-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="de812-118">Representa la clase de carpeta de una carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="de812-118">Represents the folder class for a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="de812-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="de812-120">Contiene el nombre para mostrar de una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="de812-120">Contains the display name of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="de812-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="de812-122">Representa el número total de elementos dentro de una carpeta Tasks.</span><span class="sxs-lookup"><span data-stu-id="de812-122">Represents the total count of items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="de812-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="de812-124">Representa el número de carpetas secundarias que contiene una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="de812-124">Represents the number of child folders that are contained within a Tasks folder.</span></span> <span data-ttu-id="de812-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="de812-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="de812-126">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="de812-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="de812-127">Identifica las propiedades extendidas de una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="de812-127">Identifies extended properties on a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="de812-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="de812-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="de812-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="de812-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="de812-131">Representa el número de elementos no leídos dentro de una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="de812-131">Represents the count of unread items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="de812-132">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="de812-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="de812-133">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="de812-133">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="de812-134">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="de812-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="de812-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="de812-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="de812-136">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="de812-136">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="de812-137">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="de812-137">This element is read-only.</span></span> <span data-ttu-id="de812-138">Este elemento se introdujo en Microsoft Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="de812-138">This element was introduced in Microsoft Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de812-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de812-139">Parent elements</span></span>

|<span data-ttu-id="de812-140">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de812-140">**Element**</span></span>|<span data-ttu-id="de812-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de812-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de812-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="de812-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="de812-143">Especifica los datos que se van a anexar a una propiedad de carpeta durante una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="de812-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="de812-144">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="de812-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="de812-145">Identifica una única carpeta que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="de812-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="de812-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="de812-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="de812-147">Representa una actualización de una propiedad única de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="de812-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="de812-148">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="de812-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="de812-149">Identifica una única carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="de812-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="de812-150">Folders</span><span class="sxs-lookup"><span data-stu-id="de812-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="de812-151">Contiene una matriz de carpetas que se usan en las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="de812-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de812-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de812-152">Remarks</span></span>

<span data-ttu-id="de812-153">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="de812-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de812-154">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de812-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de812-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="de812-155">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de812-156">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de812-156">Schema Name</span></span>  <br/> |<span data-ttu-id="de812-157">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="de812-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="de812-158">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de812-158">Validation File</span></span>  <br/> |<span data-ttu-id="de812-159">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="de812-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de812-160">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de812-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="de812-161">Falso</span><span class="sxs-lookup"><span data-stu-id="de812-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de812-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="de812-162">See also</span></span>

- [<span data-ttu-id="de812-163">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="de812-163">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


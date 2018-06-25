---
title: TasksFolder
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
description: El elemento TasksFolder representa una carpeta de tareas que se encuentra en un buzón de correo.
ms.openlocfilehash: b2151c68519a6ff15fbc74b48fc93a7e06af9e76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840626"
---
# <a name="tasksfolder"></a><span data-ttu-id="a53e4-103">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="a53e4-103">TasksFolder</span></span>

<span data-ttu-id="a53e4-104">El elemento **TasksFolder** representa una carpeta de tareas que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a53e4-104">The **TasksFolder** element represents a Tasks folder that is contained in a mailbox.</span></span> 
  
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

<span data-ttu-id="a53e4-105">**TasksFolderType**</span><span class="sxs-lookup"><span data-stu-id="a53e4-105">**TasksFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a53e4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a53e4-106">Attributes and elements</span></span>

<span data-ttu-id="a53e4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a53e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a53e4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a53e4-108">Attributes</span></span>

<span data-ttu-id="a53e4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a53e4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a53e4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a53e4-110">Child elements</span></span>

|<span data-ttu-id="a53e4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a53e4-111">**Element**</span></span>|<span data-ttu-id="a53e4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a53e4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a53e4-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="a53e4-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a53e4-114">Contiene el identificador y cambiar la clave de una carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-114">Contains the identifier and change key of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-115">Id</span><span class="sxs-lookup"><span data-stu-id="a53e4-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="a53e4-116">Representa el identificador de la carpeta primaria que contiene la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-116">Represents the identifier of the parent folder that contains the Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="a53e4-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="a53e4-118">Representa la clase de carpeta para una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-118">Represents the folder class for a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="a53e4-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="a53e4-120">Contiene el nombre para mostrar de una carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-120">Contains the display name of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="a53e4-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="a53e4-122">Representa el recuento total de elementos dentro de una carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-122">Represents the total count of items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="a53e4-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="a53e4-124">Representa el número de carpetas secundarias contenidas en una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-124">Represents the number of child folders that are contained within a Tasks folder.</span></span> <span data-ttu-id="a53e4-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a53e4-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a53e4-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="a53e4-127">Identifica las propiedades extendidas en una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-127">Identifies extended properties on a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="a53e4-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="a53e4-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a53e4-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="a53e4-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="a53e4-131">Representa el recuento de elementos no leídos dentro de una carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="a53e4-131">Represents the count of unread items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-132">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="a53e4-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="a53e4-133">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a53e4-133">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="a53e4-134">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a53e4-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="a53e4-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="a53e4-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="a53e4-136">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a53e4-136">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="a53e4-137">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a53e4-137">This element is read-only.</span></span> <span data-ttu-id="a53e4-138">Este elemento se introdujo en Microsoft Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="a53e4-138">This element was introduced in Microsoft Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a53e4-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a53e4-139">Parent elements</span></span>

|<span data-ttu-id="a53e4-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="a53e4-140">**Element**</span></span>|<span data-ttu-id="a53e4-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a53e4-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a53e4-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="a53e4-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="a53e4-143">Especifica los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a53e4-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a53e4-144">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a53e4-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="a53e4-145">Identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="a53e4-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="a53e4-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="a53e4-147">Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a53e4-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a53e4-148">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a53e4-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="a53e4-149">Identifica una sola carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="a53e4-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a53e4-150">Carpetas</span><span class="sxs-lookup"><span data-stu-id="a53e4-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a53e4-151">Contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a53e4-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a53e4-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a53e4-152">Remarks</span></span>

<span data-ttu-id="a53e4-153">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a53e4-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a53e4-154">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a53e4-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a53e4-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a53e4-155">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a53e4-156">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a53e4-156">Schema Name</span></span>  <br/> |<span data-ttu-id="a53e4-157">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a53e4-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="a53e4-158">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a53e4-158">Validation File</span></span>  <br/> |<span data-ttu-id="a53e4-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a53e4-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a53e4-160">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a53e4-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="a53e4-161">False</span><span class="sxs-lookup"><span data-stu-id="a53e4-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a53e4-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="a53e4-162">See also</span></span>

- [<span data-ttu-id="a53e4-163">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a53e4-163">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: SearchFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchFolder
api_type:
- schema
ms.assetid: 1a7d408b-2e98-4391-8834-085ed6d5757c
description: El elemento SearchFolder representa una carpeta de búsqueda que está contenida en un buzón.
ms.openlocfilehash: e1d5893e00f3b199451622061785e2566c6f32e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464010"
---
# <a name="searchfolder"></a><span data-ttu-id="4d9ed-103">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="4d9ed-103">SearchFolder</span></span>

<span data-ttu-id="4d9ed-104">El elemento **SearchFolder** representa una carpeta de búsqueda que está contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-104">The **SearchFolder** element represents a search folder that is contained in a mailbox.</span></span> 
  
```xml
<SearchFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <SearchParameters/>
   <PermissionSet/>
      <EffectiveRights/>
</SearchFolder>
```

 <span data-ttu-id="4d9ed-105">**SearchFolderType**</span><span class="sxs-lookup"><span data-stu-id="4d9ed-105">**SearchFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d9ed-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4d9ed-106">Attributes and elements</span></span>

<span data-ttu-id="4d9ed-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d9ed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4d9ed-108">Attributes</span></span>

<span data-ttu-id="4d9ed-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d9ed-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4d9ed-110">Child elements</span></span>

|<span data-ttu-id="4d9ed-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4d9ed-111">**Element**</span></span>|<span data-ttu-id="4d9ed-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d9ed-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d9ed-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="4d9ed-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="4d9ed-114">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="4d9ed-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="4d9ed-116">Representa el identificador de la carpeta principal que contiene la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="4d9ed-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="4d9ed-118">Representa la clase de carpeta de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="4d9ed-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="4d9ed-120">Contiene el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="4d9ed-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="4d9ed-122">Representa el número total de elementos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="4d9ed-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="4d9ed-124">Representa el número de carpetas secundarias contenidas dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-124">Represents the number of child folders contained within a folder.</span></span> <span data-ttu-id="4d9ed-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-126">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="4d9ed-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="4d9ed-127">Identifica las propiedades extendidas de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="4d9ed-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="4d9ed-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="4d9ed-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="4d9ed-131">Representa el número de elementos no leídos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-132">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="4d9ed-132">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="4d9ed-133">Contiene los parámetros que definen una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-133">Contains the parameters that define a search folder.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="4d9ed-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="4d9ed-135">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-135">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="4d9ed-136">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4d9ed-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-137">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="4d9ed-137">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="4d9ed-138">Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-138">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="4d9ed-139">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-139">This element is read-only.</span></span> <span data-ttu-id="4d9ed-140">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-140">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d9ed-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4d9ed-141">Parent elements</span></span>

|<span data-ttu-id="4d9ed-142">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4d9ed-142">**Element**</span></span>|<span data-ttu-id="4d9ed-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d9ed-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d9ed-144">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="4d9ed-144">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="4d9ed-145">Especifica los datos que se van a anexar a una propiedad de carpeta durante una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="4d9ed-145">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-146">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="4d9ed-146">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="4d9ed-147">Identifica una única carpeta que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-147">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-148">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="4d9ed-148">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="4d9ed-149">Representa una actualización de una propiedad única de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="4d9ed-149">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-150">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="4d9ed-150">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="4d9ed-151">Identifica una única carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-151">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="4d9ed-152">Folders</span><span class="sxs-lookup"><span data-stu-id="4d9ed-152">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4d9ed-153">Contiene una matriz de carpetas que se usan en las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-153">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d9ed-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d9ed-154">Remarks</span></span>

 <span data-ttu-id="4d9ed-155">**SearchFolder** se utiliza tanto para las carpetas de búsqueda normales como para las carpetas de búsqueda de MicrosoftOfficeOutlook y Outlook Web Access visibles.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-155">**SearchFolder** is used for both regular search folders and MicrosoftOfficeOutlook and Outlook Web Access visible search folders.</span></span> <span data-ttu-id="4d9ed-156">Para que una carpeta de búsqueda esté visible en Outlook y Outlook Web Access, la carpeta debe crearse en la carpeta distintiva SearchFolders.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-156">For a search folder to be visible to Outlook and Outlook Web Access, the folder must be created under the SearchFolders distinguished folder.</span></span> 
  
<span data-ttu-id="4d9ed-157">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4d9ed-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d9ed-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4d9ed-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d9ed-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d9ed-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4d9ed-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4d9ed-160">Schema Name</span></span>  <br/> |<span data-ttu-id="4d9ed-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4d9ed-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="4d9ed-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4d9ed-162">Validation File</span></span>  <br/> |<span data-ttu-id="4d9ed-163">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4d9ed-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4d9ed-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4d9ed-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="4d9ed-165">Falso</span><span class="sxs-lookup"><span data-stu-id="4d9ed-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d9ed-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d9ed-166">See also</span></span>



- [<span data-ttu-id="4d9ed-167">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4d9ed-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


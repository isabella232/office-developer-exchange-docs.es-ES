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
description: El elemento SearchFolder representa una carpeta de búsqueda que se encuentra en un buzón de correo.
ms.openlocfilehash: d842c54dab7950c68e26804b676834c2d95debad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837302"
---
# <a name="searchfolder"></a><span data-ttu-id="a5d94-103">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a5d94-103">SearchFolder</span></span>

<span data-ttu-id="a5d94-104">El elemento **SearchFolder** representa una carpeta de búsqueda que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a5d94-104">The **SearchFolder** element represents a search folder that is contained in a mailbox.</span></span> 
  
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

 <span data-ttu-id="a5d94-105">**SearchFolderType**</span><span class="sxs-lookup"><span data-stu-id="a5d94-105">**SearchFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5d94-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a5d94-106">Attributes and elements</span></span>

<span data-ttu-id="a5d94-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a5d94-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5d94-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a5d94-108">Attributes</span></span>

<span data-ttu-id="a5d94-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a5d94-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5d94-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a5d94-110">Child elements</span></span>

|<span data-ttu-id="a5d94-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5d94-111">**Element**</span></span>|<span data-ttu-id="a5d94-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5d94-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5d94-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="a5d94-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a5d94-114">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a5d94-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-115">Id</span><span class="sxs-lookup"><span data-stu-id="a5d94-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="a5d94-116">Representa el identificador de la carpeta primaria que contiene la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a5d94-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="a5d94-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="a5d94-118">Representa la clase de carpeta para una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="a5d94-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-119">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="a5d94-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="a5d94-120">Contiene el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a5d94-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="a5d94-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="a5d94-122">Representa el recuento total de elementos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="a5d94-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="a5d94-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="a5d94-124">Representa el número de carpetas secundarias contenidas dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a5d94-124">Represents the number of child folders contained within a folder.</span></span> <span data-ttu-id="a5d94-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a5d94-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a5d94-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="a5d94-127">Identifica las propiedades extendidas en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="a5d94-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="a5d94-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="a5d94-129">Contiene información acerca de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a5d94-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="a5d94-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="a5d94-131">Representa el recuento de elementos no leídos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="a5d94-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-132">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="a5d94-132">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="a5d94-133">Contiene los parámetros que definen una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a5d94-133">Contains the parameters that define a search folder.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="a5d94-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="a5d94-135">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a5d94-135">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="a5d94-136">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a5d94-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="a5d94-137">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="a5d94-137">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="a5d94-138">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a5d94-138">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="a5d94-139">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a5d94-139">This element is read-only.</span></span> <span data-ttu-id="a5d94-140">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="a5d94-140">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a5d94-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a5d94-141">Parent elements</span></span>

|<span data-ttu-id="a5d94-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5d94-142">**Element**</span></span>|<span data-ttu-id="a5d94-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5d94-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5d94-144">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="a5d94-144">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="a5d94-145">Especifica los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a5d94-145">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a5d94-146">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a5d94-146">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="a5d94-147">Identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="a5d94-147">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-148">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="a5d94-148">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="a5d94-149">Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a5d94-149">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a5d94-150">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a5d94-150">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="a5d94-151">Identifica una sola carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="a5d94-151">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a5d94-152">Carpetas</span><span class="sxs-lookup"><span data-stu-id="a5d94-152">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a5d94-153">Contiene una matriz de carpetas que se utilizan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a5d94-153">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5d94-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5d94-154">Remarks</span></span>

 <span data-ttu-id="a5d94-155">**SearchFolder** se utiliza para las carpetas de búsqueda regular y MicrosoftOfficeOutlook y Outlook Web Access visible las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a5d94-155">**SearchFolder** is used for both regular search folders and MicrosoftOfficeOutlook and Outlook Web Access visible search folders.</span></span> <span data-ttu-id="a5d94-156">Para que una carpeta de búsqueda que sean visibles en Outlook y Outlook Web Access, debe crearse la carpeta bajo la carpeta distintivo SearchFolders.</span><span class="sxs-lookup"><span data-stu-id="a5d94-156">For a search folder to be visible to Outlook and Outlook Web Access, the folder must be created under the SearchFolders distinguished folder.</span></span> 
  
<span data-ttu-id="a5d94-157">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a5d94-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5d94-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a5d94-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5d94-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5d94-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a5d94-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a5d94-160">Schema Name</span></span>  <br/> |<span data-ttu-id="a5d94-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a5d94-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="a5d94-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a5d94-162">Validation File</span></span>  <br/> |<span data-ttu-id="a5d94-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a5d94-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a5d94-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a5d94-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="a5d94-165">False</span><span class="sxs-lookup"><span data-stu-id="a5d94-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5d94-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5d94-166">See also</span></span>



- [<span data-ttu-id="a5d94-167">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a5d94-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


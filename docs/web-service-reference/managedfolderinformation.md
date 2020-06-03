---
title: ManagedFolderInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: El elemento ManagedFolderInformation contiene información sobre una carpeta personalizada administrada.
ms.openlocfilehash: ce15dcb15cccdce253494beefd2f4a2a7a0c0ad8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44450952"
---
# <a name="managedfolderinformation"></a><span data-ttu-id="c8ddc-103">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="c8ddc-103">ManagedFolderInformation</span></span>

<span data-ttu-id="c8ddc-104">El elemento **ManagedFolderInformation** contiene información sobre una carpeta personalizada administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-104">The **ManagedFolderInformation** element contains information about a managed custom folder.</span></span> 
  
```xml
<ManagedFolderInformation>
   <CanDelete/>
   <CanRenameOrMove/>
   <MustDisplayComment/>
   <HasQuota/>
   <IsManagedFoldersRoot/>
   <ManagedFolderId/>
   <Comment/>
   <StorageQuota/>
   <FolderSize/>
   <HomePage/>
</ManagedFolderInformation>
```

 <span data-ttu-id="c8ddc-105">**ManagedFolderInformationType**</span><span class="sxs-lookup"><span data-stu-id="c8ddc-105">**ManagedFolderInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8ddc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8ddc-106">Attributes and elements</span></span>

<span data-ttu-id="c8ddc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8ddc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8ddc-108">Attributes</span></span>

<span data-ttu-id="c8ddc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8ddc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8ddc-110">Child elements</span></span>

|<span data-ttu-id="c8ddc-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8ddc-111">**Element**</span></span>|<span data-ttu-id="c8ddc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8ddc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8ddc-113">CanDelete</span><span class="sxs-lookup"><span data-stu-id="c8ddc-113">CanDelete</span></span>](candelete.md) <br/> |<span data-ttu-id="c8ddc-114">Indica si un cliente puede eliminar una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-114">Indicates whether a managed folder can be deleted by a customer.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-115">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="c8ddc-115">CanRenameOrMove</span></span>](canrenameormove.md) <br/> |<span data-ttu-id="c8ddc-116">Indica si el cliente puede cambiar el nombre o mover una carpeta administrada determinada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-116">Indicates whether a given managed folder can be renamed or moved by the customer.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-117">MustDisplayComment</span><span class="sxs-lookup"><span data-stu-id="c8ddc-117">MustDisplayComment</span></span>](mustdisplaycomment.md) <br/> |<span data-ttu-id="c8ddc-118">Indica si se debe mostrar el comentario de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-118">Indicates whether the managed folder comment must be displayed.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-119">HasQuota</span><span class="sxs-lookup"><span data-stu-id="c8ddc-119">HasQuota</span></span>](hasquota.md) <br/> |<span data-ttu-id="c8ddc-120">Indica si la carpeta administrada tiene una cuota.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-120">Indicates whether the managed folder has a quota.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-121">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="c8ddc-121">IsManagedFoldersRoot</span></span>](ismanagedfoldersroot.md) <br/> |<span data-ttu-id="c8ddc-122">Indica si la carpeta administrada es la raíz de todas las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-122">Indicates whether the managed folder is the root for all managed folders.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-123">ManagedFolderId</span><span class="sxs-lookup"><span data-stu-id="c8ddc-123">ManagedFolderId</span></span>](managedfolderid.md) <br/> |<span data-ttu-id="c8ddc-124">Contiene el identificador de carpeta de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-124">Contains the folder ID of the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-125">Comment</span><span class="sxs-lookup"><span data-stu-id="c8ddc-125">Comment</span></span>](comment.md) <br/> |<span data-ttu-id="c8ddc-126">Contiene el comentario asociado con una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-126">Contains the comment that is associated with a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-127">StorageQuota</span><span class="sxs-lookup"><span data-stu-id="c8ddc-127">StorageQuota</span></span>](storagequota.md) <br/> |<span data-ttu-id="c8ddc-128">Describe la cuota de almacenamiento de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-128">Describes the storage quota for the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-129">FolderSize</span><span class="sxs-lookup"><span data-stu-id="c8ddc-129">FolderSize</span></span>](foldersize.md) <br/> |<span data-ttu-id="c8ddc-130">Describe el tamaño total de todo el contenido de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-130">Describes the total size of all the contents of a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-131">HomePage</span><span class="sxs-lookup"><span data-stu-id="c8ddc-131">HomePage</span></span>](homepage.md) <br/> |<span data-ttu-id="c8ddc-132">Especifica la dirección URL que será la Página principal predeterminada para la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-132">Specifies the URL that will be the default home page for the managed folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8ddc-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8ddc-133">Parent elements</span></span>

|<span data-ttu-id="c8ddc-134">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8ddc-134">**Element**</span></span>|<span data-ttu-id="c8ddc-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8ddc-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8ddc-136">Folder</span><span class="sxs-lookup"><span data-stu-id="c8ddc-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="c8ddc-137">Representa una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-137">Represents a folder in the Exchange store.</span></span> <span data-ttu-id="c8ddc-138">Las carpetas personalizadas administradas solo pueden ser subcarpetas de la carpeta denominada **carpetas administradas**.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-138">Managed custom folders can only be subfolders of the folder named **Managed Folders**.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-139">Hubiera</span><span class="sxs-lookup"><span data-stu-id="c8ddc-139">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="c8ddc-140">No procede.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-140">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-141">Hubiera</span><span class="sxs-lookup"><span data-stu-id="c8ddc-141">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="c8ddc-142">No procede.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-142">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="c8ddc-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="c8ddc-144">No procede.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-144">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="c8ddc-145">Hubiera</span><span class="sxs-lookup"><span data-stu-id="c8ddc-145">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="c8ddc-146">No procede.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-146">Not applicable.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8ddc-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8ddc-147">Remarks</span></span>

<span data-ttu-id="c8ddc-148">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c8ddc-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8ddc-149">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8ddc-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8ddc-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ddc-150">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8ddc-151">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8ddc-151">Schema name</span></span>  <br/> |<span data-ttu-id="c8ddc-152">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c8ddc-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8ddc-153">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8ddc-153">Validation file</span></span>  <br/> |<span data-ttu-id="c8ddc-154">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c8ddc-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8ddc-155">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8ddc-155">Can be empty</span></span>  <br/> |<span data-ttu-id="c8ddc-156">Falso</span><span class="sxs-lookup"><span data-stu-id="c8ddc-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8ddc-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8ddc-157">See also</span></span>



[<span data-ttu-id="c8ddc-158">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="c8ddc-158">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="c8ddc-159">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c8ddc-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c8ddc-160">Adición de carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="c8ddc-160">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)


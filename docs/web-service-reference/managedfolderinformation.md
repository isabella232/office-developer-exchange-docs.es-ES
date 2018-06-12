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
description: El elemento ManagedFolderInformation contiene información acerca de una carpeta personalizada administrada.
ms.openlocfilehash: ef46e2e0db440de2a8acae8316ce98d11bd6710e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836341"
---
# <a name="managedfolderinformation"></a><span data-ttu-id="a9074-103">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="a9074-103">ManagedFolderInformation</span></span>

<span data-ttu-id="a9074-104">El elemento **ManagedFolderInformation** contiene información acerca de una carpeta personalizada administrada.</span><span class="sxs-lookup"><span data-stu-id="a9074-104">The **ManagedFolderInformation** element contains information about a managed custom folder.</span></span> 
  
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

 <span data-ttu-id="a9074-105">**ManagedFolderInformationType**</span><span class="sxs-lookup"><span data-stu-id="a9074-105">**ManagedFolderInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9074-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9074-106">Attributes and elements</span></span>

<span data-ttu-id="a9074-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9074-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9074-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9074-108">Attributes</span></span>

<span data-ttu-id="a9074-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9074-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9074-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9074-110">Child elements</span></span>

|<span data-ttu-id="a9074-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9074-111">**Element**</span></span>|<span data-ttu-id="a9074-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9074-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9074-113">CanDelete</span><span class="sxs-lookup"><span data-stu-id="a9074-113">CanDelete</span></span>](candelete.md) <br/> |<span data-ttu-id="a9074-114">Indica si se puede eliminar una carpeta administrada por un cliente.</span><span class="sxs-lookup"><span data-stu-id="a9074-114">Indicates whether a managed folder can be deleted by a customer.</span></span>  <br/> |
|[<span data-ttu-id="a9074-115">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="a9074-115">CanRenameOrMove</span></span>](canrenameormove.md) <br/> |<span data-ttu-id="a9074-116">Indica si una determinada carpeta administrada se puede cambiar el nombre o movida por el cliente.</span><span class="sxs-lookup"><span data-stu-id="a9074-116">Indicates whether a given managed folder can be renamed or moved by the customer.</span></span>  <br/> |
|[<span data-ttu-id="a9074-117">MustDisplayComment</span><span class="sxs-lookup"><span data-stu-id="a9074-117">MustDisplayComment</span></span>](mustdisplaycomment.md) <br/> |<span data-ttu-id="a9074-118">Indica si se debe mostrar el comentario de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a9074-118">Indicates whether the managed folder comment must be displayed.</span></span>  <br/> |
|[<span data-ttu-id="a9074-119">HasQuota</span><span class="sxs-lookup"><span data-stu-id="a9074-119">HasQuota</span></span>](hasquota.md) <br/> |<span data-ttu-id="a9074-120">Indica si la carpeta administrada tiene una cuota.</span><span class="sxs-lookup"><span data-stu-id="a9074-120">Indicates whether the managed folder has a quota.</span></span>  <br/> |
|[<span data-ttu-id="a9074-121">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="a9074-121">IsManagedFoldersRoot</span></span>](ismanagedfoldersroot.md) <br/> |<span data-ttu-id="a9074-122">Indica si la carpeta administrada es la raíz de todas las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="a9074-122">Indicates whether the managed folder is the root for all managed folders.</span></span>  <br/> |
|[<span data-ttu-id="a9074-123">ManagedFolderId</span><span class="sxs-lookup"><span data-stu-id="a9074-123">ManagedFolderId</span></span>](managedfolderid.md) <br/> |<span data-ttu-id="a9074-124">Contiene el identificador de la carpeta de la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a9074-124">Contains the folder ID of the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="a9074-125">Comment</span><span class="sxs-lookup"><span data-stu-id="a9074-125">Comment</span></span>](comment.md) <br/> |<span data-ttu-id="a9074-126">Contiene el comentario que está asociado a una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a9074-126">Contains the comment that is associated with a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="a9074-127">StorageQuota</span><span class="sxs-lookup"><span data-stu-id="a9074-127">StorageQuota</span></span>](storagequota.md) <br/> |<span data-ttu-id="a9074-128">Describe la cuota de almacenamiento para la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a9074-128">Describes the storage quota for the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="a9074-129">FolderSize</span><span class="sxs-lookup"><span data-stu-id="a9074-129">FolderSize</span></span>](foldersize.md) <br/> |<span data-ttu-id="a9074-130">Describe el tamaño total de todo el contenido de una carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a9074-130">Describes the total size of all the contents of a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="a9074-131">Página principal</span><span class="sxs-lookup"><span data-stu-id="a9074-131">HomePage</span></span>](homepage.md) <br/> |<span data-ttu-id="a9074-132">Especifica la dirección URL que será la página principal predeterminada para la carpeta administrada.</span><span class="sxs-lookup"><span data-stu-id="a9074-132">Specifies the URL that will be the default home page for the managed folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9074-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9074-133">Parent elements</span></span>

|<span data-ttu-id="a9074-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9074-134">**Element**</span></span>|<span data-ttu-id="a9074-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9074-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9074-136">Folder</span><span class="sxs-lookup"><span data-stu-id="a9074-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="a9074-137">Representa una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9074-137">Represents a folder in the Exchange store.</span></span> <span data-ttu-id="a9074-138">Las carpetas personalizadas administradas sólo pueden ser las subcarpetas de la carpeta denominada **Carpetas administradas**.</span><span class="sxs-lookup"><span data-stu-id="a9074-138">Managed custom folders can only be subfolders of the folder named **Managed Folders**.</span></span>  <br/> |
|[<span data-ttu-id="a9074-139">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="a9074-139">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="a9074-140">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a9074-140">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="a9074-141">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="a9074-141">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="a9074-142">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a9074-142">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="a9074-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a9074-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="a9074-144">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a9074-144">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="a9074-145">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="a9074-145">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="a9074-146">No procede.</span><span class="sxs-lookup"><span data-stu-id="a9074-146">Not applicable.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9074-147">Notas</span><span class="sxs-lookup"><span data-stu-id="a9074-147">Remarks</span></span>

<span data-ttu-id="a9074-148">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a9074-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9074-149">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9074-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9074-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9074-150">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9074-151">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9074-151">Schema name</span></span>  <br/> |<span data-ttu-id="a9074-152">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a9074-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9074-153">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9074-153">Validation file</span></span>  <br/> |<span data-ttu-id="a9074-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9074-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9074-155">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9074-155">Can be empty</span></span>  <br/> |<span data-ttu-id="a9074-156">False</span><span class="sxs-lookup"><span data-stu-id="a9074-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9074-157">Ver también</span><span class="sxs-lookup"><span data-stu-id="a9074-157">See also</span></span>



[<span data-ttu-id="a9074-158">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="a9074-158">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="a9074-159">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a9074-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="a9074-160">Adición de las carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="a9074-160">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)


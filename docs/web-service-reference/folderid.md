---
title: FolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: El elemento FolderId contiene el identificador y la clave de cambio de una carpeta.
ms.openlocfilehash: 7aa5070fa7a2c51303c7159de04fe277f909a874
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461390"
---
# <a name="folderid"></a><span data-ttu-id="c4aac-103">FolderId</span><span class="sxs-lookup"><span data-stu-id="c4aac-103">FolderId</span></span>

<span data-ttu-id="c4aac-104">El elemento **FolderId** contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4aac-104">The **FolderId** element contains the identifier and change key of a folder.</span></span> 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="c4aac-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="c4aac-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4aac-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c4aac-106">Attributes and elements</span></span>

<span data-ttu-id="c4aac-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c4aac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4aac-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4aac-108">Attributes</span></span>

|<span data-ttu-id="c4aac-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c4aac-109">**Attribute**</span></span>|<span data-ttu-id="c4aac-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4aac-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4aac-111">Id</span><span class="sxs-lookup"><span data-stu-id="c4aac-111">Id</span></span>  <br/> |<span data-ttu-id="c4aac-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4aac-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="c4aac-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4aac-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="c4aac-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="c4aac-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="c4aac-115">Contiene una cadena que identifica una versión de una carpeta identificada por el atributo id.</span><span class="sxs-lookup"><span data-stu-id="c4aac-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="c4aac-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="c4aac-116">This attribute is optional.</span></span> <span data-ttu-id="c4aac-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4aac-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c4aac-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c4aac-118">Child elements</span></span>

<span data-ttu-id="c4aac-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c4aac-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4aac-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c4aac-120">Parent elements</span></span>

|<span data-ttu-id="c4aac-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c4aac-121">**Element**</span></span>|<span data-ttu-id="c4aac-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4aac-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4aac-123">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="c4aac-123">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="c4aac-124">Indica la carpeta que está destinada a las acciones que usan carpetas.</span><span class="sxs-lookup"><span data-stu-id="c4aac-124">Indicates the folder that is targeted for actions that use folders.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-125">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="c4aac-125">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="c4aac-126">Representa un evento en el que se copia un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4aac-126">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-127">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="c4aac-127">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="c4aac-128">Indica la carpeta de destino para las acciones de copiar y mover.</span><span class="sxs-lookup"><span data-stu-id="c4aac-128">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-129">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="c4aac-129">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> | <span data-ttu-id="c4aac-130">Identifica la carpeta en la que se crea una nueva carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="c4aac-130">Identifies the folder where a new folder or item is created.</span></span>  <br/><br/>  <span data-ttu-id="c4aac-131">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="c4aac-131">The following are the XPath expressions to this element:</span></span><br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[<span data-ttu-id="c4aac-132">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="c4aac-132">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="c4aac-133">Representa la colección de carpetas que se extendrán para determinar el contenido de una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c4aac-133">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-134">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c4aac-134">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="c4aac-135">Identifica una única carpeta que se va a eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="c4aac-135">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-136">Folder</span><span class="sxs-lookup"><span data-stu-id="c4aac-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="c4aac-137">Representa una carpeta en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c4aac-137">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-138">Hubiera</span><span class="sxs-lookup"><span data-stu-id="c4aac-138">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="c4aac-139">Representa una carpeta de calendario en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c4aac-139">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-140">FolderChange</span><span class="sxs-lookup"><span data-stu-id="c4aac-140">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="c4aac-141">Representa una colección de cambios que se van a realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4aac-141">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="c4aac-142">La siguiente es la expresión XPath a este elemento:`/UpdateFolder/FolderChanges/FolderChange`</span><span class="sxs-lookup"><span data-stu-id="c4aac-142">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange`</span></span> <br/> |
|[<span data-ttu-id="c4aac-143">Hubiera</span><span class="sxs-lookup"><span data-stu-id="c4aac-143">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="c4aac-144">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c4aac-144">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-145">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="c4aac-145">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="c4aac-146">Representa una carpeta de búsqueda en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c4aac-146">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-147">Hubiera</span><span class="sxs-lookup"><span data-stu-id="c4aac-147">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="c4aac-148">Representa una carpeta de tareas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c4aac-148">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-149">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="c4aac-149">ToFolderId</span></span>](tofolderid.md) <br/> | <span data-ttu-id="c4aac-150">Representa la carpeta de destino de un elemento o carpeta que se ha copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="c4aac-150">Represents the destination folder for a copied or moved item or folder.</span></span> <br/> <br/>  <span data-ttu-id="c4aac-151">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="c4aac-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[<span data-ttu-id="c4aac-152">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="c4aac-152">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> | <span data-ttu-id="c4aac-153">Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4aac-153">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/><br/>  <span data-ttu-id="c4aac-154">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="c4aac-154">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[<span data-ttu-id="c4aac-155">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="c4aac-155">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="c4aac-156">Representa la carpeta que contiene los elementos que se van a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="c4aac-156">Represents the folder that contains the items to synchronize.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-157">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c4aac-157">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="c4aac-158">Representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="c4aac-158">Represents the name of a user configuration object.</span></span> <span data-ttu-id="c4aac-159">El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="c4aac-159">The user configuration object name is the identifier for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-160">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="c4aac-160">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="c4aac-161">Identifica el identificador de la carpeta en la que se copiarán los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c4aac-161">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="c4aac-162">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="c4aac-162">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="c4aac-163">Identifica el identificador de la carpeta a la que se moverán los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c4aac-163">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4aac-164">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c4aac-164">Text value</span></span>

<span data-ttu-id="c4aac-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4aac-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4aac-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4aac-166">Remarks</span></span>

<span data-ttu-id="c4aac-167">Todos los elementos **FolderId** son del tipo **FolderIdType** .</span><span class="sxs-lookup"><span data-stu-id="c4aac-167">All **FolderId** elements are of the **FolderIdType** type.</span></span> <span data-ttu-id="c4aac-168">El elemento **FolderId** es necesario en todos los casos, excepto en elementos cuyo tipo extiende la **BaseFolderType** o donde el elemento **FolderId** forma parte de una opción.</span><span class="sxs-lookup"><span data-stu-id="c4aac-168">The **FolderId** element is required in every case except in elements whose type extends the **BaseFolderType** or where the **FolderId** element is a part of a choice.</span></span> <span data-ttu-id="c4aac-169">Revise el esquema para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4aac-169">Review the schema for more information.</span></span> 
  
<span data-ttu-id="c4aac-170">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4aac-170">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4aac-171">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c4aac-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4aac-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4aac-172">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4aac-173">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c4aac-173">Schema Name</span></span>  <br/> |<span data-ttu-id="c4aac-174">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c4aac-174">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4aac-175">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c4aac-175">Validation File</span></span>  <br/> |<span data-ttu-id="c4aac-176">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c4aac-176">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4aac-177">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c4aac-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4aac-178">Falso</span><span class="sxs-lookup"><span data-stu-id="c4aac-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4aac-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4aac-179">See also</span></span>

- [<span data-ttu-id="c4aac-180">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c4aac-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="c4aac-181">Creación de carpetas (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="c4aac-181">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)


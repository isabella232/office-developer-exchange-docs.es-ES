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
description: El elemento de FolderId contiene el identificador y cambiar la clave de una carpeta.
ms.openlocfilehash: 5764a164d5af183b8f313955ace5274dc6023a6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764683"
---
# <a name="folderid"></a><span data-ttu-id="c4fab-103">FolderId</span><span class="sxs-lookup"><span data-stu-id="c4fab-103">FolderId</span></span>

<span data-ttu-id="c4fab-104">El elemento de **FolderId** contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4fab-104">The **FolderId** element contains the identifier and change key of a folder.</span></span> 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="c4fab-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="c4fab-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4fab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c4fab-106">Attributes and elements</span></span>

<span data-ttu-id="c4fab-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c4fab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4fab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4fab-108">Attributes</span></span>

|<span data-ttu-id="c4fab-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c4fab-109">**Attribute**</span></span>|<span data-ttu-id="c4fab-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4fab-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4fab-111">Id</span><span class="sxs-lookup"><span data-stu-id="c4fab-111">Id</span></span>  <br/> |<span data-ttu-id="c4fab-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4fab-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="c4fab-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="c4fab-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="c4fab-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="c4fab-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="c4fab-115">Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo Id.</span><span class="sxs-lookup"><span data-stu-id="c4fab-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="c4fab-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="c4fab-116">This attribute is optional.</span></span> <span data-ttu-id="c4fab-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4fab-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c4fab-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c4fab-118">Child elements</span></span>

<span data-ttu-id="c4fab-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4fab-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4fab-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c4fab-120">Parent elements</span></span>

|<span data-ttu-id="c4fab-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4fab-121">**Element**</span></span>|<span data-ttu-id="c4fab-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4fab-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4fab-123">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="c4fab-123">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="c4fab-124">Indica la carpeta que está destinada a las acciones que utilizan carpetas.</span><span class="sxs-lookup"><span data-stu-id="c4fab-124">Indicates the folder that is targeted for actions that use folders.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-125">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="c4fab-125">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="c4fab-126">Representa un evento en el que se copia un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4fab-126">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-127">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="c4fab-127">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="c4fab-128">Indica la carpeta de destino para copiar y mover las acciones.</span><span class="sxs-lookup"><span data-stu-id="c4fab-128">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-129">ID (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="c4fab-129">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> | <span data-ttu-id="c4fab-130">Identifica la carpeta donde se crea una nueva carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="c4fab-130">Identifies the folder where a new folder or item is created.</span></span>  <br/><br/>  <span data-ttu-id="c4fab-131">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c4fab-131">The following are the XPath expressions to this element:</span></span><br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[<span data-ttu-id="c4fab-132">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="c4fab-132">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="c4fab-133">Representa la colección de carpetas que se extraídos para determinar el contenido de una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c4fab-133">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-134">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c4fab-134">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="c4fab-135">Identifica una sola carpeta para eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="c4fab-135">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-136">Folder</span><span class="sxs-lookup"><span data-stu-id="c4fab-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="c4fab-137">Representa una carpeta en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c4fab-137">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-138">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="c4fab-138">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="c4fab-139">Representa una carpeta del calendario en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c4fab-139">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-140">FolderChange</span><span class="sxs-lookup"><span data-stu-id="c4fab-140">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="c4fab-141">Representa una colección de los cambios que se debe realizar en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4fab-141">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="c4fab-142">La siguiente es la expresión de XPath para este elemento:`/UpdateFolder/FolderChanges/FolderChange`</span><span class="sxs-lookup"><span data-stu-id="c4fab-142">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange`</span></span> <br/> |
|[<span data-ttu-id="c4fab-143">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="c4fab-143">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="c4fab-144">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c4fab-144">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-145">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="c4fab-145">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="c4fab-146">Representa una carpeta de búsqueda en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c4fab-146">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-147">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="c4fab-147">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="c4fab-148">Representa una carpeta de tareas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c4fab-148">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-149">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="c4fab-149">ToFolderId</span></span>](tofolderid.md) <br/> | <span data-ttu-id="c4fab-150">Representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4fab-150">Represents the destination folder for a copied or moved item or folder.</span></span> <br/> <br/>  <span data-ttu-id="c4fab-151">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c4fab-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[<span data-ttu-id="c4fab-152">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="c4fab-152">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> | <span data-ttu-id="c4fab-153">Identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4fab-153">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/><br/>  <span data-ttu-id="c4fab-154">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c4fab-154">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[<span data-ttu-id="c4fab-155">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="c4fab-155">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="c4fab-156">Representa la carpeta que contiene los elementos para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="c4fab-156">Represents the folder that contains the items to synchronize.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-157">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c4fab-157">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="c4fab-158">Representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="c4fab-158">Represents the name of a user configuration object.</span></span> <span data-ttu-id="c4fab-159">El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="c4fab-159">The user configuration object name is the identifier for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-160">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="c4fab-160">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="c4fab-161">Identifica el identificador de la carpeta que se copiarán los elementos de correo electrónico a.</span><span class="sxs-lookup"><span data-stu-id="c4fab-161">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="c4fab-162">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="c4fab-162">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="c4fab-163">Identifica el identificador de la carpeta que se moverán los elementos de correo electrónico a.</span><span class="sxs-lookup"><span data-stu-id="c4fab-163">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4fab-164">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c4fab-164">Text value</span></span>

<span data-ttu-id="c4fab-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4fab-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4fab-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4fab-166">Remarks</span></span>

<span data-ttu-id="c4fab-167">Todos los elementos de **FolderId** son del tipo **FolderIdType** .</span><span class="sxs-lookup"><span data-stu-id="c4fab-167">All **FolderId** elements are of the **FolderIdType** type.</span></span> <span data-ttu-id="c4fab-168">Se requiere el elemento **FolderId** en todos los casos, excepto en los elementos cuyo tipo extiende el **BaseFolderType** o donde el elemento **FolderId** es una parte de una opción.</span><span class="sxs-lookup"><span data-stu-id="c4fab-168">The **FolderId** element is required in every case except in elements whose type extends the **BaseFolderType** or where the **FolderId** element is a part of a choice.</span></span> <span data-ttu-id="c4fab-169">Revise el esquema para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c4fab-169">Review the schema for more information.</span></span> 
  
<span data-ttu-id="c4fab-170">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4fab-170">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4fab-171">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c4fab-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4fab-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4fab-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4fab-173">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c4fab-173">Schema Name</span></span>  <br/> |<span data-ttu-id="c4fab-174">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c4fab-174">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4fab-175">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c4fab-175">Validation File</span></span>  <br/> |<span data-ttu-id="c4fab-176">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4fab-176">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4fab-177">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c4fab-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4fab-178">False</span><span class="sxs-lookup"><span data-stu-id="c4fab-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4fab-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4fab-179">See also</span></span>

- [<span data-ttu-id="c4fab-180">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4fab-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="c4fab-181">Creación de carpetas (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="c4fab-181">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)


---
title: Actualización (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 47ed8edb-2a94-471b-b965-93f91456252e
description: El elemento de actualización identifica una sola carpeta para actualizar en el almacén de cliente local.
ms.openlocfilehash: 6d4a6233df41ea95e1fd9b394502bfb2728bddb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840801"
---
# <a name="update-foldersync"></a><span data-ttu-id="de428-103">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="de428-103">Update (FolderSync)</span></span>

<span data-ttu-id="de428-104">El elemento **Update** identifica una sola carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="de428-104">The **Update** element identifies a single folder to update in the local client store.</span></span> 
  
[<span data-ttu-id="de428-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="de428-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="de428-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="de428-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="de428-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="de428-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="de428-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="de428-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="de428-109">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="de428-109">Update (FolderSync)</span></span>](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

 <span data-ttu-id="de428-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="de428-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de428-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de428-111">Attributes and elements</span></span>

<span data-ttu-id="de428-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de428-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de428-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="de428-113">Attributes</span></span>

<span data-ttu-id="de428-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="de428-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de428-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de428-115">Child elements</span></span>

|<span data-ttu-id="de428-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="de428-116">**Element**</span></span>|<span data-ttu-id="de428-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de428-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de428-118">Folder</span><span class="sxs-lookup"><span data-stu-id="de428-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="de428-119">Define la carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="de428-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="de428-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="de428-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="de428-121">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="de428-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="de428-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="de428-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="de428-123">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="de428-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="de428-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="de428-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="de428-125">Representa una carpeta de búsqueda que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="de428-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="de428-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="de428-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="de428-127">Representa una tarea de carpeta t es thcontained en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="de428-127">Represents a task folder t is thcontained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de428-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de428-128">Parent elements</span></span>

|<span data-ttu-id="de428-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="de428-129">**Element**</span></span>|<span data-ttu-id="de428-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de428-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de428-131">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="de428-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="de428-132">Contiene una matriz de tipos de cambio que representan el tipo de las diferencias entre las carpetas en el cliente y las carpetas en el servidor de Exchange de secuenciado.</span><span class="sxs-lookup"><span data-stu-id="de428-132">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de428-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de428-133">Remarks</span></span>

<span data-ttu-id="de428-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="de428-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de428-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de428-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de428-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="de428-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de428-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de428-137">Schema name</span></span>  <br/> |<span data-ttu-id="de428-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="de428-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="de428-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de428-139">Validation file</span></span>  <br/> |<span data-ttu-id="de428-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="de428-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de428-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de428-141">Can be empty</span></span>  <br/> |<span data-ttu-id="de428-142">False</span><span class="sxs-lookup"><span data-stu-id="de428-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de428-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="de428-143">See also</span></span>



[<span data-ttu-id="de428-144">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="de428-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="de428-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="de428-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


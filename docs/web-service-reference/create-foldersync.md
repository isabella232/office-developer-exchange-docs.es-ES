---
title: Crear (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: 6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1
description: El elemento Create identifica una sola carpeta para crear en el almacén de cliente local.
ms.openlocfilehash: 867eecb89c115b008d4828e162b21d078eba695c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763908"
---
# <a name="create-foldersync"></a><span data-ttu-id="c5ab6-103">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c5ab6-103">Create (FolderSync)</span></span>

<span data-ttu-id="c5ab6-104">El elemento **Create** identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-104">The **Create** element identifies a single folder to create in the local client store.</span></span> 
  
[<span data-ttu-id="c5ab6-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="c5ab6-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="c5ab6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c5ab6-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="c5ab6-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c5ab6-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="c5ab6-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="c5ab6-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="c5ab6-109">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c5ab6-109">Create (FolderSync)</span></span>](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
```

 <span data-ttu-id="c5ab6-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="c5ab6-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5ab6-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c5ab6-111">Attributes and elements</span></span>

<span data-ttu-id="c5ab6-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5ab6-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5ab6-113">Attributes</span></span>

<span data-ttu-id="c5ab6-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5ab6-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5ab6-115">Child elements</span></span>

|<span data-ttu-id="c5ab6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5ab6-116">**Element**</span></span>|<span data-ttu-id="c5ab6-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5ab6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5ab6-118">Folder</span><span class="sxs-lookup"><span data-stu-id="c5ab6-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="c5ab6-119">Define la carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="c5ab6-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="c5ab6-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="c5ab6-121">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="c5ab6-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="c5ab6-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="c5ab6-123">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c5ab6-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="c5ab6-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="c5ab6-125">Representa una carpeta de búsqueda incluida en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-125">Represents a search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c5ab6-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="c5ab6-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="c5ab6-127">Representa una carpeta de tarea incluida en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-127">Represents a task folder contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5ab6-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c5ab6-128">Parent elements</span></span>

|<span data-ttu-id="c5ab6-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5ab6-129">**Element**</span></span>|<span data-ttu-id="c5ab6-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5ab6-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5ab6-131">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="c5ab6-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="c5ab6-132">Contiene una matriz de secuencia de tipos de cambio que representan el tipo de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-132">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5ab6-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5ab6-133">Remarks</span></span>

<span data-ttu-id="c5ab6-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c5ab6-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5ab6-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c5ab6-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5ab6-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5ab6-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5ab6-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c5ab6-137">Schema name</span></span>  <br/> |<span data-ttu-id="c5ab6-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c5ab6-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5ab6-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c5ab6-139">Validation file</span></span>  <br/> |<span data-ttu-id="c5ab6-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5ab6-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5ab6-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c5ab6-141">Can be empty</span></span>  <br/> |<span data-ttu-id="c5ab6-142">False</span><span class="sxs-lookup"><span data-stu-id="c5ab6-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5ab6-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5ab6-143">See also</span></span>



[<span data-ttu-id="c5ab6-144">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="c5ab6-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="c5ab6-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c5ab6-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


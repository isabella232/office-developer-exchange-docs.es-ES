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
description: El elemento Create identifica una única carpeta que se va a crear en el almacén de cliente local.
ms.openlocfilehash: 43f6a6b3c084c8ecae767c512181bbdf50c7e786
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458379"
---
# <a name="create-foldersync"></a><span data-ttu-id="56d6e-103">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="56d6e-103">Create (FolderSync)</span></span>

<span data-ttu-id="56d6e-104">El elemento **Create** identifica una única carpeta que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="56d6e-104">The **Create** element identifies a single folder to create in the local client store.</span></span> 
  
[<span data-ttu-id="56d6e-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="56d6e-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="56d6e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="56d6e-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="56d6e-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="56d6e-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="56d6e-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="56d6e-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="56d6e-109">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="56d6e-109">Create (FolderSync)</span></span>](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
```

 <span data-ttu-id="56d6e-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="56d6e-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56d6e-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="56d6e-111">Attributes and elements</span></span>

<span data-ttu-id="56d6e-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="56d6e-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56d6e-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="56d6e-113">Attributes</span></span>

<span data-ttu-id="56d6e-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="56d6e-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56d6e-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56d6e-115">Child elements</span></span>

|<span data-ttu-id="56d6e-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="56d6e-116">**Element**</span></span>|<span data-ttu-id="56d6e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56d6e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56d6e-118">Folder</span><span class="sxs-lookup"><span data-stu-id="56d6e-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="56d6e-119">Define la carpeta que se va a crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="56d6e-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="56d6e-120">Hubiera</span><span class="sxs-lookup"><span data-stu-id="56d6e-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="56d6e-121">Representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="56d6e-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="56d6e-122">Hubiera</span><span class="sxs-lookup"><span data-stu-id="56d6e-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="56d6e-123">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="56d6e-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="56d6e-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="56d6e-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="56d6e-125">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="56d6e-125">Represents a search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="56d6e-126">Hubiera</span><span class="sxs-lookup"><span data-stu-id="56d6e-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="56d6e-127">Representa una carpeta de tareas contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="56d6e-127">Represents a task folder contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="56d6e-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="56d6e-128">Parent elements</span></span>

|<span data-ttu-id="56d6e-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="56d6e-129">**Element**</span></span>|<span data-ttu-id="56d6e-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56d6e-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56d6e-131">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="56d6e-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="56d6e-132">Contiene una matriz de secuencias de tipos de cambios que representan el tipo de diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="56d6e-132">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56d6e-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56d6e-133">Remarks</span></span>

<span data-ttu-id="56d6e-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="56d6e-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56d6e-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="56d6e-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56d6e-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="56d6e-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="56d6e-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="56d6e-137">Schema name</span></span>  <br/> |<span data-ttu-id="56d6e-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="56d6e-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="56d6e-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="56d6e-139">Validation file</span></span>  <br/> |<span data-ttu-id="56d6e-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="56d6e-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="56d6e-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="56d6e-141">Can be empty</span></span>  <br/> |<span data-ttu-id="56d6e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="56d6e-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56d6e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="56d6e-143">See also</span></span>



[<span data-ttu-id="56d6e-144">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="56d6e-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="56d6e-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="56d6e-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


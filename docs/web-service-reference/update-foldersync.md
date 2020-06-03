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
description: El elemento Update identifica una única carpeta para actualizar en el almacén de cliente local.
ms.openlocfilehash: 5c1b5b1fd87e4651125293eac431c56f732c6c02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467140"
---
# <a name="update-foldersync"></a><span data-ttu-id="e7155-103">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="e7155-103">Update (FolderSync)</span></span>

<span data-ttu-id="e7155-104">El elemento **Update** identifica una única carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="e7155-104">The **Update** element identifies a single folder to update in the local client store.</span></span> 
  
- [<span data-ttu-id="e7155-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="e7155-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="e7155-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e7155-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="e7155-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e7155-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="e7155-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="e7155-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md) 
- [<span data-ttu-id="e7155-109">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="e7155-109">Update (FolderSync)</span></span>](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

```xml
<Update>
   <CalendarFolder/>
</Update>
```

```xml
<Update>
   <ContactsFolder/>
</Update>
```

```xml
<Update>
   <TasksFolder/>
</Update>
```

```xml
<Update>
   <SearchFolder/>
</Update>
```

<span data-ttu-id="e7155-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="e7155-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e7155-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e7155-111">Attributes and elements</span></span>

<span data-ttu-id="e7155-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e7155-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7155-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7155-113">Attributes</span></span>

<span data-ttu-id="e7155-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e7155-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7155-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e7155-115">Child elements</span></span>

|<span data-ttu-id="e7155-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7155-116">**Element**</span></span>|<span data-ttu-id="e7155-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7155-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7155-118">Folder</span><span class="sxs-lookup"><span data-stu-id="e7155-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="e7155-119">Define la carpeta que se va a crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="e7155-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="e7155-120">Hubiera</span><span class="sxs-lookup"><span data-stu-id="e7155-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="e7155-121">Representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="e7155-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="e7155-122">Hubiera</span><span class="sxs-lookup"><span data-stu-id="e7155-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="e7155-123">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e7155-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e7155-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="e7155-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="e7155-125">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e7155-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e7155-126">Hubiera</span><span class="sxs-lookup"><span data-stu-id="e7155-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="e7155-127">Representa una carpeta de tareas t es thcontained en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e7155-127">Represents a task folder t is thcontained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e7155-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e7155-128">Parent elements</span></span>

|<span data-ttu-id="e7155-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7155-129">**Element**</span></span>|<span data-ttu-id="e7155-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7155-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7155-131">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="e7155-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="e7155-132">Contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas en el cliente y las carpetas en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7155-132">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7155-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7155-133">Remarks</span></span>

<span data-ttu-id="e7155-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e7155-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7155-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e7155-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7155-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7155-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7155-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e7155-137">Schema name</span></span>  <br/> |<span data-ttu-id="e7155-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e7155-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7155-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e7155-139">Validation file</span></span>  <br/> |<span data-ttu-id="e7155-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e7155-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7155-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e7155-141">Can be empty</span></span>  <br/> |<span data-ttu-id="e7155-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e7155-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7155-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7155-143">See also</span></span>

- [<span data-ttu-id="e7155-144">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e7155-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="e7155-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e7155-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


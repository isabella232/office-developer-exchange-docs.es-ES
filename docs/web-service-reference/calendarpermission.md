---
title: CalendarPermission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: El elemento CalendarPermission define el acceso que tiene un usuario a una carpeta de calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: c43f75e6cf5abc2dce9af6c04122ec9a589dcd58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529479"
---
# <a name="calendarpermission"></a><span data-ttu-id="1b074-104">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="1b074-104">CalendarPermission</span></span>

<span data-ttu-id="1b074-105">El elemento **CalendarPermission** define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="1b074-105">The **CalendarPermission** element defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="1b074-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1b074-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Permission>
   <CalendarPermissionLevel/>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 <span data-ttu-id="1b074-107">**CalendarPermissionType**</span><span class="sxs-lookup"><span data-stu-id="1b074-107">**CalendarPermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b074-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1b074-108">Attributes and elements</span></span>

<span data-ttu-id="1b074-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1b074-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b074-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b074-110">Attributes</span></span>

<span data-ttu-id="1b074-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1b074-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b074-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1b074-112">Child elements</span></span>

|<span data-ttu-id="1b074-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b074-113">**Element**</span></span>|<span data-ttu-id="1b074-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b074-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b074-115">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="1b074-115">CalendarPermissionLevel</span></span>](calendarpermissionlevel.md) <br/> |<span data-ttu-id="1b074-116">Representa el nivel de permisos que tiene un usuario en una carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="1b074-116">Represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="1b074-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-118">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="1b074-118">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="1b074-119">Indica si un usuario tiene permiso para crear elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-119">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="1b074-120">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-121">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="1b074-121">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="1b074-122">Indica si un usuario tiene permiso para crear subcarpetas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-122">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="1b074-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-124">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="1b074-124">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="1b074-125">Indica si un usuario tiene permiso para eliminar elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-125">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="1b074-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-127">EditItems</span><span class="sxs-lookup"><span data-stu-id="1b074-127">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="1b074-128">Indica si un usuario tiene permiso para editar los elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-128">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="1b074-129">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-130">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="1b074-130">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="1b074-131">Indica si un usuario es un contacto de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-131">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="1b074-132">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-133">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="1b074-133">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="1b074-134">Indica si un usuario es el propietario de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-134">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="1b074-135">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-135">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-136">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="1b074-136">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="1b074-137">Indica si un usuario puede ver una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-137">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="1b074-138">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-139">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="1b074-139">ReadItems (CalendarPermissionType)</span></span>](readitems-calendarpermissiontype.md) <br/> |<span data-ttu-id="1b074-140">Indica si un usuario tiene permiso para leer elementos dentro de una carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="1b074-140">Indicates whether a user has permission to read items within a calendar folder.</span></span> <span data-ttu-id="1b074-141">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-141">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1b074-142">UserId</span><span class="sxs-lookup"><span data-stu-id="1b074-142">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="1b074-143">Identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-143">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="1b074-144">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-144">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1b074-145">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1b074-145">Parent elements</span></span>

|<span data-ttu-id="1b074-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b074-146">**Element**</span></span>|<span data-ttu-id="1b074-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b074-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b074-148">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="1b074-148">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="1b074-149">Contiene una matriz de permisos de calendario para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b074-149">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="1b074-150">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1b074-150">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b074-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b074-151">Remarks</span></span>

<span data-ttu-id="1b074-152">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1b074-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b074-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1b074-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b074-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b074-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1b074-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1b074-155">Schema Name</span></span>  <br/> |<span data-ttu-id="1b074-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1b074-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="1b074-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1b074-157">Validation File</span></span>  <br/> |<span data-ttu-id="1b074-158">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1b074-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1b074-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1b074-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="1b074-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1b074-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b074-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b074-161">See also</span></span>



- [<span data-ttu-id="1b074-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1b074-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1b074-163">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="1b074-163">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


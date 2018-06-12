---
title: Permiso
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: El elemento de permiso define el acceso que tiene un usuario a una carpeta.
ms.openlocfilehash: 600d60f481c4f1d407c3a39ab65d6ddcf46d04e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836735"
---
# <a name="permission"></a><span data-ttu-id="d02a1-103">Permiso</span><span class="sxs-lookup"><span data-stu-id="d02a1-103">Permission</span></span>

<span data-ttu-id="d02a1-104">El elemento de **permiso** define el acceso que tiene un usuario a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-104">The **Permission** element defines the access that a user has to a folder.</span></span> 
  
```XML
<Permission>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <PermissionLevel/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 <span data-ttu-id="d02a1-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="d02a1-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d02a1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d02a1-106">Attributes and elements</span></span>

<span data-ttu-id="d02a1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d02a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d02a1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d02a1-108">Attributes</span></span>

<span data-ttu-id="d02a1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d02a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d02a1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d02a1-110">Child elements</span></span>

|<span data-ttu-id="d02a1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d02a1-111">**Element**</span></span>|<span data-ttu-id="d02a1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d02a1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d02a1-113">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="d02a1-113">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="d02a1-114">Indica si un usuario tiene permiso para crear elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-114">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="d02a1-115">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-116">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="d02a1-116">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="d02a1-117">Indica si un usuario tiene permiso para crear subcarpetas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-117">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="d02a1-118">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-119">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="d02a1-119">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="d02a1-120">Indica si un usuario tiene permiso para eliminar elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-120">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="d02a1-121">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-122">EditItems</span><span class="sxs-lookup"><span data-stu-id="d02a1-122">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="d02a1-123">Indica si un usuario tiene permiso para editar elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-123">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="d02a1-124">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-124">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-125">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="d02a1-125">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="d02a1-126">Indica si un usuario es un contacto de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-126">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="d02a1-127">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-127">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-128">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="d02a1-128">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="d02a1-129">Indica si un usuario es el propietario de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-129">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="d02a1-130">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-130">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-131">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="d02a1-131">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="d02a1-132">Indica si un usuario puede ver una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-132">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="d02a1-133">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-133">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-134">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="d02a1-134">PermissionLevel</span></span>](permissionlevel.md) <br/> |<span data-ttu-id="d02a1-135">Representa la combinación de permisos que un usuario tiene en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-135">Represents the combination of permissions that a user has on a folder.</span></span> <span data-ttu-id="d02a1-136">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-136">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-137">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="d02a1-137">ReadItems (PermissionType)</span></span>](readitems-permissiontype.md) <br/> |<span data-ttu-id="d02a1-138">Indica si un usuario tiene permiso para leer los elementos dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-138">Indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="d02a1-139">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d02a1-140">UserId</span><span class="sxs-lookup"><span data-stu-id="d02a1-140">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="d02a1-141">Identifica un usuario delegado o un usuario que tiene permisos de acceso de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-141">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="d02a1-142">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-142">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d02a1-143">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d02a1-143">Parent elements</span></span>

|<span data-ttu-id="d02a1-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="d02a1-144">**Element**</span></span>|<span data-ttu-id="d02a1-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d02a1-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d02a1-146">Permisos</span><span class="sxs-lookup"><span data-stu-id="d02a1-146">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="d02a1-147">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d02a1-147">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="d02a1-148">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d02a1-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d02a1-149">Notas</span><span class="sxs-lookup"><span data-stu-id="d02a1-149">Remarks</span></span>

<span data-ttu-id="d02a1-150">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d02a1-150">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="d02a1-151">Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d02a1-151">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="d02a1-152">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="d02a1-152">Version differences</span></span>

<span data-ttu-id="d02a1-153">Para las aplicaciones de ese destino Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013, los permisos de carpetas no se devuelven cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d02a1-153">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="d02a1-154">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud de **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="d02a1-154">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d02a1-155">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d02a1-155">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d02a1-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d02a1-156">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d02a1-157">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d02a1-157">Schema Name</span></span>  <br/> |<span data-ttu-id="d02a1-158">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d02a1-158">Types schema</span></span>  <br/> |
|<span data-ttu-id="d02a1-159">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d02a1-159">Validation File</span></span>  <br/> |<span data-ttu-id="d02a1-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d02a1-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d02a1-161">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d02a1-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="d02a1-162">False</span><span class="sxs-lookup"><span data-stu-id="d02a1-162">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d02a1-163">Ver también</span><span class="sxs-lookup"><span data-stu-id="d02a1-163">See also</span></span>



- [<span data-ttu-id="d02a1-164">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d02a1-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d02a1-165">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="d02a1-165">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


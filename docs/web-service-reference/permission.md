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
description: El elemento Permission define el acceso que tiene un usuario a una carpeta.
ms.openlocfilehash: 0f7515dbb06f8423f8d4d95e1391496e8ac73653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459261"
---
# <a name="permission"></a><span data-ttu-id="e1460-103">Permiso</span><span class="sxs-lookup"><span data-stu-id="e1460-103">Permission</span></span>

<span data-ttu-id="e1460-104">El elemento **Permission** define el acceso que tiene un usuario a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-104">The **Permission** element defines the access that a user has to a folder.</span></span> 
  
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

 <span data-ttu-id="e1460-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="e1460-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e1460-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e1460-106">Attributes and elements</span></span>

<span data-ttu-id="e1460-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e1460-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1460-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1460-108">Attributes</span></span>

<span data-ttu-id="e1460-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e1460-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1460-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e1460-110">Child elements</span></span>

|<span data-ttu-id="e1460-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e1460-111">**Element**</span></span>|<span data-ttu-id="e1460-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1460-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1460-113">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="e1460-113">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="e1460-114">Indica si un usuario tiene permiso para crear elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-114">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="e1460-115">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-116">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="e1460-116">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="e1460-117">Indica si un usuario tiene permiso para crear subcarpetas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-117">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="e1460-118">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-119">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="e1460-119">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="e1460-120">Indica si un usuario tiene permiso para eliminar elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-120">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="e1460-121">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-122">EditItems</span><span class="sxs-lookup"><span data-stu-id="e1460-122">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="e1460-123">Indica si un usuario tiene permiso para editar los elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-123">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="e1460-124">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-124">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-125">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="e1460-125">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="e1460-126">Indica si un usuario es un contacto de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-126">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="e1460-127">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-127">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-128">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="e1460-128">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="e1460-129">Indica si un usuario es el propietario de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-129">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="e1460-130">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-130">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-131">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="e1460-131">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="e1460-132">Indica si un usuario puede ver una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-132">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="e1460-133">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-133">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-134">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="e1460-134">PermissionLevel</span></span>](permissionlevel.md) <br/> |<span data-ttu-id="e1460-135">Representa la combinación de permisos que tiene un usuario en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-135">Represents the combination of permissions that a user has on a folder.</span></span> <span data-ttu-id="e1460-136">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-136">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-137">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="e1460-137">ReadItems (PermissionType)</span></span>](readitems-permissiontype.md) <br/> |<span data-ttu-id="e1460-138">Indica si un usuario tiene permiso para leer elementos dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-138">Indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="e1460-139">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e1460-140">UserId</span><span class="sxs-lookup"><span data-stu-id="e1460-140">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="e1460-141">Identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-141">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="e1460-142">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-142">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e1460-143">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e1460-143">Parent elements</span></span>

|<span data-ttu-id="e1460-144">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e1460-144">**Element**</span></span>|<span data-ttu-id="e1460-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1460-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1460-146">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1460-146">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="e1460-147">Contiene todos los permisos configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e1460-147">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="e1460-148">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e1460-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1460-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1460-149">Remarks</span></span>

<span data-ttu-id="e1460-150">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e1460-150">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="e1460-151">Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e1460-151">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="e1460-152">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="e1460-152">Version differences</span></span>

<span data-ttu-id="e1460-153">Para las aplicaciones dirigidas a Exchange Online, Exchange online como parte de Office 365 o a una versión local de Exchange a partir de Exchange 2013, no se devuelven permisos de carpeta cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e1460-153">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="e1460-154">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="e1460-154">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e1460-155">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e1460-155">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1460-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1460-156">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e1460-157">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e1460-157">Schema Name</span></span>  <br/> |<span data-ttu-id="e1460-158">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e1460-158">Types schema</span></span>  <br/> |
|<span data-ttu-id="e1460-159">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e1460-159">Validation File</span></span>  <br/> |<span data-ttu-id="e1460-160">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e1460-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e1460-161">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e1460-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="e1460-162">Falso</span><span class="sxs-lookup"><span data-stu-id="e1460-162">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1460-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1460-163">See also</span></span>



- [<span data-ttu-id="e1460-164">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e1460-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e1460-165">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="e1460-165">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


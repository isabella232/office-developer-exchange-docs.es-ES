---
title: PermissionSet (PermissionSetType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: El elemento PermissionSet contiene todos los permisos que se configuran para una carpeta.
ms.openlocfilehash: 5639ee8ba64742f39c0274f4e3aaa76d75bea42b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468134"
---
# <a name="permissionset-permissionsettype"></a><span data-ttu-id="a217d-103">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="a217d-103">PermissionSet (PermissionSetType)</span></span>

<span data-ttu-id="a217d-104">El elemento **PermissionSet** contiene todos los permisos que se configuran para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a217d-104">The **PermissionSet** element contains all the permissions that are configured for a folder.</span></span> 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="a217d-105">**PermissionSetType**</span><span class="sxs-lookup"><span data-stu-id="a217d-105">**PermissionSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a217d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a217d-106">Attributes and elements</span></span>

<span data-ttu-id="a217d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a217d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a217d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a217d-108">Attributes</span></span>

<span data-ttu-id="a217d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a217d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a217d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a217d-110">Child elements</span></span>

|<span data-ttu-id="a217d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a217d-111">**Element**</span></span>|<span data-ttu-id="a217d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a217d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a217d-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="a217d-113">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="a217d-114">Contiene la colección de permisos para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a217d-114">Contains the collection of permissions for a folder.</span></span> <span data-ttu-id="a217d-115">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="a217d-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="a217d-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="a217d-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="a217d-117">Contiene una matriz de entradas desconocidas que no se pueden resolver contra el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a217d-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="a217d-118">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="a217d-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a217d-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a217d-119">Parent elements</span></span>

|<span data-ttu-id="a217d-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a217d-120">**Element**</span></span>|<span data-ttu-id="a217d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a217d-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a217d-122">Folder</span><span class="sxs-lookup"><span data-stu-id="a217d-122">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="a217d-123">Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="a217d-123">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="a217d-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a217d-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="a217d-125">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="a217d-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a217d-126">Hubiera</span><span class="sxs-lookup"><span data-stu-id="a217d-126">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="a217d-127">Representa una carpeta de contactos contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="a217d-127">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a217d-128">Hubiera</span><span class="sxs-lookup"><span data-stu-id="a217d-128">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="a217d-129">Representa una carpeta de tareas contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="a217d-129">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a217d-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a217d-130">Remarks</span></span>

<span data-ttu-id="a217d-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a217d-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="a217d-132">Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a217d-132">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="a217d-133">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="a217d-133">Version differences</span></span>

<span data-ttu-id="a217d-134">Para las aplicaciones dirigidas a Exchange Online, Exchange online como parte de Office 365 o a una versión local de Exchange a partir de Exchange 2013, no se devuelven permisos de carpeta cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a217d-134">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="a217d-135">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="a217d-135">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a217d-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a217d-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a217d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="a217d-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a217d-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a217d-138">Schema Name</span></span>  <br/> |<span data-ttu-id="a217d-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a217d-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="a217d-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a217d-140">Validation File</span></span>  <br/> |<span data-ttu-id="a217d-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a217d-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a217d-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a217d-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="a217d-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a217d-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a217d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a217d-144">See also</span></span>



- [<span data-ttu-id="a217d-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a217d-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="a217d-146">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="a217d-146">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


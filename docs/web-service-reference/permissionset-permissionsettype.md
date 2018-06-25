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
description: El elemento PermissionSet contiene todos los permisos que están configurados para una carpeta.
ms.openlocfilehash: 0fa0ac78a0db2bf382ad413cbb8bd072aa88c6fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836732"
---
# <a name="permissionset-permissionsettype"></a><span data-ttu-id="83d47-103">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="83d47-103">PermissionSet (PermissionSetType)</span></span>

<span data-ttu-id="83d47-104">El elemento **PermissionSet** contiene todos los permisos que están configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="83d47-104">The **PermissionSet** element contains all the permissions that are configured for a folder.</span></span> 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="83d47-105">**PermissionSetType**</span><span class="sxs-lookup"><span data-stu-id="83d47-105">**PermissionSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83d47-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="83d47-106">Attributes and elements</span></span>

<span data-ttu-id="83d47-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="83d47-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83d47-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="83d47-108">Attributes</span></span>

<span data-ttu-id="83d47-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83d47-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83d47-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83d47-110">Child elements</span></span>

|<span data-ttu-id="83d47-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="83d47-111">**Element**</span></span>|<span data-ttu-id="83d47-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83d47-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83d47-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="83d47-113">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="83d47-114">Contiene la colección de permisos para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="83d47-114">Contains the collection of permissions for a folder.</span></span> <span data-ttu-id="83d47-115">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="83d47-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="83d47-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="83d47-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="83d47-117">Contiene una matriz de las entradas desconocidas que no se puede resolver con el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="83d47-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="83d47-118">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="83d47-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83d47-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="83d47-119">Parent elements</span></span>

|<span data-ttu-id="83d47-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="83d47-120">**Element**</span></span>|<span data-ttu-id="83d47-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83d47-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83d47-122">Folder</span><span class="sxs-lookup"><span data-stu-id="83d47-122">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="83d47-123">Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="83d47-123">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="83d47-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="83d47-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="83d47-125">Representa una carpeta de búsqueda que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="83d47-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="83d47-126">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="83d47-126">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="83d47-127">Representa una carpeta de contactos que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="83d47-127">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="83d47-128">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="83d47-128">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="83d47-129">Representa una carpeta de tareas que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="83d47-129">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83d47-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83d47-130">Remarks</span></span>

<span data-ttu-id="83d47-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="83d47-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="83d47-132">Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="83d47-132">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="83d47-133">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="83d47-133">Version differences</span></span>

<span data-ttu-id="83d47-134">Para las aplicaciones de ese destino Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013, los permisos de carpetas no se devuelven cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="83d47-134">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="83d47-135">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud de **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="83d47-135">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="83d47-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="83d47-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83d47-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83d47-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83d47-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="83d47-138">Schema Name</span></span>  <br/> |<span data-ttu-id="83d47-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="83d47-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="83d47-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="83d47-140">Validation File</span></span>  <br/> |<span data-ttu-id="83d47-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83d47-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83d47-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="83d47-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="83d47-143">False</span><span class="sxs-lookup"><span data-stu-id="83d47-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83d47-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="83d47-144">See also</span></span>



- [<span data-ttu-id="83d47-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="83d47-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="83d47-146">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="83d47-146">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


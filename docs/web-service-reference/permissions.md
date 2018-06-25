---
title: Permisos
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permissions
api_type:
- schema
ms.assetid: 2ba50bd9-819f-4e5f-a3bb-85a0a87d8a86
description: El elemento de permisos contiene la colección de permisos para una carpeta.
ms.openlocfilehash: 08d015c3b1afb58fce0fb4b99466965cc5c29fc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836727"
---
# <a name="permissions"></a><span data-ttu-id="026f1-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="026f1-103">Permissions</span></span>

<span data-ttu-id="026f1-104">El elemento de **permisos** contiene la colección de permisos para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="026f1-104">The **Permissions** element contains the collection of permissions for a folder.</span></span> 
  
```XML
<Permissions>
   <Permission/>
</Permissions>
```

 <span data-ttu-id="026f1-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="026f1-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="026f1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="026f1-106">Attributes and elements</span></span>

<span data-ttu-id="026f1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="026f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="026f1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="026f1-108">Attributes</span></span>

<span data-ttu-id="026f1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="026f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="026f1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="026f1-110">Child elements</span></span>

|<span data-ttu-id="026f1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="026f1-111">**Element**</span></span>|<span data-ttu-id="026f1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="026f1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="026f1-113">Permission</span><span class="sxs-lookup"><span data-stu-id="026f1-113">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="026f1-114">Define el acceso que tiene un delegado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="026f1-114">Defines the access that a delegate has to a folder.</span></span> <span data-ttu-id="026f1-115">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="026f1-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="026f1-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="026f1-116">Parent elements</span></span>

|<span data-ttu-id="026f1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="026f1-117">**Element**</span></span>|<span data-ttu-id="026f1-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="026f1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="026f1-119">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="026f1-119">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="026f1-120">Contiene todos los permisos que están configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="026f1-120">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="026f1-121">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="026f1-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="026f1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="026f1-122">Remarks</span></span>

<span data-ttu-id="026f1-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="026f1-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="026f1-124">Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="026f1-124">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="026f1-125">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="026f1-125">Version differences</span></span>

<span data-ttu-id="026f1-126">Para las aplicaciones de ese destino Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013, los permisos de carpetas no se devuelven cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="026f1-126">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="026f1-127">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud de **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="026f1-127">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="026f1-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="026f1-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="026f1-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="026f1-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="026f1-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="026f1-130">Schema Name</span></span>  <br/> |<span data-ttu-id="026f1-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="026f1-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="026f1-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="026f1-132">Validation File</span></span>  <br/> |<span data-ttu-id="026f1-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="026f1-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="026f1-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="026f1-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="026f1-135">False</span><span class="sxs-lookup"><span data-stu-id="026f1-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="026f1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="026f1-136">See also</span></span>



- [<span data-ttu-id="026f1-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="026f1-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="026f1-138">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="026f1-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


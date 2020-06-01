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
description: El elemento Permissions contiene la colección de permisos para una carpeta.
ms.openlocfilehash: b8616cefdb8c453106753fb0788a6c7d6a0ded79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459219"
---
# <a name="permissions"></a><span data-ttu-id="89579-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="89579-103">Permissions</span></span>

<span data-ttu-id="89579-104">El elemento **Permissions** contiene la colección de permisos para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="89579-104">The **Permissions** element contains the collection of permissions for a folder.</span></span> 
  
```XML
<Permissions>
   <Permission/>
</Permissions>
```

 <span data-ttu-id="89579-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="89579-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89579-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="89579-106">Attributes and elements</span></span>

<span data-ttu-id="89579-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="89579-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89579-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="89579-108">Attributes</span></span>

<span data-ttu-id="89579-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="89579-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89579-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89579-110">Child elements</span></span>

|<span data-ttu-id="89579-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="89579-111">**Element**</span></span>|<span data-ttu-id="89579-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89579-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89579-113">Permiso</span><span class="sxs-lookup"><span data-stu-id="89579-113">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="89579-114">Define el acceso que un delegado tiene a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="89579-114">Defines the access that a delegate has to a folder.</span></span> <span data-ttu-id="89579-115">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="89579-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="89579-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="89579-116">Parent elements</span></span>

|<span data-ttu-id="89579-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="89579-117">**Element**</span></span>|<span data-ttu-id="89579-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89579-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89579-119">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="89579-119">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="89579-120">Contiene todos los permisos que se configuran para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="89579-120">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="89579-121">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="89579-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89579-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89579-122">Remarks</span></span>

<span data-ttu-id="89579-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="89579-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="89579-124">Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="89579-124">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="89579-125">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="89579-125">Version differences</span></span>

<span data-ttu-id="89579-126">Para las aplicaciones dirigidas a Exchange Online, Exchange online como parte de Office 365 o a una versión local de Exchange a partir de Exchange 2013, no se devuelven permisos de carpeta cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="89579-126">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="89579-127">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="89579-127">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="89579-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="89579-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89579-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="89579-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89579-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="89579-130">Schema Name</span></span>  <br/> |<span data-ttu-id="89579-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="89579-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="89579-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="89579-132">Validation File</span></span>  <br/> |<span data-ttu-id="89579-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="89579-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="89579-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="89579-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="89579-135">Falso</span><span class="sxs-lookup"><span data-stu-id="89579-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89579-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="89579-136">See also</span></span>



- [<span data-ttu-id="89579-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="89579-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="89579-138">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="89579-138">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


---
title: PermissionSet (CalendarPermissionSetType)
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
ms.assetid: 75f20033-85eb-4627-b4f8-be85e4889e96
description: El elemento PermissionSet contiene todos los permisos que están configurados para una carpeta de calendario.
ms.openlocfilehash: b2e642fd2ee8ded4d0d4c67509a5587f7b1efa8a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836728"
---
# <a name="permissionset-calendarpermissionsettype"></a><span data-ttu-id="13911-103">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="13911-103">PermissionSet (CalendarPermissionSetType)</span></span>

<span data-ttu-id="13911-104">El elemento **PermissionSet** contiene todos los permisos que están configurados para una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="13911-104">The **PermissionSet** element contains all the permissions that are configured for a calendar folder.</span></span> 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="13911-105">**CalendarPermissonSetType**</span><span class="sxs-lookup"><span data-stu-id="13911-105">**CalendarPermissonSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13911-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="13911-106">Attributes and elements</span></span>

<span data-ttu-id="13911-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="13911-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13911-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="13911-108">Attributes</span></span>

<span data-ttu-id="13911-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="13911-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13911-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13911-110">Child elements</span></span>

|<span data-ttu-id="13911-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="13911-111">**Element**</span></span>|<span data-ttu-id="13911-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13911-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13911-113">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="13911-113">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="13911-114">Contiene una matriz de permisos para una carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="13911-114">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="13911-115">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="13911-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="13911-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="13911-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="13911-117">Contiene una matriz de las entradas desconocidas que no se puede resolver con el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="13911-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="13911-118">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="13911-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13911-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13911-119">Parent elements</span></span>

|<span data-ttu-id="13911-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="13911-120">**Element**</span></span>|<span data-ttu-id="13911-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13911-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13911-122">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="13911-122">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="13911-123">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="13911-123">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13911-124">Notas</span><span class="sxs-lookup"><span data-stu-id="13911-124">Remarks</span></span>

<span data-ttu-id="13911-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="13911-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="13911-126">Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="13911-126">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="13911-127">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="13911-127">Version differences</span></span>

<span data-ttu-id="13911-128">Para las aplicaciones de ese destino Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013, los permisos de carpetas no se devuelven cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="13911-128">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="13911-129">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud de **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="13911-129">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="13911-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13911-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13911-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13911-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13911-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="13911-132">Schema Name</span></span>  <br/> |<span data-ttu-id="13911-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="13911-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="13911-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="13911-134">Validation File</span></span>  <br/> |<span data-ttu-id="13911-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="13911-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13911-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="13911-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="13911-137">False</span><span class="sxs-lookup"><span data-stu-id="13911-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13911-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="13911-138">See also</span></span>



- [<span data-ttu-id="13911-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="13911-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="13911-140">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="13911-140">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


---
title: CalendarPermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissions
api_type:
- schema
ms.assetid: 9b659d83-45fb-42a2-b052-5bc4dbe3854d
description: El elemento CalendarPermissions contiene una matriz de permisos para una carpeta del calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 3dee635e4449cbb3717f5d2fab8838f3e43102a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763711"
---
# <a name="calendarpermissions"></a><span data-ttu-id="07629-104">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="07629-104">CalendarPermissions</span></span>

<span data-ttu-id="07629-105">El elemento **CalendarPermissions** contiene una matriz de permisos para una carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="07629-105">The **CalendarPermissions** element contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="07629-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="07629-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissions>
   <PermissionSet/>
</CalendarPermissions>
```

 <span data-ttu-id="07629-107">**ArrayOfCalendarPermissionsType**</span><span class="sxs-lookup"><span data-stu-id="07629-107">**ArrayOfCalendarPermissionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07629-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07629-108">Attributes and elements</span></span>

<span data-ttu-id="07629-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07629-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07629-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="07629-110">Attributes</span></span>

<span data-ttu-id="07629-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07629-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07629-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07629-112">Child elements</span></span>

|<span data-ttu-id="07629-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="07629-113">**Element**</span></span>|<span data-ttu-id="07629-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07629-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07629-115">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="07629-115">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="07629-116">Define el acceso que tiene un usuario delegado a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="07629-116">Defines the access that a delegate user has to a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07629-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07629-117">Parent elements</span></span>

|<span data-ttu-id="07629-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="07629-118">**Element**</span></span>|<span data-ttu-id="07629-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07629-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07629-120">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="07629-120">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="07629-121">Contiene todos los permisos configurados para una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="07629-121">Contains all the configured permissions for a calendar folder.</span></span> <span data-ttu-id="07629-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="07629-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07629-123">Notas</span><span class="sxs-lookup"><span data-stu-id="07629-123">Remarks</span></span>

<span data-ttu-id="07629-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="07629-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07629-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07629-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07629-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07629-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07629-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07629-127">Schema Name</span></span>  <br/> |<span data-ttu-id="07629-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="07629-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="07629-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07629-129">Validation File</span></span>  <br/> |<span data-ttu-id="07629-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07629-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07629-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07629-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="07629-132">False</span><span class="sxs-lookup"><span data-stu-id="07629-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07629-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="07629-133">See also</span></span>



- [<span data-ttu-id="07629-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="07629-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="07629-135">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="07629-135">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


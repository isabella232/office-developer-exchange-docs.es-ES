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
description: El elemento CalendarPermissions contiene una matriz de permisos de calendario para una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: f072339212d0fdff3983fbfb6bc8f53c272350c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529472"
---
# <a name="calendarpermissions"></a><span data-ttu-id="ce6fe-104">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="ce6fe-104">CalendarPermissions</span></span>

<span data-ttu-id="ce6fe-105">El elemento **CalendarPermissions** contiene una matriz de permisos de calendario para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ce6fe-105">The **CalendarPermissions** element contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="ce6fe-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ce6fe-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissions>
   <PermissionSet/>
</CalendarPermissions>
```

 <span data-ttu-id="ce6fe-107">**ArrayOfCalendarPermissionsType**</span><span class="sxs-lookup"><span data-stu-id="ce6fe-107">**ArrayOfCalendarPermissionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce6fe-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ce6fe-108">Attributes and elements</span></span>

<span data-ttu-id="ce6fe-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ce6fe-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce6fe-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce6fe-110">Attributes</span></span>

<span data-ttu-id="ce6fe-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ce6fe-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce6fe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce6fe-112">Child elements</span></span>

|<span data-ttu-id="ce6fe-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce6fe-113">**Element**</span></span>|<span data-ttu-id="ce6fe-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce6fe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce6fe-115">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ce6fe-115">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ce6fe-116">Define el acceso que un usuario delegado tiene a una carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="ce6fe-116">Defines the access that a delegate user has to a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce6fe-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ce6fe-117">Parent elements</span></span>

|<span data-ttu-id="ce6fe-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce6fe-118">**Element**</span></span>|<span data-ttu-id="ce6fe-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce6fe-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce6fe-120">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="ce6fe-120">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="ce6fe-121">Contiene todos los permisos configurados para una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="ce6fe-121">Contains all the configured permissions for a calendar folder.</span></span> <span data-ttu-id="ce6fe-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ce6fe-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce6fe-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce6fe-123">Remarks</span></span>

<span data-ttu-id="ce6fe-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ce6fe-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce6fe-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ce6fe-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce6fe-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce6fe-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce6fe-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ce6fe-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ce6fe-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ce6fe-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce6fe-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ce6fe-129">Validation File</span></span>  <br/> |<span data-ttu-id="ce6fe-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ce6fe-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce6fe-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ce6fe-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce6fe-132">Falso</span><span class="sxs-lookup"><span data-stu-id="ce6fe-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce6fe-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce6fe-133">See also</span></span>



- [<span data-ttu-id="ce6fe-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ce6fe-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ce6fe-135">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="ce6fe-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


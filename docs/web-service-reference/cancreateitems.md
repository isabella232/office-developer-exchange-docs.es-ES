---
title: CanCreateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanCreateItems
api_type:
- schema
ms.assetid: c4574e9a-3c42-40a1-a5f9-79b6560e9b30
description: El elemento CanCreateItems indica si un usuario tiene permiso para crear elementos en una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 313699a15ef3038dd9114c18b76b29aba15e5ab7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763727"
---
# <a name="cancreateitems"></a><span data-ttu-id="c2f2e-104">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="c2f2e-104">CanCreateItems</span></span>

<span data-ttu-id="c2f2e-105">El elemento **CanCreateItems** indica si un usuario tiene permiso para crear elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-105">The **CanCreateItems** element indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="c2f2e-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c2f2e-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CanCreateItems/>
```

 <span data-ttu-id="c2f2e-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2f2e-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2f2e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c2f2e-108">Attributes and elements</span></span>

<span data-ttu-id="c2f2e-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2f2e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2f2e-110">Attributes</span></span>

<span data-ttu-id="c2f2e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2f2e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c2f2e-112">Child elements</span></span>

<span data-ttu-id="c2f2e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c2f2e-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c2f2e-114">Parent elements</span></span>

|<span data-ttu-id="c2f2e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2f2e-115">**Element**</span></span>|<span data-ttu-id="c2f2e-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2f2e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2f2e-117">Permission</span><span class="sxs-lookup"><span data-stu-id="c2f2e-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="c2f2e-118">Define el acceso que tiene un usuario a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="c2f2e-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="c2f2e-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="c2f2e-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="c2f2e-121">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-121">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="c2f2e-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c2f2e-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c2f2e-123">Text value</span></span>

<span data-ttu-id="c2f2e-124">Un valor de texto de **true** indica que el usuario puede crear elementos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-124">A text value of **true** indicates that the user can create items in the folder.</span></span> <span data-ttu-id="c2f2e-125">Un valor de **false** indica que el usuario no puede crear elementos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-125">A value of **false** indicates that the user cannot create items in the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c2f2e-126">Notas</span><span class="sxs-lookup"><span data-stu-id="c2f2e-126">Remarks</span></span>

<span data-ttu-id="c2f2e-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c2f2e-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2f2e-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c2f2e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2f2e-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2f2e-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2f2e-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c2f2e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c2f2e-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c2f2e-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="c2f2e-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c2f2e-132">Validation File</span></span>  <br/> |<span data-ttu-id="c2f2e-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c2f2e-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2f2e-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c2f2e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2f2e-135">False</span><span class="sxs-lookup"><span data-stu-id="c2f2e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2f2e-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="c2f2e-136">See also</span></span>



- [<span data-ttu-id="c2f2e-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c2f2e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c2f2e-138">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="c2f2e-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


---
title: IsFolderOwner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFolderOwner
api_type:
- schema
ms.assetid: 6541ee78-d6e6-42a7-8e7a-d8736172b245
description: El elemento IsFolderOwner indica si un usuario es el propietario de una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: a8838b2a7ed1b16c1e332d34a38038ba8254fc3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836016"
---
# <a name="isfolderowner"></a><span data-ttu-id="b71ed-104">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="b71ed-104">IsFolderOwner</span></span>

<span data-ttu-id="b71ed-105">El elemento **IsFolderOwner** indica si un usuario es el propietario de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b71ed-105">The **IsFolderOwner** element indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="b71ed-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b71ed-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<IsFolderOwner/>
```

 <span data-ttu-id="b71ed-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b71ed-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b71ed-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b71ed-108">Attributes and elements</span></span>

<span data-ttu-id="b71ed-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b71ed-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b71ed-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b71ed-110">Attributes</span></span>

<span data-ttu-id="b71ed-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b71ed-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b71ed-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b71ed-112">Child elements</span></span>

<span data-ttu-id="b71ed-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b71ed-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b71ed-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b71ed-114">Parent elements</span></span>

|<span data-ttu-id="b71ed-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b71ed-115">**Element**</span></span>|<span data-ttu-id="b71ed-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b71ed-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b71ed-117">Permission</span><span class="sxs-lookup"><span data-stu-id="b71ed-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="b71ed-118">Define el acceso que tiene un usuario a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b71ed-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="b71ed-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="b71ed-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b71ed-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="b71ed-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="b71ed-121">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="b71ed-121">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="b71ed-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="b71ed-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b71ed-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b71ed-123">Text value</span></span>

<span data-ttu-id="b71ed-124">Un valor de texto de **true** indica que el usuario es el propietario de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b71ed-124">A text value of **true** indicates that the user is the owner of the folder.</span></span> <span data-ttu-id="b71ed-125">Un valor de **false** indica que el usuario no es el propietario de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b71ed-125">A value of **false** indicates that the user is not the owner of the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b71ed-126">Notas</span><span class="sxs-lookup"><span data-stu-id="b71ed-126">Remarks</span></span>

<span data-ttu-id="b71ed-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b71ed-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b71ed-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b71ed-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b71ed-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b71ed-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b71ed-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b71ed-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b71ed-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b71ed-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="b71ed-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b71ed-132">Validation File</span></span>  <br/> |<span data-ttu-id="b71ed-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b71ed-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b71ed-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b71ed-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b71ed-135">False</span><span class="sxs-lookup"><span data-stu-id="b71ed-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b71ed-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="b71ed-136">See also</span></span>



- [<span data-ttu-id="b71ed-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b71ed-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b71ed-138">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="b71ed-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


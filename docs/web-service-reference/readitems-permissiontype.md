---
title: ReadItems (PermissionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: 0a11a802-28e2-436b-b5a9-30fd064675a6
description: El elemento ReadItems indica si un usuario tiene permiso para leer elementos dentro de una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: bf266c77106f25b90ffd174e25fb0c3972ab91cb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836961"
---
# <a name="readitems-permissiontype"></a><span data-ttu-id="4680b-104">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="4680b-104">ReadItems (PermissionType)</span></span>

<span data-ttu-id="4680b-105">El elemento **ReadItems** indica si un usuario tiene permiso para leer elementos dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4680b-105">The **ReadItems** element indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="4680b-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4680b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or FullDetails</ReadItems>
```

 <span data-ttu-id="4680b-107">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="4680b-107">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4680b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4680b-108">Attributes and elements</span></span>

<span data-ttu-id="4680b-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4680b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4680b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="4680b-110">Attributes</span></span>

<span data-ttu-id="4680b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4680b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4680b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4680b-112">Child elements</span></span>

<span data-ttu-id="4680b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4680b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4680b-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4680b-114">Parent elements</span></span>

|<span data-ttu-id="4680b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="4680b-115">**Element**</span></span>|<span data-ttu-id="4680b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4680b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4680b-117">Permission</span><span class="sxs-lookup"><span data-stu-id="4680b-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="4680b-118">Define el acceso que tiene un usuario a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4680b-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="4680b-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="4680b-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4680b-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4680b-120">Text value</span></span>

<span data-ttu-id="4680b-121">En la siguiente tabla se enumera los valores posibles para el elemento **ReadItems** .</span><span class="sxs-lookup"><span data-stu-id="4680b-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="4680b-122">**Valores de texto de elemento ReadItems**</span><span class="sxs-lookup"><span data-stu-id="4680b-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="4680b-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4680b-123">**Value**</span></span>|<span data-ttu-id="4680b-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4680b-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4680b-125">None</span><span class="sxs-lookup"><span data-stu-id="4680b-125">None</span></span>  <br/> |<span data-ttu-id="4680b-126">Indica que el usuario no tiene permiso para leer elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4680b-126">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="4680b-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="4680b-127">FullDetails</span></span>  <br/> |<span data-ttu-id="4680b-128">Indica que el usuario tiene permiso para leer todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4680b-128">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4680b-129">Notas</span><span class="sxs-lookup"><span data-stu-id="4680b-129">Remarks</span></span>

<span data-ttu-id="4680b-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4680b-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4680b-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4680b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4680b-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4680b-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4680b-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4680b-133">Schema Name</span></span>  <br/> |<span data-ttu-id="4680b-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4680b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="4680b-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4680b-135">Validation File</span></span>  <br/> |<span data-ttu-id="4680b-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4680b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4680b-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4680b-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="4680b-138">False</span><span class="sxs-lookup"><span data-stu-id="4680b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4680b-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="4680b-139">See also</span></span>



- [<span data-ttu-id="4680b-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4680b-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4680b-141">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="4680b-141">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


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
ms.openlocfilehash: af6ef5107b5e4f2b3071c0bc9b4b528efea6dcca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468274"
---
# <a name="readitems-permissiontype"></a><span data-ttu-id="e9e06-104">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="e9e06-104">ReadItems (PermissionType)</span></span>

<span data-ttu-id="e9e06-105">El elemento **ReadItems** indica si un usuario tiene permiso para leer elementos dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e9e06-105">The **ReadItems** element indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="e9e06-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e9e06-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or FullDetails</ReadItems>
```

 <span data-ttu-id="e9e06-107">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="e9e06-107">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9e06-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e9e06-108">Attributes and elements</span></span>

<span data-ttu-id="e9e06-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e9e06-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9e06-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e9e06-110">Attributes</span></span>

<span data-ttu-id="e9e06-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e9e06-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9e06-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e9e06-112">Child elements</span></span>

<span data-ttu-id="e9e06-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e9e06-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e9e06-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e9e06-114">Parent elements</span></span>

|<span data-ttu-id="e9e06-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e9e06-115">**Element**</span></span>|<span data-ttu-id="e9e06-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9e06-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9e06-117">Permiso</span><span class="sxs-lookup"><span data-stu-id="e9e06-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="e9e06-118">Define el acceso que un usuario tiene a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e9e06-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="e9e06-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="e9e06-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e9e06-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e9e06-120">Text value</span></span>

<span data-ttu-id="e9e06-121">En la siguiente tabla se enumeran los valores posibles para el elemento **ReadItems** .</span><span class="sxs-lookup"><span data-stu-id="e9e06-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="e9e06-122">**Valores de texto del elemento ReadItems**</span><span class="sxs-lookup"><span data-stu-id="e9e06-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="e9e06-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e9e06-123">**Value**</span></span>|<span data-ttu-id="e9e06-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9e06-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9e06-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e9e06-125">None</span></span>  <br/> |<span data-ttu-id="e9e06-126">Indica que el usuario no tiene permiso para leer los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e9e06-126">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="e9e06-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e9e06-127">FullDetails</span></span>  <br/> |<span data-ttu-id="e9e06-128">Indica que el usuario tiene permiso para leer todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e9e06-128">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9e06-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9e06-129">Remarks</span></span>

<span data-ttu-id="e9e06-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e9e06-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9e06-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e9e06-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9e06-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9e06-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e9e06-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e9e06-133">Schema Name</span></span>  <br/> |<span data-ttu-id="e9e06-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e9e06-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="e9e06-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e9e06-135">Validation File</span></span>  <br/> |<span data-ttu-id="e9e06-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e9e06-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e9e06-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e9e06-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="e9e06-138">Falso</span><span class="sxs-lookup"><span data-stu-id="e9e06-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9e06-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9e06-139">See also</span></span>



- [<span data-ttu-id="e9e06-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e9e06-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e9e06-141">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="e9e06-141">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


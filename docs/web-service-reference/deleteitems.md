---
title: DeleteItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItems
api_type:
- schema
ms.assetid: a5898bfc-f5ae-451d-9713-3e55864c690c
description: El elemento DeleteItems indica qué elementos de una carpeta de un usuario tiene permiso para eliminar. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 0be2154d1ceb6a995df8b27033fdc59bca81f9ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764110"
---
# <a name="deleteitems"></a><span data-ttu-id="0e737-104">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="0e737-104">DeleteItems</span></span>

<span data-ttu-id="0e737-105">El elemento **DeleteItems** indica qué elementos de una carpeta de un usuario tiene permiso para eliminar.</span><span class="sxs-lookup"><span data-stu-id="0e737-105">The **DeleteItems** element indicates which items in a folder a user has permission to delete.</span></span> <span data-ttu-id="0e737-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0e737-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DeleteItems>None or Owned or All</DeleteItems>
```

 <span data-ttu-id="0e737-107">**PermissionActionType**</span><span class="sxs-lookup"><span data-stu-id="0e737-107">**PermissionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e737-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e737-108">Attributes and elements</span></span>

<span data-ttu-id="0e737-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e737-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e737-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e737-110">Attributes</span></span>

<span data-ttu-id="0e737-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0e737-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e737-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e737-112">Child elements</span></span>

<span data-ttu-id="0e737-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0e737-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0e737-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e737-114">Parent elements</span></span>

|<span data-ttu-id="0e737-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e737-115">**Element**</span></span>|<span data-ttu-id="0e737-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e737-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e737-117">Permission</span><span class="sxs-lookup"><span data-stu-id="0e737-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="0e737-118">Define el acceso que tiene un usuario a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e737-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="0e737-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="0e737-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0e737-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="0e737-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="0e737-121">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="0e737-121">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="0e737-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="0e737-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0e737-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0e737-123">Text value</span></span>

<span data-ttu-id="0e737-124">En la siguiente tabla se enumera los valores posibles para el elemento **DeleteItems** .</span><span class="sxs-lookup"><span data-stu-id="0e737-124">The following table lists the possible values for the **DeleteItems** element.</span></span> 
  
<span data-ttu-id="0e737-125">**Valores de texto de elemento DeleteItems**</span><span class="sxs-lookup"><span data-stu-id="0e737-125">**DeleteItems element text values**</span></span>

|<span data-ttu-id="0e737-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0e737-126">**Value**</span></span>|<span data-ttu-id="0e737-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e737-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e737-128">None</span><span class="sxs-lookup"><span data-stu-id="0e737-128">None</span></span>  <br/> |<span data-ttu-id="0e737-129">Indica que el usuario no tiene permiso para eliminar elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e737-129">Indicates that the user does not have permission to delete items in the folder.</span></span>  <br/> |
|<span data-ttu-id="0e737-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e737-130">Owned</span></span>  <br/> |<span data-ttu-id="0e737-131">Indica que el usuario tiene permiso para eliminar los elementos que posee el usuario en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e737-131">Indicates that the user has permission to delete the items that the user owns in the folder.</span></span>  <br/> |
|<span data-ttu-id="0e737-132">Todos</span><span class="sxs-lookup"><span data-stu-id="0e737-132">All</span></span>  <br/> |<span data-ttu-id="0e737-133">Indica que el usuario tiene permiso para eliminar todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0e737-133">Indicates that the user has permission to delete all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e737-134">Notas</span><span class="sxs-lookup"><span data-stu-id="0e737-134">Remarks</span></span>

<span data-ttu-id="0e737-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0e737-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e737-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e737-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e737-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e737-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0e737-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e737-138">Schema Name</span></span>  <br/> |<span data-ttu-id="0e737-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0e737-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="0e737-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e737-140">Validation File</span></span>  <br/> |<span data-ttu-id="0e737-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0e737-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0e737-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e737-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e737-143">False</span><span class="sxs-lookup"><span data-stu-id="0e737-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e737-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="0e737-144">See also</span></span>

- [<span data-ttu-id="0e737-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0e737-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0e737-146">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="0e737-146">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


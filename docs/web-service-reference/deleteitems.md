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
description: El elemento DeleteItems indica qué elementos de una carpeta tiene permiso para eliminar un usuario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: a0bbefc8b021d047bb2e001669c3e92a6e2536ce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454410"
---
# <a name="deleteitems"></a><span data-ttu-id="542ac-104">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="542ac-104">DeleteItems</span></span>

<span data-ttu-id="542ac-105">El elemento **DeleteItems** indica qué elementos de una carpeta tiene permiso para eliminar un usuario.</span><span class="sxs-lookup"><span data-stu-id="542ac-105">The **DeleteItems** element indicates which items in a folder a user has permission to delete.</span></span> <span data-ttu-id="542ac-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="542ac-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DeleteItems>None or Owned or All</DeleteItems>
```

 <span data-ttu-id="542ac-107">**PermissionActionType**</span><span class="sxs-lookup"><span data-stu-id="542ac-107">**PermissionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="542ac-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="542ac-108">Attributes and elements</span></span>

<span data-ttu-id="542ac-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="542ac-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="542ac-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="542ac-110">Attributes</span></span>

<span data-ttu-id="542ac-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="542ac-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="542ac-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="542ac-112">Child elements</span></span>

<span data-ttu-id="542ac-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="542ac-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="542ac-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="542ac-114">Parent elements</span></span>

|<span data-ttu-id="542ac-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="542ac-115">**Element**</span></span>|<span data-ttu-id="542ac-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="542ac-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="542ac-117">Permiso</span><span class="sxs-lookup"><span data-stu-id="542ac-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="542ac-118">Define el acceso que un usuario tiene a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="542ac-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="542ac-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="542ac-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="542ac-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="542ac-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="542ac-121">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="542ac-121">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="542ac-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="542ac-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="542ac-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="542ac-123">Text value</span></span>

<span data-ttu-id="542ac-124">En la siguiente tabla se enumeran los valores posibles para el elemento **DeleteItems** .</span><span class="sxs-lookup"><span data-stu-id="542ac-124">The following table lists the possible values for the **DeleteItems** element.</span></span> 
  
<span data-ttu-id="542ac-125">**Valores de texto del elemento DeleteItems**</span><span class="sxs-lookup"><span data-stu-id="542ac-125">**DeleteItems element text values**</span></span>

|<span data-ttu-id="542ac-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="542ac-126">**Value**</span></span>|<span data-ttu-id="542ac-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="542ac-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="542ac-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="542ac-128">None</span></span>  <br/> |<span data-ttu-id="542ac-129">Indica que el usuario no tiene permiso para eliminar elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="542ac-129">Indicates that the user does not have permission to delete items in the folder.</span></span>  <br/> |
|<span data-ttu-id="542ac-130">Estatal</span><span class="sxs-lookup"><span data-stu-id="542ac-130">Owned</span></span>  <br/> |<span data-ttu-id="542ac-131">Indica que el usuario tiene permiso para eliminar los elementos que el usuario posee en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="542ac-131">Indicates that the user has permission to delete the items that the user owns in the folder.</span></span>  <br/> |
|<span data-ttu-id="542ac-132">Todo</span><span class="sxs-lookup"><span data-stu-id="542ac-132">All</span></span>  <br/> |<span data-ttu-id="542ac-133">Indica que el usuario tiene permiso para eliminar todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="542ac-133">Indicates that the user has permission to delete all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="542ac-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="542ac-134">Remarks</span></span>

<span data-ttu-id="542ac-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="542ac-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="542ac-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="542ac-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="542ac-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="542ac-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="542ac-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="542ac-138">Schema Name</span></span>  <br/> |<span data-ttu-id="542ac-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="542ac-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="542ac-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="542ac-140">Validation File</span></span>  <br/> |<span data-ttu-id="542ac-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="542ac-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="542ac-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="542ac-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="542ac-143">Falso</span><span class="sxs-lookup"><span data-stu-id="542ac-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="542ac-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="542ac-144">See also</span></span>

- [<span data-ttu-id="542ac-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="542ac-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="542ac-146">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="542ac-146">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


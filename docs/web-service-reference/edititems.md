---
title: EditItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EditItems
api_type:
- schema
ms.assetid: 1cb14493-c999-4d66-b82c-ecb410dc1c00
description: El elemento EditItems indica qué elementos de una carpeta tiene permiso para editar un usuario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 0c3800b4d242dccb7455e0d0dea74e766db22854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459254"
---
# <a name="edititems"></a><span data-ttu-id="2c036-104">EditItems</span><span class="sxs-lookup"><span data-stu-id="2c036-104">EditItems</span></span>

<span data-ttu-id="2c036-105">El elemento **EditItems** indica qué elementos de una carpeta tiene permiso para editar un usuario.</span><span class="sxs-lookup"><span data-stu-id="2c036-105">The **EditItems** element indicates which items in a folder a user has permission to edit.</span></span> <span data-ttu-id="2c036-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2c036-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<EditItems>None or Owned or All</EditItems>
```

 <span data-ttu-id="2c036-107">**PermissionActionType**</span><span class="sxs-lookup"><span data-stu-id="2c036-107">**PermissionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c036-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2c036-108">Attributes and elements</span></span>

<span data-ttu-id="2c036-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2c036-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c036-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2c036-110">Attributes</span></span>

<span data-ttu-id="2c036-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2c036-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c036-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c036-112">Child elements</span></span>

<span data-ttu-id="2c036-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2c036-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c036-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2c036-114">Parent elements</span></span>

|<span data-ttu-id="2c036-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2c036-115">**Element**</span></span>|<span data-ttu-id="2c036-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c036-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c036-117">Permiso</span><span class="sxs-lookup"><span data-stu-id="2c036-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="2c036-118">Define el acceso que un usuario tiene a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c036-118">Defines the access that a user has to a folder.</span></span> <span data-ttu-id="2c036-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="2c036-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="2c036-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="2c036-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="2c036-121">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="2c036-121">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="2c036-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="2c036-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c036-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2c036-123">Text value</span></span>

<span data-ttu-id="2c036-124">En la siguiente tabla se enumeran los valores posibles para el elemento **EditItems** .</span><span class="sxs-lookup"><span data-stu-id="2c036-124">The following table lists the possible values for the **EditItems** element.</span></span> 
  
<span data-ttu-id="2c036-125">**Valores de texto del elemento EditItems**</span><span class="sxs-lookup"><span data-stu-id="2c036-125">**EditItems element text values**</span></span>

|<span data-ttu-id="2c036-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2c036-126">**Value**</span></span>|<span data-ttu-id="2c036-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c036-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c036-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2c036-128">None</span></span>  <br/> |<span data-ttu-id="2c036-129">Indica que el usuario no tiene permiso para editar los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c036-129">Indicates that the user does not have permission to edit items in the folder.</span></span>  <br/> |
|<span data-ttu-id="2c036-130">Estatal</span><span class="sxs-lookup"><span data-stu-id="2c036-130">Owned</span></span>  <br/> |<span data-ttu-id="2c036-131">Indica que el usuario tiene permiso para editar los elementos que posee el usuario en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c036-131">Indicates that the user has permission to edit the items that the user owns in the folder.</span></span>  <br/> |
|<span data-ttu-id="2c036-132">Todo</span><span class="sxs-lookup"><span data-stu-id="2c036-132">All</span></span>  <br/> |<span data-ttu-id="2c036-133">Indica que el usuario tiene permiso para editar todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c036-133">Indicates that the user has permission to edit all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c036-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c036-134">Remarks</span></span>

<span data-ttu-id="2c036-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2c036-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c036-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2c036-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c036-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c036-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c036-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2c036-138">Schema Name</span></span>  <br/> |<span data-ttu-id="2c036-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2c036-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c036-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2c036-140">Validation File</span></span>  <br/> |<span data-ttu-id="2c036-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2c036-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c036-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2c036-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c036-143">Falso</span><span class="sxs-lookup"><span data-stu-id="2c036-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c036-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c036-144">See also</span></span>

- [<span data-ttu-id="2c036-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2c036-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="2c036-146">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="2c036-146">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


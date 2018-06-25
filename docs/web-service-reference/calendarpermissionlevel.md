---
title: CalendarPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissionLevel
api_type:
- schema
ms.assetid: 6ac2b792-4326-4a3f-b6cb-977bf523b5b2
description: El elemento CalendarPermissionLevel representa el nivel de permisos que un usuario tiene en una carpeta de calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 646e4df3b70350a16cdd1f3e134260c2984a5161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763712"
---
# <a name="calendarpermissionlevel"></a><span data-ttu-id="19169-104">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="19169-104">CalendarPermissionLevel</span></span>

<span data-ttu-id="19169-105">El elemento **CalendarPermissionLevel** representa el nivel de permisos que un usuario tiene en una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="19169-105">The **CalendarPermissionLevel** element represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="19169-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="19169-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 <span data-ttu-id="19169-107">**CalendarPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="19169-107">**CalendarPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19169-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="19169-108">Attributes and elements</span></span>

<span data-ttu-id="19169-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="19169-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19169-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="19169-110">Attributes</span></span>

<span data-ttu-id="19169-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="19169-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19169-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19169-112">Child elements</span></span>

<span data-ttu-id="19169-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="19169-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19169-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="19169-114">Parent elements</span></span>

|<span data-ttu-id="19169-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="19169-115">**Element**</span></span>|<span data-ttu-id="19169-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19169-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19169-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="19169-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="19169-118">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="19169-118">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="19169-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="19169-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19169-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="19169-120">Text value</span></span>

<span data-ttu-id="19169-121">En la siguiente tabla se enumera los valores posibles para el elemento **CalendarPermissionLevel** .</span><span class="sxs-lookup"><span data-stu-id="19169-121">The following table lists the possible values for the **CalendarPermissionLevel** element.</span></span> 
  
<span data-ttu-id="19169-122">**Valores de texto de elemento CalendarPermissionLevel**</span><span class="sxs-lookup"><span data-stu-id="19169-122">**CalendarPermissionLevel element text values**</span></span>

|<span data-ttu-id="19169-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="19169-123">**Value**</span></span>|<span data-ttu-id="19169-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19169-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="19169-125">None</span><span class="sxs-lookup"><span data-stu-id="19169-125">None</span></span>  <br/> |<span data-ttu-id="19169-126">Indica que el usuario no tiene permisos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="19169-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="19169-127">Owner</span><span class="sxs-lookup"><span data-stu-id="19169-127">Owner</span></span>  <br/> |<span data-ttu-id="19169-128">Indica que el usuario puede crear, leer, modificar y eliminar todos los elementos de la carpeta y crear subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="19169-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="19169-129">El usuario es el propietario de la carpeta y el contacto de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="19169-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="19169-130">PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="19169-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="19169-131">Indica que el usuario puede crear, leer, modificar y eliminar todos los elementos de la carpeta y crear subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="19169-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="19169-132">Editor</span><span class="sxs-lookup"><span data-stu-id="19169-132">Editor</span></span>  <br/> |<span data-ttu-id="19169-133">Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="19169-133">Indicates that the user can create, read, edit and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="19169-134">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="19169-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="19169-135">Indica que el usuario puede crear y leer todos los elementos en la carpeta, editar y eliminar sólo los elementos que crea el usuario y crear subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="19169-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="19169-136">Autor</span><span class="sxs-lookup"><span data-stu-id="19169-136">Author</span></span>  <br/> |<span data-ttu-id="19169-137">Indica que el usuario puede crear y leer todos los elementos en la carpeta y editar y eliminar sólo los elementos que crea el usuario.</span><span class="sxs-lookup"><span data-stu-id="19169-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="19169-138">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="19169-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="19169-139">Indica que el usuario puede crear y leer todos los elementos en la carpeta y eliminar sólo los elementos que crea el usuario.</span><span class="sxs-lookup"><span data-stu-id="19169-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="19169-140">Reviewer</span><span class="sxs-lookup"><span data-stu-id="19169-140">Reviewer</span></span>  <br/> |<span data-ttu-id="19169-141">Indica que el usuario puede leer todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="19169-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="19169-142">Colaborador</span><span class="sxs-lookup"><span data-stu-id="19169-142">Contributor</span></span>  <br/> |<span data-ttu-id="19169-143">Indica que el usuario puede crear elementos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="19169-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="19169-144">El contenido de la carpeta no aparecen.</span><span class="sxs-lookup"><span data-stu-id="19169-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="19169-145">FreeBusyTimeOnly</span><span class="sxs-lookup"><span data-stu-id="19169-145">FreeBusyTimeOnly</span></span>  <br/> |<span data-ttu-id="19169-146">Indica que el usuario puede ver solo las horas de disponibilidad del calendario.</span><span class="sxs-lookup"><span data-stu-id="19169-146">Indicates that the user can view only free/busy time within the calendar.</span></span>  <br/> |
|<span data-ttu-id="19169-147">FreeBusyTimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="19169-147">FreeBusyTimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="19169-148">Indica que el usuario puede ver el tiempo libre/ocupada en el calendario y el asunto y la ubicación de las citas.</span><span class="sxs-lookup"><span data-stu-id="19169-148">Indicates that the user can view free/busy time within the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="19169-149">Personalizado</span><span class="sxs-lookup"><span data-stu-id="19169-149">Custom</span></span>  <br/> |<span data-ttu-id="19169-150">Indica que el usuario tiene permisos de acceso personalizados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="19169-150">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19169-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19169-151">Remarks</span></span>

<span data-ttu-id="19169-152">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="19169-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19169-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="19169-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19169-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19169-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19169-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="19169-155">Schema Name</span></span>  <br/> |<span data-ttu-id="19169-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="19169-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="19169-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="19169-157">Validation File</span></span>  <br/> |<span data-ttu-id="19169-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19169-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19169-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="19169-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="19169-160">False</span><span class="sxs-lookup"><span data-stu-id="19169-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19169-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="19169-161">See also</span></span>



- [<span data-ttu-id="19169-162">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="19169-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="19169-163">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="19169-163">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


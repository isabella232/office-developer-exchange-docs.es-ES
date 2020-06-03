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
description: El elemento CalendarPermissionLevel representa el nivel de permisos que tiene un usuario en una carpeta calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 670f78e0b3cef7a40339c83d84916871f8969536
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527183"
---
# <a name="calendarpermissionlevel"></a><span data-ttu-id="a26b2-104">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="a26b2-104">CalendarPermissionLevel</span></span>

<span data-ttu-id="a26b2-105">El elemento **CalendarPermissionLevel** representa el nivel de permisos que tiene un usuario en una carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="a26b2-105">The **CalendarPermissionLevel** element represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="a26b2-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a26b2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 <span data-ttu-id="a26b2-107">**CalendarPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="a26b2-107">**CalendarPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a26b2-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a26b2-108">Attributes and elements</span></span>

<span data-ttu-id="a26b2-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a26b2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a26b2-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="a26b2-110">Attributes</span></span>

<span data-ttu-id="a26b2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a26b2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a26b2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a26b2-112">Child elements</span></span>

<span data-ttu-id="a26b2-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a26b2-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a26b2-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a26b2-114">Parent elements</span></span>

|<span data-ttu-id="a26b2-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a26b2-115">**Element**</span></span>|<span data-ttu-id="a26b2-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a26b2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a26b2-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="a26b2-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="a26b2-118">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="a26b2-118">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="a26b2-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="a26b2-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a26b2-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a26b2-120">Text value</span></span>

<span data-ttu-id="a26b2-121">En la siguiente tabla se enumeran los valores posibles para el elemento **CalendarPermissionLevel** .</span><span class="sxs-lookup"><span data-stu-id="a26b2-121">The following table lists the possible values for the **CalendarPermissionLevel** element.</span></span> 
  
<span data-ttu-id="a26b2-122">**Valores de texto del elemento CalendarPermissionLevel**</span><span class="sxs-lookup"><span data-stu-id="a26b2-122">**CalendarPermissionLevel element text values**</span></span>

|<span data-ttu-id="a26b2-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a26b2-123">**Value**</span></span>|<span data-ttu-id="a26b2-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a26b2-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a26b2-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a26b2-125">None</span></span>  <br/> |<span data-ttu-id="a26b2-126">Indica que el usuario no tiene permisos para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a26b2-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="a26b2-127">Owner</span><span class="sxs-lookup"><span data-stu-id="a26b2-127">Owner</span></span>  <br/> |<span data-ttu-id="a26b2-128">Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta, así como crear subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="a26b2-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="a26b2-129">El usuario es el propietario de la carpeta y el contacto de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a26b2-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="a26b2-130">Publishingeditorcreateitems</span><span class="sxs-lookup"><span data-stu-id="a26b2-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="a26b2-131">Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta, así como crear subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="a26b2-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="a26b2-132">Editor</span><span class="sxs-lookup"><span data-stu-id="a26b2-132">Editor</span></span>  <br/> |<span data-ttu-id="a26b2-133">Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a26b2-133">Indicates that the user can create, read, edit and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="a26b2-134">Publishingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="a26b2-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="a26b2-135">Indica que el usuario puede crear y leer todos los elementos de la carpeta, editar y eliminar sólo los elementos que crea el usuario y crear subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="a26b2-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="a26b2-136">Autor</span><span class="sxs-lookup"><span data-stu-id="a26b2-136">Author</span></span>  <br/> |<span data-ttu-id="a26b2-137">Indica que el usuario puede crear y leer todos los elementos de la carpeta, y editar y eliminar sólo los elementos creados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a26b2-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="a26b2-138">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="a26b2-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="a26b2-139">Indica que el usuario puede crear y leer todos los elementos de la carpeta, y eliminar sólo los elementos que crea el usuario.</span><span class="sxs-lookup"><span data-stu-id="a26b2-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="a26b2-140">Reviewer</span><span class="sxs-lookup"><span data-stu-id="a26b2-140">Reviewer</span></span>  <br/> |<span data-ttu-id="a26b2-141">Indica que el usuario puede leer todos los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a26b2-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="a26b2-142">Colaborador</span><span class="sxs-lookup"><span data-stu-id="a26b2-142">Contributor</span></span>  <br/> |<span data-ttu-id="a26b2-143">Indica que el usuario puede crear elementos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a26b2-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="a26b2-144">El contenido de la carpeta no aparece.</span><span class="sxs-lookup"><span data-stu-id="a26b2-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="a26b2-145">FreeBusyTimeOnly</span><span class="sxs-lookup"><span data-stu-id="a26b2-145">FreeBusyTimeOnly</span></span>  <br/> |<span data-ttu-id="a26b2-146">Indica que el usuario puede ver solo la hora de disponibilidad en el calendario.</span><span class="sxs-lookup"><span data-stu-id="a26b2-146">Indicates that the user can view only free/busy time within the calendar.</span></span>  <br/> |
|<span data-ttu-id="a26b2-147">FreeBusyTimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="a26b2-147">FreeBusyTimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="a26b2-148">Indica que el usuario puede ver la fecha de disponibilidad en el calendario y el asunto y la ubicación de las citas.</span><span class="sxs-lookup"><span data-stu-id="a26b2-148">Indicates that the user can view free/busy time within the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="a26b2-149">Personalizado</span><span class="sxs-lookup"><span data-stu-id="a26b2-149">Custom</span></span>  <br/> |<span data-ttu-id="a26b2-150">Indica que el usuario tiene permisos de acceso personalizados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a26b2-150">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a26b2-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a26b2-151">Remarks</span></span>

<span data-ttu-id="a26b2-152">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a26b2-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a26b2-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a26b2-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a26b2-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="a26b2-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a26b2-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a26b2-155">Schema Name</span></span>  <br/> |<span data-ttu-id="a26b2-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a26b2-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="a26b2-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a26b2-157">Validation File</span></span>  <br/> |<span data-ttu-id="a26b2-158">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a26b2-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a26b2-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a26b2-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="a26b2-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a26b2-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a26b2-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="a26b2-161">See also</span></span>



- [<span data-ttu-id="a26b2-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a26b2-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="a26b2-163">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="a26b2-163">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)


---
title: TasksFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TasksFolderPermissionLevel
api_type:
- schema
ms.assetid: 0f70b79b-3443-4048-b410-692d4e2464fc
description: El elemento TasksFolderPermissionLevel contiene los permisos para la carpeta tareas predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 49807896f9175bafbef106c41d1c9dff8f6178c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840625"
---
# <a name="tasksfolderpermissionlevel"></a><span data-ttu-id="5a7c8-104">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="5a7c8-104">TasksFolderPermissionLevel</span></span>

<span data-ttu-id="5a7c8-105">El elemento **TasksFolderPermissionLevel** contiene los permisos para la carpeta tareas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-105">The **TasksFolderPermissionLevel** element contains the permissions for the default Tasks folder.</span></span> <span data-ttu-id="5a7c8-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5a7c8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<TasksFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</TasksFolderPermissionLevel>
```

<span data-ttu-id="5a7c8-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="5a7c8-107">**DelegateFolderPermissionLevelType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5a7c8-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5a7c8-108">Attributes and elements</span></span>

<span data-ttu-id="5a7c8-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a7c8-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5a7c8-110">Attributes</span></span>

<span data-ttu-id="5a7c8-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a7c8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a7c8-112">Child elements</span></span>

<span data-ttu-id="5a7c8-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5a7c8-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5a7c8-114">Parent elements</span></span>

|<span data-ttu-id="5a7c8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a7c8-115">**Element**</span></span>|<span data-ttu-id="5a7c8-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a7c8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a7c8-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="5a7c8-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="5a7c8-118">Contiene la configuración de nivel de permisos de delegado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="5a7c8-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5a7c8-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5a7c8-120">Text value</span></span>

<span data-ttu-id="5a7c8-121">En la siguiente tabla se enumera los valores de texto que representan los niveles de permisos.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="5a7c8-122">**Valores de texto de nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="5a7c8-122">**Permission level text values**</span></span>

|<span data-ttu-id="5a7c8-123">**Nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="5a7c8-123">**Permission level**</span></span>|<span data-ttu-id="5a7c8-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a7c8-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a7c8-125">None</span><span class="sxs-lookup"><span data-stu-id="5a7c8-125">None</span></span>  <br/> |<span data-ttu-id="5a7c8-126">El usuario delegado no tiene ningún permiso de acceso a la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-126">The delegate user has no access permissions to the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="5a7c8-127">Reviewer</span><span class="sxs-lookup"><span data-stu-id="5a7c8-127">Reviewer</span></span>  <br/> |<span data-ttu-id="5a7c8-128">El usuario delegado puede leer elementos de la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-128">The delegate user can read items in the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="5a7c8-129">Autor</span><span class="sxs-lookup"><span data-stu-id="5a7c8-129">Author</span></span>  <br/> |<span data-ttu-id="5a7c8-130">El usuario delegado puede leer y crear elementos en la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-130">The delegate user can read and create items in the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="5a7c8-131">Editor</span><span class="sxs-lookup"><span data-stu-id="5a7c8-131">Editor</span></span>  <br/> |<span data-ttu-id="5a7c8-132">El usuario delegado puede leer, crear y modificar elementos en la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-132">The delegate user can read, create, and modify items in the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="5a7c8-133">Personalizado</span><span class="sxs-lookup"><span data-stu-id="5a7c8-133">Custom</span></span>  <br/> |<span data-ttu-id="5a7c8-134">El usuario delegado tiene permisos de acceso personalizados a la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-134">The delegate user has custom access permissions to the Tasks folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a7c8-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a7c8-135">Remarks</span></span>

<span data-ttu-id="5a7c8-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a7c8-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5a7c8-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a7c8-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a7c8-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a7c8-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5a7c8-139">Schema Name</span></span>  <br/> |<span data-ttu-id="5a7c8-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5a7c8-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a7c8-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5a7c8-141">Validation File</span></span>  <br/> |<span data-ttu-id="5a7c8-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5a7c8-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a7c8-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5a7c8-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a7c8-144">False</span><span class="sxs-lookup"><span data-stu-id="5a7c8-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a7c8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a7c8-145">See also</span></span>

- [<span data-ttu-id="5a7c8-146">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="5a7c8-146">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="5a7c8-147">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="5a7c8-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="5a7c8-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5a7c8-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="5a7c8-149">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="5a7c8-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)


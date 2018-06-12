---
title: CalendarFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarFolderPermissionLevel
api_type:
- schema
ms.assetid: 2a5c9381-dc2c-4fc6-b9b5-893477d0970e
description: El elemento CalendarFolderPermissionLevel contiene los permisos para la carpeta Calendario predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 5d51fea522656910d8417e7f75214214e2c162c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763702"
---
# <a name="calendarfolderpermissionlevel"></a><span data-ttu-id="c4930-104">CalendarFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="c4930-104">CalendarFolderPermissionLevel</span></span>

<span data-ttu-id="c4930-105">El elemento **CalendarFolderPermissionLevel** contiene los permisos para la carpeta Calendario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c4930-105">The **CalendarFolderPermissionLevel** element contains the permissions for the default Calendar folder.</span></span> <span data-ttu-id="c4930-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c4930-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</CalendarFolderPermissionLevel>
```

 <span data-ttu-id="c4930-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="c4930-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4930-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c4930-108">Attributes and elements</span></span>

<span data-ttu-id="c4930-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c4930-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4930-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4930-110">Attributes</span></span>

<span data-ttu-id="c4930-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4930-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4930-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c4930-112">Child elements</span></span>

<span data-ttu-id="c4930-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4930-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4930-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c4930-114">Parent elements</span></span>

|<span data-ttu-id="c4930-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4930-115">**Element**</span></span>|<span data-ttu-id="c4930-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4930-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4930-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="c4930-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="c4930-118">Contiene la configuración de nivel de permisos de delegado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c4930-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="c4930-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c4930-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4930-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c4930-120">Text value</span></span>

<span data-ttu-id="c4930-121">En la siguiente tabla se enumera los valores de texto que representan los niveles de permisos.</span><span class="sxs-lookup"><span data-stu-id="c4930-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="c4930-122">**Valores de texto de nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="c4930-122">**Permission level text values**</span></span>

|<span data-ttu-id="c4930-123">**Nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="c4930-123">**Permission level**</span></span>|<span data-ttu-id="c4930-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4930-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4930-125">None</span><span class="sxs-lookup"><span data-stu-id="c4930-125">None</span></span>  <br/> |<span data-ttu-id="c4930-126">El usuario delegado no tiene ningún permiso de acceso a la carpeta Calendario.</span><span class="sxs-lookup"><span data-stu-id="c4930-126">The delegate user has no access permissions to the Calendar folder.</span></span>  <br/> |
|<span data-ttu-id="c4930-127">Reviewer</span><span class="sxs-lookup"><span data-stu-id="c4930-127">Reviewer</span></span>  <br/> |<span data-ttu-id="c4930-128">El usuario delegado puede leer los elementos de la carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="c4930-128">The delegate user can read items in the Calendar folder.</span></span>  <br/> |
|<span data-ttu-id="c4930-129">Autor</span><span class="sxs-lookup"><span data-stu-id="c4930-129">Author</span></span>  <br/> |<span data-ttu-id="c4930-130">El usuario delegado puede leer y crear elementos en la carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="c4930-130">The delegate user can read and create items in the Calendar folder.</span></span>  <br/> |
|<span data-ttu-id="c4930-131">Editor</span><span class="sxs-lookup"><span data-stu-id="c4930-131">Editor</span></span>  <br/> |<span data-ttu-id="c4930-132">El usuario delegado puede leer, crear y modificar elementos en la carpeta Calendario.</span><span class="sxs-lookup"><span data-stu-id="c4930-132">The delegate user can read, create, and modify items in the Calendar folder.</span></span>  <br/> |
|<span data-ttu-id="c4930-133">Personalizado</span><span class="sxs-lookup"><span data-stu-id="c4930-133">Custom</span></span>  <br/> |<span data-ttu-id="c4930-134">El usuario delegado tiene permisos de acceso personalizados a la carpeta Calendario.</span><span class="sxs-lookup"><span data-stu-id="c4930-134">The delegate user has custom access permissions to the Calendar folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4930-135">Notas</span><span class="sxs-lookup"><span data-stu-id="c4930-135">Remarks</span></span>

<span data-ttu-id="c4930-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c4930-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4930-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c4930-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4930-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4930-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4930-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c4930-139">Schema Name</span></span>  <br/> |<span data-ttu-id="c4930-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c4930-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4930-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c4930-141">Validation File</span></span>  <br/> |<span data-ttu-id="c4930-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4930-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4930-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c4930-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4930-144">False</span><span class="sxs-lookup"><span data-stu-id="c4930-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4930-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="c4930-145">See also</span></span>



[<span data-ttu-id="c4930-146">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="c4930-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="c4930-147">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="c4930-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="c4930-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4930-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c4930-149">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="c4930-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)


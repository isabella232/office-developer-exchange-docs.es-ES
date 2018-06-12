---
title: NotesFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NotesFolderPermissionLevel
api_type:
- schema
ms.assetid: 76a2520c-f453-4fd7-b3eb-1c5f4666680a
description: El elemento NotesFolderPermissionLevel contiene los permisos para la carpeta de notas de forma predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: dd8644210692e0c342079d055ddf00b8d9283d7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836552"
---
# <a name="notesfolderpermissionlevel"></a><span data-ttu-id="d4b0b-104">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="d4b0b-104">NotesFolderPermissionLevel</span></span>

<span data-ttu-id="d4b0b-105">El elemento **NotesFolderPermissionLevel** contiene los permisos para la carpeta de notas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-105">The **NotesFolderPermissionLevel** element contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="d4b0b-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d4b0b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<NotesFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</NotesFolderPermissionLevel>
```

 <span data-ttu-id="d4b0b-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="d4b0b-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4b0b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d4b0b-108">Attributes and elements</span></span>

<span data-ttu-id="d4b0b-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4b0b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d4b0b-110">Attributes</span></span>

<span data-ttu-id="d4b0b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4b0b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d4b0b-112">Child elements</span></span>

<span data-ttu-id="d4b0b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d4b0b-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d4b0b-114">Parent elements</span></span>

|<span data-ttu-id="d4b0b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4b0b-115">**Element**</span></span>|<span data-ttu-id="d4b0b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4b0b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4b0b-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="d4b0b-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="d4b0b-118">Contiene la configuración de nivel de permisos de delegado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="d4b0b-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d4b0b-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d4b0b-120">Text value</span></span>

<span data-ttu-id="d4b0b-121">En la siguiente tabla se enumera los valores de texto que representan los niveles de permisos.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="d4b0b-122">**Valores de texto de nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="d4b0b-122">**Permission level text values**</span></span>

|<span data-ttu-id="d4b0b-123">**Nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="d4b0b-123">**Permission level**</span></span>|<span data-ttu-id="d4b0b-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4b0b-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4b0b-125">None</span><span class="sxs-lookup"><span data-stu-id="d4b0b-125">None</span></span>  <br/> |<span data-ttu-id="d4b0b-126">El usuario delegado no tiene ningún permiso de acceso a la carpeta notas.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-126">The delegate user has no access permissions to the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="d4b0b-127">Reviewer</span><span class="sxs-lookup"><span data-stu-id="d4b0b-127">Reviewer</span></span>  <br/> |<span data-ttu-id="d4b0b-128">El usuario delegado puede leer los elementos de la carpeta notas.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-128">The delegate user can read items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="d4b0b-129">Autor</span><span class="sxs-lookup"><span data-stu-id="d4b0b-129">Author</span></span>  <br/> |<span data-ttu-id="d4b0b-130">El usuario delegado puede leer y crear elementos en la carpeta notas.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-130">The delegate user can read and create items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="d4b0b-131">Editor</span><span class="sxs-lookup"><span data-stu-id="d4b0b-131">Editor</span></span>  <br/> |<span data-ttu-id="d4b0b-132">El usuario delegado puede leer, crear y modificar elementos en la carpeta notas.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-132">The delegate user can read, create, and modify items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="d4b0b-133">Personalizado</span><span class="sxs-lookup"><span data-stu-id="d4b0b-133">Custom</span></span>  <br/> |<span data-ttu-id="d4b0b-134">El usuario delegado tiene permisos de acceso personalizados a la carpeta notas.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-134">The delegate user has custom access permissions to the Notes folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4b0b-135">Notas</span><span class="sxs-lookup"><span data-stu-id="d4b0b-135">Remarks</span></span>

<span data-ttu-id="d4b0b-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d4b0b-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4b0b-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d4b0b-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4b0b-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4b0b-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4b0b-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d4b0b-139">Schema Name</span></span>  <br/> |<span data-ttu-id="d4b0b-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d4b0b-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4b0b-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d4b0b-141">Validation File</span></span>  <br/> |<span data-ttu-id="d4b0b-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4b0b-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4b0b-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d4b0b-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4b0b-144">False</span><span class="sxs-lookup"><span data-stu-id="d4b0b-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4b0b-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="d4b0b-145">See also</span></span>



[<span data-ttu-id="d4b0b-146">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="d4b0b-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="d4b0b-147">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="d4b0b-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="d4b0b-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d4b0b-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d4b0b-149">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="d4b0b-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)


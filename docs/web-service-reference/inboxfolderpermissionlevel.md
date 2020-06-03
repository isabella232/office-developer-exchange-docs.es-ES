---
title: InboxFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InboxFolderPermissionLevel
api_type:
- schema
ms.assetid: f250d31b-9193-4c1c-8350-900dead3a023
description: El elemento InboxFolderPermissionLevel contiene los permisos para la carpeta Bandeja de entrada predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 8a497a38a58e6455f2bd754aa8da97b421a2bca3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465712"
---
# <a name="inboxfolderpermissionlevel"></a><span data-ttu-id="2173c-104">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="2173c-104">InboxFolderPermissionLevel</span></span>

<span data-ttu-id="2173c-105">El elemento **InboxFolderPermissionLevel** contiene los permisos para la carpeta Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2173c-105">The **InboxFolderPermissionLevel** element contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="2173c-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2173c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<InboxFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</InboxFolderPermissionLevel>
```

 <span data-ttu-id="2173c-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="2173c-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2173c-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2173c-108">Attributes and elements</span></span>

<span data-ttu-id="2173c-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2173c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2173c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2173c-110">Attributes</span></span>

<span data-ttu-id="2173c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2173c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2173c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2173c-112">Child elements</span></span>

<span data-ttu-id="2173c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2173c-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2173c-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2173c-114">Parent elements</span></span>

|<span data-ttu-id="2173c-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2173c-115">**Element**</span></span>|<span data-ttu-id="2173c-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2173c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2173c-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="2173c-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="2173c-118">Contiene la configuración del nivel de permisos de delegado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="2173c-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="2173c-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="2173c-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2173c-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2173c-120">Text value</span></span>

<span data-ttu-id="2173c-121">En la siguiente tabla se enumeran los valores de texto que representan los niveles de permisos.</span><span class="sxs-lookup"><span data-stu-id="2173c-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="2173c-122">**Valores de texto de nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="2173c-122">**Permission level text values**</span></span>

|<span data-ttu-id="2173c-123">**Nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="2173c-123">**Permission level**</span></span>|<span data-ttu-id="2173c-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2173c-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2173c-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2173c-125">None</span></span>  <br/> |<span data-ttu-id="2173c-126">El usuario delegado no tiene permisos de acceso a la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2173c-126">The delegate user has no access permissions to the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="2173c-127">Reviewer</span><span class="sxs-lookup"><span data-stu-id="2173c-127">Reviewer</span></span>  <br/> |<span data-ttu-id="2173c-128">El usuario delegado puede leer los elementos de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2173c-128">The delegate user can read items in the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="2173c-129">Autor</span><span class="sxs-lookup"><span data-stu-id="2173c-129">Author</span></span>  <br/> |<span data-ttu-id="2173c-130">El usuario delegado puede leer y crear elementos en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2173c-130">The delegate user can read and create items in the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="2173c-131">Editor</span><span class="sxs-lookup"><span data-stu-id="2173c-131">Editor</span></span>  <br/> |<span data-ttu-id="2173c-132">El usuario delegado puede leer, crear y modificar los elementos de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2173c-132">The delegate user can read, create, and modify items in the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="2173c-133">Personalizado</span><span class="sxs-lookup"><span data-stu-id="2173c-133">Custom</span></span>  <br/> |<span data-ttu-id="2173c-134">El usuario delegado tiene permisos de acceso personalizados a la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2173c-134">The delegate user has custom access permissions to the Inbox folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2173c-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2173c-135">Remarks</span></span>

<span data-ttu-id="2173c-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2173c-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2173c-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2173c-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2173c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2173c-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2173c-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2173c-139">Schema Name</span></span>  <br/> |<span data-ttu-id="2173c-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2173c-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="2173c-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2173c-141">Validation File</span></span>  <br/> |<span data-ttu-id="2173c-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2173c-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2173c-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2173c-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="2173c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="2173c-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2173c-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="2173c-145">See also</span></span>



[<span data-ttu-id="2173c-146">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="2173c-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="2173c-147">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="2173c-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="2173c-148">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2173c-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2173c-149">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="2173c-149">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)


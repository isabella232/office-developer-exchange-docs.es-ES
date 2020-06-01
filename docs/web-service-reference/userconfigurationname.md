---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: El elemento UserConfigurationName representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.
ms.openlocfilehash: 020b55919f7f81602a5eb072652d82168607d306
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466034"
---
# <a name="userconfigurationname"></a><span data-ttu-id="5d1dc-104">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5d1dc-104">UserConfigurationName</span></span>

<span data-ttu-id="5d1dc-105">El elemento **UserConfigurationName** representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-105">The **UserConfigurationName** element represents the name of a user configuration object.</span></span> <span data-ttu-id="5d1dc-106">El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-106">The user configuration object name is the identifier for a user configuration object.</span></span> 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

```XML
<UserConfigurationName Name="">
   <DistinguishedFolderId/> 
</UserConfigurationName>
```

<span data-ttu-id="5d1dc-107">**UserConfigurationNameType**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-107">**UserConfigurationNameType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5d1dc-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5d1dc-108">Attributes and elements</span></span>

<span data-ttu-id="5d1dc-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d1dc-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d1dc-110">Attributes</span></span>

|<span data-ttu-id="5d1dc-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-111">**Attribute**</span></span>|<span data-ttu-id="5d1dc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d1dc-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-113">**Name**</span></span> <br/> |<span data-ttu-id="5d1dc-114">Contiene un valor de tipo String que representa el nombre de un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-114">Contains a string value that represents the name of a user configuration object.</span></span> <span data-ttu-id="5d1dc-115">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5d1dc-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d1dc-116">Child elements</span></span>

|<span data-ttu-id="5d1dc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-117">**Element**</span></span>|<span data-ttu-id="5d1dc-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d1dc-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="5d1dc-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="5d1dc-120">Representa el identificador de la carpeta que contiene el objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-120">Represents the folder identifier of the folder that contains the user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="5d1dc-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="5d1dc-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="5d1dc-122">Representa un nombre de carpeta distinguido de la carpeta que contiene el objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-122">Represents a distinguished folder name of the folder that contains the user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d1dc-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5d1dc-123">Parent elements</span></span>

|<span data-ttu-id="5d1dc-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-124">**Element**</span></span>|<span data-ttu-id="5d1dc-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d1dc-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d1dc-126">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d1dc-126">DeleteUserConfiguration</span></span>](deleteuserconfiguration.md) <br/> |<span data-ttu-id="5d1dc-127">Representa una solicitud para eliminar un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-127">Represents a request to delete a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="5d1dc-128">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d1dc-128">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="5d1dc-129">Representa una solicitud para obtener un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-129">Represents a request to get a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="5d1dc-130">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d1dc-130">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="5d1dc-131">Define un objeto de configuración de usuario único.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-131">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5d1dc-132">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5d1dc-132">Text value</span></span>

<span data-ttu-id="5d1dc-133">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d1dc-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d1dc-134">Remarks</span></span>

<span data-ttu-id="5d1dc-135">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d1dc-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d1dc-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5d1dc-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d1dc-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d1dc-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d1dc-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5d1dc-138">Schema Name</span></span>  <br/> |<span data-ttu-id="5d1dc-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5d1dc-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="5d1dc-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5d1dc-140">Validation File</span></span>  <br/> |<span data-ttu-id="5d1dc-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5d1dc-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d1dc-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5d1dc-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d1dc-143">Falso</span><span class="sxs-lookup"><span data-stu-id="5d1dc-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d1dc-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d1dc-144">See also</span></span>

- [<span data-ttu-id="5d1dc-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5d1dc-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


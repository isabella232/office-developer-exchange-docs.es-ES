---
title: ApplicationRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00003b9b-f8f1-4452-a0af-157f789f8892
description: El elemento ApplicationRoles especifica los roles de aplicación que usa la aplicación de asociado de llamada para la llamada actual.
ms.openlocfilehash: 8dfe5c745896d02217cbf91375d355954a4e22eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464703"
---
# <a name="applicationroles"></a><span data-ttu-id="c9771-103">ApplicationRoles</span><span class="sxs-lookup"><span data-stu-id="c9771-103">ApplicationRoles</span></span>

<span data-ttu-id="c9771-104">El elemento **ApplicationRoles** especifica los roles de aplicación que usa la aplicación de asociado de llamada para la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="c9771-104">The **ApplicationRoles** element specifies the application roles that the calling partner application uses for the current call.</span></span> 
  
```XML
<ApplicationRoles>
    <Role></Role>
</ApplicationRoles>
```

 <span data-ttu-id="c9771-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="c9771-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9771-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c9771-106">Attributes and elements</span></span>

<span data-ttu-id="c9771-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c9771-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9771-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9771-108">Attributes</span></span>

<span data-ttu-id="c9771-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c9771-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9771-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c9771-110">Child elements</span></span>

|<span data-ttu-id="c9771-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9771-111">**Element**</span></span>|<span data-ttu-id="c9771-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9771-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9771-113">Rol</span><span class="sxs-lookup"><span data-stu-id="c9771-113">Role</span></span>](role.md) <br/> |<span data-ttu-id="c9771-114">Especifica una cadena que representa una función de administración.</span><span class="sxs-lookup"><span data-stu-id="c9771-114">Specifies a string that represents a management role.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c9771-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c9771-115">Parent elements</span></span>

|<span data-ttu-id="c9771-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9771-116">**Element**</span></span>|<span data-ttu-id="c9771-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9771-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9771-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="c9771-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="c9771-119">Especifica el rol de administración.</span><span class="sxs-lookup"><span data-stu-id="c9771-119">Specifies the management role.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9771-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9771-120">Remarks</span></span>

<span data-ttu-id="c9771-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9771-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c9771-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9771-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9771-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c9771-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9771-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9771-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9771-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c9771-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c9771-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c9771-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c9771-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c9771-127">Validation File</span></span>  <br/> |<span data-ttu-id="c9771-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c9771-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9771-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c9771-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c9771-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9771-130">See also</span></span>

- [<span data-ttu-id="c9771-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c9771-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


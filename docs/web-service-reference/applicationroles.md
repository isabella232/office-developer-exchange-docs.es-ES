---
title: ApplicationRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00003b9b-f8f1-4452-a0af-157f789f8892
description: El elemento ApplicationRoles especifica las funciones de aplicación que la aplicación de socio llamada se usa para la llamada actual.
ms.openlocfilehash: ff32b693dae573416263bcb7c0fbb552a933b8d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763450"
---
# <a name="applicationroles"></a><span data-ttu-id="07cb0-103">ApplicationRoles</span><span class="sxs-lookup"><span data-stu-id="07cb0-103">ApplicationRoles</span></span>

<span data-ttu-id="07cb0-104">El elemento **ApplicationRoles** especifica las funciones de aplicación que la aplicación de socio llamada se usa para la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="07cb0-104">The **ApplicationRoles** element specifies the application roles that the calling partner application uses for the current call.</span></span> 
  
```XML
<ApplicationRoles>
    <Role></Role>
</ApplicationRoles>
```

 <span data-ttu-id="07cb0-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="07cb0-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07cb0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07cb0-106">Attributes and elements</span></span>

<span data-ttu-id="07cb0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07cb0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07cb0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="07cb0-108">Attributes</span></span>

<span data-ttu-id="07cb0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07cb0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07cb0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07cb0-110">Child elements</span></span>

|<span data-ttu-id="07cb0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="07cb0-111">**Element**</span></span>|<span data-ttu-id="07cb0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07cb0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07cb0-113">Role</span><span class="sxs-lookup"><span data-stu-id="07cb0-113">Role</span></span>](role.md) <br/> |<span data-ttu-id="07cb0-114">Especifica una cadena que representa un rol de administración.</span><span class="sxs-lookup"><span data-stu-id="07cb0-114">Specifies a string that represents a management role.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07cb0-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07cb0-115">Parent elements</span></span>

|<span data-ttu-id="07cb0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="07cb0-116">**Element**</span></span>|<span data-ttu-id="07cb0-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07cb0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07cb0-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="07cb0-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="07cb0-119">Especifica la función de administración.</span><span class="sxs-lookup"><span data-stu-id="07cb0-119">Specifies the management role.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07cb0-120">Notas</span><span class="sxs-lookup"><span data-stu-id="07cb0-120">Remarks</span></span>

<span data-ttu-id="07cb0-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="07cb0-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="07cb0-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="07cb0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07cb0-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07cb0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07cb0-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07cb0-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07cb0-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07cb0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="07cb0-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="07cb0-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="07cb0-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07cb0-127">Validation File</span></span>  <br/> |<span data-ttu-id="07cb0-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07cb0-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="07cb0-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07cb0-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="07cb0-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="07cb0-130">See also</span></span>

- [<span data-ttu-id="07cb0-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="07cb0-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


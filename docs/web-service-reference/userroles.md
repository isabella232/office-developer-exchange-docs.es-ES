---
title: UserRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be003e12-3496-468d-a61c-48af0b819654
description: El elemento UserRoles especifica las funciones de usuario que el usuario realiza la llamada, o el usuario que la aplicación de socio llamada actúa como, desea aplicar a la llamada actual.
ms.openlocfilehash: 19dc1a7e00decb9141326b53b650d72101013c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840926"
---
# <a name="userroles"></a><span data-ttu-id="903a2-103">UserRoles</span><span class="sxs-lookup"><span data-stu-id="903a2-103">UserRoles</span></span>

<span data-ttu-id="903a2-104">El elemento **UserRoles** especifica las funciones de usuario que el usuario realiza la llamada, o el usuario que la aplicación de socio llamada actúa como, desea aplicar a la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="903a2-104">The **UserRoles** element specifies the user roles that the calling user, or the user that the calling partner application is acting as, wants to apply to the current call.</span></span> 
  
```XML
<UserRoles>
   <Role/>
</UserRoles>
```

 <span data-ttu-id="903a2-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="903a2-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="903a2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="903a2-106">Attributes and elements</span></span>

<span data-ttu-id="903a2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="903a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="903a2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="903a2-108">Attributes</span></span>

<span data-ttu-id="903a2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="903a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="903a2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="903a2-110">Child elements</span></span>

[<span data-ttu-id="903a2-111">Role</span><span class="sxs-lookup"><span data-stu-id="903a2-111">Role</span></span>](role.md)
  
### <a name="parent-elements"></a><span data-ttu-id="903a2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="903a2-112">Parent elements</span></span>

[<span data-ttu-id="903a2-113">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="903a2-113">ManagementRole</span></span>](managementrole.md)
  
## <a name="remarks"></a><span data-ttu-id="903a2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="903a2-114">Remarks</span></span>

<span data-ttu-id="903a2-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="903a2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="903a2-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="903a2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="903a2-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="903a2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="903a2-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="903a2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="903a2-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="903a2-119">Schema name</span></span>  <br/> |<span data-ttu-id="903a2-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="903a2-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="903a2-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="903a2-121">Validation file</span></span>  <br/> |<span data-ttu-id="903a2-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="903a2-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="903a2-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="903a2-123">Can be empty</span></span>  <br/> ||
   


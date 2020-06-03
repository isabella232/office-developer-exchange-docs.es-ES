---
title: UserRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be003e12-3496-468d-a61c-48af0b819654
description: El elemento UserRoles especifica las funciones de usuario que el usuario que realiza la llamada o el usuario en el que actúa la aplicación de socio de llamada desea aplicar a la llamada actual.
ms.openlocfilehash: 5155b82781321b16d1b58fdcaffe7b8cf2372717
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467133"
---
# <a name="userroles"></a><span data-ttu-id="c3ede-103">UserRoles</span><span class="sxs-lookup"><span data-stu-id="c3ede-103">UserRoles</span></span>

<span data-ttu-id="c3ede-104">El elemento **UserRoles** especifica las funciones de usuario que el usuario que realiza la llamada o el usuario en el que actúa la aplicación de socio de llamada desea aplicar a la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="c3ede-104">The **UserRoles** element specifies the user roles that the calling user, or the user that the calling partner application is acting as, wants to apply to the current call.</span></span> 
  
```XML
<UserRoles>
   <Role/>
</UserRoles>
```

 <span data-ttu-id="c3ede-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="c3ede-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3ede-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c3ede-106">Attributes and elements</span></span>

<span data-ttu-id="c3ede-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c3ede-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3ede-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3ede-108">Attributes</span></span>

<span data-ttu-id="c3ede-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c3ede-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3ede-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3ede-110">Child elements</span></span>

[<span data-ttu-id="c3ede-111">Rol</span><span class="sxs-lookup"><span data-stu-id="c3ede-111">Role</span></span>](role.md)
  
### <a name="parent-elements"></a><span data-ttu-id="c3ede-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c3ede-112">Parent elements</span></span>

[<span data-ttu-id="c3ede-113">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="c3ede-113">ManagementRole</span></span>](managementrole.md)
  
## <a name="remarks"></a><span data-ttu-id="c3ede-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3ede-114">Remarks</span></span>

<span data-ttu-id="c3ede-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c3ede-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c3ede-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3ede-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3ede-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c3ede-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3ede-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3ede-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c3ede-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c3ede-119">Schema name</span></span>  <br/> |<span data-ttu-id="c3ede-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c3ede-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="c3ede-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c3ede-121">Validation file</span></span>  <br/> |<span data-ttu-id="c3ede-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c3ede-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c3ede-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c3ede-123">Can be empty</span></span>  <br/> ||
   


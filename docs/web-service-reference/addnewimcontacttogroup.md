---
title: AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5913619-0c13-429d-b9d2-057e8af220f1
description: El elemento AddNewImContactToGroup define una solicitud para agregar un nuevo contacto de mensajería instantáneo a un grupo de mensajería instantáneo.
ms.openlocfilehash: 2736bac6880a11101e9bffee12033c838705700e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763406"
---
# <a name="addnewimcontacttogroup"></a><span data-ttu-id="f0a5d-103">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="f0a5d-103">AddNewImContactToGroup</span></span>

<span data-ttu-id="f0a5d-104">El elemento **AddNewImContactToGroup** define una solicitud para agregar un nuevo contacto de mensajería instantáneo a un grupo de mensajería instantáneo.</span><span class="sxs-lookup"><span data-stu-id="f0a5d-104">The **AddNewImContactToGroup** element defines a request to add a new instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddNewImContactToGroup>
   <ImAddress/>
   <DisplayName/>
   <GroupId/>
</AddNewImContactToGroup>
```

 <span data-ttu-id="f0a5d-105">**AddNewImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="f0a5d-105">**AddNewImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0a5d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0a5d-106">Attributes and elements</span></span>

<span data-ttu-id="f0a5d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0a5d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0a5d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0a5d-108">Attributes</span></span>

<span data-ttu-id="f0a5d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0a5d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0a5d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0a5d-110">Child elements</span></span>

<span data-ttu-id="f0a5d-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="f0a5d-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f0a5d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0a5d-112">Parent elements</span></span>

<span data-ttu-id="f0a5d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0a5d-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0a5d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0a5d-114">Remarks</span></span>

<span data-ttu-id="f0a5d-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f0a5d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f0a5d-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0a5d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0a5d-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f0a5d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0a5d-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0a5d-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f0a5d-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f0a5d-119">Schema name</span></span>  <br/> |<span data-ttu-id="f0a5d-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f0a5d-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f0a5d-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f0a5d-121">Validation file</span></span>  <br/> |<span data-ttu-id="f0a5d-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f0a5d-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f0a5d-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f0a5d-123">Can be empty</span></span>  <br/> |<span data-ttu-id="f0a5d-124">falso</span><span class="sxs-lookup"><span data-stu-id="f0a5d-124">false</span></span>  <br/> |
   


---
title: AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5913619-0c13-429d-b9d2-057e8af220f1
description: El elemento AddNewImContactToGroup define una solicitud para agregar un nuevo contacto de mensajería instantánea a un grupo de mensajería instantánea.
ms.openlocfilehash: c493ba81b23832a462acd425eb60297801f8768f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463653"
---
# <a name="addnewimcontacttogroup"></a><span data-ttu-id="58155-103">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="58155-103">AddNewImContactToGroup</span></span>

<span data-ttu-id="58155-104">El elemento **AddNewImContactToGroup** define una solicitud para agregar un nuevo contacto de mensajería instantánea a un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="58155-104">The **AddNewImContactToGroup** element defines a request to add a new instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddNewImContactToGroup>
   <ImAddress/>
   <DisplayName/>
   <GroupId/>
</AddNewImContactToGroup>
```

 <span data-ttu-id="58155-105">**AddNewImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="58155-105">**AddNewImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58155-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="58155-106">Attributes and elements</span></span>

<span data-ttu-id="58155-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="58155-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58155-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="58155-108">Attributes</span></span>

<span data-ttu-id="58155-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="58155-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58155-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58155-110">Child elements</span></span>

<span data-ttu-id="58155-111">[IMAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md)  |  [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)  |  [GROUPID](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="58155-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58155-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58155-112">Parent elements</span></span>

<span data-ttu-id="58155-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58155-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58155-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58155-114">Remarks</span></span>

<span data-ttu-id="58155-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58155-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="58155-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="58155-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58155-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58155-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58155-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="58155-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="58155-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="58155-119">Schema name</span></span>  <br/> |<span data-ttu-id="58155-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="58155-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="58155-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="58155-121">Validation file</span></span>  <br/> |<span data-ttu-id="58155-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="58155-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="58155-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="58155-123">Can be empty</span></span>  <br/> |<span data-ttu-id="58155-124">false</span><span class="sxs-lookup"><span data-stu-id="58155-124">false</span></span>  <br/> |
   


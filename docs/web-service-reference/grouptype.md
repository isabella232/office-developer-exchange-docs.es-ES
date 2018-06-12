---
title: GroupType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c31552f-22b8-4bf0-8cac-046fd92ac0d4
description: El elemento GroupType especifica la clase de grupo de un grupo (IM) de mensajería instantánea.
ms.openlocfilehash: 330a1567ce85877ba73c6205898ea66b59585e16
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835800"
---
# <a name="grouptype"></a><span data-ttu-id="25d23-103">GroupType</span><span class="sxs-lookup"><span data-stu-id="25d23-103">GroupType</span></span>

<span data-ttu-id="25d23-104">El elemento **GroupType** especifica la clase de grupo de un grupo (IM) de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="25d23-104">The **GroupType** element specifies the group class of an instant messaging (IM) group.</span></span> 
  
```XML
<GroupType></GroupType>
```

 <span data-ttu-id="25d23-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="25d23-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25d23-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25d23-106">Attributes and elements</span></span>

<span data-ttu-id="25d23-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25d23-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25d23-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25d23-108">Attributes</span></span>

<span data-ttu-id="25d23-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25d23-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25d23-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25d23-110">Child elements</span></span>

<span data-ttu-id="25d23-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25d23-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25d23-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25d23-112">Parent elements</span></span>

|<span data-ttu-id="25d23-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="25d23-113">**Element**</span></span>|<span data-ttu-id="25d23-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25d23-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25d23-115">ImGroup</span><span class="sxs-lookup"><span data-stu-id="25d23-115">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="25d23-116">Representa un grupo de mensajería instantáneo.</span><span class="sxs-lookup"><span data-stu-id="25d23-116">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25d23-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25d23-117">Text value</span></span>

<span data-ttu-id="25d23-118">El valor de texto del elemento **GroupType** es un valor de tipo string que especifica el tipo del grupo.</span><span class="sxs-lookup"><span data-stu-id="25d23-118">The text value of the **GroupType** element is a string value that specifies type of the group.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25d23-119">Notas</span><span class="sxs-lookup"><span data-stu-id="25d23-119">Remarks</span></span>

<span data-ttu-id="25d23-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25d23-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="25d23-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="25d23-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25d23-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25d23-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25d23-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25d23-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25d23-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25d23-124">Schema Name</span></span>  <br/> |<span data-ttu-id="25d23-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="25d23-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="25d23-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25d23-126">Validation File</span></span>  <br/> |<span data-ttu-id="25d23-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="25d23-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="25d23-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25d23-128">Can Be Empty</span></span>  <br/> |<span data-ttu-id="25d23-129">False</span><span class="sxs-lookup"><span data-stu-id="25d23-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25d23-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="25d23-130">See also</span></span>



- [<span data-ttu-id="25d23-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="25d23-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: IsMembershipGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: El elemento IsMembershipGroup especifica un valor booleano que indica si la entidad es un grupo de distribución o un buzón.
ms.openlocfilehash: ed79961c6d13ab226c0b489103ef3d2c4a08668d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459289"
---
# <a name="ismembershipgroup"></a><span data-ttu-id="50275-103">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="50275-103">IsMembershipGroup</span></span>

<span data-ttu-id="50275-104">El elemento **IsMembershipGroup** especifica un valor booleano que indica si la entidad es un grupo de distribución o un buzón.</span><span class="sxs-lookup"><span data-stu-id="50275-104">The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox.</span></span> 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 <span data-ttu-id="50275-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="50275-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50275-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="50275-106">Attributes and elements</span></span>

<span data-ttu-id="50275-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="50275-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50275-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="50275-108">Attributes</span></span>

<span data-ttu-id="50275-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="50275-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50275-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="50275-110">Child elements</span></span>

<span data-ttu-id="50275-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="50275-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="50275-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="50275-112">Parent elements</span></span>

|<span data-ttu-id="50275-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50275-113">**Element**</span></span>|<span data-ttu-id="50275-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50275-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50275-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="50275-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="50275-116">Especifica un buzón devuelto desde una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="50275-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="50275-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="50275-117">Text value</span></span>

<span data-ttu-id="50275-118">Un valor de texto de **true** para el elemento **IsMembershipGroup** indica que la entidad es un grupo de distribución o un buzón.</span><span class="sxs-lookup"><span data-stu-id="50275-118">A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox.</span></span> <span data-ttu-id="50275-119">Un valor de False indica que la entidad no es un grupo de distribución o un buzón.</span><span class="sxs-lookup"><span data-stu-id="50275-119">A value of false indicates that the entity is not a distribution group or a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="50275-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50275-120">Remarks</span></span>

<span data-ttu-id="50275-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="50275-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="50275-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="50275-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50275-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="50275-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50275-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="50275-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50275-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="50275-125">Schema Name</span></span>  <br/> |<span data-ttu-id="50275-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="50275-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="50275-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="50275-127">Validation File</span></span>  <br/> |<span data-ttu-id="50275-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="50275-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="50275-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="50275-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="50275-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="50275-130">See also</span></span>



- [<span data-ttu-id="50275-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="50275-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: BlockStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 08556ee9-0923-437c-99a4-bb630f04e973
description: El elemento BlockStatus especifica el estado de bloqueo de un elemento.
ms.openlocfilehash: e88236274bfa70216e872025c2a94231f837df1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462279"
---
# <a name="blockstatus"></a><span data-ttu-id="a23b4-103">BlockStatus</span><span class="sxs-lookup"><span data-stu-id="a23b4-103">BlockStatus</span></span>

<span data-ttu-id="a23b4-104">El elemento **BlockStatus** especifica el estado de bloqueo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a23b4-104">The **BlockStatus** element specifies the block status of an item.</span></span> 
  
```XML
<BlockStatus> true | false </BlockStatus
```

 <span data-ttu-id="a23b4-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a23b4-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a23b4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a23b4-106">Attributes and elements</span></span>

<span data-ttu-id="a23b4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a23b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a23b4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a23b4-108">Attributes</span></span>

<span data-ttu-id="a23b4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a23b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a23b4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a23b4-110">Child elements</span></span>

<span data-ttu-id="a23b4-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a23b4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a23b4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a23b4-112">Parent elements</span></span>

|<span data-ttu-id="a23b4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a23b4-113">**Element**</span></span>|<span data-ttu-id="a23b4-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a23b4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a23b4-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a23b4-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a23b4-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a23b4-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a23b4-117">Contacto</span><span class="sxs-lookup"><span data-stu-id="a23b4-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="a23b4-118">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a23b4-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a23b4-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="a23b4-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="a23b4-120">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="a23b4-120">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="a23b4-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="a23b4-121">Item</span></span>](item.md) <br/> |<span data-ttu-id="a23b4-122">Representa un elemento genérico del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a23b4-122">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a23b4-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a23b4-123">Text value</span></span>

<span data-ttu-id="a23b4-124">Un valor de texto de **true** para el elemento **BlockStatus** indica que un elemento está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a23b4-124">A text value of **true** for the **BlockStatus** element indicates that an item is blocked.</span></span> <span data-ttu-id="a23b4-125">Un valor de **false** indica que no se bloquea un elemento.</span><span class="sxs-lookup"><span data-stu-id="a23b4-125">A value of **false** indicates that an item is not blocked.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a23b4-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a23b4-126">Remarks</span></span>

<span data-ttu-id="a23b4-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a23b4-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a23b4-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a23b4-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a23b4-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a23b4-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a23b4-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a23b4-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a23b4-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a23b4-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a23b4-132">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="a23b4-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="a23b4-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a23b4-133">Validation File</span></span>  <br/> |<span data-ttu-id="a23b4-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a23b4-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a23b4-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a23b4-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a23b4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a23b4-136">See also</span></span>



- [<span data-ttu-id="a23b4-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a23b4-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


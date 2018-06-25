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
ms.openlocfilehash: 5733738d733578c47b849b9d7c62c9b66cd8922e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763631"
---
# <a name="blockstatus"></a><span data-ttu-id="fa59e-103">BlockStatus</span><span class="sxs-lookup"><span data-stu-id="fa59e-103">BlockStatus</span></span>

<span data-ttu-id="fa59e-104">El elemento **BlockStatus** especifica el estado de bloqueo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fa59e-104">The **BlockStatus** element specifies the block status of an item.</span></span> 
  
```XML
<BlockStatus> true | false </BlockStatus
```

 <span data-ttu-id="fa59e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa59e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa59e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa59e-106">Attributes and elements</span></span>

<span data-ttu-id="fa59e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa59e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa59e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa59e-108">Attributes</span></span>

<span data-ttu-id="fa59e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa59e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa59e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa59e-110">Child elements</span></span>

<span data-ttu-id="fa59e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa59e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa59e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa59e-112">Parent elements</span></span>

|<span data-ttu-id="fa59e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa59e-113">**Element**</span></span>|<span data-ttu-id="fa59e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa59e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa59e-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="fa59e-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fa59e-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa59e-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fa59e-117">Contact</span><span class="sxs-lookup"><span data-stu-id="fa59e-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="fa59e-118">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa59e-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fa59e-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="fa59e-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="fa59e-120">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="fa59e-120">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="fa59e-121">Item</span><span class="sxs-lookup"><span data-stu-id="fa59e-121">Item</span></span>](item.md) <br/> |<span data-ttu-id="fa59e-122">Representa un elemento genérico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa59e-122">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa59e-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa59e-123">Text value</span></span>

<span data-ttu-id="fa59e-124">Un valor de texto de **true** para el elemento **BlockStatus** indica que un elemento está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="fa59e-124">A text value of **true** for the **BlockStatus** element indicates that an item is blocked.</span></span> <span data-ttu-id="fa59e-125">Un valor de **false** indica que no se bloquea un elemento.</span><span class="sxs-lookup"><span data-stu-id="fa59e-125">A value of **false** indicates that an item is not blocked.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa59e-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa59e-126">Remarks</span></span>

<span data-ttu-id="fa59e-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fa59e-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa59e-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa59e-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa59e-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa59e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa59e-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa59e-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa59e-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa59e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="fa59e-132">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="fa59e-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="fa59e-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa59e-133">Validation File</span></span>  <br/> |<span data-ttu-id="fa59e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa59e-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa59e-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa59e-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa59e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa59e-136">See also</span></span>



- [<span data-ttu-id="fa59e-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fa59e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


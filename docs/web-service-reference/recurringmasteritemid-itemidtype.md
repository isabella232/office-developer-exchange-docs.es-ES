---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: El elemento RecurringMasterItemId (ItemIdType) identifica un elemento principal de periodicidad mediante la identificación de los identificadores de uno de los elementos de repeticiones relacionados.
ms.openlocfilehash: c725998ad3a728ef1f47ff6491592b461753b895
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468442"
---
# <a name="recurringmasteritemid-itemidtype"></a><span data-ttu-id="e5a6a-103">RecurringMasterItemId (ItemIdType)</span><span class="sxs-lookup"><span data-stu-id="e5a6a-103">RecurringMasterItemId (ItemIdType)</span></span>

<span data-ttu-id="e5a6a-104">El elemento **RecurringMasterItemId (ItemIdType)** identifica un elemento principal de periodicidad mediante la identificación de los identificadores de uno de los elementos de repeticiones relacionados.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-104">The **RecurringMasterItemId (ItemIdType)** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="e5a6a-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="e5a6a-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e5a6a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e5a6a-106">Attributes and elements</span></span>

<span data-ttu-id="e5a6a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5a6a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e5a6a-108">Attributes</span></span>

****

|<span data-ttu-id="e5a6a-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e5a6a-109">**Attribute**</span></span>|<span data-ttu-id="e5a6a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5a6a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5a6a-111">Id</span><span class="sxs-lookup"><span data-stu-id="e5a6a-111">Id</span></span>  <br/> |<span data-ttu-id="e5a6a-112">Identifica una única ocurrencia de un elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="e5a6a-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="e5a6a-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="e5a6a-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="e5a6a-115">Identifica una versión específica de una ocurrencia única de un elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="e5a6a-116">Además, el elemento maestro periódico también se identifica porque éste y la única instancia contendrán la misma clave de cambio.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="e5a6a-117">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e5a6a-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e5a6a-118">Child elements</span></span>

<span data-ttu-id="e5a6a-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e5a6a-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e5a6a-120">Parent elements</span></span>

[<span data-ttu-id="e5a6a-121">Aviso</span><span class="sxs-lookup"><span data-stu-id="e5a6a-121">Reminder</span></span>](reminder.md)
  
## <a name="remarks"></a><span data-ttu-id="e5a6a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5a6a-122">Remarks</span></span>

<span data-ttu-id="e5a6a-123">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e5a6a-123">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="e5a6a-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e5a6a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5a6a-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e5a6a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5a6a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5a6a-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5a6a-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e5a6a-127">Schema Name</span></span>  <br/> |<span data-ttu-id="e5a6a-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e5a6a-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="e5a6a-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e5a6a-129">Validation File</span></span>  <br/> |<span data-ttu-id="e5a6a-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e5a6a-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5a6a-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e5a6a-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="e5a6a-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e5a6a-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5a6a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5a6a-133">See also</span></span>



[<span data-ttu-id="e5a6a-134">Aviso</span><span class="sxs-lookup"><span data-stu-id="e5a6a-134">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="e5a6a-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e5a6a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


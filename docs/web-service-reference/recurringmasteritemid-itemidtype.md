---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: El elemento RecurringMasterItemId (ItemIdType) identifica un elemento de patrón de periodicidad mediante la identificación de los identificadores de uno de sus elementos de repetición relacionados.
ms.openlocfilehash: 89089067963e99ac1a6cae6ea6e1e8350d148e82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837010"
---
# <a name="recurringmasteritemid-itemidtype"></a><span data-ttu-id="77f4b-103">RecurringMasterItemId (ItemIdType)</span><span class="sxs-lookup"><span data-stu-id="77f4b-103">RecurringMasterItemId (ItemIdType)</span></span>

<span data-ttu-id="77f4b-104">El elemento **RecurringMasterItemId (ItemIdType)** identifica un elemento de patrón de periodicidad mediante la identificación de los identificadores de uno de sus elementos de repetición relacionados.</span><span class="sxs-lookup"><span data-stu-id="77f4b-104">The **RecurringMasterItemId (ItemIdType)** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="77f4b-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="77f4b-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77f4b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="77f4b-106">Attributes and elements</span></span>

<span data-ttu-id="77f4b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="77f4b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77f4b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="77f4b-108">Attributes</span></span>

****

|<span data-ttu-id="77f4b-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="77f4b-109">**Attribute**</span></span>|<span data-ttu-id="77f4b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f4b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77f4b-111">Id</span><span class="sxs-lookup"><span data-stu-id="77f4b-111">Id</span></span>  <br/> |<span data-ttu-id="77f4b-112">Identifica una sola aparición de un elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="77f4b-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="77f4b-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="77f4b-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="77f4b-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="77f4b-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="77f4b-115">Identifica una versión específica de una sola aparición de un elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="77f4b-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="77f4b-116">Además, el elemento maestro periódico también se identifica porque se y la aparición único va a contener la misma clave de cambio.</span><span class="sxs-lookup"><span data-stu-id="77f4b-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="77f4b-117">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="77f4b-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="77f4b-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="77f4b-118">Child elements</span></span>

<span data-ttu-id="77f4b-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="77f4b-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="77f4b-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="77f4b-120">Parent elements</span></span>

[<span data-ttu-id="77f4b-121">Aviso</span><span class="sxs-lookup"><span data-stu-id="77f4b-121">Reminder</span></span>](reminder.md)
  
## <a name="remarks"></a><span data-ttu-id="77f4b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77f4b-122">Remarks</span></span>

<span data-ttu-id="77f4b-123">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="77f4b-123">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="77f4b-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="77f4b-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77f4b-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="77f4b-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f4b-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77f4b-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77f4b-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="77f4b-127">Schema Name</span></span>  <br/> |<span data-ttu-id="77f4b-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="77f4b-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="77f4b-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="77f4b-129">Validation File</span></span>  <br/> |<span data-ttu-id="77f4b-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77f4b-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77f4b-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="77f4b-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="77f4b-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="77f4b-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77f4b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="77f4b-133">See also</span></span>



[<span data-ttu-id="77f4b-134">Aviso</span><span class="sxs-lookup"><span data-stu-id="77f4b-134">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="77f4b-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="77f4b-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


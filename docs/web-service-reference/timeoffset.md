---
title: TimeOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeOffset
api_type:
- schema
ms.assetid: b70bf498-cc3a-4fa6-8236-514acb973b33
description: El elemento TimeOffset representa el desplazamiento de tiempo desde la hora universal coordinada (UTC) para la transición de zona horaria.
ms.openlocfilehash: 8cfd43477f0548227204da9ebc6d7e9307786845
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460291"
---
# <a name="timeoffset"></a><span data-ttu-id="a96f9-103">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="a96f9-103">TimeOffset</span></span>

<span data-ttu-id="a96f9-104">El elemento **TimeOffset** representa el desplazamiento de tiempo desde la hora universal coordinada (UTC) para la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a96f9-104">The **TimeOffset** element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span> 
  
```XML
<TimeOffset/>
```

 <span data-ttu-id="a96f9-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="a96f9-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a96f9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a96f9-106">Attributes and elements</span></span>

<span data-ttu-id="a96f9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a96f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a96f9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a96f9-108">Attributes</span></span>

<span data-ttu-id="a96f9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a96f9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a96f9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a96f9-110">Child elements</span></span>

<span data-ttu-id="a96f9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a96f9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a96f9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a96f9-112">Parent elements</span></span>

|<span data-ttu-id="a96f9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a96f9-113">**Element**</span></span>|<span data-ttu-id="a96f9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a96f9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a96f9-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="a96f9-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="a96f9-116">Representa una transición de zona horaria que tiene lugar en una fecha específica cada año.</span><span class="sxs-lookup"><span data-stu-id="a96f9-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="a96f9-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="a96f9-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="a96f9-118">Representa una transición de zona horaria que se produce el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="a96f9-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a96f9-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a96f9-119">Text value</span></span>

<span data-ttu-id="a96f9-120">El valor de texto del elemento **TimeOffset** es una duración que especifica el desplazamiento de tiempo respecto a la hora UTC para la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a96f9-120">The text value of the **TimeOffset** element is a duration that specifies the time offset from UTC for the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a96f9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a96f9-121">Remarks</span></span>

<span data-ttu-id="a96f9-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a96f9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a96f9-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a96f9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a96f9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a96f9-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a96f9-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a96f9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a96f9-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a96f9-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="a96f9-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a96f9-127">Validation File</span></span>  <br/> |<span data-ttu-id="a96f9-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a96f9-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a96f9-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a96f9-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="a96f9-130">Falso</span><span class="sxs-lookup"><span data-stu-id="a96f9-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a96f9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a96f9-131">See also</span></span>



- [<span data-ttu-id="a96f9-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a96f9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


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
description: El elemento TimeOffset representa el desplazamiento de tiempo de la hora Universal coordinada (UTC) para la transición de la zona horaria.
ms.openlocfilehash: 46b1b2c8eec9bae871b4dafe43036e9d725075ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840653"
---
# <a name="timeoffset"></a><span data-ttu-id="9fb7d-103">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="9fb7d-103">TimeOffset</span></span>

<span data-ttu-id="9fb7d-104">El elemento **TimeOffset** representa el desplazamiento de tiempo de la hora Universal coordinada (UTC) para la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-104">The **TimeOffset** element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span> 
  
```XML
<TimeOffset/>
```

 <span data-ttu-id="9fb7d-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="9fb7d-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fb7d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9fb7d-106">Attributes and elements</span></span>

<span data-ttu-id="9fb7d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fb7d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9fb7d-108">Attributes</span></span>

<span data-ttu-id="9fb7d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fb7d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9fb7d-110">Child elements</span></span>

<span data-ttu-id="9fb7d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fb7d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9fb7d-112">Parent elements</span></span>

|<span data-ttu-id="9fb7d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fb7d-113">**Element**</span></span>|<span data-ttu-id="9fb7d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fb7d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fb7d-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="9fb7d-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="9fb7d-116">Representa una transición de la zona horaria que se produce en una fecha específica de cada año.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="9fb7d-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="9fb7d-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="9fb7d-118">Representa una transición de la zona horaria que se produce en el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9fb7d-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9fb7d-119">Text value</span></span>

<span data-ttu-id="9fb7d-120">El valor de texto del elemento **TimeOffset** es una duración que especifica el desplazamiento de tiempo de la hora UTC para la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-120">The text value of the **TimeOffset** element is a duration that specifies the time offset from UTC for the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9fb7d-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fb7d-121">Remarks</span></span>

<span data-ttu-id="9fb7d-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9fb7d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fb7d-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9fb7d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fb7d-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9fb7d-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9fb7d-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9fb7d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9fb7d-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9fb7d-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="9fb7d-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9fb7d-127">Validation File</span></span>  <br/> |<span data-ttu-id="9fb7d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9fb7d-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9fb7d-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9fb7d-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fb7d-130">False</span><span class="sxs-lookup"><span data-stu-id="9fb7d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fb7d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fb7d-131">See also</span></span>



- [<span data-ttu-id="9fb7d-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9fb7d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


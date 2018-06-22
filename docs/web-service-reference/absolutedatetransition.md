---
title: AbsoluteDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteDateTransition
api_type:
- schema
ms.assetid: 8f5731eb-bed0-45bf-ba89-4aaf20c34a39
description: El elemento AbsoluteDateTransition representa una transición de la zona horaria que se produce en una fecha específica y a una hora específica.
ms.openlocfilehash: 1e9e5f3f2269814a82b827efe46c71a172e21348
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763382"
---
# <a name="absolutedatetransition"></a><span data-ttu-id="440da-103">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="440da-103">AbsoluteDateTransition</span></span>

<span data-ttu-id="440da-104">El elemento **AbsoluteDateTransition** representa una transición de la zona horaria que se produce en una fecha específica y a una hora específica.</span><span class="sxs-lookup"><span data-stu-id="440da-104">The **AbsoluteDateTransition** element represents a time zone transition that occurs on a specific date and at a specific time.</span></span> 
  
```xml
<AbsoluteDateTransition>
   <To/>
   <DateTime/>
</AbsoluteDateTransition>
```

<span data-ttu-id="440da-105">**AbsoluteDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="440da-105">**AbsoluteDateTransitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="440da-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="440da-106">Attributes and elements</span></span>

<span data-ttu-id="440da-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="440da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="440da-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="440da-108">Attributes</span></span>

<span data-ttu-id="440da-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="440da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="440da-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="440da-110">Child elements</span></span>

|<span data-ttu-id="440da-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="440da-111">**Element**</span></span>|<span data-ttu-id="440da-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="440da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="440da-113">To</span><span class="sxs-lookup"><span data-stu-id="440da-113">To</span></span>](to.md) <br/> |<span data-ttu-id="440da-114">Especifica el [período](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="440da-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="440da-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="440da-115">DateTime</span></span>](datetime.md) <br/> |<span data-ttu-id="440da-116">Representa la fecha y hora en que se produce la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="440da-116">Represents the date and time at which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="440da-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="440da-117">Parent elements</span></span>

|<span data-ttu-id="440da-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="440da-118">**Element**</span></span>|<span data-ttu-id="440da-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="440da-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="440da-120">Transiciones</span><span class="sxs-lookup"><span data-stu-id="440da-120">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="440da-121">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="440da-121">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="440da-122">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="440da-122">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="440da-123">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="440da-123">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="440da-124">Notas</span><span class="sxs-lookup"><span data-stu-id="440da-124">Remarks</span></span>

<span data-ttu-id="440da-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="440da-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="440da-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="440da-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="440da-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="440da-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="440da-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="440da-128">Schema Name</span></span>  <br/> |<span data-ttu-id="440da-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="440da-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="440da-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="440da-130">Validation File</span></span>  <br/> |<span data-ttu-id="440da-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="440da-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="440da-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="440da-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="440da-133">False</span><span class="sxs-lookup"><span data-stu-id="440da-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="440da-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="440da-134">See also</span></span>

- [<span data-ttu-id="440da-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="440da-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


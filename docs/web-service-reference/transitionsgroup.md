---
title: TransitionsGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TransitionsGroup
api_type:
- schema
ms.assetid: 19d56080-546a-4d53-929e-363d56186759
description: El elemento TransitionsGroup representa una matriz de las transiciones de zona horaria.
ms.openlocfilehash: e5991ad7f73a1694e0d4abadd8d252acc04970e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840726"
---
# <a name="transitionsgroup"></a><span data-ttu-id="925e7-103">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="925e7-103">TransitionsGroup</span></span>

<span data-ttu-id="925e7-104">El elemento **TransitionsGroup** representa una matriz de las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="925e7-104">The **TransitionsGroup** element represents an array of time zone transitions.</span></span> 
  
```xml
<TransitionsGroup Id="">
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 <span data-ttu-id="925e7-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="925e7-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="925e7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="925e7-106">Attributes and elements</span></span>

<span data-ttu-id="925e7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="925e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="925e7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="925e7-108">Attributes</span></span>

|<span data-ttu-id="925e7-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="925e7-109">**Attribute**</span></span>|<span data-ttu-id="925e7-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="925e7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="925e7-111">Id</span><span class="sxs-lookup"><span data-stu-id="925e7-111">Id</span></span>  <br/> |<span data-ttu-id="925e7-112">Un valor de tipo string que representa el identificador único del grupo de transiciones.</span><span class="sxs-lookup"><span data-stu-id="925e7-112">A string value that represents the unique identifier of the transitions group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="925e7-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="925e7-113">Child elements</span></span>

|<span data-ttu-id="925e7-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="925e7-114">**Element**</span></span>|<span data-ttu-id="925e7-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="925e7-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="925e7-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="925e7-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="925e7-117">Representa una transición de la zona horaria que se produce en una fecha específica y a una hora específica.</span><span class="sxs-lookup"><span data-stu-id="925e7-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="925e7-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="925e7-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="925e7-119">Representa una transición de la zona horaria que se produce en el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="925e7-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="925e7-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="925e7-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="925e7-121">Representa una transición de la zona horaria que se produce en un día del año especificado.</span><span class="sxs-lookup"><span data-stu-id="925e7-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="925e7-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="925e7-122">Parent elements</span></span>

|<span data-ttu-id="925e7-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="925e7-123">**Element**</span></span>|<span data-ttu-id="925e7-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="925e7-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="925e7-125">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="925e7-125">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="925e7-126">Representa una matriz de grupos de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="925e7-126">Represents an array of time zone transition groups.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="925e7-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="925e7-127">Remarks</span></span>

<span data-ttu-id="925e7-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="925e7-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="925e7-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="925e7-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="925e7-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="925e7-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="925e7-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="925e7-131">Schema Name</span></span>  <br/> |<span data-ttu-id="925e7-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="925e7-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="925e7-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="925e7-133">Validation File</span></span>  <br/> |<span data-ttu-id="925e7-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="925e7-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="925e7-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="925e7-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="925e7-136">False</span><span class="sxs-lookup"><span data-stu-id="925e7-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="925e7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="925e7-137">See also</span></span>



- [<span data-ttu-id="925e7-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="925e7-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


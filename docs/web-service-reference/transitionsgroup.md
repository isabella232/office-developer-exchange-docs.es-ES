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
description: El elemento TransitionsGroup representa una matriz de transiciones de zona horaria.
ms.openlocfilehash: 9f08dec048d410dadab9580e7886b2499d943176
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467420"
---
# <a name="transitionsgroup"></a><span data-ttu-id="a3d88-103">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="a3d88-103">TransitionsGroup</span></span>

<span data-ttu-id="a3d88-104">El elemento **TransitionsGroup** representa una matriz de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a3d88-104">The **TransitionsGroup** element represents an array of time zone transitions.</span></span> 
  
```xml
<TransitionsGroup Id="">
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 <span data-ttu-id="a3d88-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="a3d88-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3d88-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a3d88-106">Attributes and elements</span></span>

<span data-ttu-id="a3d88-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a3d88-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3d88-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a3d88-108">Attributes</span></span>

|<span data-ttu-id="a3d88-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a3d88-109">**Attribute**</span></span>|<span data-ttu-id="a3d88-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3d88-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3d88-111">Id</span><span class="sxs-lookup"><span data-stu-id="a3d88-111">Id</span></span>  <br/> |<span data-ttu-id="a3d88-112">Un valor de tipo String que representa el identificador único del grupo de transiciones.</span><span class="sxs-lookup"><span data-stu-id="a3d88-112">A string value that represents the unique identifier of the transitions group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3d88-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3d88-113">Child elements</span></span>

|<span data-ttu-id="a3d88-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a3d88-114">**Element**</span></span>|<span data-ttu-id="a3d88-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3d88-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3d88-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="a3d88-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="a3d88-117">Representa una transición de zona horaria que se produce en una fecha específica y a una hora específica.</span><span class="sxs-lookup"><span data-stu-id="a3d88-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="a3d88-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="a3d88-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="a3d88-119">Representa una transición de zona horaria que se produce el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="a3d88-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="a3d88-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="a3d88-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="a3d88-121">Representa una transición de zona horaria que se produce en un día del año especificado.</span><span class="sxs-lookup"><span data-stu-id="a3d88-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3d88-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a3d88-122">Parent elements</span></span>

|<span data-ttu-id="a3d88-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a3d88-123">**Element**</span></span>|<span data-ttu-id="a3d88-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3d88-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3d88-125">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="a3d88-125">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="a3d88-126">Representa una matriz de grupos de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a3d88-126">Represents an array of time zone transition groups.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3d88-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3d88-127">Remarks</span></span>

<span data-ttu-id="a3d88-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a3d88-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3d88-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a3d88-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3d88-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3d88-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a3d88-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a3d88-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a3d88-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a3d88-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="a3d88-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a3d88-133">Validation File</span></span>  <br/> |<span data-ttu-id="a3d88-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a3d88-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a3d88-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a3d88-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3d88-136">Falso</span><span class="sxs-lookup"><span data-stu-id="a3d88-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3d88-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3d88-137">See also</span></span>



- [<span data-ttu-id="a3d88-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a3d88-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


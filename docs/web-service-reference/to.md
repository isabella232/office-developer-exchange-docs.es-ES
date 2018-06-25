---
title: Para
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: El elemento especifica el destino de la transición de la zona horaria. El destino es un período de zona horaria o un grupo de transiciones de zona horaria.
ms.openlocfilehash: dc7df8ed3ddd6a9b4222ffab4c2b47b00ee4ba0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840682"
---
# <a name="to"></a><span data-ttu-id="f0727-104">Para</span><span class="sxs-lookup"><span data-stu-id="f0727-104">To</span></span>

<span data-ttu-id="f0727-105">El elemento **que** especifica el destino de la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f0727-105">The **To** element specifies the target of the time zone transition.</span></span> <span data-ttu-id="f0727-106">El destino es un período de zona horaria o un grupo de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f0727-106">The target is either a time zone period or a group of time zone transitions.</span></span> 
  
```xml
<To Kind=""/>
```

 <span data-ttu-id="f0727-107">**TransitionTargetType**</span><span class="sxs-lookup"><span data-stu-id="f0727-107">**TransitionTargetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0727-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0727-108">Attributes and elements</span></span>

<span data-ttu-id="f0727-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0727-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0727-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0727-110">Attributes</span></span>

|<span data-ttu-id="f0727-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f0727-111">**Attribute**</span></span>|<span data-ttu-id="f0727-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0727-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0727-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0727-113">Kind</span></span>  <br/> |<span data-ttu-id="f0727-114">Indica si el destino de la transición de zona horaria es un período de zona horaria o de un grupo de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f0727-114">Indicates whether the time zone transition target is a time zone period or of a group of time zone transitions.</span></span>  <br/> |
   
#### <a name="kind-attribute-values"></a><span data-ttu-id="f0727-115">Valores de atributo Kind</span><span class="sxs-lookup"><span data-stu-id="f0727-115">Kind attribute values</span></span>

|<span data-ttu-id="f0727-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f0727-116">**Value**</span></span>|<span data-ttu-id="f0727-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0727-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0727-118">Punto</span><span class="sxs-lookup"><span data-stu-id="f0727-118">Period</span></span>  <br/> |<span data-ttu-id="f0727-119">Especifica que el destino de la transición de zona horaria es un período de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f0727-119">Specifies that the time zone transition target is a time zone period.</span></span>  <br/> |
|<span data-ttu-id="f0727-120">Group</span><span class="sxs-lookup"><span data-stu-id="f0727-120">Group</span></span>  <br/> |<span data-ttu-id="f0727-121">Especifica que el destino de la transición de zona horaria es un grupo de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f0727-121">Specifies that the time zone transition target is a group of time zone transitions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f0727-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0727-122">Child elements</span></span>

<span data-ttu-id="f0727-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0727-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f0727-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0727-124">Parent elements</span></span>

|<span data-ttu-id="f0727-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0727-125">**Element**</span></span>|<span data-ttu-id="f0727-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0727-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0727-127">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="f0727-127">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="f0727-128">Representa una transición de la zona horaria que se produce en una fecha específica y a una hora específica.</span><span class="sxs-lookup"><span data-stu-id="f0727-128">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="f0727-129">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="f0727-129">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="f0727-130">Representa una transición de la zona horaria que se produce en el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="f0727-130">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="f0727-131">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="f0727-131">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="f0727-132">Representa una transición de la zona horaria que se produce en un día del año especificado.</span><span class="sxs-lookup"><span data-stu-id="f0727-132">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="f0727-133">Transición</span><span class="sxs-lookup"><span data-stu-id="f0727-133">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="f0727-134">Representa una transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f0727-134">Represents a time zone transition.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f0727-135">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f0727-135">Text value</span></span>

<span data-ttu-id="f0727-136">El valor de texto es una cadena que especifica el identificador exclusivo del [período](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f0727-136">The text value is a string that specifies the unique identifier of the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f0727-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0727-137">Remarks</span></span>

<span data-ttu-id="f0727-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f0727-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0727-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f0727-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0727-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0727-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0727-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f0727-141">Schema Name</span></span>  <br/> |<span data-ttu-id="f0727-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f0727-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="f0727-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f0727-143">Validation File</span></span>  <br/> |<span data-ttu-id="f0727-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f0727-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0727-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f0727-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0727-146">False</span><span class="sxs-lookup"><span data-stu-id="f0727-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0727-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0727-147">See also</span></span>



- [<span data-ttu-id="f0727-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f0727-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


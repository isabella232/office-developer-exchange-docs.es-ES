---
title: TimeWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeWindow
api_type:
- schema
ms.assetid: 49c79266-353a-4036-a8e2-8a4660d0d8ea
description: El elemento TimeWindow identifica el intervalo de tiempo consultado para la información de disponibilidad del usuario.
ms.openlocfilehash: 5c66614520f9d616687d67ad609b3d55d9cf6571
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458932"
---
# <a name="timewindow"></a><span data-ttu-id="76221-103">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="76221-103">TimeWindow</span></span>

<span data-ttu-id="76221-104">El elemento **TimeWindow** identifica el intervalo de tiempo consultado para la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="76221-104">The **TimeWindow** element identifies the time span queried for the user availability information.</span></span> 
  
[<span data-ttu-id="76221-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="76221-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="76221-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="76221-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="76221-107">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="76221-107">TimeWindow</span></span>](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 <span data-ttu-id="76221-108">**Duración**</span><span class="sxs-lookup"><span data-stu-id="76221-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76221-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="76221-109">Attributes and elements</span></span>

<span data-ttu-id="76221-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="76221-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76221-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="76221-111">Attributes</span></span>

<span data-ttu-id="76221-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="76221-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76221-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="76221-113">Child elements</span></span>

|<span data-ttu-id="76221-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="76221-114">**Element**</span></span>|<span data-ttu-id="76221-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76221-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76221-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="76221-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="76221-117">Representa el inicio de un intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="76221-117">Represents the start of a time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="76221-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="76221-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="76221-119">Representa el final de un intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="76221-119">Represents the end of a time span queried for the user availability information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76221-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="76221-120">Parent elements</span></span>

|<span data-ttu-id="76221-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="76221-121">**Element**</span></span>|<span data-ttu-id="76221-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76221-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76221-123">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="76221-123">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="76221-124">Especifica el tipo de información de disponibilidad devuelta en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76221-124">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="76221-125">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="76221-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76221-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76221-126">Remarks</span></span>

<span data-ttu-id="76221-127">El valor máximo para este período de tiempo es de 42 días.</span><span class="sxs-lookup"><span data-stu-id="76221-127">The maximum value for this time period is 42 days.</span></span> <span data-ttu-id="76221-128">Este valor máximo se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="76221-128">This maximum value can be modified.</span></span> <span data-ttu-id="76221-129">Cualquier solicitud de información de disponibilidad del usuario que no supere el valor máximo devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="76221-129">Any requests for user availability information beyond the maximum value will return an error.</span></span> <span data-ttu-id="76221-130">Si alguna de las citas se encuentra parcialmente en el intervalo de tiempo definido por los elementos [startTime](starttime.md) y [EndTime](endtime.md) , la cita se incluirá en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="76221-130">If any appointments are partially in the time span defined by the [StartTime](starttime.md) and [EndTime](endtime.md) elements, that appointment is included in its entirety.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="76221-131">El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="76221-131">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="76221-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="76221-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76221-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="76221-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="76221-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="76221-134">Schema Name</span></span>  <br/> |<span data-ttu-id="76221-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="76221-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="76221-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="76221-136">Validation File</span></span>  <br/> |<span data-ttu-id="76221-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="76221-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="76221-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="76221-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="76221-139">Falso</span><span class="sxs-lookup"><span data-stu-id="76221-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76221-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="76221-140">See also</span></span>



[<span data-ttu-id="76221-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="76221-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="76221-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="76221-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


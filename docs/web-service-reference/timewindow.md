---
title: Ventana de tiempo
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
description: El elemento de la ventana de tiempo identifica el intervalo de tiempo de consulta para la información de disponibilidad del usuario.
ms.openlocfilehash: 05858b4d62b72b3ff9904c90652bb1bff78ceb41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840677"
---
# <a name="timewindow"></a><span data-ttu-id="4562b-103">Ventana de tiempo</span><span class="sxs-lookup"><span data-stu-id="4562b-103">TimeWindow</span></span>

<span data-ttu-id="4562b-104">El elemento de la **ventana de tiempo** identifica el intervalo de tiempo de consulta para la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="4562b-104">The **TimeWindow** element identifies the time span queried for the user availability information.</span></span> 
  
[<span data-ttu-id="4562b-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="4562b-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="4562b-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="4562b-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="4562b-107">Ventana de tiempo</span><span class="sxs-lookup"><span data-stu-id="4562b-107">TimeWindow</span></span>](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 <span data-ttu-id="4562b-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="4562b-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4562b-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4562b-109">Attributes and elements</span></span>

<span data-ttu-id="4562b-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4562b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4562b-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="4562b-111">Attributes</span></span>

<span data-ttu-id="4562b-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4562b-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4562b-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4562b-113">Child elements</span></span>

|<span data-ttu-id="4562b-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="4562b-114">**Element**</span></span>|<span data-ttu-id="4562b-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4562b-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4562b-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="4562b-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="4562b-117">Representa el inicio de un intervalo de tiempo de consulta para la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="4562b-117">Represents the start of a time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="4562b-118">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="4562b-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="4562b-119">Representa el final de un intervalo de tiempo de consulta para la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="4562b-119">Represents the end of a time span queried for the user availability information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4562b-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4562b-120">Parent elements</span></span>

|<span data-ttu-id="4562b-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4562b-121">**Element**</span></span>|<span data-ttu-id="4562b-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4562b-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4562b-123">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="4562b-123">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="4562b-124">Especifica el tipo de información de libre/ocupado devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4562b-124">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="4562b-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="4562b-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4562b-126">Notas</span><span class="sxs-lookup"><span data-stu-id="4562b-126">Remarks</span></span>

<span data-ttu-id="4562b-127">El valor máximo para este período de tiempo es 42 días.</span><span class="sxs-lookup"><span data-stu-id="4562b-127">The maximum value for this time period is 42 days.</span></span> <span data-ttu-id="4562b-128">Este valor máximo puede modificarse.</span><span class="sxs-lookup"><span data-stu-id="4562b-128">This maximum value can be modified.</span></span> <span data-ttu-id="4562b-129">Las solicitudes de usuario la información de disponibilidad más allá del valor máximo devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="4562b-129">Any requests for user availability information beyond the maximum value will return an error.</span></span> <span data-ttu-id="4562b-130">Si todas las citas se encuentran parcialmente en el intervalo de tiempo definido por los elementos [StartTime](starttime.md) y [EndTime](endtime.md) , esa cita se incluye en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="4562b-130">If any appointments are partially in the time span defined by the [StartTime](starttime.md) and [EndTime](endtime.md) elements, that appointment is included in its entirety.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4562b-131">El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4562b-131">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4562b-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4562b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4562b-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4562b-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4562b-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4562b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4562b-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4562b-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4562b-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4562b-136">Validation File</span></span>  <br/> |<span data-ttu-id="4562b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4562b-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4562b-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4562b-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4562b-139">False</span><span class="sxs-lookup"><span data-stu-id="4562b-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4562b-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="4562b-140">See also</span></span>



[<span data-ttu-id="4562b-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="4562b-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="4562b-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="4562b-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


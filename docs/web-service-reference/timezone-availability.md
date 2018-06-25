---
title: TimeZone (disponibilidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: El elemento TimeZone contiene elementos que identifican la información de zona horaria. Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano.
ms.openlocfilehash: dc2466e8039819edc82294ff05f1746ada64cb43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840693"
---
# <a name="timezone-availability"></a><span data-ttu-id="58899-104">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="58899-104">TimeZone (Availability)</span></span>

<span data-ttu-id="58899-105">El elemento **TimeZone** contiene elementos que identifican la información de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="58899-105">The **TimeZone** element contains elements that identify time zone information.</span></span> <span data-ttu-id="58899-106">Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="58899-106">This element also contains information about the transition between standard time and daylight saving time.</span></span> 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 <span data-ttu-id="58899-107">**SerializableTimeZone**</span><span class="sxs-lookup"><span data-stu-id="58899-107">**SerializableTimeZone**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58899-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="58899-108">Attributes and elements</span></span>

<span data-ttu-id="58899-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="58899-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58899-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="58899-110">Attributes</span></span>

<span data-ttu-id="58899-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58899-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58899-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58899-112">Child elements</span></span>

|<span data-ttu-id="58899-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="58899-113">**Element**</span></span>|<span data-ttu-id="58899-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58899-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58899-115">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="58899-115">Bias (UTC)</span></span>](bias-utc.md) <br/> |<span data-ttu-id="58899-116">Representa el desplazamiento general de la hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="58899-116">Represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="58899-117">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="58899-117">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="58899-118">StandardTime</span><span class="sxs-lookup"><span data-stu-id="58899-118">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="58899-119">Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="58899-119">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="58899-120">Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="58899-120">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/> |
|[<span data-ttu-id="58899-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="58899-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="58899-122">Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="58899-122">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="58899-123">Este elemento también contiene información acerca de cuándo se produce la transición al horario de verano de tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="58899-123">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="58899-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58899-124">Parent elements</span></span>

|<span data-ttu-id="58899-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="58899-125">**Element**</span></span>|<span data-ttu-id="58899-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58899-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58899-127">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="58899-127">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="58899-128">Contiene los argumentos utilizados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="58899-128">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="58899-129">Esto es un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="58899-129">This is a root element.</span></span>  <br/> <span data-ttu-id="58899-130">El elemento de la **zona horaria** en el mensaje GetUserAvailabilityRequest representa la zona horaria en la que se especifican los valores de fecha y hora de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58899-130">The **TimeZone** element in the GetUserAvailabilityRequest message represents the time zone in which the DateTime values in the request are specified.</span></span> <span data-ttu-id="58899-131">Los valores de fecha y hora devueltos por el servicio de disponibilidad también están en esta zona horaria.</span><span class="sxs-lookup"><span data-stu-id="58899-131">The DateTime values returned by the Availability service are also in this time zone.</span></span>  <br/> <span data-ttu-id="58899-132">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="58899-132">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[<span data-ttu-id="58899-133">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="58899-133">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="58899-134">Representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="58899-134">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="58899-135">El elemento de la **zona horaria** en el mensaje GetUserAvailabilityResponse representa la configuración de zona horaria del usuario de buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="58899-135">The **TimeZone** element in the GetUserAvailabilityResponse message represents the time zone settings of the requested mailbox user.</span></span>  <br/> <span data-ttu-id="58899-136">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="58899-136">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58899-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58899-137">Remarks</span></span>

<span data-ttu-id="58899-138">Este elemento es necesario en el elemento [GetUserAvailabilityRequest](getuseravailabilityrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="58899-138">This element is required in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) element.</span></span> <span data-ttu-id="58899-139">Este elemento se produce como máximo una vez o al menos cero veces cuando el elemento primario es el elemento [WorkingHours](workinghours-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="58899-139">This element occurs at most once or at least zero times when the parent element is the [WorkingHours](workinghours-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="58899-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58899-140">Example</span></span>

<span data-ttu-id="58899-141">En el ejemplo siguiente se muestra parte de una solicitud XML que identifica un desplazamiento de la hora UTC de 8 horas en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="58899-141">The following example shows part of an XML request that identifies an offset from UTC of 8 hours in the client application.</span></span>
  
```XML
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>11</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>2</DayOrder>
    <Month>3</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

## <a name="element-information"></a><span data-ttu-id="58899-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58899-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58899-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58899-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58899-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="58899-144">Schema Name</span></span>  <br/> |<span data-ttu-id="58899-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="58899-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="58899-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="58899-146">Validation File</span></span>  <br/> |<span data-ttu-id="58899-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58899-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58899-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="58899-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="58899-149">False</span><span class="sxs-lookup"><span data-stu-id="58899-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58899-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="58899-150">See also</span></span>



[<span data-ttu-id="58899-151">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="58899-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="58899-152">Bias</span><span class="sxs-lookup"><span data-stu-id="58899-152">Bias</span></span>](bias.md)


[<span data-ttu-id="58899-153">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="58899-153">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


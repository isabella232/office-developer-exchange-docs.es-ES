---
title: Zona horaria (disponibilidad)
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
description: El elemento TimeZone contiene elementos que identifican la información de la zona horaria. Este elemento también contiene información sobre la transición entre el horario estándar y el horario de verano.
ms.openlocfilehash: ba4b0a4805dba54450e01e89c5e9ef746404b716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460277"
---
# <a name="timezone-availability"></a><span data-ttu-id="fbf99-104">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="fbf99-104">TimeZone (Availability)</span></span>

<span data-ttu-id="fbf99-105">El elemento **TimeZone** contiene elementos que identifican la información de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fbf99-105">The **TimeZone** element contains elements that identify time zone information.</span></span> <span data-ttu-id="fbf99-106">Este elemento también contiene información sobre la transición entre el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="fbf99-106">This element also contains information about the transition between standard time and daylight saving time.</span></span> 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 <span data-ttu-id="fbf99-107">**SerializableTimeZone**</span><span class="sxs-lookup"><span data-stu-id="fbf99-107">**SerializableTimeZone**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbf99-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fbf99-108">Attributes and elements</span></span>

<span data-ttu-id="fbf99-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fbf99-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbf99-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbf99-110">Attributes</span></span>

<span data-ttu-id="fbf99-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fbf99-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbf99-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fbf99-112">Child elements</span></span>

|<span data-ttu-id="fbf99-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbf99-113">**Element**</span></span>|<span data-ttu-id="fbf99-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbf99-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbf99-115">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="fbf99-115">Bias (UTC)</span></span>](bias-utc.md) <br/> |<span data-ttu-id="fbf99-116">Representa el desplazamiento general desde la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="fbf99-116">Represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fbf99-117">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="fbf99-117">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="fbf99-118">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="fbf99-118">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="fbf99-119">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf99-119">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="fbf99-120">Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="fbf99-120">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/> |
|[<span data-ttu-id="fbf99-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="fbf99-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="fbf99-122">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="fbf99-122">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="fbf99-123">Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="fbf99-123">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbf99-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fbf99-124">Parent elements</span></span>

|<span data-ttu-id="fbf99-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbf99-125">**Element**</span></span>|<span data-ttu-id="fbf99-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbf99-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbf99-127">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="fbf99-127">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="fbf99-128">Contiene los argumentos usados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="fbf99-128">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="fbf99-129">Se trata de un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="fbf99-129">This is a root element.</span></span>  <br/> <span data-ttu-id="fbf99-130">El elemento **TimeZone** del mensaje GetUserAvailabilityRequest representa la zona horaria en la que se especifican los valores DATETIME de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbf99-130">The **TimeZone** element in the GetUserAvailabilityRequest message represents the time zone in which the DateTime values in the request are specified.</span></span> <span data-ttu-id="fbf99-131">Los valores de fecha y hora devueltos por el servicio de disponibilidad también están en esta zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fbf99-131">The DateTime values returned by the Availability service are also in this time zone.</span></span>  <br/> <span data-ttu-id="fbf99-132">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="fbf99-132">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[<span data-ttu-id="fbf99-133">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="fbf99-133">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fbf99-134">Representa la configuración de la zona horaria y el horario laboral del usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="fbf99-134">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="fbf99-135">El elemento **TimeZone** del mensaje GetUserAvailabilityResponse representa la configuración de la zona horaria del usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="fbf99-135">The **TimeZone** element in the GetUserAvailabilityResponse message represents the time zone settings of the requested mailbox user.</span></span>  <br/> <span data-ttu-id="fbf99-136">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="fbf99-136">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbf99-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbf99-137">Remarks</span></span>

<span data-ttu-id="fbf99-138">Este elemento es obligatorio en el elemento [GetUserAvailabilityRequest](getuseravailabilityrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf99-138">This element is required in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) element.</span></span> <span data-ttu-id="fbf99-139">Este elemento se produce al menos una vez o al menos cero veces cuando el elemento primario es el elemento [WorkingHours](workinghours-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf99-139">This element occurs at most once or at least zero times when the parent element is the [WorkingHours](workinghours-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fbf99-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fbf99-140">Example</span></span>

<span data-ttu-id="fbf99-141">En el ejemplo siguiente se muestra parte de una solicitud XML que identifica un desplazamiento respecto a la hora UTC de 8 horas en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="fbf99-141">The following example shows part of an XML request that identifies an offset from UTC of 8 hours in the client application.</span></span>
  
```XML
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="fbf99-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fbf99-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbf99-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbf99-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbf99-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fbf99-144">Schema Name</span></span>  <br/> |<span data-ttu-id="fbf99-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fbf99-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="fbf99-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fbf99-146">Validation File</span></span>  <br/> |<span data-ttu-id="fbf99-147">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fbf99-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbf99-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fbf99-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="fbf99-149">Falso</span><span class="sxs-lookup"><span data-stu-id="fbf99-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbf99-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbf99-150">See also</span></span>



[<span data-ttu-id="fbf99-151">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="fbf99-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="fbf99-152">Sesgo</span><span class="sxs-lookup"><span data-stu-id="fbf99-152">Bias</span></span>](bias.md)


[<span data-ttu-id="fbf99-153">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="fbf99-153">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


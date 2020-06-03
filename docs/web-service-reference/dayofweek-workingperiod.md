---
title: DayOfWeek (WorkingPeriod)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 7a8a8cc1-392b-4db5-bb76-710477e31396
description: El elemento DayOfWeek contiene la lista de días laborables programados para el usuario del buzón.
ms.openlocfilehash: 06d4a7d5541b3b71fcbf9be9beb7512d06853283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457448"
---
# <a name="dayofweek-workingperiod"></a><span data-ttu-id="2c886-103">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="2c886-103">DayOfWeek (WorkingPeriod)</span></span>

<span data-ttu-id="2c886-104">El elemento **DayOfWeek** contiene la lista de días laborables programados para el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="2c886-104">The **DayOfWeek** element contains the list of working days scheduled for the mailbox user.</span></span> 
  
- [<span data-ttu-id="2c886-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2c886-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="2c886-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="2c886-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)  
- [<span data-ttu-id="2c886-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="2c886-107">FreeBusyResponse</span></span>](freebusyresponse.md)  
- [<span data-ttu-id="2c886-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="2c886-108">FreeBusyView</span></span>](freebusyview.md)  
- [<span data-ttu-id="2c886-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="2c886-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)  
- [<span data-ttu-id="2c886-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="2c886-110">WorkingPeriodArray</span></span>](workingperiodarray.md) 
- [<span data-ttu-id="2c886-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="2c886-111">WorkingPeriod</span></span>](workingperiod.md)  
- [<span data-ttu-id="2c886-112">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="2c886-112">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

<span data-ttu-id="2c886-113">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="2c886-113">**DaysOfWeek**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2c886-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2c886-114">Attributes and elements</span></span>

<span data-ttu-id="2c886-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2c886-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c886-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="2c886-116">Attributes</span></span>

<span data-ttu-id="2c886-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2c886-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c886-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c886-118">Child elements</span></span>

<span data-ttu-id="2c886-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2c886-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c886-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2c886-120">Parent elements</span></span>

|<span data-ttu-id="2c886-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2c886-121">**Element**</span></span>|<span data-ttu-id="2c886-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c886-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c886-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="2c886-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="2c886-124">Contiene la semana laboral días y horas del usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2c886-124">Contains the work week days and hours of the mailbox user.</span></span><br/><br/><span data-ttu-id="2c886-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="2c886-125">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c886-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2c886-126">Text value</span></span>

<span data-ttu-id="2c886-127">Se devuelve un valor de texto si el usuario del buzón de correo tiene días establecidos para representar la semana laboral.</span><span class="sxs-lookup"><span data-stu-id="2c886-127">A text value is returned if the mailbox user has days set to represent the work week.</span></span> <span data-ttu-id="2c886-128">A continuación se muestran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="2c886-128">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="2c886-129">Domingo</span><span class="sxs-lookup"><span data-stu-id="2c886-129">Sunday</span></span>    
- <span data-ttu-id="2c886-130">lunes</span><span class="sxs-lookup"><span data-stu-id="2c886-130">Monday</span></span>    
- <span data-ttu-id="2c886-131">martes</span><span class="sxs-lookup"><span data-stu-id="2c886-131">Tuesday</span></span>    
- <span data-ttu-id="2c886-132">miércoles</span><span class="sxs-lookup"><span data-stu-id="2c886-132">Wednesday</span></span>    
- <span data-ttu-id="2c886-133">jueves</span><span class="sxs-lookup"><span data-stu-id="2c886-133">Thursday</span></span>    
- <span data-ttu-id="2c886-134">viernes</span><span class="sxs-lookup"><span data-stu-id="2c886-134">Friday</span></span>    
- <span data-ttu-id="2c886-135">Sábado</span><span class="sxs-lookup"><span data-stu-id="2c886-135">Saturday</span></span> 
    
<span data-ttu-id="2c886-136">Los valores de texto se devolverán en ese orden.</span><span class="sxs-lookup"><span data-stu-id="2c886-136">The text values will be returned in that order.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c886-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c886-137">Remarks</span></span>

<span data-ttu-id="2c886-138">Es importante tener en cuenta que la diferencia entre este elemento y el elemento de disponibilidad de [DayOfWeek (TimeZone)](dayofweek-timezone.md) es el tipo.</span><span class="sxs-lookup"><span data-stu-id="2c886-138">It is important to note that the difference between this element and the Availability [DayOfWeek (TimeZone)](dayofweek-timezone.md) element is the type.</span></span> 
  
<span data-ttu-id="2c886-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2c886-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c886-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2c886-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c886-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c886-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c886-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2c886-142">Schema Name</span></span>  <br/> |<span data-ttu-id="2c886-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2c886-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c886-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2c886-144">Validation File</span></span>  <br/> |<span data-ttu-id="2c886-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2c886-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c886-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2c886-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c886-147">Falso</span><span class="sxs-lookup"><span data-stu-id="2c886-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c886-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c886-148">See also</span></span>

- [<span data-ttu-id="2c886-149">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="2c886-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="2c886-150">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2c886-150">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="2c886-151">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="2c886-151">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


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
description: El elemento DayOfWeek contiene la lista de días de trabajo programado para el usuario del buzón.
ms.openlocfilehash: a6a68017291ba13f45b3970307669222d583fcbb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764058"
---
# <a name="dayofweek-workingperiod"></a><span data-ttu-id="e7393-103">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="e7393-103">DayOfWeek (WorkingPeriod)</span></span>

<span data-ttu-id="e7393-104">El elemento **DayOfWeek** contiene la lista de días de trabajo programado para el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="e7393-104">The **DayOfWeek** element contains the list of working days scheduled for the mailbox user.</span></span> 
  
- [<span data-ttu-id="e7393-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e7393-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="e7393-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="e7393-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)  
- [<span data-ttu-id="e7393-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="e7393-107">FreeBusyResponse</span></span>](freebusyresponse.md)  
- [<span data-ttu-id="e7393-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="e7393-108">FreeBusyView</span></span>](freebusyview.md)  
- [<span data-ttu-id="e7393-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="e7393-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)  
- [<span data-ttu-id="e7393-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="e7393-110">WorkingPeriodArray</span></span>](workingperiodarray.md) 
- [<span data-ttu-id="e7393-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="e7393-111">WorkingPeriod</span></span>](workingperiod.md)  
- [<span data-ttu-id="e7393-112">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="e7393-112">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

<span data-ttu-id="e7393-113">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="e7393-113">**DaysOfWeek**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e7393-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e7393-114">Attributes and elements</span></span>

<span data-ttu-id="e7393-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e7393-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7393-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7393-116">Attributes</span></span>

<span data-ttu-id="e7393-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e7393-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7393-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e7393-118">Child elements</span></span>

<span data-ttu-id="e7393-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e7393-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7393-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e7393-120">Parent elements</span></span>

|<span data-ttu-id="e7393-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7393-121">**Element**</span></span>|<span data-ttu-id="e7393-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7393-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7393-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="e7393-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="e7393-124">Contiene la semana laboral días y las horas del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e7393-124">Contains the work week days and hours of the mailbox user.</span></span><br/><br/><span data-ttu-id="e7393-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="e7393-125">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e7393-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e7393-126">Text value</span></span>

<span data-ttu-id="e7393-127">Si el usuario del buzón tiene días que se establezca para representar la semana laboral, se devuelve un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="e7393-127">A text value is returned if the mailbox user has days set to represent the work week.</span></span> <span data-ttu-id="e7393-128">Los siguientes son los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="e7393-128">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="e7393-129">Domingo</span><span class="sxs-lookup"><span data-stu-id="e7393-129">Sunday</span></span>    
- <span data-ttu-id="e7393-130">Lunes</span><span class="sxs-lookup"><span data-stu-id="e7393-130">Monday</span></span>    
- <span data-ttu-id="e7393-131">Martes</span><span class="sxs-lookup"><span data-stu-id="e7393-131">Tuesday</span></span>    
- <span data-ttu-id="e7393-132">Miércoles</span><span class="sxs-lookup"><span data-stu-id="e7393-132">Wednesday</span></span>    
- <span data-ttu-id="e7393-133">Jueves</span><span class="sxs-lookup"><span data-stu-id="e7393-133">Thursday</span></span>    
- <span data-ttu-id="e7393-134">Viernes</span><span class="sxs-lookup"><span data-stu-id="e7393-134">Friday</span></span>    
- <span data-ttu-id="e7393-135">Sábado</span><span class="sxs-lookup"><span data-stu-id="e7393-135">Saturday</span></span> 
    
<span data-ttu-id="e7393-136">En ese orden, se devolverán los valores de texto.</span><span class="sxs-lookup"><span data-stu-id="e7393-136">The text values will be returned in that order.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7393-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7393-137">Remarks</span></span>

<span data-ttu-id="e7393-138">Es importante tener en cuenta que la diferencia entre este elemento y el elemento de disponibilidad [DayOfWeek (TimeZone)](dayofweek-timezone.md) es el tipo.</span><span class="sxs-lookup"><span data-stu-id="e7393-138">It is important to note that the difference between this element and the Availability [DayOfWeek (TimeZone)](dayofweek-timezone.md) element is the type.</span></span> 
  
<span data-ttu-id="e7393-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e7393-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7393-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e7393-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7393-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7393-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7393-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e7393-142">Schema Name</span></span>  <br/> |<span data-ttu-id="e7393-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e7393-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7393-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e7393-144">Validation File</span></span>  <br/> |<span data-ttu-id="e7393-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7393-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7393-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e7393-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="e7393-147">False</span><span class="sxs-lookup"><span data-stu-id="e7393-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7393-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7393-148">See also</span></span>

- [<span data-ttu-id="e7393-149">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="e7393-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="e7393-150">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e7393-150">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="e7393-151">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="e7393-151">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


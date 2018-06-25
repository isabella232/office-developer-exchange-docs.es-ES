---
title: EndTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTimeInMinutes
api_type:
- schema
ms.assetid: ef05bdda-7a66-44db-bb73-a2ce8316c257
description: El elemento EndTimeInMinutes representa el final del día laborable para un usuario de buzón de correo.
ms.openlocfilehash: 2885d810512eb0e575aa25b4f38d28332a10b8f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764430"
---
# <a name="endtimeinminutes"></a><span data-ttu-id="f0bab-103">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f0bab-103">EndTimeInMinutes</span></span>

<span data-ttu-id="f0bab-104">El elemento **EndTimeInMinutes** representa el final del día laborable para un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f0bab-104">The **EndTimeInMinutes** element represents the end of the working day for a mailbox user.</span></span> 
  
[<span data-ttu-id="f0bab-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f0bab-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="f0bab-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="f0bab-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="f0bab-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="f0bab-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="f0bab-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="f0bab-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="f0bab-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="f0bab-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="f0bab-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="f0bab-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="f0bab-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="f0bab-111">WorkingPeriod</span></span>](workingperiod.md)
  
[<span data-ttu-id="f0bab-112">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f0bab-112">EndTimeInMinutes</span></span>](endtimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

 <span data-ttu-id="f0bab-113">**int**</span><span class="sxs-lookup"><span data-stu-id="f0bab-113">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0bab-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0bab-114">Attributes and elements</span></span>

<span data-ttu-id="f0bab-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0bab-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0bab-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0bab-116">Attributes</span></span>

<span data-ttu-id="f0bab-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0bab-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0bab-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0bab-118">Child elements</span></span>

<span data-ttu-id="f0bab-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0bab-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f0bab-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0bab-120">Parent elements</span></span>

|<span data-ttu-id="f0bab-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0bab-121">**Element**</span></span>|<span data-ttu-id="f0bab-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0bab-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0bab-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="f0bab-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="f0bab-124">Contiene la semana laboral días y las horas del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f0bab-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="f0bab-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f0bab-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f0bab-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f0bab-126">Text value</span></span>

<span data-ttu-id="f0bab-127">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="f0bab-127">A text value is required.</span></span> <span data-ttu-id="f0bab-128">El valor de texto representa el final del día laborable por ¿cuántos minutos han transcurrido desde que empezó el día.</span><span class="sxs-lookup"><span data-stu-id="f0bab-128">The text value represents the end of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="f0bab-129">Por ejemplo, una hora de finalización de 6 P.M.</span><span class="sxs-lookup"><span data-stu-id="f0bab-129">For example, an end time of 6 P.M.</span></span> <span data-ttu-id="f0bab-130">está representado por minutos 1080.</span><span class="sxs-lookup"><span data-stu-id="f0bab-130">is represented by 1080 minutes.</span></span>
  
<span data-ttu-id="f0bab-131">El intervalo de valores posibles para este elemento es 0 y 1440.</span><span class="sxs-lookup"><span data-stu-id="f0bab-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0bab-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0bab-132">Remarks</span></span>

<span data-ttu-id="f0bab-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f0bab-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0bab-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f0bab-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0bab-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0bab-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0bab-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f0bab-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f0bab-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f0bab-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="f0bab-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f0bab-138">Validation File</span></span>  <br/> |<span data-ttu-id="f0bab-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f0bab-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0bab-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f0bab-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0bab-141">False</span><span class="sxs-lookup"><span data-stu-id="f0bab-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0bab-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0bab-142">See also</span></span>



[<span data-ttu-id="f0bab-143">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f0bab-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="f0bab-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f0bab-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="f0bab-145">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="f0bab-145">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


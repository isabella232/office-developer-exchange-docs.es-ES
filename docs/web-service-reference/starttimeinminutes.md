---
title: StartTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeInMinutes
api_type:
- schema
ms.assetid: 0fb60a78-6e79-4601-8e2f-5bd245c46d69
description: El elemento StartTimeInMinutes representa el comienzo del día laborable para un usuario de buzón de correo.
ms.openlocfilehash: f3f1d26731d0406ff8a0fd45fc0243a9feabf886
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837558"
---
# <a name="starttimeinminutes"></a><span data-ttu-id="f0bd4-103">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f0bd4-103">StartTimeInMinutes</span></span>

<span data-ttu-id="f0bd4-104">El elemento **StartTimeInMinutes** representa el comienzo del día laborable para un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-104">The **StartTimeInMinutes** element represents the start of the working day for a mailbox user.</span></span> 
  
- [<span data-ttu-id="f0bd4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f0bd4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="f0bd4-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="f0bd4-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
- [<span data-ttu-id="f0bd4-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="f0bd4-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
- [<span data-ttu-id="f0bd4-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="f0bd4-108">FreeBusyView</span></span>](freebusyview.md)
  
- [<span data-ttu-id="f0bd4-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="f0bd4-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
- [<span data-ttu-id="f0bd4-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="f0bd4-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
- [<span data-ttu-id="f0bd4-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="f0bd4-111">WorkingPeriod</span></span>](workingperiod.md)
  
- [<span data-ttu-id="f0bd4-112">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f0bd4-112">StartTimeInMinutes</span></span>](starttimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

<span data-ttu-id="f0bd4-113">**int**</span><span class="sxs-lookup"><span data-stu-id="f0bd4-113">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f0bd4-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0bd4-114">Attributes and elements</span></span>

<span data-ttu-id="f0bd4-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0bd4-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0bd4-116">Attributes</span></span>

<span data-ttu-id="f0bd4-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0bd4-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0bd4-118">Child elements</span></span>

<span data-ttu-id="f0bd4-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f0bd4-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0bd4-120">Parent elements</span></span>

|<span data-ttu-id="f0bd4-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0bd4-121">**Element**</span></span>|<span data-ttu-id="f0bd4-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0bd4-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0bd4-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="f0bd4-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="f0bd4-124">Contiene la semana laboral días y las horas del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="f0bd4-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f0bd4-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f0bd4-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f0bd4-126">Text value</span></span>

<span data-ttu-id="f0bd4-127">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-127">A text value is required.</span></span> <span data-ttu-id="f0bd4-128">El valor de texto representa el comienzo del día laborable por ¿cuántos minutos han transcurrido desde que empezó el día.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-128">The text value represents the start of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="f0bd4-129">Por ejemplo, una hora de inicio de 8 A.M.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-129">For example, a start time of 8 A.M.</span></span> <span data-ttu-id="f0bd4-130">está representado por 480 minutos.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-130">is represented by 480 minutes.</span></span>
  
<span data-ttu-id="f0bd4-131">El intervalo de valores posibles para este elemento es 0 y 1440.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0bd4-132">Notas</span><span class="sxs-lookup"><span data-stu-id="f0bd4-132">Remarks</span></span>

<span data-ttu-id="f0bd4-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f0bd4-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0bd4-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f0bd4-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0bd4-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0bd4-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0bd4-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f0bd4-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f0bd4-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f0bd4-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="f0bd4-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f0bd4-138">Validation File</span></span>  <br/> |<span data-ttu-id="f0bd4-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f0bd4-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0bd4-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f0bd4-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0bd4-141">False</span><span class="sxs-lookup"><span data-stu-id="f0bd4-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0bd4-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="f0bd4-142">See also</span></span>

- [<span data-ttu-id="f0bd4-143">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f0bd4-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="f0bd4-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f0bd4-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="f0bd4-145">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="f0bd4-145">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


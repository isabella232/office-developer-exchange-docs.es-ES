---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: El elemento MergedFreeBusy contiene la secuencia de datos de disponibilidad combinada.
ms.openlocfilehash: a1483449534f0d886e3c97a23d28c5d78f865042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468729"
---
# <a name="mergedfreebusy"></a><span data-ttu-id="33368-103">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="33368-103">MergedFreeBusy</span></span>

<span data-ttu-id="33368-104">El elemento **MergedFreeBusy** contiene la secuencia de datos de disponibilidad combinada.</span><span class="sxs-lookup"><span data-stu-id="33368-104">The **MergedFreeBusy** element contains the merged free/busy stream of data.</span></span> 
  
[<span data-ttu-id="33368-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="33368-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="33368-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="33368-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="33368-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="33368-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="33368-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="33368-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="33368-109">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="33368-109">MergedFreeBusy</span></span>](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 <span data-ttu-id="33368-110">**string**</span><span class="sxs-lookup"><span data-stu-id="33368-110">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33368-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="33368-111">Attributes and elements</span></span>

<span data-ttu-id="33368-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="33368-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33368-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="33368-113">Attributes</span></span>

<span data-ttu-id="33368-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="33368-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33368-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="33368-115">Child elements</span></span>

<span data-ttu-id="33368-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="33368-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="33368-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="33368-117">Parent elements</span></span>

|<span data-ttu-id="33368-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="33368-118">**Element**</span></span>|<span data-ttu-id="33368-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33368-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33368-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="33368-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="33368-121">Contiene la información de disponibilidad de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="33368-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="33368-122">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="33368-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="33368-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="33368-123">Text value</span></span>

<span data-ttu-id="33368-124">El servidor proporciona un valor de texto si el valor del elemento [FreeBusyViewType](freebusyviewtype.md) es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="33368-124">A text value is provided by the server if the value for the [FreeBusyViewType](freebusyviewtype.md) element is one of the following:</span></span> 
  
- <span data-ttu-id="33368-125">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="33368-125">DetailedMerged</span></span>
    
- <span data-ttu-id="33368-126">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="33368-126">FreeBusyMerged</span></span>
    
- <span data-ttu-id="33368-127">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="33368-127">MergedOnly</span></span>
    
<span data-ttu-id="33368-128">El valor de texto es una secuencia de información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="33368-128">The text value is a stream of free/busy information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="33368-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33368-129">Remarks</span></span>

<span data-ttu-id="33368-130">La secuencia de datos proporcionada por este elemento se define mediante los elementos [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) y [TimeWindow](timewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="33368-130">The stream of data provided by this element is defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) and [TimeWindow](timewindow.md) elements.</span></span> <span data-ttu-id="33368-131">El elemento [TimeWindow](timewindow.md) define el intervalo de tiempo consultado para la disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="33368-131">The [TimeWindow](timewindow.md) element defines the time span queried for availability.</span></span> <span data-ttu-id="33368-132">El elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) define cómo se divide la hora del elemento [TimeWindow](timewindow.md) en intervalos devueltos en el elemento **MergedFreeBusy** .</span><span class="sxs-lookup"><span data-stu-id="33368-132">The [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element defines how the time from the [TimeWindow](timewindow.md) element is broken into intervals returned in the **MergedFreeBusy** element.</span></span> <span data-ttu-id="33368-133">Cada número de la secuencia **MergedFreeBusy** representa un intervalo único definido por el elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) .</span><span class="sxs-lookup"><span data-stu-id="33368-133">Each number in the **MergedFreeBusy** stream represents a single interval defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element.</span></span> <span data-ttu-id="33368-134">En la siguiente tabla se enumeran los valores posibles para un intervalo individual.</span><span class="sxs-lookup"><span data-stu-id="33368-134">The following table lists the possible values for an individual interval.</span></span> 
  
|<span data-ttu-id="33368-135">**Digitaliza**</span><span class="sxs-lookup"><span data-stu-id="33368-135">**Digit**</span></span>|<span data-ttu-id="33368-136">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="33368-136">**Availability**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33368-137">comprendi</span><span class="sxs-lookup"><span data-stu-id="33368-137">0</span></span>  <br/> |<span data-ttu-id="33368-138">Libre</span><span class="sxs-lookup"><span data-stu-id="33368-138">Free</span></span>  <br/> |
|<span data-ttu-id="33368-139">1 </span><span class="sxs-lookup"><span data-stu-id="33368-139">1</span></span>  <br/> |<span data-ttu-id="33368-140">Provisional</span><span class="sxs-lookup"><span data-stu-id="33368-140">Tentative</span></span>  <br/> |
|<span data-ttu-id="33368-141">segundo</span><span class="sxs-lookup"><span data-stu-id="33368-141">2</span></span>  <br/> |<span data-ttu-id="33368-142">Ocupado</span><span class="sxs-lookup"><span data-stu-id="33368-142">Busy</span></span>  <br/> |
|<span data-ttu-id="33368-143">3</span><span class="sxs-lookup"><span data-stu-id="33368-143">3</span></span>  <br/> |<span data-ttu-id="33368-144">Fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="33368-144">Out of Office (OOF)</span></span>  <br/> |
|<span data-ttu-id="33368-145">4 </span><span class="sxs-lookup"><span data-stu-id="33368-145">4</span></span>  <br/> |<span data-ttu-id="33368-146">No hay datos</span><span class="sxs-lookup"><span data-stu-id="33368-146">No data</span></span>  <br/> |
   
<span data-ttu-id="33368-147">Por ejemplo, una solicitud de datos de disponibilidad incluye un elemento [TimeWindow](timewindow.md) que representa cuatro horas y un elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) que representa 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="33368-147">For example, a request for free/busy data includes a [TimeWindow](timewindow.md) element that represents four hours and a [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element that represents 60 minutes.</span></span> <span data-ttu-id="33368-148">Si el calendario del usuario solicitado es OOF para los primeros 60 minutos, ocupado durante los siguientes 90 minutos y no programado para los 90 minutos finales en el intervalo de tiempo, la secuencia **MergedFreeBusy** será 3220.</span><span class="sxs-lookup"><span data-stu-id="33368-148">If the requested user's calendar is OOF for the first 60 minutes, busy for the following 90 minutes, and unscheduled for the final 90 minutes in the time window, the **MergedFreeBusy** stream will be 3220.</span></span> <span data-ttu-id="33368-149">Si un intervalo contiene más de una clasificación de disponibilidad, el número más alto se usa para clasificar ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="33368-149">If an interval contains more than one availability classification, the highest number is used to classify that interval.</span></span> 
  
<span data-ttu-id="33368-150">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.</span><span class="sxs-lookup"><span data-stu-id="33368-150">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="33368-151">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="33368-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33368-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="33368-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33368-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="33368-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="33368-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="33368-154">Schema Name</span></span>  <br/> |<span data-ttu-id="33368-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="33368-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="33368-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="33368-156">Validation File</span></span>  <br/> |<span data-ttu-id="33368-157">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="33368-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="33368-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="33368-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="33368-159">Falso</span><span class="sxs-lookup"><span data-stu-id="33368-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33368-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="33368-160">See also</span></span>



[<span data-ttu-id="33368-161">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="33368-161">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="33368-162">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="33368-162">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="33368-163">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="33368-163">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


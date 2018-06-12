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
description: El elemento MergedFreeBusy contiene la secuencia de libre/ocupado combinada de datos.
ms.openlocfilehash: 542b9fae0c36b0236bd806e8a9117753968e812c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836449"
---
# <a name="mergedfreebusy"></a><span data-ttu-id="430da-103">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="430da-103">MergedFreeBusy</span></span>

<span data-ttu-id="430da-104">El elemento **MergedFreeBusy** contiene la secuencia de libre/ocupado combinada de datos.</span><span class="sxs-lookup"><span data-stu-id="430da-104">The **MergedFreeBusy** element contains the merged free/busy stream of data.</span></span> 
  
[<span data-ttu-id="430da-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="430da-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="430da-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="430da-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="430da-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="430da-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="430da-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="430da-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="430da-109">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="430da-109">MergedFreeBusy</span></span>](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 <span data-ttu-id="430da-110">**string**</span><span class="sxs-lookup"><span data-stu-id="430da-110">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="430da-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="430da-111">Attributes and elements</span></span>

<span data-ttu-id="430da-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="430da-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="430da-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="430da-113">Attributes</span></span>

<span data-ttu-id="430da-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="430da-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="430da-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="430da-115">Child elements</span></span>

<span data-ttu-id="430da-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="430da-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="430da-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="430da-117">Parent elements</span></span>

|<span data-ttu-id="430da-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="430da-118">**Element**</span></span>|<span data-ttu-id="430da-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="430da-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="430da-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="430da-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="430da-121">Contiene la información de disponibilidad para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="430da-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="430da-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="430da-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="430da-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="430da-123">Text value</span></span>

<span data-ttu-id="430da-124">Un valor de texto es proporcionado por el servidor si el valor para el elemento [FreeBusyViewType](freebusyviewtype.md) es una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="430da-124">A text value is provided by the server if the value for the [FreeBusyViewType](freebusyviewtype.md) element is one of the following:</span></span> 
  
- <span data-ttu-id="430da-125">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="430da-125">DetailedMerged</span></span>
    
- <span data-ttu-id="430da-126">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="430da-126">FreeBusyMerged</span></span>
    
- <span data-ttu-id="430da-127">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="430da-127">MergedOnly</span></span>
    
<span data-ttu-id="430da-128">El valor de texto es una secuencia de información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="430da-128">The text value is a stream of free/busy information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="430da-129">Notas</span><span class="sxs-lookup"><span data-stu-id="430da-129">Remarks</span></span>

<span data-ttu-id="430da-130">La secuencia de datos proporcionados por este elemento se define por los elementos [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) y [ventana de tiempo](timewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="430da-130">The stream of data provided by this element is defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) and [TimeWindow](timewindow.md) elements.</span></span> <span data-ttu-id="430da-131">El elemento de la [ventana de tiempo](timewindow.md) define el intervalo de tiempo de consulta de la disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="430da-131">The [TimeWindow](timewindow.md) element defines the time span queried for availability.</span></span> <span data-ttu-id="430da-132">El elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) define cómo se divide el tiempo desde el elemento de la [ventana de tiempo](timewindow.md) en intervalos devueltos en el elemento **MergedFreeBusy** .</span><span class="sxs-lookup"><span data-stu-id="430da-132">The [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element defines how the time from the [TimeWindow](timewindow.md) element is broken into intervals returned in the **MergedFreeBusy** element.</span></span> <span data-ttu-id="430da-133">Cada número en la secuencia de **MergedFreeBusy** representa un intervalo único definido por el elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) .</span><span class="sxs-lookup"><span data-stu-id="430da-133">Each number in the **MergedFreeBusy** stream represents a single interval defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element.</span></span> <span data-ttu-id="430da-134">En la siguiente tabla se enumera los valores posibles para un intervalo individual.</span><span class="sxs-lookup"><span data-stu-id="430da-134">The following table lists the possible values for an individual interval.</span></span> 
  
|<span data-ttu-id="430da-135">**Estilo de dígitos**</span><span class="sxs-lookup"><span data-stu-id="430da-135">**Digit**</span></span>|<span data-ttu-id="430da-136">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="430da-136">**Availability**</span></span>|
|:-----|:-----|
|<span data-ttu-id="430da-137">0</span><span class="sxs-lookup"><span data-stu-id="430da-137">0</span></span>  <br/> |<span data-ttu-id="430da-138">Gratuito</span><span class="sxs-lookup"><span data-stu-id="430da-138">Free</span></span>  <br/> |
|<span data-ttu-id="430da-139">1</span><span class="sxs-lookup"><span data-stu-id="430da-139">1</span></span>  <br/> |<span data-ttu-id="430da-140">Provisional</span><span class="sxs-lookup"><span data-stu-id="430da-140">Tentative</span></span>  <br/> |
|<span data-ttu-id="430da-141">2</span><span class="sxs-lookup"><span data-stu-id="430da-141">2</span></span>  <br/> |<span data-ttu-id="430da-142">Ocupado</span><span class="sxs-lookup"><span data-stu-id="430da-142">Busy</span></span>  <br/> |
|<span data-ttu-id="430da-143">3</span><span class="sxs-lookup"><span data-stu-id="430da-143">3</span></span>  <br/> |<span data-ttu-id="430da-144">Fuera de la oficina (OOF)</span><span class="sxs-lookup"><span data-stu-id="430da-144">Out of Office (OOF)</span></span>  <br/> |
|<span data-ttu-id="430da-145">4</span><span class="sxs-lookup"><span data-stu-id="430da-145">4</span></span>  <br/> |<span data-ttu-id="430da-146">No hay datos</span><span class="sxs-lookup"><span data-stu-id="430da-146">No data</span></span>  <br/> |
   
<span data-ttu-id="430da-147">Por ejemplo, una solicitud de datos de disponibilidad incluye un elemento de la [ventana de tiempo](timewindow.md) que representa cuatro horas y un elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) que representa 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="430da-147">For example, a request for free/busy data includes a [TimeWindow](timewindow.md) element that represents four hours and a [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element that represents 60 minutes.</span></span> <span data-ttu-id="430da-148">Si el calendario del usuario solicitado es OOF durante los primeros 60 minutos, ocupado para el siguientes 90 minutos y no programada para el final de 90 minutos en la ventana de tiempo, la secuencia de **MergedFreeBusy** será 3220.</span><span class="sxs-lookup"><span data-stu-id="430da-148">If the requested user's calendar is OOF for the first 60 minutes, busy for the following 90 minutes, and unscheduled for the final 90 minutes in the time window, the **MergedFreeBusy** stream will be 3220.</span></span> <span data-ttu-id="430da-149">Si un intervalo contiene más de una clasificación de disponibilidad, el número más alto se utiliza para clasificar de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="430da-149">If an interval contains more than one availability classification, the highest number is used to classify that interval.</span></span> 
  
<span data-ttu-id="430da-150">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.</span><span class="sxs-lookup"><span data-stu-id="430da-150">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="430da-151">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="430da-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="430da-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="430da-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="430da-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="430da-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="430da-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="430da-154">Schema Name</span></span>  <br/> |<span data-ttu-id="430da-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="430da-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="430da-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="430da-156">Validation File</span></span>  <br/> |<span data-ttu-id="430da-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="430da-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="430da-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="430da-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="430da-159">False</span><span class="sxs-lookup"><span data-stu-id="430da-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="430da-160">Ver también</span><span class="sxs-lookup"><span data-stu-id="430da-160">See also</span></span>



[<span data-ttu-id="430da-161">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="430da-161">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="430da-162">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="430da-162">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="430da-163">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="430da-163">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


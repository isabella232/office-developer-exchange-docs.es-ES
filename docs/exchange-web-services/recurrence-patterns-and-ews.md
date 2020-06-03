---
title: Patrones de periodicidad y EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: Obtenga información sobre los patrones de periodicidad y la serie periódica en Exchange.
ms.openlocfilehash: 681dfee7e0a66a483b8638810da5e4e0ac0f05ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459331"
---
# <a name="recurrence-patterns-and-ews"></a><span data-ttu-id="aae61-103">Patrones de periodicidad y EWS</span><span class="sxs-lookup"><span data-stu-id="aae61-103">Recurrence patterns and EWS</span></span>

<span data-ttu-id="aae61-104">Obtenga información sobre los patrones de periodicidad y la serie periódica en Exchange.</span><span class="sxs-lookup"><span data-stu-id="aae61-104">Learn about recurrence patterns and recurring series in Exchange.</span></span>
  
<span data-ttu-id="aae61-105">Una serie periódica es una cita o reunión que se repite según un patrón definido.</span><span class="sxs-lookup"><span data-stu-id="aae61-105">A recurring series is an appointment or meeting that repeats according to a defined pattern.</span></span> <span data-ttu-id="aae61-106">Una serie periódica puede tener un número específico de repeticiones o puede repetirse indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="aae61-106">A recurring series can either have a specific number of occurrences or can repeat indefinitely.</span></span> <span data-ttu-id="aae61-107">Además, una serie periódica puede tener excepciones que no siguen el patrón del resto de las repeticiones y pueden tener ocurrencias que se han eliminado del patrón.</span><span class="sxs-lookup"><span data-stu-id="aae61-107">Additionally, a recurring series can have exceptions that don't follow the pattern of the rest of the occurrences, and can have occurrences that have been deleted from the pattern.</span></span> <span data-ttu-id="aae61-108">Puede usar la API administrada de EWS y EWS para trabajar con la serie periódica y sus elementos de calendario asociados.</span><span class="sxs-lookup"><span data-stu-id="aae61-108">You can use the EWS Managed API and EWS to work with recurring series and their associated calendar items.</span></span>
  
## <a name="recurring-calendar-items"></a><span data-ttu-id="aae61-109">Elementos de calendario periódicos</span><span class="sxs-lookup"><span data-stu-id="aae61-109">Recurring calendar items</span></span>

<span data-ttu-id="aae61-110">Todos los elementos de calendario se dividen en una de las cuatro categorías siguientes:</span><span class="sxs-lookup"><span data-stu-id="aae61-110">All calendar items fall into one of the following four categories:</span></span>
  
- <span data-ttu-id="aae61-111">Elementos de calendario no periódicos</span><span class="sxs-lookup"><span data-stu-id="aae61-111">Non-recurring calendar items</span></span>
    
- <span data-ttu-id="aae61-112">Maestros periódicos</span><span class="sxs-lookup"><span data-stu-id="aae61-112">Recurring masters</span></span>
    
- <span data-ttu-id="aae61-113">Ocurrencias en una serie</span><span class="sxs-lookup"><span data-stu-id="aae61-113">Occurrences in a series</span></span>
    
- <span data-ttu-id="aae61-114">Instancias modificadas en una serie, conocidas como excepciones</span><span class="sxs-lookup"><span data-stu-id="aae61-114">Modified occurrences in a series, known as exceptions</span></span>
    
<span data-ttu-id="aae61-115">En este artículo, analizaremos los tres tipos de elementos de calendario que forman parte de una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="aae61-115">In this article, we'll look at the three types of calendar items that are part of a recurring series.</span></span>
  
<span data-ttu-id="aae61-116">Es útil comprender cómo se implementan las series periódicas en el servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="aae61-116">It's helpful to understand how recurring series are implemented on the Exchange server.</span></span> <span data-ttu-id="aae61-117">En lugar de crear un elemento diferente distinto para cada repetición en una serie periódica, el servidor crea solo un elemento real en el calendario, conocido como maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="aae61-117">Instead of creating a separate distinct item for each occurrence in a recurring series, the server creates only one actual item in the calendar, known as the recurring master.</span></span> <span data-ttu-id="aae61-118">El formato de un patrón recurrente es muy similar a una cita no recurrente, además de la información del patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="aae61-118">The format of a recurring master is very similar to a non-recurring appointment, with the addition of recurrence pattern information.</span></span> <span data-ttu-id="aae61-119">A continuación, el servidor genera repeticiones según el patrón de periodicidad en respuesta a las solicitudes de información de la cita de los clientes, mediante un proceso denominado expansión.</span><span class="sxs-lookup"><span data-stu-id="aae61-119">The server then generates occurrences based on the recurrence pattern in response to client requests for appointment information, using a process called expansion.</span></span> <span data-ttu-id="aae61-120">Estas ocurrencias generadas no se almacenan de forma permanente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="aae61-120">These generated occurrences are not permanently stored on the server.</span></span> <span data-ttu-id="aae61-121">Esto es importante para comprender porque la forma en que se buscan los elementos del calendario determina la información que se recibe y si se produce la expansión.</span><span class="sxs-lookup"><span data-stu-id="aae61-121">This is important to understand because the way that you search for calendar items determines what information you receive and whether expansion occurs.</span></span>
  
## <a name="recurrence-patterns"></a><span data-ttu-id="aae61-122">Patrones de periodicidad</span><span class="sxs-lookup"><span data-stu-id="aae61-122">Recurrence patterns</span></span>

<span data-ttu-id="aae61-123">La pieza clave para una serie periódica que hace que la expansión sea posible es el patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="aae61-123">The key piece to a recurring series that makes expansion possible is the recurrence pattern.</span></span> <span data-ttu-id="aae61-124">El patrón de periodicidad se encuentra en el patrón recurrente y describe un conjunto de criterios para calcular los repeticiones en función de la fecha y la hora del patrón recurrente.</span><span class="sxs-lookup"><span data-stu-id="aae61-124">The recurrence pattern is found on the recurring master, and describes a set of criteria for calculating occurrences based on the date and time of the recurring master.</span></span>
  
<span data-ttu-id="aae61-125">**Tabla 1. Patrones de periodicidad disponibles**</span><span class="sxs-lookup"><span data-stu-id="aae61-125">**Table 1. Available recurrence patterns**</span></span>

|<span data-ttu-id="aae61-126">**Clase de API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="aae61-126">**EWS Managed API class**</span></span>|<span data-ttu-id="aae61-127">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="aae61-127">**EWS element**</span></span>|<span data-ttu-id="aae61-128">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="aae61-128">**Examples**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aae61-129">Recurrence. DailyPattern</span><span class="sxs-lookup"><span data-stu-id="aae61-129">Recurrence.DailyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-130">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-130">DailyRecurrence</span></span>](https://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-131">Repita todos los días.</span><span class="sxs-lookup"><span data-stu-id="aae61-131">Repeat every day.</span></span>  <br/> <span data-ttu-id="aae61-132">Repetir cada dos días.</span><span class="sxs-lookup"><span data-stu-id="aae61-132">Repeat every other day.</span></span>  <br/> |
|[<span data-ttu-id="aae61-133">Recurrence. MonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="aae61-133">Recurrence.MonthlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-134">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-134">AbsoluteMonthlyRecurrence</span></span>](https://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-135">Repetir cada mes el décimo día del mes.</span><span class="sxs-lookup"><span data-stu-id="aae61-135">Repeat every month on the tenth day of the month.</span></span>  <br/> <span data-ttu-id="aae61-136">Repita cada dos meses en el vigésimo primer día del mes.</span><span class="sxs-lookup"><span data-stu-id="aae61-136">Repeat every other month on the twenty-first day of the month.</span></span>  <br/> |
|[<span data-ttu-id="aae61-137">Recurrence. RelativeMonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="aae61-137">Recurrence.RelativeMonthlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-138">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-138">RelativeMonthlyRecurrence</span></span>](https://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-139">Repetir el segundo martes de cada mes.</span><span class="sxs-lookup"><span data-stu-id="aae61-139">Repeat on the second Tuesday of every month.</span></span>  <br/> <span data-ttu-id="aae61-140">Repita el tercer jueves del mes cada tres meses.</span><span class="sxs-lookup"><span data-stu-id="aae61-140">Repeat on the third Thursday of the month every three months.</span></span>  <br/> |
|[<span data-ttu-id="aae61-141">Recurrence. RelativeYearlyPattern</span><span class="sxs-lookup"><span data-stu-id="aae61-141">Recurrence.RelativeYearlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-142">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-142">RelativeYearlyRecurrence</span></span>](https://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-143">Repetir el primer lunes de agosto de cada año.</span><span class="sxs-lookup"><span data-stu-id="aae61-143">Repeat on the first Monday of August every year.</span></span>  <br/> |
|[<span data-ttu-id="aae61-144">Recurrence. WeeklyPattern</span><span class="sxs-lookup"><span data-stu-id="aae61-144">Recurrence.WeeklyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-145">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-145">WeeklyRecurrence</span></span>](https://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-146">Repita cada lunes.</span><span class="sxs-lookup"><span data-stu-id="aae61-146">Repeat every Monday.</span></span>  <br/> <span data-ttu-id="aae61-147">Repita cada martes y jueves cada dos semanas.</span><span class="sxs-lookup"><span data-stu-id="aae61-147">Repeat every Tuesday and Thursday every other week.</span></span>  <br/> |
|[<span data-ttu-id="aae61-148">Recurrence. YearlyPattern</span><span class="sxs-lookup"><span data-stu-id="aae61-148">Recurrence.YearlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-149">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-149">AbsoluteYearlyRecurrence</span></span>](https://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-150">Repetir el 1 de septiembre de cada año.</span><span class="sxs-lookup"><span data-stu-id="aae61-150">Repeat on September 1st every year.</span></span>  <br/> |
   
<span data-ttu-id="aae61-151">La otra información importante para un patrón de periodicidad es cuando finaliza la periodicidad.</span><span class="sxs-lookup"><span data-stu-id="aae61-151">The other important piece of information for a recurrence pattern is when the recurrence ends.</span></span> <span data-ttu-id="aae61-152">Esto puede expresarse como un número establecido de repeticiones, como una fecha de finalización o como sin fin.</span><span class="sxs-lookup"><span data-stu-id="aae61-152">This can be expressed as either a set number of occurrences, as an end date, or as having no end.</span></span>
  
<span data-ttu-id="aae61-153">**Tabla 2. Opciones para el final de una serie periódica**</span><span class="sxs-lookup"><span data-stu-id="aae61-153">**Table 2. Options for the end of a recurring series**</span></span>

|<span data-ttu-id="aae61-154">**Método o propiedad de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="aae61-154">**EWS Managed API method/property**</span></span>|<span data-ttu-id="aae61-155">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="aae61-155">**EWS element**</span></span>|<span data-ttu-id="aae61-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aae61-156">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aae61-157">Recurrence. NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="aae61-157">Recurrence.NumberOfOccurrences</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-158">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-158">NumberedRecurrence</span></span>](https://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-159">El valor de esta propiedad o elemento especifica el número de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="aae61-159">The value of this property or element specifies the number of occurrences.</span></span>  <br/> |
|[<span data-ttu-id="aae61-160">Recurrence. EndDate</span><span class="sxs-lookup"><span data-stu-id="aae61-160">Recurrence.EndDate</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-161">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-161">EndDateRecurrence</span></span>](https://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-162">La última aparición en la serie cae en o antes de la fecha especificada por esta propiedad o elemento.</span><span class="sxs-lookup"><span data-stu-id="aae61-162">The last occurrence in the series falls on or before the date specified by this property or element.</span></span>  <br/> |
|[<span data-ttu-id="aae61-163">Recurrence. HasEnd</span><span class="sxs-lookup"><span data-stu-id="aae61-163">Recurrence.HasEnd</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="aae61-164">Recurrence. NeverEnds</span><span class="sxs-lookup"><span data-stu-id="aae61-164">Recurrence.NeverEnds</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aae61-165">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="aae61-165">NoEndRecurrence</span></span>](https://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |<span data-ttu-id="aae61-166">La serie no tiene fin.</span><span class="sxs-lookup"><span data-stu-id="aae61-166">The series has no end.</span></span>  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a><span data-ttu-id="aae61-167">Vistas expandidas frente a vistas no expandidas</span><span class="sxs-lookup"><span data-stu-id="aae61-167">Expanded vs. non-expanded views</span></span>

<span data-ttu-id="aae61-168">El uso del método **FindAppointments** en la API administrada de EWS (o la operación **FindItem** con un elemento **CalendarView** en EWS) invoca el proceso de expansión.</span><span class="sxs-lookup"><span data-stu-id="aae61-168">Using the **FindAppointments** method in the EWS Managed API (or the **FindItem** operation with a **CalendarView** element in EWS) invokes the expansion process.</span></span> <span data-ttu-id="aae61-169">De esta forma, se ocultan las citas maestras periódicas del conjunto de resultados y, en su lugar, se presenta una vista expandida de esa serie periódica.</span><span class="sxs-lookup"><span data-stu-id="aae61-169">This hides recurring master appointments from the result set, and instead presents an expanded view of that recurring series.</span></span> <span data-ttu-id="aae61-170">Las repeticiones y excepciones al patrón periódico que se encuentran dentro de los parámetros de la vista de calendario se incluyen en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="aae61-170">Occurrences of and exceptions to the recurring master that fall within the parameters of the calendar view are included in the result set.</span></span> <span data-ttu-id="aae61-171">Por el contrario, si se usa el método **FindItems** en la API administrada de EWS (o la operación **FindItem** con un elemento **IndexedPageItemView** o **FractionalPageItemView** en EWS), no se invoca el proceso de expansión y no se incluyen las repeticiones ni las excepciones.</span><span class="sxs-lookup"><span data-stu-id="aae61-171">Conversely, using the **FindItems** method in the EWS Managed API (or the **FindItem** operation with a **IndexedPageItemView** or **FractionalPageItemView** element in EWS), does not invoke the expansion process, and occurrences and exceptions are not included.</span></span> <span data-ttu-id="aae61-172">Veamos un ejemplo de comparación de los dos métodos.</span><span class="sxs-lookup"><span data-stu-id="aae61-172">Let's look at an example comparing the two methods.</span></span> 
  
<span data-ttu-id="aae61-173">**Tabla 3. Métodos y operaciones para buscar citas**</span><span class="sxs-lookup"><span data-stu-id="aae61-173">**Table 3. Methods and operations for finding appointments**</span></span>

|<span data-ttu-id="aae61-174">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="aae61-174">**EWS Managed API method**</span></span>|<span data-ttu-id="aae61-175">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="aae61-175">**EWS operation**</span></span>|<span data-ttu-id="aae61-176">**¿Expande la serie?**</span><span class="sxs-lookup"><span data-stu-id="aae61-176">**Expands series?**</span></span>|<span data-ttu-id="aae61-177">**Elementos incluidos en los resultados**</span><span class="sxs-lookup"><span data-stu-id="aae61-177">**Items included in results**</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="aae61-178">ExchangeService. FindAppointments</span><span class="sxs-lookup"><span data-stu-id="aae61-178">ExchangeService.FindAppointments</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="aae61-179">[Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae61-179">[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="aae61-180">Sí</span><span class="sxs-lookup"><span data-stu-id="aae61-180">Yes</span></span>  <br/> |<span data-ttu-id="aae61-181">Citas no periódicas, ocurrencias únicas de una serie periódica y excepciones a la serie periódica</span><span class="sxs-lookup"><span data-stu-id="aae61-181">Non-recurring appointments, single occurrences of recurring series, and exceptions to recurring series</span></span>  <br/> |
|[<span data-ttu-id="aae61-182">ExchangeService. FindItems</span><span class="sxs-lookup"><span data-stu-id="aae61-182">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="aae61-183">[Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o un elemento [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae61-183">[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="aae61-184">No</span><span class="sxs-lookup"><span data-stu-id="aae61-184">No</span></span>  <br/> |<span data-ttu-id="aae61-185">Citas no periódicas y citas maestras periódicas</span><span class="sxs-lookup"><span data-stu-id="aae61-185">Non-recurring appointments and recurring master appointments</span></span>  <br/> |
   
<span data-ttu-id="aae61-186">Sadie acaba de firmar su hijo para el equipo de natación.</span><span class="sxs-lookup"><span data-stu-id="aae61-186">Sadie has just signed her son up for swim team.</span></span> <span data-ttu-id="aae61-187">El equipo se ha practicado cada miércoles por la mañana a las 8:30 A.M., a partir del 2 de julio, con la última práctica de 6 de agosto.</span><span class="sxs-lookup"><span data-stu-id="aae61-187">The team has practice every Wednesday morning at 8:30 AM, starting July 2, with the last practice being on August 6.</span></span> <span data-ttu-id="aae61-188">Si no desea olvidarse de la práctica, Sadie agrega una cita periódica a su calendario para recordarla.</span><span class="sxs-lookup"><span data-stu-id="aae61-188">Not wanting to forget about practice, Sadie adds a recurring appointment to her calendar to remind her.</span></span>
  
<span data-ttu-id="aae61-189">**Tabla 4. Cita periódica de Sadie**</span><span class="sxs-lookup"><span data-stu-id="aae61-189">**Table 4. Sadie's recurring appointment**</span></span>

|<span data-ttu-id="aae61-190">**Campo de cita**</span><span class="sxs-lookup"><span data-stu-id="aae61-190">**Appointment field**</span></span>|<span data-ttu-id="aae61-191">**Valor**</span><span class="sxs-lookup"><span data-stu-id="aae61-191">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aae61-192">Subject</span><span class="sxs-lookup"><span data-stu-id="aae61-192">Subject</span></span>  <br/> |<span data-ttu-id="aae61-193">Práctica del equipo de nadar</span><span class="sxs-lookup"><span data-stu-id="aae61-193">Swim Team Practice</span></span>  <br/> |
|<span data-ttu-id="aae61-194">Iniciar</span><span class="sxs-lookup"><span data-stu-id="aae61-194">Start</span></span>  <br/> |<span data-ttu-id="aae61-195">2 de julio de 2014 8:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="aae61-195">July 2, 2014 8:30 AM</span></span>  <br/> |
|<span data-ttu-id="aae61-196">End</span><span class="sxs-lookup"><span data-stu-id="aae61-196">End</span></span>  <br/> |<span data-ttu-id="aae61-197">2 de julio de 2014 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="aae61-197">July 2, 2014 10:00 AM</span></span>  <br/> |
|<span data-ttu-id="aae61-198">Repetitivo</span><span class="sxs-lookup"><span data-stu-id="aae61-198">Recurs</span></span>  <br/> |<span data-ttu-id="aae61-199">Todos los miércoles</span><span class="sxs-lookup"><span data-stu-id="aae61-199">Every Wednesday</span></span>  <br/> |
|<span data-ttu-id="aae61-200">Última ocurrencia</span><span class="sxs-lookup"><span data-stu-id="aae61-200">Last occurrence</span></span>  <br/> |<span data-ttu-id="aae61-201">6 de agosto de 2014 8:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="aae61-201">August 6, 2014 8:30 AM</span></span>  <br/> |
   
<span data-ttu-id="aae61-202">Un vistazo rápido a un calendario muestra que el equipo tendrá un total de seis prácticas.</span><span class="sxs-lookup"><span data-stu-id="aae61-202">A quick look at a calendar shows that the team will have a total of six practices.</span></span> <span data-ttu-id="aae61-203">Sin embargo, no hay seis elementos de cita distintos en el calendario.</span><span class="sxs-lookup"><span data-stu-id="aae61-203">However, there aren't six distinct appointment items in the calendar.</span></span> <span data-ttu-id="aae61-204">En su lugar, solo hay una cita de patrón recurrente que representa la serie.</span><span class="sxs-lookup"><span data-stu-id="aae61-204">Instead, there is just one recurring master appointment representing the series.</span></span>
  
<span data-ttu-id="aae61-205">Veamos ahora cómo buscar citas en el calendario de Sadie que se produzcan dentro del mes de julio.</span><span class="sxs-lookup"><span data-stu-id="aae61-205">Now let's look at finding appointments on Sadie's calendar that occur within the month of July.</span></span> <span data-ttu-id="aae61-206">El siguiente ejemplo de código usa el método **FindItems** en la API administrada de Exchange para generar una vista no expandida del calendario de Sadie.</span><span class="sxs-lookup"><span data-stu-id="aae61-206">The following code example uses the **FindItems** method in the Exchange Managed API to produce a non-expanded view of Sadie's calendar.</span></span> 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
#region FindItems + ItemView method
ItemView itemView = new ItemView(100);
itemView.PropertySet = propSet;
List<SearchFilter> filterList = new List<SearchFilter>();
// Find appointments that start after midnight on July 1, 2014.
SearchFilter.IsGreaterThan startFilter = new SearchFilter.IsGreaterThan(AppointmentSchema.Start,
    new DateTime(2014, 7, 1));
// Find appointments that end before midnight on July 31, 2014
SearchFilter.IsLessThan endFilter = new SearchFilter.IsLessThan(AppointmentSchema.End,
    new DateTime(2014, 7, 31));
filterList.Add(startFilter);
filterList.Add(endFilter);
SearchFilter.SearchFilterCollection calendarFilter = new SearchFilter.SearchFilterCollection(LogicalOperator.And, filterList);
// This results in a call to EWS.
FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Calendar, calendarFilter, itemView);
foreach(Item appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

<span data-ttu-id="aae61-207">El código da como resultado la siguiente solicitud de [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aae61-207">That code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="100" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:IsGreaterThan>
            <t:FieldURI FieldURI="calendar:Start" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-01T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsGreaterThan>
          <t:IsLessThan>
            <t:FieldURI FieldURI="calendar:End" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-31T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsLessThan>
        </t:And>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="aae61-208">La respuesta del servidor incluye solo un elemento único, el patrón recurrente, indicado por el valor del elemento [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) de **RecurringMaster**.</span><span class="sxs-lookup"><span data-stu-id="aae61-208">The server's response includes only a single item, the recurring master, indicated by the [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element value of **RecurringMaster**.</span></span> <span data-ttu-id="aae61-209">El valor del elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="aae61-209">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="aae61-210">Ahora, vamos a comparar con una vista expandida.</span><span class="sxs-lookup"><span data-stu-id="aae61-210">Now let's compare with an expanded view.</span></span> <span data-ttu-id="aae61-211">El siguiente ejemplo de código usa el método **FindAppointments** en la API administrada de EWS para crear una vista expandida del calendario de Sadie.</span><span class="sxs-lookup"><span data-stu-id="aae61-211">The following code example uses the **FindAppointments** method in the EWS Managed API to create an expanded view of Sadie's calendar.</span></span> 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
CalendarView calView = new CalendarView(new DateTime(2014, 7, 1),
    new DateTime(2014, 7, 31));
calView.PropertySet = propSet;
FindItemsResults<Appointment> results = service.FindAppointments(WellKnownFolderName.Calendar, calView);
foreach(Appointment appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

<span data-ttu-id="aae61-212">Este código da como resultado la siguiente solicitud de [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aae61-212">This code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView StartDate="2014-07-01T07:00:00.000Z" EndDate="2014-07-31T07:00:00.000Z" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="aae61-213">Esta vez, la respuesta del servidor incluye cinco repeticiones, una para cada miércoles en julio.</span><span class="sxs-lookup"><span data-stu-id="aae61-213">This time, the server response includes five occurrences, one for each Wednesday in July.</span></span> <span data-ttu-id="aae61-214">Todos los elementos [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) de estos elementos tienen un valor de **ocurrencia**.</span><span class="sxs-lookup"><span data-stu-id="aae61-214">The [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) elements on these items all have a value of **Occurrence**.</span></span> <span data-ttu-id="aae61-215">Tenga en cuenta que el patrón recurrente no está presente en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aae61-215">Note that the recurring master is not present in the response.</span></span> <span data-ttu-id="aae61-216">Los valores de los elementos [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="aae61-216">The values of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="5" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-09T15:30:00Z</t:Start>
                <t:End>2014-07-09T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA8..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-16T15:30:00Z</t:Start>
                <t:End>2014-07-16T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA9..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-23T15:30:00Z</t:Start>
                <t:End>2014-07-23T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADAA..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-30T15:30:00Z</t:Start>
                <t:End>2014-07-30T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="aae61-217">Una vez que tenga un patrón recurrente, una ocurrencia o una excepción, siempre podrá [recuperar los demás elementos relacionados](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="aae61-217">After you have a recurring master, an occurrence, or an exception, you can always [retrieve the other related items](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="aae61-218">Una vez transcurrida o excepción, puede recuperar el patrón recurrente y viceversa.</span><span class="sxs-lookup"><span data-stu-id="aae61-218">Given an occurrence or exception, you can retrieve the recurring master, and vice versa.</span></span>
  
## <a name="working-with-recurring-calendar-items"></a><span data-ttu-id="aae61-219">Trabajar con elementos de calendario periódicos</span><span class="sxs-lookup"><span data-stu-id="aae61-219">Working with recurring calendar items</span></span>

<span data-ttu-id="aae61-220">Use los mismos métodos y operaciones para trabajar con series periódicas mientras usa para trabajar con elementos de calendario no periódicos.</span><span class="sxs-lookup"><span data-stu-id="aae61-220">You use all the same methods and operations to work with recurring series as you use to work with non-recurring calendar items.</span></span> <span data-ttu-id="aae61-221">La diferencia estriba en que, en función del elemento que se use para invocar dichos métodos u operaciones, las acciones que se realicen se pueden aplicar a toda la serie o solo a una única incidencia.</span><span class="sxs-lookup"><span data-stu-id="aae61-221">The difference is that, depending on the item you use to invoke those methods or operations, the actions you take can apply to the entire series, or just a single occurrence.</span></span> <span data-ttu-id="aae61-222">Las [acciones realizadas en el maestro periódico](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) se aplicarán a todas las repeticiones de la serie, mientras que [las acciones realizadas en una sola ocurrencia o excepción](how-to-update-a-recurring-series-by-using-ews.md) solo se aplicarán a esa ocurrencia o excepción.</span><span class="sxs-lookup"><span data-stu-id="aae61-222">[Actions taken on the recurring master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) will apply to all occurrences in the series, while [actions taken to a single occurrence or exception](how-to-update-a-recurring-series-by-using-ews.md) will only apply to that occurrence or exception.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="aae61-223">En esta sección</span><span class="sxs-lookup"><span data-stu-id="aae61-223">In this section</span></span>

- [<span data-ttu-id="aae61-224">Obtener acceso a una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aae61-224">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="aae61-225">Crear una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aae61-225">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="aae61-226">Eliminar citas en una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aae61-226">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="aae61-227">Actualizar una serie periódica mediante EWS</span><span class="sxs-lookup"><span data-stu-id="aae61-227">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="aae61-228">Actualizar una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aae61-228">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="aae61-229">Vea también</span><span class="sxs-lookup"><span data-stu-id="aae61-229">See also</span></span>


- [<span data-ttu-id="aae61-230">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aae61-230">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="aae61-231">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="aae61-231">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="aae61-232">Obtener citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aae61-232">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    


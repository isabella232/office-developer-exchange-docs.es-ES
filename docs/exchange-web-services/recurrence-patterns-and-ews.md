---
title: Patrones de periodicidad y EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: Obtenga información sobre los patrones de periodicidad y serie periódica en Exchange.
ms.openlocfilehash: ac10e9b9a347abb5907b77f0e0e7315e4e86d97a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763302"
---
# <a name="recurrence-patterns-and-ews"></a><span data-ttu-id="d2388-103">Patrones de periodicidad y EWS</span><span class="sxs-lookup"><span data-stu-id="d2388-103">Recurrence patterns and EWS</span></span>

<span data-ttu-id="d2388-104">Obtenga información sobre los patrones de periodicidad y serie periódica en Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2388-104">Learn about recurrence patterns and recurring series in Exchange.</span></span>
  
<span data-ttu-id="d2388-105">Una serie periódica es una cita o reunión que se repite según un patrón definido.</span><span class="sxs-lookup"><span data-stu-id="d2388-105">A recurring series is an appointment or meeting that repeats according to a defined pattern.</span></span> <span data-ttu-id="d2388-106">Una serie periódica puede tener un número específico de repeticiones o puede repetir indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="d2388-106">A recurring series can either have a specific number of occurrences or can repeat indefinitely.</span></span> <span data-ttu-id="d2388-107">Además, una serie periódica puede tener excepciones que no siguen el modelo del resto de las apariciones y pueden tener todas las veces que se han eliminado de la trama.</span><span class="sxs-lookup"><span data-stu-id="d2388-107">Additionally, a recurring series can have exceptions that don't follow the pattern of the rest of the occurrences, and can have occurrences that have been deleted from the pattern.</span></span> <span data-ttu-id="d2388-108">Puede usar la API administrada de EWS y EWS para trabajar con una serie periódica y sus elementos de calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="d2388-108">You can use the EWS Managed API and EWS to work with recurring series and their associated calendar items.</span></span>
  
## <a name="recurring-calendar-items"></a><span data-ttu-id="d2388-109">Elementos de calendario periódicos</span><span class="sxs-lookup"><span data-stu-id="d2388-109">Recurring calendar items</span></span>

<span data-ttu-id="d2388-110">Todos los elementos de calendario se dividen en una de las siguientes cuatro categorías:</span><span class="sxs-lookup"><span data-stu-id="d2388-110">All calendar items fall into one of the following four categories:</span></span>
  
- <span data-ttu-id="d2388-111">Elementos de calendario no periódicos</span><span class="sxs-lookup"><span data-stu-id="d2388-111">Non-recurring calendar items</span></span>
    
- <span data-ttu-id="d2388-112">Masters periódicas</span><span class="sxs-lookup"><span data-stu-id="d2388-112">Recurring masters</span></span>
    
- <span data-ttu-id="d2388-113">Repeticiones de una serie</span><span class="sxs-lookup"><span data-stu-id="d2388-113">Occurrences in a series</span></span>
    
- <span data-ttu-id="d2388-114">Repeticiones de modificado en una serie, conocido como excepciones</span><span class="sxs-lookup"><span data-stu-id="d2388-114">Modified occurrences in a series, known as exceptions</span></span>
    
<span data-ttu-id="d2388-115">En este artículo, analizaremos los tres tipos de elementos de calendario que forman parte de una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="d2388-115">In this article, we'll look at the three types of calendar items that are part of a recurring series.</span></span>
  
<span data-ttu-id="d2388-116">Resulta útil comprender serie periódica cómo se implementan en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2388-116">It's helpful to understand how recurring series are implemented on the Exchange server.</span></span> <span data-ttu-id="d2388-117">En lugar de crear un elemento de distinto independiente para cada ocurrencia de una serie periódica, el servidor crea un solo elemento real en el calendario, conocido como el maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="d2388-117">Instead of creating a separate distinct item for each occurrence in a recurring series, the server creates only one actual item in the calendar, known as the recurring master.</span></span> <span data-ttu-id="d2388-118">El formato de un patrón periódico es muy similar a una cita recurrente, con la incorporación de información de patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="d2388-118">The format of a recurring master is very similar to a non-recurring appointment, with the addition of recurrence pattern information.</span></span> <span data-ttu-id="d2388-119">El servidor, a continuación, genera ocurrencias basándose en el patrón de periodicidad en respuesta a las solicitudes de cliente para obtener información de cita, mediante un proceso de expansión.</span><span class="sxs-lookup"><span data-stu-id="d2388-119">The server then generates occurrences based on the recurrence pattern in response to client requests for appointment information, using a process called expansion.</span></span> <span data-ttu-id="d2388-120">Estas repeticiones generadas no se almacenan de forma permanente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d2388-120">These generated occurrences are not permanently stored on the server.</span></span> <span data-ttu-id="d2388-121">Esto es importante comprender debido a que el modo en que se busca los elementos de calendario determina qué información recibe y si se produce la expansión.</span><span class="sxs-lookup"><span data-stu-id="d2388-121">This is important to understand because the way that you search for calendar items determines what information you receive and whether expansion occurs.</span></span>
  
## <a name="recurrence-patterns"></a><span data-ttu-id="d2388-122">Patrones de periodicidad</span><span class="sxs-lookup"><span data-stu-id="d2388-122">Recurrence patterns</span></span>

<span data-ttu-id="d2388-123">La clave de una serie periódica que hace posible la expansión es el patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="d2388-123">The key piece to a recurring series that makes expansion possible is the recurrence pattern.</span></span> <span data-ttu-id="d2388-124">El patrón de periodicidad se encuentra en el maestro de periódico y describe un conjunto de criterios para calcular ocurrencias basándose en la fecha y hora del patrón periódico.</span><span class="sxs-lookup"><span data-stu-id="d2388-124">The recurrence pattern is found on the recurring master, and describes a set of criteria for calculating occurrences based on the date and time of the recurring master.</span></span>
  
<span data-ttu-id="d2388-125">**La tabla 1. Patrones de periodicidad disponibles**</span><span class="sxs-lookup"><span data-stu-id="d2388-125">**Table 1. Available recurrence patterns**</span></span>

|<span data-ttu-id="d2388-126">**Clase de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="d2388-126">**EWS Managed API class**</span></span>|<span data-ttu-id="d2388-127">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="d2388-127">**EWS element**</span></span>|<span data-ttu-id="d2388-128">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="d2388-128">**Examples**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d2388-129">Recurrence.DailyPattern</span><span class="sxs-lookup"><span data-stu-id="d2388-129">Recurrence.DailyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-130">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-130">DailyRecurrence</span></span>](http://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-131">Repita todos los días.</span><span class="sxs-lookup"><span data-stu-id="d2388-131">Repeat every day.</span></span>  <br/> <span data-ttu-id="d2388-132">Repita todos los demás días.</span><span class="sxs-lookup"><span data-stu-id="d2388-132">Repeat every other day.</span></span>  <br/> |
|[<span data-ttu-id="d2388-133">Recurrence.MonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="d2388-133">Recurrence.MonthlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-134">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-134">AbsoluteMonthlyRecurrence</span></span>](http://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-135">Repita todos los meses en el décimo día del mes.</span><span class="sxs-lookup"><span data-stu-id="d2388-135">Repeat every month on the tenth day of the month.</span></span>  <br/> <span data-ttu-id="d2388-136">Repetir cada dos meses en el día del mes de vigésimo primero.</span><span class="sxs-lookup"><span data-stu-id="d2388-136">Repeat every other month on the twenty-first day of the month.</span></span>  <br/> |
|[<span data-ttu-id="d2388-137">Recurrence.RelativeMonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="d2388-137">Recurrence.RelativeMonthlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-138">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-138">RelativeMonthlyRecurrence</span></span>](http://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-139">Repita el segundo martes de cada mes.</span><span class="sxs-lookup"><span data-stu-id="d2388-139">Repeat on the second Tuesday of every month.</span></span>  <br/> <span data-ttu-id="d2388-140">Repita el tercer jueves del mes cada tres meses.</span><span class="sxs-lookup"><span data-stu-id="d2388-140">Repeat on the third Thursday of the month every three months.</span></span>  <br/> |
|[<span data-ttu-id="d2388-141">Recurrence.RelativeYearlyPattern</span><span class="sxs-lookup"><span data-stu-id="d2388-141">Recurrence.RelativeYearlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-142">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-142">RelativeYearlyRecurrence</span></span>](http://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-143">Repita el primer lunes de agosto de cada año.</span><span class="sxs-lookup"><span data-stu-id="d2388-143">Repeat on the first Monday of August every year.</span></span>  <br/> |
|[<span data-ttu-id="d2388-144">Recurrence.WeeklyPattern</span><span class="sxs-lookup"><span data-stu-id="d2388-144">Recurrence.WeeklyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-145">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-145">WeeklyRecurrence</span></span>](http://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-146">Repita todos los lunes.</span><span class="sxs-lookup"><span data-stu-id="d2388-146">Repeat every Monday.</span></span>  <br/> <span data-ttu-id="d2388-147">Repita todos los martes y el jueves cada dos semanas.</span><span class="sxs-lookup"><span data-stu-id="d2388-147">Repeat every Tuesday and Thursday every other week.</span></span>  <br/> |
|[<span data-ttu-id="d2388-148">Recurrence.YearlyPattern</span><span class="sxs-lookup"><span data-stu-id="d2388-148">Recurrence.YearlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-149">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-149">AbsoluteYearlyRecurrence</span></span>](http://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-150">Repita el 1 de septiembre de cada año.</span><span class="sxs-lookup"><span data-stu-id="d2388-150">Repeat on September 1st every year.</span></span>  <br/> |
   
<span data-ttu-id="d2388-151">La otra parte importante de información de un patrón de periodicidad es cuando finaliza la periodicidad.</span><span class="sxs-lookup"><span data-stu-id="d2388-151">The other important piece of information for a recurrence pattern is when the recurrence ends.</span></span> <span data-ttu-id="d2388-152">Esto se puede expresar como puede ser un número de conjunto de repeticiones, como una fecha de finalización o como no tener ningún extremo.</span><span class="sxs-lookup"><span data-stu-id="d2388-152">This can be expressed as either a set number of occurrences, as an end date, or as having no end.</span></span>
  
<span data-ttu-id="d2388-153">**Tabla 2. Opciones para el final de una serie periódica**</span><span class="sxs-lookup"><span data-stu-id="d2388-153">**Table 2. Options for the end of a recurring series**</span></span>

|<span data-ttu-id="d2388-154">**Método o propiedad de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="d2388-154">**EWS Managed API method/property**</span></span>|<span data-ttu-id="d2388-155">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="d2388-155">**EWS element**</span></span>|<span data-ttu-id="d2388-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2388-156">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d2388-157">Recurrence.NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="d2388-157">Recurrence.NumberOfOccurrences</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-158">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-158">NumberedRecurrence</span></span>](http://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-159">El valor de esta propiedad o este elemento especifica el número de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="d2388-159">The value of this property or element specifies the number of occurrences.</span></span>  <br/> |
|[<span data-ttu-id="d2388-160">Recurrence.EndDate</span><span class="sxs-lookup"><span data-stu-id="d2388-160">Recurrence.EndDate</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-161">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-161">EndDateRecurrence</span></span>](http://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-162">La última aparición de la serie recae en o antes de la fecha especificada por esta propiedad o este elemento.</span><span class="sxs-lookup"><span data-stu-id="d2388-162">The last occurrence in the series falls on or before the date specified by this property or element.</span></span>  <br/> |
|[<span data-ttu-id="d2388-163">Recurrence.HasEnd</span><span class="sxs-lookup"><span data-stu-id="d2388-163">Recurrence.HasEnd</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="d2388-164">Recurrence.NeverEnds</span><span class="sxs-lookup"><span data-stu-id="d2388-164">Recurrence.NeverEnds</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d2388-165">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="d2388-165">NoEndRecurrence</span></span>](http://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |<span data-ttu-id="d2388-166">La serie no tiene fin.</span><span class="sxs-lookup"><span data-stu-id="d2388-166">The series has no end.</span></span>  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a><span data-ttu-id="d2388-167">Expandido frente a las vistas que no sean expandido</span><span class="sxs-lookup"><span data-stu-id="d2388-167">Expanded vs. non-expanded views</span></span>

<span data-ttu-id="d2388-168">Mediante el método **FindAppointments** en la API administrada de EWS (o la operación **FindItem** con un elemento **CalendarView** en EWS), invoca el proceso de expansión.</span><span class="sxs-lookup"><span data-stu-id="d2388-168">Using the **FindAppointments** method in the EWS Managed API (or the **FindItem** operation with a **CalendarView** element in EWS) invokes the expansion process.</span></span> <span data-ttu-id="d2388-169">Esto oculta citas maestras periódicas desde el conjunto de resultados y, en su lugar, presenta una vista expandida de esa serie periódica.</span><span class="sxs-lookup"><span data-stu-id="d2388-169">This hides recurring master appointments from the result set, and instead presents an expanded view of that recurring series.</span></span> <span data-ttu-id="d2388-170">Repeticiones de y excepciones al patrón de periódicas que entran dentro de los parámetros de la vista de calendario se incluyen en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d2388-170">Occurrences of and exceptions to the recurring master that fall within the parameters of the calendar view are included in the result set.</span></span> <span data-ttu-id="d2388-171">Por el contrario, con el método **FindItems** en la API administrada de EWS (o la operación **FindItem** con un elemento **IndexedPageItemView** o **FractionalPageItemView** en EWS), no invoca el proceso de expansión y repeticiones y no se incluyen las excepciones.</span><span class="sxs-lookup"><span data-stu-id="d2388-171">Conversely, using the **FindItems** method in the EWS Managed API (or the **FindItem** operation with a **IndexedPageItemView** or **FractionalPageItemView** element in EWS), does not invoke the expansion process, and occurrences and exceptions are not included.</span></span> <span data-ttu-id="d2388-172">Veamos un ejemplo de comparación de los dos métodos.</span><span class="sxs-lookup"><span data-stu-id="d2388-172">Let's look at an example comparing the two methods.</span></span> 
  
<span data-ttu-id="d2388-173">**Tabla 3. Los métodos y las operaciones de la búsqueda de citas**</span><span class="sxs-lookup"><span data-stu-id="d2388-173">**Table 3. Methods and operations for finding appointments**</span></span>

|<span data-ttu-id="d2388-174">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="d2388-174">**EWS Managed API method**</span></span>|<span data-ttu-id="d2388-175">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="d2388-175">**EWS operation**</span></span>|<span data-ttu-id="d2388-176">**¿Expande la serie?**</span><span class="sxs-lookup"><span data-stu-id="d2388-176">**Expands series?**</span></span>|<span data-ttu-id="d2388-177">**Elementos que se incluyen en los resultados**</span><span class="sxs-lookup"><span data-stu-id="d2388-177">**Items included in results**</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="d2388-178">ExchangeService.FindAppointments</span><span class="sxs-lookup"><span data-stu-id="d2388-178">ExchangeService.FindAppointments</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="d2388-179">[Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2388-179">[FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with a [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="d2388-180">Sí</span><span class="sxs-lookup"><span data-stu-id="d2388-180">Yes</span></span>  <br/> |<span data-ttu-id="d2388-181">Citas periódicas no, único repeticiones de una serie periódica y las excepciones de una serie periódica</span><span class="sxs-lookup"><span data-stu-id="d2388-181">Non-recurring appointments, single occurrences of recurring series, and exceptions to recurring series</span></span>  <br/> |
|[<span data-ttu-id="d2388-182">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="d2388-182">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="d2388-183">[Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento de [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o elemento de [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2388-183">[FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with an [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="d2388-184">No</span><span class="sxs-lookup"><span data-stu-id="d2388-184">No</span></span>  <br/> |<span data-ttu-id="d2388-185">Las citas periódicas no y citas maestras periódicas</span><span class="sxs-lookup"><span data-stu-id="d2388-185">Non-recurring appointments and recurring master appointments</span></span>  <br/> |
   
<span data-ttu-id="d2388-186">Sadie acaba de iniciar sesión a su son para el equipo de natación.</span><span class="sxs-lookup"><span data-stu-id="d2388-186">Sadie has just signed her son up for swim team.</span></span> <span data-ttu-id="d2388-187">El equipo tiene práctica cada mañana miércoles a las 8:30 A.M., iniciar el 2 de julio, con el último procedimiento recomendado que se va a 6 de agosto.</span><span class="sxs-lookup"><span data-stu-id="d2388-187">The team has practice every Wednesday morning at 8:30 AM, starting July 2, with the last practice being on August 6.</span></span> <span data-ttu-id="d2388-188">Desean no se olvide de práctica, Sadie agrega una cita periódica a su calendario que se debe recordar a ella.</span><span class="sxs-lookup"><span data-stu-id="d2388-188">Not wanting to forget about practice, Sadie adds a recurring appointment to her calendar to remind her.</span></span>
  
<span data-ttu-id="d2388-189">**Tabla 4. Cita periódica de Sadie**</span><span class="sxs-lookup"><span data-stu-id="d2388-189">**Table 4. Sadie's recurring appointment**</span></span>

|<span data-ttu-id="d2388-190">**Campo de cita**</span><span class="sxs-lookup"><span data-stu-id="d2388-190">**Appointment field**</span></span>|<span data-ttu-id="d2388-191">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d2388-191">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2388-192">Subject</span><span class="sxs-lookup"><span data-stu-id="d2388-192">Subject</span></span>  <br/> |<span data-ttu-id="d2388-193">Nadar práctica de equipo</span><span class="sxs-lookup"><span data-stu-id="d2388-193">Swim Team Practice</span></span>  <br/> |
|<span data-ttu-id="d2388-194">Inicio</span><span class="sxs-lookup"><span data-stu-id="d2388-194">Start</span></span>  <br/> |<span data-ttu-id="d2388-195">2 de julio de 2014 8:30 AM</span><span class="sxs-lookup"><span data-stu-id="d2388-195">July 2, 2014 8:30 AM</span></span>  <br/> |
|<span data-ttu-id="d2388-196">End</span><span class="sxs-lookup"><span data-stu-id="d2388-196">End</span></span>  <br/> |<span data-ttu-id="d2388-197">2 de julio de 2014 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="d2388-197">July 2, 2014 10:00 AM</span></span>  <br/> |
|<span data-ttu-id="d2388-198">Se repite</span><span class="sxs-lookup"><span data-stu-id="d2388-198">Recurs</span></span>  <br/> |<span data-ttu-id="d2388-199">Todos los miércoles</span><span class="sxs-lookup"><span data-stu-id="d2388-199">Every Wednesday</span></span>  <br/> |
|<span data-ttu-id="d2388-200">Última aparición</span><span class="sxs-lookup"><span data-stu-id="d2388-200">Last occurrence</span></span>  <br/> |<span data-ttu-id="d2388-201">6 de agosto de 2014 8:30 AM</span><span class="sxs-lookup"><span data-stu-id="d2388-201">August 6, 2014 8:30 AM</span></span>  <br/> |
   
<span data-ttu-id="d2388-202">Un vistazo rápido a un calendario se muestra que el equipo tendrá un total de seis recomendados.</span><span class="sxs-lookup"><span data-stu-id="d2388-202">A quick look at a calendar shows that the team will have a total of six practices.</span></span> <span data-ttu-id="d2388-203">Sin embargo, no son seis elementos de cita distintos en el calendario.</span><span class="sxs-lookup"><span data-stu-id="d2388-203">However, there aren't six distinct appointment items in the calendar.</span></span> <span data-ttu-id="d2388-204">En su lugar, hay una sola cita principal periódica que representa la serie.</span><span class="sxs-lookup"><span data-stu-id="d2388-204">Instead, there is just one recurring master appointment representing the series.</span></span>
  
<span data-ttu-id="d2388-205">Ahora vamos a examinar buscar citas en el calendario de Sadie que se producen dentro del mes de julio.</span><span class="sxs-lookup"><span data-stu-id="d2388-205">Now let's look at finding appointments on Sadie's calendar that occur within the month of July.</span></span> <span data-ttu-id="d2388-206">En el ejemplo de código siguiente se usa el método **FindItems** en la API administrada de Exchange para producir una vista que no sean expandida de calendario de Sadie.</span><span class="sxs-lookup"><span data-stu-id="d2388-206">The following code example uses the **FindItems** method in the Exchange Managed API to produce a non-expanded view of Sadie's calendar.</span></span> 
  
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

<span data-ttu-id="d2388-207">Ese código da como resultado la siguiente solicitud de [operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d2388-207">That code results in the following [FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with an [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="d2388-208">La respuesta del servidor incluye sólo un único elemento, el patrón periódico, indicada por el valor del elemento [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) de **RecurringMaster**.</span><span class="sxs-lookup"><span data-stu-id="d2388-208">The server's response includes only a single item, the recurring master, indicated by the [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element value of **RecurringMaster**.</span></span> <span data-ttu-id="d2388-209">El valor del elemento [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d2388-209">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="d2388-210">Ahora vamos a comparar con una vista expandida.</span><span class="sxs-lookup"><span data-stu-id="d2388-210">Now let's compare with an expanded view.</span></span> <span data-ttu-id="d2388-211">En el ejemplo de código siguiente se usa el método **FindAppointments** en la API administrada de EWS para crear una vista de calendario de Sadie expandida.</span><span class="sxs-lookup"><span data-stu-id="d2388-211">The following code example uses the **FindAppointments** method in the EWS Managed API to create an expanded view of Sadie's calendar.</span></span> 
  
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

<span data-ttu-id="d2388-212">Este código da como resultado la siguiente solicitud de [operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d2388-212">This code results in the following [FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with a [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="d2388-213">En este momento, la respuesta del servidor incluye cinco repeticiones, uno para cada miércoles en julio.</span><span class="sxs-lookup"><span data-stu-id="d2388-213">This time, the server response includes five occurrences, one for each Wednesday in July.</span></span> <span data-ttu-id="d2388-214">Los elementos de [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) en estos todos los elementos tienen un valor de **aparición**.</span><span class="sxs-lookup"><span data-stu-id="d2388-214">The [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) elements on these items all have a value of **Occurrence**.</span></span> <span data-ttu-id="d2388-215">Tenga en cuenta que el maestro periódico no está presente en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2388-215">Note that the recurring master is not present in the response.</span></span> <span data-ttu-id="d2388-216">Los valores de los elementos de [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d2388-216">The values of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="d2388-217">Una vez que tenga un maestro periódico, huérfana o una excepción, siempre puede [recuperar los otros elementos relacionados](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d2388-217">After you have a recurring master, an occurrence, or an exception, you can always [retrieve the other related items](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="d2388-218">Dado un aparición o una excepción, puede recuperar el patrón de periódico y viceversa.</span><span class="sxs-lookup"><span data-stu-id="d2388-218">Given an occurrence or exception, you can retrieve the recurring master, and vice versa.</span></span>
  
## <a name="working-with-recurring-calendar-items"></a><span data-ttu-id="d2388-219">Trabajar con elementos de calendario periódicos</span><span class="sxs-lookup"><span data-stu-id="d2388-219">Working with recurring calendar items</span></span>

<span data-ttu-id="d2388-220">Todos los mismos usar operaciones y métodos para trabajar con la serie periódica tal y como se utiliza para trabajar con elementos de calendario no periódicos.</span><span class="sxs-lookup"><span data-stu-id="d2388-220">You use all the same methods and operations to work with recurring series as you use to work with non-recurring calendar items.</span></span> <span data-ttu-id="d2388-221">La diferencia es que, en función del elemento que se utiliza para invocar los métodos o las operaciones, pueden aplicar las acciones que realizar para toda la serie o sólo una sola aparición.</span><span class="sxs-lookup"><span data-stu-id="d2388-221">The difference is that, depending on the item you use to invoke those methods or operations, the actions you take can apply to the entire series, or just a single occurrence.</span></span> <span data-ttu-id="d2388-222">[Acciones realizadas en el maestro de periódico](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) se aplicará a todas las apariciones de la serie, mientras [acciones realizadas a una sola aparición o excepción](how-to-update-a-recurring-series-by-using-ews.md) sólo se aplicará a esa aparición o una excepción.</span><span class="sxs-lookup"><span data-stu-id="d2388-222">[Actions taken on the recurring master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) will apply to all occurrences in the series, while [actions taken to a single occurrence or exception](how-to-update-a-recurring-series-by-using-ews.md) will only apply to that occurrence or exception.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d2388-223">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d2388-223">In this section</span></span>

- [<span data-ttu-id="d2388-224">Obtener acceso a una serie periódica mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2388-224">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d2388-225">Creación de una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2388-225">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d2388-226">Eliminar las citas de una serie periódica mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2388-226">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d2388-227">Actualización de una serie periódica mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="d2388-227">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="d2388-228">Actualización de una serie periódica mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2388-228">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="d2388-229">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2388-229">See also</span></span>


- [<span data-ttu-id="d2388-230">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2388-230">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="d2388-231">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="d2388-231">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="d2388-232">Obtener las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2388-232">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    


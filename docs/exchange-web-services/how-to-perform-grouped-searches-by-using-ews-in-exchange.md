---
title: Realizar búsquedas agrupadas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 55de92eb-8e8b-4156-8ad9-dd3828024242
description: Descubra cómo realizar búsquedas agrupadas en la API administrada de EWS o en la aplicación EWS dirigida a Exchange.
ms.openlocfilehash: 65c6f75ea6b8ab848a263349dcceceead52fa210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527929"
---
# <a name="perform-grouped-searches-by-using-ews-in-exchange"></a><span data-ttu-id="b6edd-103">Realizar búsquedas agrupadas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b6edd-103">Perform grouped searches by using EWS in Exchange</span></span>

<span data-ttu-id="b6edd-104">Descubra cómo realizar búsquedas agrupadas en la API administrada de EWS o en la aplicación EWS dirigida a Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6edd-104">Find out how to perform grouped searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="b6edd-105">Las búsquedas agrupadas resultan útiles en cuanto a que le permiten controlar el modo en que se organizan los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b6edd-105">Grouped searches are useful in that they gives you control over how search results are organized.</span></span> <span data-ttu-id="b6edd-106">Los resultados de búsqueda organizados pueden facilitar a su aplicación la tarea de procesar los resultados o mostrarlos a un usuario final de una manera fácil de administrar.</span><span class="sxs-lookup"><span data-stu-id="b6edd-106">Organized search results can make it easier for your application to process results or display them to an end user in a manageable way.</span></span>
  
<span data-ttu-id="b6edd-107">La agrupación funciona poniendo todos los elementos dentro del conjunto de resultados que tienen el mismo valor de un campo específico en un grupo.</span><span class="sxs-lookup"><span data-stu-id="b6edd-107">Grouping works by putting all items within the result set that have the same value of a specific field into a group.</span></span> <span data-ttu-id="b6edd-108">Por ejemplo, puede agrupar los resultados por el remitente y todos los elementos de la misma persona estarán en un grupo independiente y los elementos dentro de cada grupo se ordenarán según el orden que especifique en la vista.</span><span class="sxs-lookup"><span data-stu-id="b6edd-108">For example, you can group your results by the sender, and all items from the same person will be in a separate group, and the items within each group will be sorted according to the order you specify on the view.</span></span> <span data-ttu-id="b6edd-109">Los propios grupos se ordenan por un valor agregado en función de un campo que elija.</span><span class="sxs-lookup"><span data-stu-id="b6edd-109">The groups themselves are sorted by an aggregate value based on a field you choose.</span></span>
  
<span data-ttu-id="b6edd-110">**Tabla 1. Métodos de la API administrada de EWS y operaciones EWS para organizar los resultados de búsqueda**</span><span class="sxs-lookup"><span data-stu-id="b6edd-110">**Table 1. EWS Managed API methods and EWS operations for organizing search results**</span></span>

|<span data-ttu-id="b6edd-111">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="b6edd-111">**If you want to…**</span></span>|<span data-ttu-id="b6edd-112">**En la API administrada de EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="b6edd-112">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="b6edd-113">**En EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="b6edd-113">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6edd-114">Organizar elementos con el mismo valor en una propiedad específica de los resultados en grupos</span><span class="sxs-lookup"><span data-stu-id="b6edd-114">Organize items with the same value in a specific property in your results into groups</span></span>  <br/> |[<span data-ttu-id="b6edd-115">Agrupación. GroupOn</span><span class="sxs-lookup"><span data-stu-id="b6edd-115">Grouping.GroupOn</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.groupon%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="b6edd-116">Elemento [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) como elemento secundario del elemento [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6edd-116">[FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="b6edd-117">Ordenar elementos dentro de cada grupo por el valor de una propiedad específica</span><span class="sxs-lookup"><span data-stu-id="b6edd-117">Sort items within each group by the value in a specific property</span></span>  <br/> |[<span data-ttu-id="b6edd-118">ItemView. OrderBy</span><span class="sxs-lookup"><span data-stu-id="b6edd-118">ItemView.OrderBy</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="b6edd-119">Elemento [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6edd-119">[SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="b6edd-120">Ordenar los grupos</span><span class="sxs-lookup"><span data-stu-id="b6edd-120">Sort the groups</span></span>  <br/> |[<span data-ttu-id="b6edd-121">Agrupación. AggregateOn</span><span class="sxs-lookup"><span data-stu-id="b6edd-121">Grouping.AggregateOn</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="b6edd-122">Agrupación. AggregateType</span><span class="sxs-lookup"><span data-stu-id="b6edd-122">Grouping.AggregateType</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="b6edd-123">Agrupación. SortDirection</span><span class="sxs-lookup"><span data-stu-id="b6edd-123">Grouping.SortDirection</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="b6edd-124">Elemento **FieldURI** como elemento secundario del elemento [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6edd-124">**FieldURI** element as a child of the [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element</span></span><br/><br/> <span data-ttu-id="b6edd-125">Atributo **Aggregate** en el elemento **AggregateOn**</span><span class="sxs-lookup"><span data-stu-id="b6edd-125">**Aggregate** attribute on the **AggregateOn** element</span></span><br/><br/><span data-ttu-id="b6edd-126">Atributo **Order** en el elemento **GroupBy**</span><span class="sxs-lookup"><span data-stu-id="b6edd-126">**Order** attribute on the **GroupBy** element</span></span>  <br/> |
   
<span data-ttu-id="b6edd-127">Vamos a hacerlo paso a paso.</span><span class="sxs-lookup"><span data-stu-id="b6edd-127">Let's take it step by step.</span></span>
  
## <a name="group-results-by-a-specific-property"></a><span data-ttu-id="b6edd-128">Resultados de grupo por una propiedad específica</span><span class="sxs-lookup"><span data-stu-id="b6edd-128">Group results by a specific property</span></span>
<span data-ttu-id="b6edd-129"><a name="bk_GroupResults"> </a></span><span class="sxs-lookup"><span data-stu-id="b6edd-129"><a name="bk_GroupResults"> </a></span></span>

<span data-ttu-id="b6edd-130">El primer paso para usar la agrupación es seleccionar una propiedad o atributo en los elementos del almacén de Exchange para agrupar por.</span><span class="sxs-lookup"><span data-stu-id="b6edd-130">The first step to using grouping is to select a property, or attribute on the items in the Exchange store, to group by.</span></span> <span data-ttu-id="b6edd-131">La API administrada de EWS las expone como propiedades de clase en las clases correspondientes, mientras que EWS las expone como elementos XML.</span><span class="sxs-lookup"><span data-stu-id="b6edd-131">The EWS Managed API exposes these as class properties on the corresponding classes, while EWS exposes them as XML elements.</span></span> <span data-ttu-id="b6edd-132">Puede elegir cualquier propiedad, incluidas las personalizadas o extendidas, pero es útil comprender cómo se agrupan los elementos según el valor de la propiedad que elija.</span><span class="sxs-lookup"><span data-stu-id="b6edd-132">You can choose any property, including custom or extended properties, but it is helpful to understand how items are grouped based on the value of the property you choose.</span></span> 

<span data-ttu-id="b6edd-133">Todos los elementos que tienen el mismo valor en la propiedad que seleccione para agrupar se agruparán juntos.</span><span class="sxs-lookup"><span data-stu-id="b6edd-133">All items that have the same value in the property you choose to group by will be grouped together.</span></span> <span data-ttu-id="b6edd-134">Esto puede parecer obvio, pero es un detalle importante.</span><span class="sxs-lookup"><span data-stu-id="b6edd-134">This might seem obvious, but it is an important detail.</span></span> <span data-ttu-id="b6edd-135">Considere qué ocurre si agrupa por una propiedad de fecha y hora, como [Item. DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) en la API administrada de EWS o el elemento [DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) en EWS.</span><span class="sxs-lookup"><span data-stu-id="b6edd-135">Consider what happens if you group by a date/time property, such as [Item.DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) in the EWS Managed API, or the [DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="b6edd-136">La intención podría ser organizar los resultados en grupos, con cada grupo que contenga elementos del mismo día.</span><span class="sxs-lookup"><span data-stu-id="b6edd-136">The intent might be to organize the results into groups, with each group containing items from the same day.</span></span> <span data-ttu-id="b6edd-137">Sin embargo, la agrupación examina el valor completo, que incluye la hora.</span><span class="sxs-lookup"><span data-stu-id="b6edd-137">However, grouping looks at the entire value, which includes the time.</span></span> 

<span data-ttu-id="b6edd-138">El resultado final es que los elementos se agruparán para que los elementos recibidos al mismo tiempo, hasta el segundo, estén en sus propios grupos.</span><span class="sxs-lookup"><span data-stu-id="b6edd-138">The end result is that the items will be grouped so that items received at the same time, down to the second, are in their own groups.</span></span> <span data-ttu-id="b6edd-139">Lo más probable es que los resultados se ordenen en un gran número de grupos con un número pequeño de elementos en cada grupo.</span><span class="sxs-lookup"><span data-stu-id="b6edd-139">The results will most likely be sorted into a large number of groups with a small number of items in each group.</span></span> 
  
<span data-ttu-id="b6edd-140">Para obtener un conjunto de resultados con un número de grupos más pequeño y un número mayor de elementos en cada grupo, elija una propiedad que probablemente tenga un número menor de valores, como [EmailMessage. from](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) o [Item. Categories](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) en la API administrada [de](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) EWS o en [categorías](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="b6edd-140">To get a results set with a smaller number of groups and a larger number of items in each group, choose a property that is likely to have a smaller number of values, such as [EmailMessage.From](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) or [Item.Categories](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) in the EWS Managed API, or [From](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) or [Categories](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) in EWS.</span></span> <span data-ttu-id="b6edd-141">En la siguiente figura se muestra una lista de los correos electrónicos que aparecen en la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6edd-141">The following figure shows a list of emails that appear in an Inbox.</span></span> 
  
<span data-ttu-id="b6edd-142">**Figura 1. Mensajes de una bandeja de entrada**</span><span class="sxs-lookup"><span data-stu-id="b6edd-142">**Figure 1. Messages in an Inbox**</span></span>

![Muestra de una lista de mensajes en la bandeja de entrada de un usuario.](media/Ex15_GroupedSearch_MsgList.png)
  
<span data-ttu-id="b6edd-144">Si agrupa los elementos de la figura 1 por la propiedad **EmailMessage. from** , el resultado será dos grupos, uno para los mensajes enviados por la esperanza bruta y otro para los mensajes enviados por Sadie Daniels.</span><span class="sxs-lookup"><span data-stu-id="b6edd-144">If you group the items in Figure 1 by the **EmailMessage.From** property, the result will be two groups, one for messages sent by Hope Gross, and one for messages sent by Sadie Daniels.</span></span> 
  
<span data-ttu-id="b6edd-145">**Figura 2. Mensajes separados en grupos basados en la propiedad From**</span><span class="sxs-lookup"><span data-stu-id="b6edd-145">**Figure 2. Messages separated into groups based on the From property**</span></span>

![Una imagen que muestra mensajes ordenados en dos listas por la propiedad De.](media/Ex15_GroupedSearch_SeparateGroups.png)
  
## <a name="sort-the-items-within-groups"></a><span data-ttu-id="b6edd-147">Ordenar los elementos dentro de los grupos</span><span class="sxs-lookup"><span data-stu-id="b6edd-147">Sort the items within groups</span></span>
<span data-ttu-id="b6edd-148"><a name="bk_SortItems"> </a></span><span class="sxs-lookup"><span data-stu-id="b6edd-148"><a name="bk_SortItems"> </a></span></span>

<span data-ttu-id="b6edd-149">Puede controlar cómo se ordenan los elementos dentro de cada grupo mediante la propiedad [ItemView. OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) en la API administrada EWS o el elemento [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="b6edd-149">You can control how items are sorted within each group by using the [ItemView.OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="b6edd-150">La misma ordenación se aplica a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="b6edd-150">The same ordering applies to each group.</span></span> <span data-ttu-id="b6edd-151">Por ejemplo, si ordena los elementos de la figura 1 por la propiedad **Item. DateTimeReceived** , en orden descendente, el último elemento recibido de la esperanza bruta será el primero en el grupo de esperanza bruto y el último elemento recibido de Sadie Daniels será el primero en el grupo Sadie Daniels.</span><span class="sxs-lookup"><span data-stu-id="b6edd-151">For example, if you sort the items from Figure 1 by the **Item.DateTimeReceived** property, in descending order, the item most recently received from Hope Gross will be first in the Hope Gross group, and the item most recently received from Sadie Daniels will be first in the Sadie Daniels group.</span></span> <span data-ttu-id="b6edd-152">Convenientemente, los grupos de la figura 2 ya están ordenados de esta forma.</span><span class="sxs-lookup"><span data-stu-id="b6edd-152">Conveniently, the groups in Figure 2 are already sorted this way.</span></span> 
  
## <a name="sort-the-groups"></a><span data-ttu-id="b6edd-153">Ordenar los grupos</span><span class="sxs-lookup"><span data-stu-id="b6edd-153">Sort the groups</span></span>
<span data-ttu-id="b6edd-154"><a name="bk_SortGroups"> </a></span><span class="sxs-lookup"><span data-stu-id="b6edd-154"><a name="bk_SortGroups"> </a></span></span>

<span data-ttu-id="b6edd-155">Ahora que ha liquidado los grupos, el último paso consiste en ordenar los grupos.</span><span class="sxs-lookup"><span data-stu-id="b6edd-155">Now that you have your groups settled, the final step is sorting the groups themselves.</span></span> <span data-ttu-id="b6edd-156">Debido a que los propios grupos no tienen valores específicos, el proceso de agrupación tiene que asignar un valor de ordenación a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="b6edd-156">Because the groups themselves have no specific values, the grouping process has to assign a sort value to each group.</span></span> <span data-ttu-id="b6edd-157">Esto se realiza mediante la agregación de los valores de una propiedad específica dentro de cada grupo, especificado por la propiedad [Grouping. AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) en la API administrada EWS, o el elemento [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) como elemento secundario del elemento [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) en EWS.</span><span class="sxs-lookup"><span data-stu-id="b6edd-157">This is done by aggregation of the values of a specific property within each group, specified by the [Grouping.AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="b6edd-158">La propiedad [Grouping. AggregateType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) de la API administrada de EWS (o el atributo **Aggregate** del elemento **AggregateOn** de EWS) especifica qué valor de los elementos de cada grupo se asigna al valor de ordenación del grupo, ya sea el valor más grande o el valor menor.</span><span class="sxs-lookup"><span data-stu-id="b6edd-158">The [Grouping.AggregateType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) property in the EWS Managed API (or the **Aggregate** attribute on the **AggregateOn** element in EWS) specifies which value from the items within each group is assigned to the sort value for the group — either the largest value or the smallest value.</span></span> <span data-ttu-id="b6edd-159">Por último, el criterio de ordenación (descendente o ascendente) se especifica mediante la propiedad [Grouping. SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) en la API administrada EWS o el atributo **Order** del elemento [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) en EWS.</span><span class="sxs-lookup"><span data-stu-id="b6edd-159">Finally, the sort order (descending or ascending) is specified by the [Grouping.SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) property in the EWS Managed API, or the **Order** attribute on the [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element in EWS.</span></span> 
  
<span data-ttu-id="b6edd-160">Por ejemplo, si los grupos de la figura 2 se ordenan agregando la propiedad **Item. DateTimeReceived** , usando el menor valor y orden descendente, los elementos se devuelven en el orden indicado en la figura 3.</span><span class="sxs-lookup"><span data-stu-id="b6edd-160">For example, if the groups from Figure 2 are sorted by aggregating on the **Item.DateTimeReceived** property, using the smallest value, and sorting in descending order, the items are returned in the order in shown Figure 3.</span></span> 
  
<span data-ttu-id="b6edd-161">**Figura 3. Resultados de la búsqueda agrupados con los grupos ordenados por la propiedad DateTimeReceived**</span><span class="sxs-lookup"><span data-stu-id="b6edd-161">**Figure 3. Grouped search results with the groups sorted by the DateTimeReceived property**</span></span>

![Una imagen que muestra una lista ordenada de mensajes, agrupados por la propiedad De, con los grupos ordenados por la fecha y hora de recepción más antigua.](media/Ex15_GroupedSearch_Results.png)
  
<span data-ttu-id="b6edd-163">En las secciones siguientes se muestra cómo se puede agrupar y ordenar juntos en el código.</span><span class="sxs-lookup"><span data-stu-id="b6edd-163">The next sections show you how you might pull grouping and sorting together in code.</span></span>
  
## <a name="example-perform-a-grouped-search-by-using-the-ews-managed-api"></a><span data-ttu-id="b6edd-164">Ejemplo: realizar una búsqueda agrupada mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b6edd-164">Example: Perform a grouped search by using the EWS Managed API</span></span>
<span data-ttu-id="b6edd-165"><a name="bk_GroupSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="b6edd-165"><a name="bk_GroupSearchEWSMA"> </a></span></span>

<span data-ttu-id="b6edd-166">Los siguientes métodos de la API administrada de EWS pueden usar la agrupación:</span><span class="sxs-lookup"><span data-stu-id="b6edd-166">The following EWS Managed API methods can use grouping:</span></span>
  
- [<span data-ttu-id="b6edd-167">ExchangeService. FindItems</span><span class="sxs-lookup"><span data-stu-id="b6edd-167">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="b6edd-168">Folder. FindItems</span><span class="sxs-lookup"><span data-stu-id="b6edd-168">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="b6edd-169">En el ejemplo siguiente se usa el método **ExchangeService. FindItems** ; sin embargo, las mismas reglas y conceptos se aplican al método **Folder. FindItems** .</span><span class="sxs-lookup"><span data-stu-id="b6edd-169">The following example uses the **ExchangeService.FindItems** method; however, the same rules and concepts apply to the **Folder.FindItems** method.</span></span> <span data-ttu-id="b6edd-170">En este ejemplo, se define un método denominado **GroupItemsByFrom** .</span><span class="sxs-lookup"><span data-stu-id="b6edd-170">In this example, a method called **GroupItemsByFrom** is defined.</span></span> <span data-ttu-id="b6edd-171">Toma un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) y un objeto [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) como parámetros.</span><span class="sxs-lookup"><span data-stu-id="b6edd-171">It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object as parameters.</span></span> <span data-ttu-id="b6edd-172">Solicita los primeros 50 elementos en la carpeta, agrupados por la propiedad **EmailMessage. from** , ordenados por la propiedad **Item. DateTimeReceived** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="b6edd-172">It requests the first 50 items in the folder, grouped by the **EmailMessage.From** property, sorted by the **Item.DateTimeReceived** property in descending order.</span></span> <span data-ttu-id="b6edd-173">Los propios grupos se ordenan por el valor de la propiedad **Item. DateTimeReceived** más pequeño de sus elementos, en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="b6edd-173">The groups themselves are sorted by the smallest **Item.DateTimeReceived** property value on their items, in descending order.</span></span> 
  
<span data-ttu-id="b6edd-174">En este ejemplo se supone que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b6edd-174">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
static void GroupItemsByFrom(ExchangeService service, WellKnownFolderName folder)
{
    // Limit the result set to 50 items.
    ItemView view = new ItemView(50);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.From,
                                       ItemSchema.Categories);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Specify the sorting done within the groups.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    // Configure grouping.
    Grouping groupByFrom = new Grouping();
    groupByFrom.GroupOn = EmailMessageSchema.From;
    groupByFrom.AggregateOn = ItemSchema.DateTimeReceived;
    groupByFrom.AggregateType = AggregateType.Minimum;
    groupByFrom.SortDirection = SortDirection.Descending;
    try
    {
        GroupedFindItemsResults<Item> results = service.FindItems(folder,
            view, groupByFrom);
        foreach (ItemGroup<Item> group in results.ItemGroups)
        {
            Console.WriteLine("Group: {0}", group.GroupIndex);
            foreach (Item item in group.Items)
            {
                if (item is EmailMessage)
                {
                    EmailMessage message = item as EmailMessage;
                    Console.WriteLine("From: {0}", message.From);
                    Console.WriteLine("Subject: {0}", message.Subject);
                    Console.WriteLine("Id: {0}\n", message.Id.ToString());
                }
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="example-perform-a-grouped-search-by-using-ews"></a><span data-ttu-id="b6edd-175">Ejemplo: realizar una búsqueda agrupada con EWS</span><span class="sxs-lookup"><span data-stu-id="b6edd-175">Example: Perform a grouped search by using EWS</span></span>
<span data-ttu-id="b6edd-176"><a name="bk_GroupSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="b6edd-176"><a name="bk_GroupSearchEWS"> </a></span></span>

<span data-ttu-id="b6edd-177">En el siguiente ejemplo de solicitud se muestra una solicitud de [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para los primeros 50 elementos de la carpeta, agrupados por el elemento **from** , ordenados por el elemento **DateTimeReceived** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="b6edd-177">The following request example shows a [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request for the first 50 items in the folder, grouped by the **From** element, sorted by the **DateTimeReceived** element in descending order.</span></span> <span data-ttu-id="b6edd-178">Los propios grupos se ordenan por el valor del elemento **DateTimeReceived** más pequeño de sus elementos, en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="b6edd-178">The groups themselves are sorted by the smallest **DateTimeReceived** element value on their items, in descending order.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:From" />
          <t:FieldURI FieldURI="item:Categories" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="50" Offset="0" BasePoint="Beginning" />
      <m:GroupBy Order="Descending">
        <t:FieldURI FieldURI="message:From" />
        <t:AggregateOn Aggregate="Minimum">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:AggregateOn>
      </m:GroupBy>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b6edd-179">El servidor devuelve la siguiente respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6edd-179">The server returns the following response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
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
          <m:RootFolder IndexedPagingOffset="10" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>0</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Planning resources</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:41:05Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Timeline</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:40:37Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Project</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>For your perusal</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:51:16Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>meeting notes</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Blue category</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Meeting notes</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>1</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Query</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:43:15Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Update</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:42:33Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Project</t:String>
                      <t:String>Blue category</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>This cat is hilarious!</t:Subject>
                    <t:DateTimeReceived>2013-10-15T20:22:12Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="version-differences"></a><span data-ttu-id="b6edd-180">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="b6edd-180">Version differences</span></span>
<span data-ttu-id="b6edd-181"><a name="bk_VersionDiffs"> </a></span><span class="sxs-lookup"><span data-stu-id="b6edd-181"><a name="bk_VersionDiffs"> </a></span></span>

<span data-ttu-id="b6edd-182">Las versiones de Exchange que comienzan con la versión principal 15 y terminan con la compilación 15.0.775.38 los elementos de **Grupo** devuelven (del tipo **GroupedItemsType**) en vez de los elementos [GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) en la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="b6edd-182">Versions of Exchange starting with major version 15 and ending with build 15.0.775.38 return **Group** elements (of type **GroupedItemsType**) in place of [GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) elements in the SOAP response.</span></span> <span data-ttu-id="b6edd-183">Si usa la API administrada de EWS, esto hará que la colección [GroupedFindItemsResults. ItemGroups](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx) contenga 0 objetos.</span><span class="sxs-lookup"><span data-stu-id="b6edd-183">If you are using the EWS Managed API, this will cause the [GroupedFindItemsResults.ItemGroups](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx) collection to contain 0 objects.</span></span> <span data-ttu-id="b6edd-184">Si usa EWS, los elementos **Group** deben administrarse como elementos **GroupedItems** .</span><span class="sxs-lookup"><span data-stu-id="b6edd-184">If you are using EWS, **Group** elements should be handled as **GroupedItems** elements.</span></span> 
  
<span data-ttu-id="b6edd-185">Las versiones de Exchange que comienzan con la versión principal 15 devuelven elementos adicionales **Group** o **GroupedItems** con el atributo **xsi: nil** establecido en **true** en la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="b6edd-185">Versions of Exchange starting with major version 15 return extra **Group** or **GroupedItems** elements with the **xsi:nil** attribute set to **true** in the SOAP response.</span></span> <span data-ttu-id="b6edd-186">Si usa la API administrada de EWS, estos elementos adicionales harán que se inicie una [ServiceXmlDeserializationException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b6edd-186">If you are using the EWS Managed API, these extra elements will cause a [ServiceXmlDeserializationException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) to be thrown.</span></span> <span data-ttu-id="b6edd-187">Si está usando EWS, estos elementos adicionales deben omitirse.</span><span class="sxs-lookup"><span data-stu-id="b6edd-187">If you are using EWS, these extra elements should be ignored.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6edd-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6edd-188">See also</span></span>

- [<span data-ttu-id="b6edd-189">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b6edd-189">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="b6edd-190">ExchangeService. FindItems</span><span class="sxs-lookup"><span data-stu-id="b6edd-190">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="b6edd-191">Folder. FindItems</span><span class="sxs-lookup"><span data-stu-id="b6edd-191">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)   
- [<span data-ttu-id="b6edd-192">Clase Grouping</span><span class="sxs-lookup"><span data-stu-id="b6edd-192">Grouping class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="b6edd-193">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="b6edd-193">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    


---
title: Realizar búsquedas agrupadas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 55de92eb-8e8b-4156-8ad9-dd3828024242
description: Encuentre información acerca de cómo realizar búsquedas agrupadas en la API administrada de EWS o la aplicación de EWS dirigido a Exchange.
ms.openlocfilehash: 63a796e2c724351c15287a5596a9a063954f8b40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763151"
---
# <a name="perform-grouped-searches-by-using-ews-in-exchange"></a><span data-ttu-id="2a5f4-103">Realizar búsquedas agrupadas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2a5f4-103">Perform grouped searches by using EWS in Exchange</span></span>

<span data-ttu-id="2a5f4-104">Encuentre información acerca de cómo realizar búsquedas agrupadas en la API administrada de EWS o la aplicación de EWS dirigido a Exchange.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-104">Find out how to perform grouped searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="2a5f4-105">Las búsquedas agrupadas son útiles en que permite controlar cómo los resultados de búsqueda están organizados.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-105">Grouped searches are useful in that they gives you control over how search results are organized.</span></span> <span data-ttu-id="2a5f4-106">Los resultados de búsqueda organizado pueden facilitar a su aplicación procesar los resultados o mostrar a un usuario final de una manera fácil de administrar.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-106">Organized search results can make it easier for your application to process results or display them to an end user in a manageable way.</span></span>
  
<span data-ttu-id="2a5f4-107">Esta opción funciona al colocar todos los elementos dentro del conjunto de resultados que tienen el mismo valor de un campo específico en un grupo.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-107">Grouping works by putting all items within the result set that have the same value of a specific field into a group.</span></span> <span data-ttu-id="2a5f4-108">Por ejemplo, puede agrupar los resultados por el remitente y todos los elementos de la misma persona estará en un grupo independiente y los elementos dentro de cada grupo se ordenarán según el orden que especifique en la vista.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-108">For example, you can group your results by the sender, and all items from the same person will be in a separate group, and the items within each group will be sorted according to the order you specify on the view.</span></span> <span data-ttu-id="2a5f4-109">Los grupos se ordenan por un valor agregado basado en un campo que elija.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-109">The groups themselves are sorted by an aggregate value based on a field you choose.</span></span>
  
<span data-ttu-id="2a5f4-110">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para organizar los resultados de búsqueda**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-110">**Table 1. EWS Managed API methods and EWS operations for organizing search results**</span></span>

|<span data-ttu-id="2a5f4-111">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-111">**If you want to…**</span></span>|<span data-ttu-id="2a5f4-112">**En la API administrada de EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-112">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="2a5f4-113">**En EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-113">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a5f4-114">Organizar los elementos con el mismo valor en una propiedad concreta en los resultados en grupos</span><span class="sxs-lookup"><span data-stu-id="2a5f4-114">Organize items with the same value in a specific property in your results into groups</span></span>  <br/> |[<span data-ttu-id="2a5f4-115">Grouping.GroupOn</span><span class="sxs-lookup"><span data-stu-id="2a5f4-115">Grouping.GroupOn</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.groupon%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="2a5f4-116">Elemento [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) como un elemento secundario del elemento [GroupBy](http://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a5f4-116">[FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [GroupBy](http://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="2a5f4-117">Ordenar los elementos dentro de cada grupo en el valor de una propiedad concreta</span><span class="sxs-lookup"><span data-stu-id="2a5f4-117">Sort items within each group by the value in a specific property</span></span>  <br/> |[<span data-ttu-id="2a5f4-118">ItemView.OrderBy</span><span class="sxs-lookup"><span data-stu-id="2a5f4-118">ItemView.OrderBy</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="2a5f4-119">Elemento [SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a5f4-119">[SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="2a5f4-120">Ordenar los grupos</span><span class="sxs-lookup"><span data-stu-id="2a5f4-120">Sort the groups</span></span>  <br/> |[<span data-ttu-id="2a5f4-121">Grouping.AggregateOn</span><span class="sxs-lookup"><span data-stu-id="2a5f4-121">Grouping.AggregateOn</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="2a5f4-122">Grouping.AggregateType</span><span class="sxs-lookup"><span data-stu-id="2a5f4-122">Grouping.AggregateType</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="2a5f4-123">Grouping.SortDirection</span><span class="sxs-lookup"><span data-stu-id="2a5f4-123">Grouping.SortDirection</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="2a5f4-124">Elemento **FieldURI** como un elemento secundario del elemento [AggregateOn](http://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a5f4-124">**FieldURI** element as a child of the [AggregateOn](http://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element</span></span><br/><br/> <span data-ttu-id="2a5f4-125">Atributo de **agregado** en el elemento **AggregateOn**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-125">**Aggregate** attribute on the **AggregateOn** element</span></span><br/><br/><span data-ttu-id="2a5f4-126">Atributo de **orden** en el elemento **GroupBy**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-126">**Order** attribute on the **GroupBy** element</span></span>  <br/> |
   
<span data-ttu-id="2a5f4-127">Vamos a echarlo paso a paso.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-127">Let's take it step by step.</span></span>
  
## <a name="group-results-by-a-specific-property"></a><span data-ttu-id="2a5f4-128">Resultados de grupo por una propiedad concreta</span><span class="sxs-lookup"><span data-stu-id="2a5f4-128">Group results by a specific property</span></span>
<span data-ttu-id="2a5f4-129"><a name="bk_GroupResults"> </a></span><span class="sxs-lookup"><span data-stu-id="2a5f4-129"></span></span>

<span data-ttu-id="2a5f4-130">Seleccione una propiedad o atributo en los elementos en el almacén de Exchange, que se agrupa es el primer paso para utilizar agrupación.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-130">The first step to using grouping is to select a property, or attribute on the items in the Exchange store, to group by.</span></span> <span data-ttu-id="2a5f4-131">La API administrada de EWS expone estos elementos como propiedades de la clase en las clases correspondientes, mientras EWS expone como elementos XML.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-131">The EWS Managed API exposes these as class properties on the corresponding classes, while EWS exposes them as XML elements.</span></span> <span data-ttu-id="2a5f4-132">Puede elegir cualquier propiedad, incluidas las propiedades extendidas o personalizadas, pero es útil comprender cómo se agrupan los elementos en función del valor de la propiedad que elija.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-132">You can choose any property, including custom or extended properties, but it is helpful to understand how items are grouped based on the value of the property you choose.</span></span> 

<span data-ttu-id="2a5f4-133">Todos los elementos que tienen el mismo valor de la propiedad por que optar por agrupar se agrupan.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-133">All items that have the same value in the property you choose to group by will be grouped together.</span></span> <span data-ttu-id="2a5f4-134">Esto puede parecer obvio, pero es un detalle importante.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-134">This might seem obvious, but it is an important detail.</span></span> <span data-ttu-id="2a5f4-135">Tenga en cuenta lo que sucede si agrupa por una propiedad de fecha y hora, como [Item.DateTimeReceived](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) en la API administrada de EWS, o el elemento de [DateTimeReceived](http://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-135">Consider what happens if you group by a date/time property, such as [Item.DateTimeReceived](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) in the EWS Managed API, or the [DateTimeReceived](http://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="2a5f4-136">La intención es posible organizar los resultados en grupos, con cada grupo que contiene los elementos desde el mismo día.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-136">The intent might be to organize the results into groups, with each group containing items from the same day.</span></span> <span data-ttu-id="2a5f4-137">Sin embargo, agrupación examina el valor completo, que incluye la hora.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-137">However, grouping looks at the entire value, which includes the time.</span></span> 

<span data-ttu-id="2a5f4-138">El resultado final es que se va a agrupar los elementos para que los elementos recibidos al mismo tiempo, hacia abajo hasta la segunda, estén en sus propios grupos.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-138">The end result is that the items will be grouped so that items received at the same time, down to the second, are in their own groups.</span></span> <span data-ttu-id="2a5f4-139">Los resultados se ordenarán más probable es que en un gran número de grupos con un pequeño número de elementos de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-139">The results will most likely be sorted into a large number of groups with a small number of items in each group.</span></span> 
  
<span data-ttu-id="2a5f4-140">Para obtener un conjunto con un menor número de grupos y un número mayor de elementos de cada grupo de resultados, elija una propiedad que es probable que tenga una cantidad más pequeña de valores, como [EmailMessage.From](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) o [Item.Categories](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) en la API administrada de EWS, o [desde](http://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) o de [categorías](http://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-140">To get a results set with a smaller number of groups and a larger number of items in each group, choose a property that is likely to have a smaller number of values, such as [EmailMessage.From](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) or [Item.Categories](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) in the EWS Managed API, or [From](http://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) or [Categories](http://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) in EWS.</span></span> <span data-ttu-id="2a5f4-141">En la siguiente figura se muestra una lista de mensajes de correo electrónico que aparecen en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-141">The following figure shows a list of emails that appear in an Inbox.</span></span> 
  
<span data-ttu-id="2a5f4-142">**En la figura 1. Mensajes en una bandeja de entrada**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-142">**Figure 1. Messages in an Inbox**</span></span>

![Muestra de una lista de mensajes en la bandeja de entrada de un usuario.](media/Ex15_GroupedSearch_MsgList.png)
  
<span data-ttu-id="2a5f4-144">Si agrupa los elementos en la figura 1 por la propiedad **EmailMessage.From** , el resultado será dos grupos, uno para los mensajes enviados por espero bruto y otro para los mensajes enviados por Sadie Daniels.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-144">If you group the items in Figure 1 by the **EmailMessage.From** property, the result will be two groups, one for messages sent by Hope Gross, and one for messages sent by Sadie Daniels.</span></span> 
  
<span data-ttu-id="2a5f4-145">**La figura 2. Los mensajes se dividen en grupos basados en la propiedad From**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-145">**Figure 2. Messages separated into groups based on the From property**</span></span>

![Una imagen que muestra mensajes ordenados en dos listas por la propiedad De.](media/Ex15_GroupedSearch_SeparateGroups.png)
  
## <a name="sort-the-items-within-groups"></a><span data-ttu-id="2a5f4-147">Ordenar los elementos dentro de los grupos</span><span class="sxs-lookup"><span data-stu-id="2a5f4-147">Sort the items within groups</span></span>
<span data-ttu-id="2a5f4-148"><a name="bk_SortItems"> </a></span><span class="sxs-lookup"><span data-stu-id="2a5f4-148"></span></span>

<span data-ttu-id="2a5f4-149">Puede controlar cómo se ordenan los elementos dentro de cada grupo mediante el uso de la propiedad [ItemView.OrderBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) en la API administrada de EWS, o el elemento de [SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-149">You can control how items are sorted within each group by using the [ItemView.OrderBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="2a5f4-150">El mismo orden se aplica a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-150">The same ordering applies to each group.</span></span> <span data-ttu-id="2a5f4-151">Por ejemplo, si ordena los elementos de la figura 1 por la propiedad **Item.DateTimeReceived** , en orden descendente, el elemento recibido más recientemente de espero bruto será la primero en el grupo de salto bruto y será el elemento recibido más recientemente de Sadie Daniels en primer lugar en el grupo Sadie Daniels.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-151">For example, if you sort the items from Figure 1 by the **Item.DateTimeReceived** property, in descending order, the item most recently received from Hope Gross will be first in the Hope Gross group, and the item most recently received from Sadie Daniels will be first in the Sadie Daniels group.</span></span> <span data-ttu-id="2a5f4-152">Para su comodidad, los grupos en la figura 2 ya están ordenados de esta forma.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-152">Conveniently, the groups in Figure 2 are already sorted this way.</span></span> 
  
## <a name="sort-the-groups"></a><span data-ttu-id="2a5f4-153">Ordenar los grupos</span><span class="sxs-lookup"><span data-stu-id="2a5f4-153">Sort the groups</span></span>
<span data-ttu-id="2a5f4-154"><a name="bk_SortGroups"> </a></span><span class="sxs-lookup"><span data-stu-id="2a5f4-154"></span></span>

<span data-ttu-id="2a5f4-155">Ahora que tiene los grupos que establecen, el último paso es ordenar los propios grupos.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-155">Now that you have your groups settled, the final step is sorting the groups themselves.</span></span> <span data-ttu-id="2a5f4-156">Debido a que los propios grupos no tienen ningún valores específicos, el proceso de agrupación tiene que asignar un valor de ordenación a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-156">Because the groups themselves have no specific values, the grouping process has to assign a sort value to each group.</span></span> <span data-ttu-id="2a5f4-157">Esto se realiza mediante la agregación de los valores de una propiedad concreta dentro de cada grupo, especificado por la propiedad [Grouping.AggregateOn](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) en la API administrada de EWS, o el elemento [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) como un elemento secundario del elemento [AggregateOn](http://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) en EWS.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-157">This is done by aggregation of the values of a specific property within each group, specified by the [Grouping.AggregateOn](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [AggregateOn](http://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="2a5f4-158">La propiedad [Grouping.AggregateType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) en la API administrada de EWS (o el atributo **agregado** en el elemento **AggregateOn** en EWS) especifica qué valor de los elementos dentro de cada grupo se asigna al valor de ordenación para el grupo, puede ser el mayor valor o el valor más pequeño.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-158">The [Grouping.AggregateType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) property in the EWS Managed API (or the **Aggregate** attribute on the **AggregateOn** element in EWS) specifies which value from the items within each group is assigned to the sort value for the group — either the largest value or the smallest value.</span></span> <span data-ttu-id="2a5f4-159">Por último, el criterio de ordenación (ascendente o descendente) se especifica mediante la propiedad [Grouping.SortDirection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) en la API administrada de EWS, o el atributo de **orden** en el elemento [GroupBy](http://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) EWS.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-159">Finally, the sort order (descending or ascending) is specified by the [Grouping.SortDirection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) property in the EWS Managed API, or the **Order** attribute on the [GroupBy](http://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element in EWS.</span></span> 
  
<span data-ttu-id="2a5f4-160">Por ejemplo, si se ordenan los grupos de la figura 2 agregando en la propiedad **Item.DateTimeReceived** , utilizando el valor más pequeño y ordenar en orden descendente, los elementos se devuelven en el orden en que se muestra en la figura 3.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-160">For example, if the groups from Figure 2 are sorted by aggregating on the **Item.DateTimeReceived** property, using the smallest value, and sorting in descending order, the items are returned in the order in shown Figure 3.</span></span> 
  
<span data-ttu-id="2a5f4-161">**La figura 3. Resultados de búsqueda agrupados con los grupos ordenados por la propiedad DateTimeReceived**</span><span class="sxs-lookup"><span data-stu-id="2a5f4-161">**Figure 3. Grouped search results with the groups sorted by the DateTimeReceived property**</span></span>

![Una imagen que muestra una lista ordenada de mensajes, agrupados por la propiedad De, con los grupos ordenados por la fecha y hora de recepción más antigua.](media/Ex15_GroupedSearch_Results.png)
  
<span data-ttu-id="2a5f4-163">Las secciones siguientes muestran cómo es posible que extraen de agrupación y ordenación juntos en el código.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-163">The next sections show you how you might pull grouping and sorting together in code.</span></span>
  
## <a name="example-perform-a-grouped-search-by-using-the-ews-managed-api"></a><span data-ttu-id="2a5f4-164">Ejemplo: Realizar una búsqueda agrupada mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="2a5f4-164">Example: Perform a grouped search by using the EWS Managed API</span></span>
<span data-ttu-id="2a5f4-165"><a name="bk_GroupSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="2a5f4-165"></span></span>

<span data-ttu-id="2a5f4-166">Pueden utilizar la agrupación de los siguientes métodos de la API administrada de EWS:</span><span class="sxs-lookup"><span data-stu-id="2a5f4-166">The following EWS Managed API methods can use grouping:</span></span>
  
- [<span data-ttu-id="2a5f4-167">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="2a5f4-167">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2a5f4-168">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="2a5f4-168">Folder.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="2a5f4-169">En el ejemplo siguiente se utiliza el método **ExchangeService.FindItems** ; Sin embargo, las mismas reglas y los conceptos se aplican al método **Folder.FindItems** .</span><span class="sxs-lookup"><span data-stu-id="2a5f4-169">The following example uses the **ExchangeService.FindItems** method; however, the same rules and concepts apply to the **Folder.FindItems** method.</span></span> <span data-ttu-id="2a5f4-170">En este ejemplo, se define un método denominado **GroupItemsByFrom** .</span><span class="sxs-lookup"><span data-stu-id="2a5f4-170">In this example, a method called **GroupItemsByFrom** is defined.</span></span> <span data-ttu-id="2a5f4-171">Toma un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) y un objeto [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) como parámetros.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-171">It takes an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and a [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object as parameters.</span></span> <span data-ttu-id="2a5f4-172">Solicita los 50 primeros elementos en la carpeta, agrupadas por la propiedad **EmailMessage.From** , ordenada por la propiedad **Item.DateTimeReceived** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-172">It requests the first 50 items in the folder, grouped by the **EmailMessage.From** property, sorted by the **Item.DateTimeReceived** property in descending order.</span></span> <span data-ttu-id="2a5f4-173">Los grupos se ordenan por el menor valor de la propiedad **Item.DateTimeReceived** en sus elementos, en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-173">The groups themselves are sorted by the smallest **Item.DateTimeReceived** property value on their items, in descending order.</span></span> 
  
<span data-ttu-id="2a5f4-174">En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2a5f4-174">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="example-perform-a-grouped-search-by-using-ews"></a><span data-ttu-id="2a5f4-175">Ejemplo: Realizar una búsqueda agrupada mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="2a5f4-175">Example: Perform a grouped search by using EWS</span></span>
<span data-ttu-id="2a5f4-176"><a name="bk_GroupSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="2a5f4-176"></span></span>

<span data-ttu-id="2a5f4-177">El siguiente ejemplo de solicitud muestra una solicitud de [operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para los 50 primeros elementos en la carpeta, agrupada por el elemento **desde** , ordenado por el elemento **DateTimeReceived** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-177">The following request example shows a [FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request for the first 50 items in the folder, grouped by the **From** element, sorted by the **DateTimeReceived** element in descending order.</span></span> <span data-ttu-id="2a5f4-178">Los grupos se ordenan por el valor más pequeño del elemento **DateTimeReceived** en sus elementos, en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-178">The groups themselves are sorted by the smallest **DateTimeReceived** element value on their items, in descending order.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2a5f4-179">El servidor devuelve la respuesta siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-179">The server returns the following response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
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

## <a name="version-differences"></a><span data-ttu-id="2a5f4-180">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="2a5f4-180">Version differences</span></span>
<span data-ttu-id="2a5f4-181"><a name="bk_VersionDiffs"> </a></span><span class="sxs-lookup"><span data-stu-id="2a5f4-181"></span></span>

<span data-ttu-id="2a5f4-182">Versiones de Exchange con la versión principal 15 iniciales y finales con compilación 15.0.775.38 **grupo de** elementos devueltos (de tipo **GroupedItemsType**) en lugar de [GroupedItems](http://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) elementos en la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-182">Versions of Exchange starting with major version 15 and ending with build 15.0.775.38 return **Group** elements (of type **GroupedItemsType**) in place of [GroupedItems](http://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) elements in the SOAP response.</span></span> <span data-ttu-id="2a5f4-183">Si está utilizando la API administrada de EWS, esto hará que la colección [GroupedFindItemsResults.ItemGroups](http://msdn.microsoft.com/en-us/library/office/dd633961%28v=exchg.80%29.aspx) que se va a contener objetos 0.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-183">If you are using the EWS Managed API, this will cause the [GroupedFindItemsResults.ItemGroups](http://msdn.microsoft.com/en-us/library/office/dd633961%28v=exchg.80%29.aspx) collection to contain 0 objects.</span></span> <span data-ttu-id="2a5f4-184">Si usa EWS, elementos de **grupo** deben controlarse como elementos de **GroupedItems** .</span><span class="sxs-lookup"><span data-stu-id="2a5f4-184">If you are using EWS, **Group** elements should be handled as **GroupedItems** elements.</span></span> 
  
<span data-ttu-id="2a5f4-185">Las versiones de Exchange a partir de la versión principal 15 devuelven elementos de **grupo** o **GroupedItems** adicionales con el atributo **xsi: nil** establecido en **true** en la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-185">Versions of Exchange starting with major version 15 return extra **Group** or **GroupedItems** elements with the **xsi:nil** attribute set to **true** in the SOAP response.</span></span> <span data-ttu-id="2a5f4-186">Si está utilizando la API administrada de EWS, estos elementos adicionales provocará un [ServiceXmlDeserializationException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) que se inicie.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-186">If you are using the EWS Managed API, these extra elements will cause a [ServiceXmlDeserializationException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) to be thrown.</span></span> <span data-ttu-id="2a5f4-187">Si usa EWS, se deben omitir estos elementos adicionales.</span><span class="sxs-lookup"><span data-stu-id="2a5f4-187">If you are using EWS, these extra elements should be ignored.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a5f4-188">Ver también</span><span class="sxs-lookup"><span data-stu-id="2a5f4-188">See also</span></span>

- [<span data-ttu-id="2a5f4-189">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2a5f4-189">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="2a5f4-190">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="2a5f4-190">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="2a5f4-191">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="2a5f4-191">Folder.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)   
- [<span data-ttu-id="2a5f4-192">Clase de agrupación</span><span class="sxs-lookup"><span data-stu-id="2a5f4-192">Grouping class</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="2a5f4-193">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="2a5f4-193">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    


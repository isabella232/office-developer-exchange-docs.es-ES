---
title: Realizar búsquedas paginadas utilizando EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Descubra cómo realizar búsquedas paginadas en su API administrada de EWS o en la aplicación EWS destinada a Exchange.
localization_priority: Priority
ms.openlocfilehash: fa36a2ce77150f29e5a62876138c9693a3b4ab1f
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348825"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="236ae-103">Realizar búsquedas paginadas utilizando EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="236ae-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="236ae-104">Descubra cómo realizar búsquedas paginadas en su API administrada de EWS o en la aplicación EWS destinada a Exchange.</span><span class="sxs-lookup"><span data-stu-id="236ae-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="236ae-105">La paginación es una función de EWS que le permite controlar el tamaño de los resultados de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="236ae-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="236ae-106">En lugar de recuperar el conjunto de resultados completo en una respuesta de EWS, puede recuperar conjuntos más pequeños en varias respuestas de EWS.</span><span class="sxs-lookup"><span data-stu-id="236ae-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="236ae-107">Por ejemplo, imagine que un usuario tiene 10 000 mensajes de correo electrónico en su bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="236ae-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="236ae-108">Hipotéticamente, podría recuperar los 10 000 mensajes de correo electrónico en una respuesta muy grande, pero es posible que desee dividir los resultados en partes más manejables por razones de ancho de banda o rendimiento.</span><span class="sxs-lookup"><span data-stu-id="236ae-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="236ae-109">La paginación proporciona las herramientas necesarias para hacer precisamente eso.</span><span class="sxs-lookup"><span data-stu-id="236ae-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="236ae-110">Si bien hipotéticamente puede recuperar 10 000 elementos en una solicitud, en realidad, esto es poco probable debido a la limitación de EWS.</span><span class="sxs-lookup"><span data-stu-id="236ae-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="236ae-111">Para obtener más información, consulte [Limitación de EWS en Exchange](ews-throttling-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="236ae-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="236ae-112">**Tabla 1. Parámetros de paginación en la API administrada de EWS y EWS**</span><span class="sxs-lookup"><span data-stu-id="236ae-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="236ae-113">**Para configurar o recuperar el…**</span><span class="sxs-lookup"><span data-stu-id="236ae-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="236ae-114">**En la API administrada de EWS, use…**</span><span class="sxs-lookup"><span data-stu-id="236ae-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="236ae-115">**En EWS, use…**</span><span class="sxs-lookup"><span data-stu-id="236ae-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="236ae-116">Número máximo de elementos o carpetas en una respuesta</span><span class="sxs-lookup"><span data-stu-id="236ae-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="236ae-117">Parámetro **pageSize** para el [constructor ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) o el [constructor FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-117">The **pageSize** parameter to the [ItemView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="236ae-118">O bien</span><span class="sxs-lookup"><span data-stu-id="236ae-118">Or</span></span>  <br/> <span data-ttu-id="236ae-119">Propiedad [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-119">The [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="236ae-120">Atributo **MaxEntriesReturned** en el elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o el elemento [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="236ae-121">Punto de partida en la lista de elementos o carpetas</span><span class="sxs-lookup"><span data-stu-id="236ae-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="236ae-122">Parámetro **offsetBasePoint** para el constructor **ItemView** o el constructor **FolderView**</span><span class="sxs-lookup"><span data-stu-id="236ae-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="236ae-123">O bien</span><span class="sxs-lookup"><span data-stu-id="236ae-123">Or</span></span>  <br/> <span data-ttu-id="236ae-124">Propiedad [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-124">The [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="236ae-125">Atributo **BasePoint** en el elemento **IndexedPageItemView** o el elemento **IndexedPageFolderView**</span><span class="sxs-lookup"><span data-stu-id="236ae-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="236ae-126">Desplazamiento desde el punto de partida</span><span class="sxs-lookup"><span data-stu-id="236ae-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="236ae-127">Parámetro **offset** para el constructor **ItemView** o el constructor **FolderView**</span><span class="sxs-lookup"><span data-stu-id="236ae-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="236ae-128">O bien</span><span class="sxs-lookup"><span data-stu-id="236ae-128">Or</span></span>  <br/> <span data-ttu-id="236ae-129">Propiedad [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-129">The [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="236ae-130">Atributo **Offset** en el elemento **IndexedPageItemView** o el elemento **IndexedPageFolderView**</span><span class="sxs-lookup"><span data-stu-id="236ae-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="236ae-131">Número total de resultados en el servidor</span><span class="sxs-lookup"><span data-stu-id="236ae-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="236ae-132">Propiedad [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) o propiedad [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-132">The [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="236ae-133">Atributo **TotalItemsInView** en el elemento [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) o el elemento [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="236ae-134">Desplazamiento del primer elemento o carpeta no incluidos en la respuesta actual</span><span class="sxs-lookup"><span data-stu-id="236ae-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="236ae-135">Propiedad [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) o propiedad [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-135">The [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="236ae-136">Atributo **IndexedPagingOffset** en el elemento **RootFolder**</span><span class="sxs-lookup"><span data-stu-id="236ae-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="236ae-137">Indicador de que la respuesta incluye el último elemento o carpeta de la lista</span><span class="sxs-lookup"><span data-stu-id="236ae-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="236ae-138">Propiedad [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) o propiedad [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ae-138">The [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="236ae-139">Atributo **IncludesLastItemInRange** en el elemento **RootFolder**</span><span class="sxs-lookup"><span data-stu-id="236ae-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="236ae-140">Cómo funciona la paginación</span><span class="sxs-lookup"><span data-stu-id="236ae-140">How paging works</span></span>
<span data-ttu-id="236ae-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="236ae-141"><a name="bk_HowPagingWorks"> </a></span></span>

<span data-ttu-id="236ae-142">Para comprender cómo funciona la paginación, es útil visualizar los mensajes en una carpeta como vallas publicitarias alineadas una al lado de la otra en una explanada.</span><span class="sxs-lookup"><span data-stu-id="236ae-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="236ae-143">Imagine que puede ver algunas de estas vallas publicitarias a través de una ventana mágica.</span><span class="sxs-lookup"><span data-stu-id="236ae-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="236ae-144">Puede cambiar el tamaño de la ventana (para ver más o menos vallas publicitarias a la vez) y mover la ventana (para controlar qué vallas publicitarias puede ver).</span><span class="sxs-lookup"><span data-stu-id="236ae-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="236ae-145">Esta manipulación de la ventana es como la paginación.</span><span class="sxs-lookup"><span data-stu-id="236ae-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="236ae-146">Cuando envía su solicitud al servidor Exchange, especifica el tamaño de su ventana indicando cuántos artículos quiere que se devuelvan.</span><span class="sxs-lookup"><span data-stu-id="236ae-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="236ae-147">La posición de la ventana se establece especificando un punto de inicio (ya sea el comienzo de la línea o el final de la línea) y un desplazamiento desde ese punto de inicio, que se expresa como número de elementos.</span><span class="sxs-lookup"><span data-stu-id="236ae-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="236ae-148">El comienzo de la ventana es el número de elementos que especifica el desplazamiento desde el punto de inicio.</span><span class="sxs-lookup"><span data-stu-id="236ae-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="236ae-149">Donde la paginación se vuelve un poco más interesante es en la respuesta del servidor y en la manera en la que su aplicación puede usar esa respuesta para dar forma a su próxima solicitud.</span><span class="sxs-lookup"><span data-stu-id="236ae-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="236ae-150">El servidor le proporciona tres datos que puede utilizar para determinar cómo configurar su "ventana" para su próxima solicitud:</span><span class="sxs-lookup"><span data-stu-id="236ae-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="236ae-151">Si los resultados de la respuesta incluyen o no el último elemento del conjunto de resultados general en el servidor.</span><span class="sxs-lookup"><span data-stu-id="236ae-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="236ae-152">El número total de elementos del conjunto de resultados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="236ae-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="236ae-153">Cuál debería ser el siguiente valor del desplazamiento, si desea avanzar su ventana al siguiente elemento del conjunto de resultados que no se incluya en la respuesta actual.</span><span class="sxs-lookup"><span data-stu-id="236ae-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="236ae-154">Veamos un ejemplo sencillo.</span><span class="sxs-lookup"><span data-stu-id="236ae-154">Let's look at a simple example.</span></span> <span data-ttu-id="236ae-155">Imagine una bandeja de entrada con 15 mensajes.</span><span class="sxs-lookup"><span data-stu-id="236ae-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="236ae-156">Su aplicación envía una solicitud inicial para recuperar un máximo de 10 elementos, comenzando por el principio de la lista de mensajes (por lo que el desplazamiento es cero).</span><span class="sxs-lookup"><span data-stu-id="236ae-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="236ae-157">El servidor responde con los primeros 10 mensajes e indica que la respuesta no incluye el último elemento, que hay un total de 15 elementos y que el próximo desplazamiento debe ser 10.</span><span class="sxs-lookup"><span data-stu-id="236ae-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="236ae-158">**Ilustración 1. Solicitud de 10 elementos en el desplazamiento 0 del comienzo de una lista de 15 elementos**</span><span class="sxs-lookup"><span data-stu-id="236ae-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![Un diagrama que muestra los resultados de solicitar 10 elementos en el desplazamiento 0 desde el comienzo de una lista de 15 elementos.](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="236ae-160">Luego, su aplicación reenvía la misma solicitud al servidor, con la única diferencia de que el desplazamiento es ahora 10.</span><span class="sxs-lookup"><span data-stu-id="236ae-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="236ae-161">El servidor devuelve los últimos cinco elementos e indica que la respuesta incluye el último elemento, que hay un total de 15 elementos y que el próximo desplazamiento debe ser 15 (aunque, obviamente, como ha llegado al final, no habrá un próximo desplazamiento).</span><span class="sxs-lookup"><span data-stu-id="236ae-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="236ae-162">**Ilustración 2. Solicitud de 10 elementos en el desplazamiento 10 del principio de una lista de 15 elementos**</span><span class="sxs-lookup"><span data-stu-id="236ae-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![Diagrama que muestra los resultados de solicitar 10 elementos en el desplazamiento 10 desde el comienzo de una lista de 15 elementos.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="236ae-164">Consideraciones de diseño para la paginación</span><span class="sxs-lookup"><span data-stu-id="236ae-164">Design considerations for paging</span></span>
<span data-ttu-id="236ae-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="236ae-165"><a name="bk_DesignConsiderations"> </a></span></span>

<span data-ttu-id="236ae-166">Aprovechar al máximo la paginación en su aplicación requiere tener en cuenta ciertos aspectos.</span><span class="sxs-lookup"><span data-stu-id="236ae-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="236ae-167">Por ejemplo, ¿cuál será el tamaño de su "ventana"?</span><span class="sxs-lookup"><span data-stu-id="236ae-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="236ae-168">¿Qué hará si los resultados en el servidor cambian mientras mueve su "ventana"?</span><span class="sxs-lookup"><span data-stu-id="236ae-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="236ae-169">Determinar el tamaño de su ventana</span><span class="sxs-lookup"><span data-stu-id="236ae-169">Determine the size of your window</span></span>

<span data-ttu-id="236ae-170">No existe un número máximo de entradas "único" que todas las aplicaciones deban utilizar.</span><span class="sxs-lookup"><span data-stu-id="236ae-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="236ae-171">Determinar el número adecuado para su aplicación depende de varios factores.</span><span class="sxs-lookup"><span data-stu-id="236ae-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="236ae-172">Sin embargo, es útil tener en cuenta las siguientes pautas:</span><span class="sxs-lookup"><span data-stu-id="236ae-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="236ae-173">De forma predeterminada, Exchange establece que el número máximo de artículos que se pueden devolver en una sola solicitud sea 1000.</span><span class="sxs-lookup"><span data-stu-id="236ae-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="236ae-174">Establecer el número máximo de entradas en un número mayor da como resultado tener que enviar menos solicitudes para obtener todos los elementos, pero se deberá esperar más tiempo para obtener respuestas.</span><span class="sxs-lookup"><span data-stu-id="236ae-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="236ae-175">Establecer el número máximo de entradas en un número menor da como resultado tiempos de respuesta más rápidos, pero implica enviar más solicitudes para obtener todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="236ae-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="236ae-176">Gestionar cambios en el conjunto de resultados</span><span class="sxs-lookup"><span data-stu-id="236ae-176">Handling changes to the result set</span></span>

<span data-ttu-id="236ae-177">En el ejemplo simple de este artículo, el número de elementos en la bandeja de entrada del usuario se mantuvo constante.</span><span class="sxs-lookup"><span data-stu-id="236ae-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="236ae-178">Sin embargo, en realidad, la cantidad de elementos de una bandeja de entrada puede cambiar con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="236ae-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="236ae-179">Pueden llegar nuevos mensajes y los elementos se pueden eliminar o mover en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="236ae-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="236ae-180">Pero, ¿cómo afecta esto a la paginación?</span><span class="sxs-lookup"><span data-stu-id="236ae-180">But how does this impact paging?</span></span> <span data-ttu-id="236ae-181">Modifiquemos el escenario de ejemplo anterior para averiguarlo.</span><span class="sxs-lookup"><span data-stu-id="236ae-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="236ae-182">Comenzaremos de nuevo con los 15 elementos de la bandeja de entrada del usuario y enviaremos la misma solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="236ae-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="236ae-183">Como antes, el servidor responde con los primeros 10 mensajes e indica que la respuesta no incluye el último elemento, que hay un total de 15 elementos y que el siguiente desplazamiento debe ser 10, como se muestra en la ilustración 1.</span><span class="sxs-lookup"><span data-stu-id="236ae-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="236ae-184">Ahora, mientras su aplicación procesa esos 10 elementos, llega un nuevo mensaje a la bandeja de entrada y se agrega al conjunto de resultados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="236ae-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="236ae-185">Su aplicación reenvía la misma solicitud al servidor (solo con el desplazamiento establecido en 10).</span><span class="sxs-lookup"><span data-stu-id="236ae-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="236ae-186">Esta vez, el servidor recupera 6 elementos e indica que hay un total de 16 elementos en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="236ae-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="236ae-187">En este punto, es posible que se pregunte si esto es un problema.</span><span class="sxs-lookup"><span data-stu-id="236ae-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="236ae-188">Después de todo, obtuvo 16 elementos en las dos respuestas, así que ¿por qué podría ser esto un problema?</span><span class="sxs-lookup"><span data-stu-id="236ae-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="236ae-189">La respuesta depende de en qué lugar de la lista se coloque el nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="236ae-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="236ae-190">Si la lista está ordenada de modo que los elementos más antiguos (por fecha/hora de recepción) sean los primeros, no hay motivo de preocupación en este escenario.</span><span class="sxs-lookup"><span data-stu-id="236ae-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="236ae-191">El nuevo elemento se colocará al final de la lista y se incluirá en la segunda respuesta.</span><span class="sxs-lookup"><span data-stu-id="236ae-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="236ae-192">**Ilustración 3. Solicitud de 10 elementos en el desplazamiento 10 desde el principio de una lista de 16 elementos, siendo nuevo el elemento 16 de la lista**</span><span class="sxs-lookup"><span data-stu-id="236ae-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![Diagrama que muestra los resultados de solicitar 10 elementos en el desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento 16 se agregó al final de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="236ae-194">Si la lista está ordenada para que los elementos más nuevos sean los primeros, cambia la historia.</span><span class="sxs-lookup"><span data-stu-id="236ae-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="236ae-195">En este caso, el primer elemento de la segunda solicitud sería el último elemento de la solicitud anterior más los cinco elementos restantes de los 15 originales.</span><span class="sxs-lookup"><span data-stu-id="236ae-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="236ae-196">Para decirlo en términos de nuestra ventana mágica imaginaria, cambió su ventana 10 posiciones, pero las vallas publicitarias también avanzaron una posición.</span><span class="sxs-lookup"><span data-stu-id="236ae-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="236ae-197">**Ilustración 4. Solicitud de 10 elementos en el desplazamiento 10 desde el principio de una lista de 16 elementos, siendo nuevo el primer elemento de la lista**</span><span class="sxs-lookup"><span data-stu-id="236ae-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento número 16 se agregó al comienzo de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="236ae-199">Una forma de detectar un cambio en los resultados en el servidor es utilizar el concepto de elemento delimitador.</span><span class="sxs-lookup"><span data-stu-id="236ae-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="236ae-200">Un elemento delimitador es un elemento adicional en su respuesta que no se procesa junto con el resto de los resultados, pero se utiliza para realizar una comparación con los siguientes resultados para ver si los elementos han cambiado.</span><span class="sxs-lookup"><span data-stu-id="236ae-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="236ae-201">Volviendo a nuestro ejemplo simple, si su aplicación utiliza un tamaño de "ventana" de 10, en realidad establece que el número máximo de elementos que se pueda devolver sea 11.</span><span class="sxs-lookup"><span data-stu-id="236ae-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="236ae-202">Su aplicación procesa los primeros 10 elementos de la respuesta como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="236ae-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="236ae-203">Para el último elemento, guarde el identificador del elemento como delimitador y, luego, emita la siguiente solicitud con un desplazamiento de 10.</span><span class="sxs-lookup"><span data-stu-id="236ae-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="236ae-204">Si los datos no han cambiado, el primer elemento de la segunda respuesta deberá tener un identificador de elemento que coincida con el delimitador.</span><span class="sxs-lookup"><span data-stu-id="236ae-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="236ae-205">Si los identificadores de elemento no coinciden, sabrá que los datos se han eliminado o insertado en las partes de la lista en las que ya ha aplicado la paginación.</span><span class="sxs-lookup"><span data-stu-id="236ae-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="236ae-206">Incluso aunque sepa que los datos han cambiado, deberá decidir cómo actuar en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="236ae-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="236ae-207">Tampoco existe una respuesta única a esta pregunta.</span><span class="sxs-lookup"><span data-stu-id="236ae-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="236ae-208">Sus acciones dependerán de su tipo de aplicación y de lo importante que sea capturar todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="236ae-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="236ae-209">Puede ignorar los cambios por completo, reiniciar el proceso desde el principio o retroceder e intentar detectar dónde se produjo el cambio.</span><span class="sxs-lookup"><span data-stu-id="236ae-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="236ae-210">Ejemplo: realizar una búsqueda paginada mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="236ae-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="236ae-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="236ae-211"><a name="bk_PagedSearchEWSMA"> </a></span></span>

<span data-ttu-id="236ae-212">La paginación es compatible con los siguientes métodos de API administrada de EWS:</span><span class="sxs-lookup"><span data-stu-id="236ae-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="236ae-213">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="236ae-213">ExchangeService.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="236ae-214">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="236ae-214">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="236ae-215">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="236ae-215">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="236ae-216">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="236ae-216">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="236ae-217">Si utiliza la API administrada de EWS, su aplicación configurará la paginación con la clase [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) o [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) y recibirá información del servidor con respecto a la paginación de la clase [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) o [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="236ae-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="236ae-218">En el siguiente ejemplo se recuperan todos los elementos de una carpeta mediante una búsqueda paginada que devuelve cinco elementos en cada respuesta.</span><span class="sxs-lookup"><span data-stu-id="236ae-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="236ae-219">También se recupera un elemento adicional que sirve como delimitador para detectar cambios en los resultados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="236ae-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="236ae-220">En este ejemplo se asume que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="236ae-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void PageSearchItems(ExchangeService service, WellKnownFolderName folder)
{
    int pageSize = 5;
    int offset = 0;
    // Request one more item than your actual pageSize.
    // This will be used to detect a change to the result
    // set while paging.
    ItemView view = new ItemView(pageSize + 1, offset);
    view.PropertySet = new PropertySet(ItemSchema.Subject);
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    view.Traversal = ItemTraversal.Shallow;
    bool moreItems = true;
    ItemId anchorId = null;
    while (moreItems)
    {
        try
        {
            FindItemsResults<Item> results = service.FindItems(folder, view);
            moreItems = results.MoreAvailable;
            if (moreItems && anchorId != null)
            {
                // Check the first result to make sure it matches
                // the last result (anchor) from the previous page.
                // If it doesn't, that means that something was added
                // or deleted since you started the search.
                if (results.Items.First<Item>().Id != anchorId)
                {
                    Console.WriteLine("The collection has changed while paging. Some results may be missed.");
                }
            }
            if (moreItems)
                view.Offset += pageSize;
                
            anchorId = results.Items.Last<Item>().Id;
            
            // Because you're including an additional item on the end of your results
            // as an anchor, you don't want to display it.
            // Set the number to loop as the smaller value between
            // the number of items in the collection and the page size.
            int displayCount = 0;
            if ((results.MoreAvailable == false && results.Items.Count > pageSize) || (results.Items.Count < pageSize))
            {
                displayCount = results.Items.Count;
            }
            else
            {
                displayCount = pageSize;
            }
            
            for (int i = 0; i < displayCount; i++)
            {
                Item item = results.Items[i];
                Console.WriteLine("Subject: {0}", item.Subject);
                Console.WriteLine("Id: {0}\n", item.Id.ToString());
            }
        }
        catch (Exception ex)
        {
            Console.WriteLine("Exception while paging results: {0}", ex.Message);
        }
    }
}
```

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="236ae-221">Ejemplo: realizar una búsqueda paginada mediante EWS</span><span class="sxs-lookup"><span data-stu-id="236ae-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="236ae-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="236ae-222"><a name="bk_PagedSearchEWS"> </a></span></span>

<span data-ttu-id="236ae-223">La paginación es compatible con las siguientes operaciones de EWS:</span><span class="sxs-lookup"><span data-stu-id="236ae-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="236ae-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="236ae-224">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="236ae-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="236ae-225">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="236ae-226">Si utiliza EWS, su aplicación configurará la paginación con el elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o el elemento [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) y recibirá información del servidor con respecto a la paginación del elemento [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) o del elemento [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="236ae-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="236ae-227">En este ejemplo de solicitud, se enviará una solicitud **FindItem** para un máximo de seis elementos, comenzando con un desplazamiento de cero desde el comienzo de la lista de elementos en la bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="236ae-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
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
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="236ae-228">El servidor devuelve la siguiente respuesta, que contiene seis elementos.</span><span class="sxs-lookup"><span data-stu-id="236ae-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="236ae-229">La respuesta también indica que hay un total de ocho elementos en los resultados del servidor y que el último elemento de la lista de resultados no está presente en esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="236ae-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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
          <m:RootFolder IndexedPagingOffset="6" TotalItemsInView="8" IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Query</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Update</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Planning resources</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Timeline</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>For your perusal</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="236ae-230">En este ejemplo, se envía la misma solicitud, pero esta vez, el atributo **Offset** se cambia a cinco, lo que indica que el servidor debe devolver como máximo seis elementos comenzando en el desplazamiento cinco desde el principio.</span><span class="sxs-lookup"><span data-stu-id="236ae-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
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
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="5" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="236ae-231">El servidor envía la siguiente respuesta, que contiene tres elementos.</span><span class="sxs-lookup"><span data-stu-id="236ae-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="236ae-232">La respuesta también indica que el número total de elementos de los resultados en el servidor sigue siendo ocho y que el último elemento de la lista de resultados se incluye en esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="236ae-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>This cat is hilarious!</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="236ae-233">Vea también</span><span class="sxs-lookup"><span data-stu-id="236ae-233">See also</span></span>


- [<span data-ttu-id="236ae-234">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="236ae-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="236ae-235">Método ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="236ae-235">ExchangeService.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="236ae-236">Método ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="236ae-236">ExchangeService.FindItems method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="236ae-237">Método Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="236ae-237">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="236ae-238">Método Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="236ae-238">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="236ae-239">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="236ae-239">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="236ae-240">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="236ae-240">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="236ae-241">Limitación de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="236ae-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    


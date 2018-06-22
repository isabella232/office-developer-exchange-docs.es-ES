---
title: Realizar búsquedas paginadas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Encuentre información acerca de cómo realizar búsquedas paginadas en la API administrada de EWS o aplicación de EWS dirigido a Exchange.
ms.openlocfilehash: 3f82f46d0582b0b7ff8be63de8a7054b5f3cacab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763154"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="701b1-103">Realizar búsquedas paginadas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="701b1-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="701b1-104">Encuentre información acerca de cómo realizar búsquedas paginadas en la API administrada de EWS o aplicación de EWS dirigido a Exchange.</span><span class="sxs-lookup"><span data-stu-id="701b1-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="701b1-105">Paginación es una característica de EWS que le permite controlar el tamaño de los resultados de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="701b1-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="701b1-106">En lugar de recuperar el completo conjunto de resultados en una respuesta EWS, puede recuperar conjuntos más pequeños en varias respuestas EWS.</span><span class="sxs-lookup"><span data-stu-id="701b1-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="701b1-107">Por ejemplo, considere la posibilidad de un usuario con 10.000 mensajes de correo electrónico en su Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="701b1-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="701b1-108">En teoría, podría recuperar todos los correos 10.000 electrónicos en una respuesta muy grande, pero es posible que desee dividir en fragmentos más manejables por motivos de rendimiento o ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="701b1-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="701b1-109">Paginación le ofrece las herramientas necesarias para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="701b1-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="701b1-110">Mientras teoría puede recuperar 10.000 elementos en una sola solicitud, en realidad, esto es poco probable debido a la limitación de EWS.</span><span class="sxs-lookup"><span data-stu-id="701b1-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="701b1-111">Para obtener más información, vea la [limitación de EWS en Exchange](ews-throttling-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="701b1-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="701b1-112">**La tabla 1. Parámetros de paginación en la API administrada de EWS y EWS**</span><span class="sxs-lookup"><span data-stu-id="701b1-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="701b1-113">**Para configurar o recuperar la...**</span><span class="sxs-lookup"><span data-stu-id="701b1-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="701b1-114">**En la API administrada de EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="701b1-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="701b1-115">**En EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="701b1-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="701b1-116">Número máximo de elementos o carpetas en una respuesta</span><span class="sxs-lookup"><span data-stu-id="701b1-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="701b1-117">El parámetro **pageSize** para el [constructor artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) o el [constructor FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-117">The **pageSize** parameter to the [ItemView constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="701b1-118">O</span><span class="sxs-lookup"><span data-stu-id="701b1-118">Or</span></span>  <br/> <span data-ttu-id="701b1-119">La propiedad [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-119">The [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="701b1-120">El atributo **MaxEntriesReturned** en el elemento [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o el elemento [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="701b1-121">Punto de inicio en la lista de elementos o carpetas</span><span class="sxs-lookup"><span data-stu-id="701b1-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="701b1-122">El parámetro **offsetBasePoint** para el constructor **artículoVer** o el constructor **FolderView**</span><span class="sxs-lookup"><span data-stu-id="701b1-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="701b1-123">O</span><span class="sxs-lookup"><span data-stu-id="701b1-123">Or</span></span>  <br/> <span data-ttu-id="701b1-124">La propiedad [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-124">The [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="701b1-125">El atributo de **punto base** en el elemento **IndexedPageItemView** o el elemento **IndexedPageFolderView**</span><span class="sxs-lookup"><span data-stu-id="701b1-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="701b1-126">Desplazamiento desde el punto de partida</span><span class="sxs-lookup"><span data-stu-id="701b1-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="701b1-127">El parámetro **offset** para el constructor **artículoVer** o el constructor **FolderView**</span><span class="sxs-lookup"><span data-stu-id="701b1-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="701b1-128">O</span><span class="sxs-lookup"><span data-stu-id="701b1-128">Or</span></span>  <br/> <span data-ttu-id="701b1-129">La propiedad [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-129">The [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="701b1-130">El atributo de **desplazamiento** en el elemento **IndexedPageItemView** o el elemento **IndexedPageFolderView**</span><span class="sxs-lookup"><span data-stu-id="701b1-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="701b1-131">Número total de resultados en el servidor</span><span class="sxs-lookup"><span data-stu-id="701b1-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="701b1-132">La propiedad [FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-132">The [FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="701b1-133">El atributo **TotalItemsInView** en el elemento [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) o el elemento [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="701b1-134">Desplazamiento del primer elemento o carpeta no incluida en la respuesta actual</span><span class="sxs-lookup"><span data-stu-id="701b1-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="701b1-135">La propiedad [FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-135">The [FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="701b1-136">El atributo **IndexedPagingOffset** en el elemento **RootFolder**</span><span class="sxs-lookup"><span data-stu-id="701b1-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="701b1-137">Indicador de que la respuesta incluye el último elemento o la carpeta en la lista</span><span class="sxs-lookup"><span data-stu-id="701b1-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="701b1-138">La propiedad [FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="701b1-138">The [FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="701b1-139">El atributo **IncludesLastItemInRange** en el elemento **RootFolder**</span><span class="sxs-lookup"><span data-stu-id="701b1-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="701b1-140">Cómo funciona la paginación</span><span class="sxs-lookup"><span data-stu-id="701b1-140">How paging works</span></span>
<span data-ttu-id="701b1-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="701b1-141"></span></span>

<span data-ttu-id="701b1-142">Para comprender cómo funciona la paginación, es útil visualizar los mensajes de una carpeta como mensajes alineadas en paralelo en un campo de fuera de su casa.</span><span class="sxs-lookup"><span data-stu-id="701b1-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="701b1-143">Puede ver algunos de estos mensajes a través de una ventana mágica.</span><span class="sxs-lookup"><span data-stu-id="701b1-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="701b1-144">Tiene la posibilidad de cambiar el tamaño de la ventana (para ver más o menos mensajes a la vez) y para mover la ventana (para controlar qué mensajes se puede ver).</span><span class="sxs-lookup"><span data-stu-id="701b1-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="701b1-145">Esta manipulación de la ventana de paginación.</span><span class="sxs-lookup"><span data-stu-id="701b1-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="701b1-146">Al enviar la solicitud al servidor de Exchange, especifique el tamaño de la ventana en términos de número de elementos para devolver.</span><span class="sxs-lookup"><span data-stu-id="701b1-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="701b1-147">Establecer la posición de la ventana mediante la especificación de un punto de partida bien (el principio de la línea) o el final de la línea y un desplazamiento desde ese punto de partida, expresado en un número de elementos.</span><span class="sxs-lookup"><span data-stu-id="701b1-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="701b1-148">El principio de la ventana es el número de elementos especificados por el desplazamiento desde el punto de partida.</span><span class="sxs-lookup"><span data-stu-id="701b1-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="701b1-149">Donde paginación Obtiene un poco más interesante se encuentra en la respuesta del servidor, y cómo la aplicación puede usar esa respuesta a su solicitud siguiente de la forma.</span><span class="sxs-lookup"><span data-stu-id="701b1-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="701b1-150">El servidor le ofrece tres partes de la información que se puede utilizar para determinar cómo configurar su "ventana" para la solicitud siguiente:</span><span class="sxs-lookup"><span data-stu-id="701b1-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="701b1-151">Si los resultados en la respuesta incluyen el último elemento del general conjunto de resultados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="701b1-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="701b1-152">El número total de elementos en el conjunto de resultados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="701b1-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="701b1-153">Lo que el valor de desplazamiento siguiente debe ser, si desea avanzar su ventana hasta el siguiente elemento en el conjunto de resultados que no está incluido en la respuesta actual.</span><span class="sxs-lookup"><span data-stu-id="701b1-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="701b1-154">Veamos un ejemplo sencillo.</span><span class="sxs-lookup"><span data-stu-id="701b1-154">Let's look at a simple example.</span></span> <span data-ttu-id="701b1-155">Imagine una bandeja de entrada con 15 mensajes en ella.</span><span class="sxs-lookup"><span data-stu-id="701b1-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="701b1-156">La aplicación envía una solicitud inicial para recuperar un máximo de 10 elementos, empezando en el principio de la lista de mensajes (de manera que el desplazamiento es cero).</span><span class="sxs-lookup"><span data-stu-id="701b1-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="701b1-157">El servidor responde con los 10 primeros mensajes y se indica que la respuesta no incluye el último elemento, que no hay un total de 15 elementos y que el desplazamiento siguiente debe ser 10.</span><span class="sxs-lookup"><span data-stu-id="701b1-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="701b1-158">**En la figura 1. Solicitud de 10 elementos con un desplazamiento 0 desde el principio de una lista de 15 elementos**</span><span class="sxs-lookup"><span data-stu-id="701b1-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 0 desde el principio de una lista de 15 elementos.](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="701b1-160">A continuación, la aplicación vuelve a enviar la solicitud misma en el servidor, con el único cambio que el desplazamiento es ahora 10.</span><span class="sxs-lookup"><span data-stu-id="701b1-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="701b1-161">El servidor devuelve los últimos cinco elementos y se indica que la respuesta incluye el último elemento, que no hay un total de 15 elementos y que el desplazamiento siguiente debe ser 15 (aunque, por supuesto, ha llegado el final, por lo que no habrá un desplazamiento siguiente.)</span><span class="sxs-lookup"><span data-stu-id="701b1-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="701b1-162">**La figura 2. Solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 15 elementos**</span><span class="sxs-lookup"><span data-stu-id="701b1-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 15 elementos.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="701b1-164">Consideraciones de diseño para la paginación</span><span class="sxs-lookup"><span data-stu-id="701b1-164">Design considerations for paging</span></span>
<span data-ttu-id="701b1-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="701b1-165"></span></span>

<span data-ttu-id="701b1-166">Hacer que el máximo partido de paginación en su aplicación requieren algunos consideración.</span><span class="sxs-lookup"><span data-stu-id="701b1-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="701b1-167">¿Por ejemplo, cómo grande puede hacer que la ventana de""?</span><span class="sxs-lookup"><span data-stu-id="701b1-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="701b1-168">¿Qué hace si cambian los resultados en el servidor mientras se está moviendo su ventana de""?</span><span class="sxs-lookup"><span data-stu-id="701b1-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="701b1-169">Determinar el tamaño de la ventana</span><span class="sxs-lookup"><span data-stu-id="701b1-169">Determine the size of your window</span></span>

<span data-ttu-id="701b1-170">No hay ningún "única" número máximo de entradas que deben usar todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="701b1-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="701b1-171">Determinación del número que es el adecuado para su aplicación depende de varios factores diferentes.</span><span class="sxs-lookup"><span data-stu-id="701b1-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="701b1-172">Sin embargo, es útil para que tenga en cuenta las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="701b1-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="701b1-173">De forma predeterminada, Exchange limita el número máximo de elementos que se pueden devolver en una única solicitud y 1000.</span><span class="sxs-lookup"><span data-stu-id="701b1-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="701b1-174">Si se establece el número máximo de entradas a un mayor número como resultado tener que enviar solicitudes menos para obtener todos los elementos, costo de tener que esperar más tiempo para las respuestas.</span><span class="sxs-lookup"><span data-stu-id="701b1-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="701b1-175">Si se establece el número máximo de entradas a un número como resultado más pequeñas en tiempos de respuesta más rápidos a costa de tener que enviar solicitudes más para obtener todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="701b1-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="701b1-176">Control de cambios para el conjunto de resultados</span><span class="sxs-lookup"><span data-stu-id="701b1-176">Handling changes to the result set</span></span>

<span data-ttu-id="701b1-177">En el ejemplo simple anteriormente en este artículo, el número de elementos en la Bandeja de entrada del usuario se mantuvo constante.</span><span class="sxs-lookup"><span data-stu-id="701b1-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="701b1-178">Sin embargo, en realidad, el número de elementos en una bandeja de entrada puede cambiar con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="701b1-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="701b1-179">Pueden reciben mensajes nuevos y los elementos pueden ser eliminados o movidos en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="701b1-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="701b1-180">Pero ¿cómo este paginación impacto?</span><span class="sxs-lookup"><span data-stu-id="701b1-180">But how does this impact paging?</span></span> <span data-ttu-id="701b1-181">Vamos a modificar el escenario de ejemplo anterior para averiguar.</span><span class="sxs-lookup"><span data-stu-id="701b1-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="701b1-182">Se podrá iniciar de nuevo con los 15 elementos en la Bandeja de entrada del usuario y enviar la misma solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="701b1-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="701b1-183">Como antes, el servidor responde con los 10 primeros mensajes e indica que la respuesta no incluye el último elemento, que no hay un total de 15 elementos y que el desplazamiento siguiente debe ser 10, tal como se muestra en la figura 1.</span><span class="sxs-lookup"><span data-stu-id="701b1-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="701b1-184">Ahora, mientras que la aplicación está procesando esos 10 elementos, un nuevo mensaje llega a la Bandeja de entrada y se agrega al conjunto de resultados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="701b1-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="701b1-185">La aplicación vuelve a enviar la solicitud al servidor misma (sólo con el desplazamiento establecido en 10).</span><span class="sxs-lookup"><span data-stu-id="701b1-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="701b1-186">Esta vez el servidor obtiene back seis elementos e indica que no hay un total de 16 elementos en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="701b1-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="701b1-187">En este momento es posible que se pregunte si esto incluso es un problema.</span><span class="sxs-lookup"><span data-stu-id="701b1-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="701b1-188">Después de todo, obtuvo 16 elementos volver a través de las dos respuestas, ¿por qué todos los elementos innecesarios?</span><span class="sxs-lookup"><span data-stu-id="701b1-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="701b1-189">La respuesta depende de dónde se coloca el nuevo elemento en la lista.</span><span class="sxs-lookup"><span data-stu-id="701b1-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="701b1-190">Si se ordena la lista para que los elementos más antiguos (por fecha/hora de recepción) son primera, no hay ningún motivo de preocupación en este escenario.</span><span class="sxs-lookup"><span data-stu-id="701b1-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="701b1-191">El nuevo elemento se colocará al final de la lista y se incluirá en la segunda respuesta.</span><span class="sxs-lookup"><span data-stu-id="701b1-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="701b1-192">**La figura 3. Solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos, con el elemento número 16 en la lista que se va a nuevo**</span><span class="sxs-lookup"><span data-stu-id="701b1-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento número 16 se agregó al final de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="701b1-194">Si la lista se ordena por lo que los elementos más recientes son primer, es un artículo diferente.</span><span class="sxs-lookup"><span data-stu-id="701b1-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="701b1-195">En este caso, el primer elemento de la segunda solicitud sería el último elemento de la solicitud anterior además de los cinco elementos restantes desde el 15 original.</span><span class="sxs-lookup"><span data-stu-id="701b1-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="701b1-196">Para ponerla en términos de nuestra ventana mágico imaginario, del cambio de posición de la ventana por 10, pero los mensajes a sí mismos también se desplazan por 1.</span><span class="sxs-lookup"><span data-stu-id="701b1-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="701b1-197">**La figura 4. Solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos, con el primer elemento de la lista que se va a nuevo**</span><span class="sxs-lookup"><span data-stu-id="701b1-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento número 16 se agregó al comienzo de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="701b1-199">Una forma de detectar un cambio en los resultados en el servidor es usar el concepto de un elemento delimitador.</span><span class="sxs-lookup"><span data-stu-id="701b1-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="701b1-200">Un elemento delimitador es un elemento adicional en la respuesta que no se procesará junto con el resto de los resultados, pero se usa para comparar con los resultados de la siguiente para ver si han variado los mismos elementos.</span><span class="sxs-lookup"><span data-stu-id="701b1-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="701b1-201">Creación de nuevo en nuestro ejemplo sencillo, si la aplicación usa un tamaño de "ventana de" de 10, establezca el número máximo de elementos para volver a 11 realmente.</span><span class="sxs-lookup"><span data-stu-id="701b1-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="701b1-202">La aplicación procesa los primeros 10 elementos en la respuesta como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="701b1-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="701b1-203">Para el último elemento, guarde el identificador del elemento como un delimitador, a continuación, emitir la siguiente solicitud con un desplazamiento de 10.</span><span class="sxs-lookup"><span data-stu-id="701b1-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="701b1-204">Si no ha cambiado los datos, el primer elemento de la segunda respuesta debe tener un identificador de elemento que coincida con el delimitador.</span><span class="sxs-lookup"><span data-stu-id="701b1-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="701b1-205">Si no coinciden con los identificadores de elemento, sabrá que los datos se haya eliminado o insertado en los elementos de la lista que haya ya "paginar" a través de.</span><span class="sxs-lookup"><span data-stu-id="701b1-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="701b1-206">Incluso cuando se sabe que los datos ha cambiado, necesitará decidir cómo reaccionar.</span><span class="sxs-lookup"><span data-stu-id="701b1-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="701b1-207">O bien no hay una única respuesta a esta pregunta.</span><span class="sxs-lookup"><span data-stu-id="701b1-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="701b1-208">Sus acciones dependerá de la naturaleza de la aplicación y lo importante que es capturar todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="701b1-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="701b1-209">Es posible que pasar por alto por completo, reiniciar el proceso desde el principio, o realizar una copia de seguimiento e intente detectar en que se produjo el cambio.</span><span class="sxs-lookup"><span data-stu-id="701b1-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="701b1-210">Ejemplo: Realizar una búsqueda paginada mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="701b1-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="701b1-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="701b1-211"></span></span>

<span data-ttu-id="701b1-212">Paginación es compatible con los siguientes métodos de la API administrada de EWS:</span><span class="sxs-lookup"><span data-stu-id="701b1-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="701b1-213">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="701b1-213">ExchangeService.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="701b1-214">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="701b1-214">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="701b1-215">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="701b1-215">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="701b1-216">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="701b1-216">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="701b1-217">Si está utilizando la API administrada de EWS, su aplicación configura la paginación con la clase [artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) o [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) y recibe información desde el servidor con respecto a paginación desde el [FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx) o [FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) clase.</span><span class="sxs-lookup"><span data-stu-id="701b1-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="701b1-218">En el ejemplo siguiente se recupera todos los elementos de una carpeta mediante una búsqueda paginada que devuelve cinco elementos en cada respuesta.</span><span class="sxs-lookup"><span data-stu-id="701b1-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="701b1-219">También recupera un elemento adicional para que sirva como un delimitador para detectar cambios en los resultados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="701b1-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="701b1-220">En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="701b1-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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
            if (moreItems &amp;&amp; anchorId != null)
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
            int displayCount = results.Items.Count > pageSize ? pageSize : results.Items.Count;
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

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="701b1-221">Ejemplo: Realizar una búsqueda paginada mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="701b1-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="701b1-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="701b1-222"></span></span>

<span data-ttu-id="701b1-223">Paginación es compatible con las siguientes operaciones de EWS:</span><span class="sxs-lookup"><span data-stu-id="701b1-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="701b1-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="701b1-224">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="701b1-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="701b1-225">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="701b1-226">Si está usando EWS, su aplicación configura la paginación con el elemento [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o el elemento [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) y recibe información desde el servidor con respecto a paginación desde el [() RootFolder FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) el elemento [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) o un elemento.</span><span class="sxs-lookup"><span data-stu-id="701b1-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="701b1-227">En este ejemplo de solicitud, se envía una solicitud de **FindItem** para un máximo de seis elementos, comenzando en un desplazamiento de cero desde el principio de la lista de elementos en la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="701b1-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
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

<span data-ttu-id="701b1-228">El servidor devuelve la respuesta siguiente, que contiene seis elementos.</span><span class="sxs-lookup"><span data-stu-id="701b1-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="701b1-229">La respuesta también indica que no hay un total de ocho elementos en los resultados en el servidor y que el último elemento de la lista de resultados no está presente en esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="701b1-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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

<span data-ttu-id="701b1-230">En este ejemplo, se envía la solicitud de la misma, pero esta vez, el atributo de **desplazamiento** se cambia a cinco, lo que indica que el servidor debería devolver como máximo seis elementos empezando por el desplazamiento cinco desde el principio.</span><span class="sxs-lookup"><span data-stu-id="701b1-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
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

<span data-ttu-id="701b1-231">El servidor envía la respuesta siguiente, que contiene tres elementos.</span><span class="sxs-lookup"><span data-stu-id="701b1-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="701b1-232">La respuesta también indica que el número total de elementos en los resultados en el servidor es ocho aún y que el último elemento de los resultados de la lista se incluye en esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="701b1-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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

## <a name="see-also"></a><span data-ttu-id="701b1-233">Ver también</span><span class="sxs-lookup"><span data-stu-id="701b1-233">See also</span></span>


- [<span data-ttu-id="701b1-234">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="701b1-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="701b1-235">ExchangeService.FindFolders (método)</span><span class="sxs-lookup"><span data-stu-id="701b1-235">ExchangeService.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="701b1-236">ExchangeService.FindItems (método)</span><span class="sxs-lookup"><span data-stu-id="701b1-236">ExchangeService.FindItems method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="701b1-237">Folder.FindFolders (método)</span><span class="sxs-lookup"><span data-stu-id="701b1-237">Folder.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="701b1-238">Folder.FindFolders (método)</span><span class="sxs-lookup"><span data-stu-id="701b1-238">Folder.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="701b1-239">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="701b1-239">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="701b1-240">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="701b1-240">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="701b1-241">EWS limitación en Exchange</span><span class="sxs-lookup"><span data-stu-id="701b1-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    


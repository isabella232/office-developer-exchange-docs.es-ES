---
title: Realizar búsquedas paginadas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Descubra cómo realizar búsquedas paginadas en la API administrada de EWS o en la aplicación EWS dirigida a Exchange.
localization_priority: Priority
ms.openlocfilehash: 2b608584918c936f62883b8b444d59c05c5952ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456848"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a>Realizar búsquedas paginadas mediante EWS en Exchange

Descubra cómo realizar búsquedas paginadas en la API administrada de EWS o en la aplicación EWS dirigida a Exchange.
  
La paginación es una característica de EWS que permite controlar el tamaño de los resultados de una búsqueda. En lugar de recuperar todo el conjunto de resultados en una respuesta de EWS, puede recuperar conjuntos más pequeños en varias respuestas de EWS. Por ejemplo, considere un usuario con 10.000 mensajes de correo electrónico en su bandeja de entrada. Como es hipotético, puede recuperar todos los correos electrónicos de 10.000 en una respuesta de gran tamaño, pero es posible que desee dividirlos en fragmentos más manejables por motivos de ancho de banda o de rendimiento. La paginación le proporciona las herramientas que debe hacer exactamente eso.
  
> [!NOTE]
> Aunque es posible recuperar de forma hipotética 10.000 elementos en una solicitud, en realidad, esto es improbable debido a la limitación de EWS. Para obtener más información, consulte [limitación de EWS en Exchange](ews-throttling-in-exchange.md). 
  
**Tabla 1. Parámetros de paginación en la API administrada de EWS y EWS**

|**Para configurar o recuperar...**|**En la API administrada de EWS, use...**|**En EWS, use...**|
|:-----|:-----|:-----|
|Número máximo de elementos o carpetas en una respuesta  <br/> |El parámetro **pageSize** para el constructor [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) o el [constructor FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) <br/> O bien:  <br/> Propiedad [PagedView. PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)  <br/> |El atributo **MaxEntriesReturned** del elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o del elemento [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)  <br/> |
|Punto de inicio de la lista de elementos o carpetas  <br/> |El parámetro **offsetBasePoint** para el constructor **ItemView** o el constructor **FolderView**  <br/> O bien:  <br/> Propiedad [PagedView. OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)  <br/> |El atributo **BasePoint** del elemento **IndexedPageItemView** o del elemento **IndexedPageFolderView**  <br/> |
|Desplazamiento desde el punto inicial  <br/> |El parámetro **offset** para el constructor **ItemView** o el constructor **FolderView**  <br/> O bien:  <br/> Propiedad [PagedView. offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)  <br/> |El atributo **offset** en el elemento **IndexedPageItemView** o en el elemento **IndexedPageFolderView**  <br/> |
|Número total de resultados en el servidor  <br/> |La propiedad [FindItemsResults. totalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults. totalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)  <br/> |El atributo **TotalItemsInView** del elemento [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) o de la elemento [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)  <br/> |
|Desplazamiento del primer elemento o carpeta no incluido en la respuesta actual  <br/> |La propiedad [FindItemsResults. NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults. NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)  <br/> |El atributo **IndexedPagingOffset** del elemento **RootFolder**  <br/> |
|Indicador de que la respuesta incluye el último elemento o carpeta de la lista  <br/> |La propiedad [FindItemsResults. MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults. MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)  <br/> |El atributo **IncludesLastItemInRange** del elemento **RootFolder**  <br/> |
   
## <a name="how-paging-works"></a>Cómo funciona la paginación
<a name="bk_HowPagingWorks"> </a>

Para comprender cómo funciona la paginación, es útil visualizar los mensajes de una carpeta como las cartelera alineadas en paralelo en un campo fuera de la casa. Puede ver algunas de estas cartelera a través de una ventana mágica. Tiene la posibilidad de cambiar el tamaño de la ventana (para ver más o menos cartelera a la vez) y para mover la ventana (para controlar qué cartelera puede ver). Esta manipulación de la ventana es la paginación. 
  
Cuando se envía la solicitud al servidor de Exchange, se especifica el tamaño de la ventana en función de cuántos elementos se van a devolver. Para establecer la posición de la ventana, especifique un punto inicial (ya sea el principio o el final de la línea) y un desplazamiento a partir de ese punto de inicio, expresado en un número de elementos. El principio de la ventana es el número de elementos especificado por el desplazamiento desde el punto de inicio.
  
Donde la paginación es un poco más interesante está en la respuesta del servidor y cómo la aplicación puede usar esa respuesta para dar forma a su solicitud siguiente. El servidor le ofrece tres datos que puede usar para determinar cómo configurar la "ventana" para la siguiente solicitud: 
  
- Si los resultados en la respuesta incluyen el último elemento del conjunto de resultados general en el servidor.
    
- El número total de elementos en el conjunto de resultados en el servidor.
    
- Cuál debería ser el siguiente valor de desplazamiento, si desea hacer avanzar la ventana al siguiente elemento del conjunto de resultados que no está incluido en la respuesta actual.
    
Veamos un ejemplo sencillo. Imagínese una bandeja de entrada con 15 mensajes en ella. La aplicación envía una solicitud inicial para recuperar un máximo de 10 elementos, comenzando al principio de la lista de mensajes (por lo que el desplazamiento es cero). El servidor responde con los 10 primeros mensajes e indica que la respuesta no incluye el último elemento, que hay un total de 15 elementos y que el siguiente desplazamiento debe ser 10.
  
**Figura 1. Solicitar 10 elementos en desplazamiento 0 desde el principio de una lista de 15 elementos**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 0 desde el principio de una lista de 15 elementos.](media/Ex15_PagedSearch_FirstPage.png)
  
A continuación, la aplicación reenvía la misma solicitud al servidor, con el único cambio de que el desplazamiento es ahora 10. El servidor devuelve los últimos cinco elementos e indica que la respuesta incluye el último elemento, que hay un total de 15 elementos y que el siguiente desplazamiento debe ser 15 (aunque, por supuesto, ha alcanzado el final, por lo que no habrá un desplazamiento próximo).
  
**Figura 2. Solicitar 10 elementos con un desplazamiento 10 desde el principio de una lista de 15 elementos**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 15 elementos.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a>Consideraciones de diseño para la paginación
<a name="bk_DesignConsiderations"> </a>

Para sacar el máximo partido de la paginación en la aplicación es necesario tener en cuenta. Por ejemplo, ¿en qué tamaño se realiza la "ventana"? ¿Qué debe hacer si los resultados en el servidor cambian mientras está moviendo la "ventana"?
  
### <a name="determine-the-size-of-your-window"></a>Determinar el tamaño de la ventana

No existe el número máximo de entradas "de tamaño único" que deben usar todas las aplicaciones. La determinación del número adecuado para la aplicación depende de varios factores diferentes. Sin embargo, es útil tener en cuenta las siguientes directrices:
  
- De forma predeterminada, Exchange limita el número máximo de elementos que se pueden devolver en una única solicitud a 1000.
    
- Si se establece el número máximo de entradas en un número mayor, se deben enviar menos solicitudes para obtener todos los elementos, con el costo de esperar más a las respuestas.
    
- Establecer el número máximo de entradas en un número menor da como resultado tiempos de respuesta más rápidos, al costo de tener que enviar más solicitudes para obtener todos los elementos.
    
### <a name="handling-changes-to-the-result-set"></a>Control de cambios en el conjunto de resultados

En el ejemplo sencillo descrito anteriormente en este artículo, el número de elementos de la bandeja de entrada del usuario seguía siendo constante. Sin embargo, en realidad, el número de elementos de una bandeja de entrada puede cambiar con frecuencia. Los mensajes nuevos pueden llegar y los elementos se pueden eliminar o mover en cualquier momento. Pero ¿cómo afecta esto a la paginación? Vamos a modificar el escenario de ejemplo anterior para averiguarlo.
  
Comenzaremos de nuevo con los 15 elementos en la bandeja de entrada del usuario y enviarán la misma solicitud inicial. Como antes, el servidor responde con los 10 primeros mensajes, e indica que la respuesta no incluye el último elemento, que hay un total de 15 elementos y que el siguiente desplazamiento debe ser 10, tal como se muestra en la figura 1.
  
Ahora, mientras la aplicación procesa los 10 elementos, llega un nuevo mensaje en la bandeja de entrada y se agrega al conjunto de resultados en el servidor. La aplicación reenvía la misma solicitud al servidor (solo con el desplazamiento establecido en 10). Esta vez el servidor devuelve seis elementos e indica que hay un total de 16 elementos en el conjunto de resultados.
  
En este momento, es posible que se pregunte si incluso es un problema. Después de todo, obtuvo 16 elementos por las dos respuestas, así que ¿por qué no? La respuesta depende de la ubicación de la lista en la que se encuentra el elemento nuevo. Si la lista está ordenada de modo que los elementos más antiguos (por fecha y hora de recepción) son los primeros, no hay que preocuparse por este escenario. El nuevo elemento se colocará al final de la lista y se incluirá en la segunda respuesta.
  
**Figura 3. Solicitar 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos, donde el elemento 16 de la lista es nuevo**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento número 16 se agregó al final de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
Si la lista está ordenada para que los elementos más recientes sean los primeros, es un artículo diferente. En este caso, el primer elemento de la segunda solicitud sería el último elemento de la solicitud anterior más los cinco elementos restantes a partir del 15 original. Para colocarla en términos de nuestra ventana de mágico imaginaria, ha desplazado la posición de la ventana en 10, pero las propias cartelera también se han desplazado con 1.
  
**Figura 4. Solicitar 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos, con el primer elemento de la lista siendo nuevo**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento número 16 se agregó al comienzo de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
Una forma de detectar un cambio en los resultados en el servidor es usar el concepto de un elemento de delimitador. Un elemento de delimitador es un elemento adicional de la respuesta que no se procesa junto con el resto de los resultados, pero que se usa para comparar con los siguientes resultados para ver si los propios elementos se han desplazado. Volver a compilar en nuestro sencillo ejemplo, si la aplicación usa un tamaño de "Window" de 10, en realidad se establece el número máximo de elementos que se devuelven a 11. La aplicación procesa los primeros 10 elementos de la respuesta de la forma habitual. Para el último elemento, se guarda el identificador del elemento como un delimitador y, a continuación, se emite la siguiente solicitud con un desplazamiento de 10. Si los datos no han cambiado, el primer elemento de la segunda respuesta debe tener un identificador de elemento que coincida con el delimitador. Si los identificadores de elemento no coinciden, sabrá que los datos se han quitado o insertado en las partes de la lista a las que ya ha "paginado".
  
Incluso cuando se sabe que los datos han cambiado, sigue siendo necesario decidir cómo reaccionar. No hay ninguna respuesta de un solo tamaño que se ajuste a esta pregunta. Las acciones dependerán de la naturaleza de la aplicación y de la importancia de la captura de todos los elementos. Puede omitirlo por completo, reiniciar el proceso desde el principio o la pista posterior e intentar detectar dónde se produjo el cambio.
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a>Ejemplo: realizar una búsqueda paginada mediante la API administrada de EWS
<a name="bk_PagedSearchEWSMA"> </a>

La paginación es compatible con los siguientes métodos de la API administrada de EWS:
  
- [ExchangeService. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
Si usa la API administrada de EWS, la aplicación configura la paginación con la clase [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) o [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) y recibe información del servidor en relación con la paginación de la clase [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) o [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) . 
  
En el siguiente ejemplo se recuperan todos los elementos de una carpeta mediante una búsqueda paginada que devuelve cinco elementos en cada respuesta. También recupera un elemento adicional para que sirva como delimitador para detectar los cambios en los resultados en el servidor. 
  
En este ejemplo se supone que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . 
  
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

## <a name="example-perform-a-paged-search-by-using-ews"></a>Ejemplo: realizar una búsqueda paginada con EWS
<a name="bk_PagedSearchEWS"> </a>

La paginación es compatible con las siguientes operaciones de EWS:
  
- [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
Si está usando EWS, la aplicación configura la paginación con el elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o el elemento [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) y recibe información del servidor en relación con la paginación desde el elemento [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) o el elemento [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) . 
  
En este ejemplo de solicitud, se envía una solicitud **FindItem** para un máximo de seis elementos, comenzando por un desplazamiento de cero desde el principio de la lista de elementos de la bandeja de entrada del usuario. 
  
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

El servidor devuelve la siguiente respuesta, que contiene seis elementos. La respuesta también indica que hay un total de ocho elementos en los resultados en el servidor y que el último elemento de la lista de resultados no está presente en esta respuesta.
  
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

En este ejemplo, se envía la misma solicitud, pero esta vez el atributo **offset** cambia a cinco, lo que indica que el servidor debe devolver como máximo seis elementos a partir del desplazamiento cinco desde el principio. 
  
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

El servidor envía la siguiente respuesta, que contiene tres elementos. La respuesta también indica que el número total de elementos de los resultados en el servidor sigue siendo ocho y que el último elemento de la lista de resultados se incluye en esta respuesta.
  
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

## <a name="see-also"></a>Vea también


- [Búsqueda y EWS en Exchange](search-and-ews-in-exchange.md)
    
- [Método ExchangeService. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [Método ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Método Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Método Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [Operación FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [Limitación de EWS en Exchange](ews-throttling-in-exchange.md)
    


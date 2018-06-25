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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763154"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a>Realizar búsquedas paginadas mediante EWS en Exchange

Encuentre información acerca de cómo realizar búsquedas paginadas en la API administrada de EWS o aplicación de EWS dirigido a Exchange.
  
Paginación es una característica de EWS que le permite controlar el tamaño de los resultados de una búsqueda. En lugar de recuperar el completo conjunto de resultados en una respuesta EWS, puede recuperar conjuntos más pequeños en varias respuestas EWS. Por ejemplo, considere la posibilidad de un usuario con 10.000 mensajes de correo electrónico en su Bandeja de entrada. En teoría, podría recuperar todos los correos 10.000 electrónicos en una respuesta muy grande, pero es posible que desee dividir en fragmentos más manejables por motivos de rendimiento o ancho de banda. Paginación le ofrece las herramientas necesarias para hacerlo.
  
> [!NOTE]
> Mientras teoría puede recuperar 10.000 elementos en una sola solicitud, en realidad, esto es poco probable debido a la limitación de EWS. Para obtener más información, vea la [limitación de EWS en Exchange](ews-throttling-in-exchange.md). 
  
**La tabla 1. Parámetros de paginación en la API administrada de EWS y EWS**

|**Para configurar o recuperar la...**|**En la API administrada de EWS, use...**|**En EWS, use...**|
|:-----|:-----|:-----|
|Número máximo de elementos o carpetas en una respuesta  <br/> |El parámetro **pageSize** para el [constructor artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) o el [constructor FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) <br/> O  <br/> La propiedad [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)  <br/> |El atributo **MaxEntriesReturned** en el elemento [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o el elemento [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)  <br/> |
|Punto de inicio en la lista de elementos o carpetas  <br/> |El parámetro **offsetBasePoint** para el constructor **artículoVer** o el constructor **FolderView**  <br/> O  <br/> La propiedad [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)  <br/> |El atributo de **punto base** en el elemento **IndexedPageItemView** o el elemento **IndexedPageFolderView**  <br/> |
|Desplazamiento desde el punto de partida  <br/> |El parámetro **offset** para el constructor **artículoVer** o el constructor **FolderView**  <br/> O  <br/> La propiedad [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)  <br/> |El atributo de **desplazamiento** en el elemento **IndexedPageItemView** o el elemento **IndexedPageFolderView**  <br/> |
|Número total de resultados en el servidor  <br/> |La propiedad [FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)  <br/> |El atributo **TotalItemsInView** en el elemento [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) o el elemento [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)  <br/> |
|Desplazamiento del primer elemento o carpeta no incluida en la respuesta actual  <br/> |La propiedad [FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)  <br/> |El atributo **IndexedPagingOffset** en el elemento **RootFolder**  <br/> |
|Indicador de que la respuesta incluye el último elemento o la carpeta en la lista  <br/> |La propiedad [FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) o la propiedad [FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)  <br/> |El atributo **IncludesLastItemInRange** en el elemento **RootFolder**  <br/> |
   
## <a name="how-paging-works"></a>Cómo funciona la paginación
<a name="bk_HowPagingWorks"> </a>

Para comprender cómo funciona la paginación, es útil visualizar los mensajes de una carpeta como mensajes alineadas en paralelo en un campo de fuera de su casa. Puede ver algunos de estos mensajes a través de una ventana mágica. Tiene la posibilidad de cambiar el tamaño de la ventana (para ver más o menos mensajes a la vez) y para mover la ventana (para controlar qué mensajes se puede ver). Esta manipulación de la ventana de paginación. 
  
Al enviar la solicitud al servidor de Exchange, especifique el tamaño de la ventana en términos de número de elementos para devolver. Establecer la posición de la ventana mediante la especificación de un punto de partida bien (el principio de la línea) o el final de la línea y un desplazamiento desde ese punto de partida, expresado en un número de elementos. El principio de la ventana es el número de elementos especificados por el desplazamiento desde el punto de partida.
  
Donde paginación Obtiene un poco más interesante se encuentra en la respuesta del servidor, y cómo la aplicación puede usar esa respuesta a su solicitud siguiente de la forma. El servidor le ofrece tres partes de la información que se puede utilizar para determinar cómo configurar su "ventana" para la solicitud siguiente: 
  
- Si los resultados en la respuesta incluyen el último elemento del general conjunto de resultados en el servidor.
    
- El número total de elementos en el conjunto de resultados en el servidor.
    
- Lo que el valor de desplazamiento siguiente debe ser, si desea avanzar su ventana hasta el siguiente elemento en el conjunto de resultados que no está incluido en la respuesta actual.
    
Veamos un ejemplo sencillo. Imagine una bandeja de entrada con 15 mensajes en ella. La aplicación envía una solicitud inicial para recuperar un máximo de 10 elementos, empezando en el principio de la lista de mensajes (de manera que el desplazamiento es cero). El servidor responde con los 10 primeros mensajes y se indica que la respuesta no incluye el último elemento, que no hay un total de 15 elementos y que el desplazamiento siguiente debe ser 10.
  
**En la figura 1. Solicitud de 10 elementos con un desplazamiento 0 desde el principio de una lista de 15 elementos**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 0 desde el principio de una lista de 15 elementos.](media/Ex15_PagedSearch_FirstPage.png)
  
A continuación, la aplicación vuelve a enviar la solicitud misma en el servidor, con el único cambio que el desplazamiento es ahora 10. El servidor devuelve los últimos cinco elementos y se indica que la respuesta incluye el último elemento, que no hay un total de 15 elementos y que el desplazamiento siguiente debe ser 15 (aunque, por supuesto, ha llegado el final, por lo que no habrá un desplazamiento siguiente.)
  
**La figura 2. Solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 15 elementos**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 15 elementos.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a>Consideraciones de diseño para la paginación
<a name="bk_DesignConsiderations"> </a>

Hacer que el máximo partido de paginación en su aplicación requieren algunos consideración. ¿Por ejemplo, cómo grande puede hacer que la ventana de""? ¿Qué hace si cambian los resultados en el servidor mientras se está moviendo su ventana de""?
  
### <a name="determine-the-size-of-your-window"></a>Determinar el tamaño de la ventana

No hay ningún "única" número máximo de entradas que deben usar todas las aplicaciones. Determinación del número que es el adecuado para su aplicación depende de varios factores diferentes. Sin embargo, es útil para que tenga en cuenta las siguientes directrices:
  
- De forma predeterminada, Exchange limita el número máximo de elementos que se pueden devolver en una única solicitud y 1000.
    
- Si se establece el número máximo de entradas a un mayor número como resultado tener que enviar solicitudes menos para obtener todos los elementos, costo de tener que esperar más tiempo para las respuestas.
    
- Si se establece el número máximo de entradas a un número como resultado más pequeñas en tiempos de respuesta más rápidos a costa de tener que enviar solicitudes más para obtener todos los elementos.
    
### <a name="handling-changes-to-the-result-set"></a>Control de cambios para el conjunto de resultados

En el ejemplo simple anteriormente en este artículo, el número de elementos en la Bandeja de entrada del usuario se mantuvo constante. Sin embargo, en realidad, el número de elementos en una bandeja de entrada puede cambiar con frecuencia. Pueden reciben mensajes nuevos y los elementos pueden ser eliminados o movidos en cualquier momento. Pero ¿cómo este paginación impacto? Vamos a modificar el escenario de ejemplo anterior para averiguar.
  
Se podrá iniciar de nuevo con los 15 elementos en la Bandeja de entrada del usuario y enviar la misma solicitud inicial. Como antes, el servidor responde con los 10 primeros mensajes e indica que la respuesta no incluye el último elemento, que no hay un total de 15 elementos y que el desplazamiento siguiente debe ser 10, tal como se muestra en la figura 1.
  
Ahora, mientras que la aplicación está procesando esos 10 elementos, un nuevo mensaje llega a la Bandeja de entrada y se agrega al conjunto de resultados en el servidor. La aplicación vuelve a enviar la solicitud al servidor misma (sólo con el desplazamiento establecido en 10). Esta vez el servidor obtiene back seis elementos e indica que no hay un total de 16 elementos en el conjunto de resultados.
  
En este momento es posible que se pregunte si esto incluso es un problema. Después de todo, obtuvo 16 elementos volver a través de las dos respuestas, ¿por qué todos los elementos innecesarios? La respuesta depende de dónde se coloca el nuevo elemento en la lista. Si se ordena la lista para que los elementos más antiguos (por fecha/hora de recepción) son primera, no hay ningún motivo de preocupación en este escenario. El nuevo elemento se colocará al final de la lista y se incluirá en la segunda respuesta.
  
**La figura 3. Solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos, con el elemento número 16 en la lista que se va a nuevo**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento número 16 se agregó al final de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
Si la lista se ordena por lo que los elementos más recientes son primer, es un artículo diferente. En este caso, el primer elemento de la segunda solicitud sería el último elemento de la solicitud anterior además de los cinco elementos restantes desde el 15 original. Para ponerla en términos de nuestra ventana mágico imaginario, del cambio de posición de la ventana por 10, pero los mensajes a sí mismos también se desplazan por 1.
  
**La figura 4. Solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos, con el primer elemento de la lista que se va a nuevo**

![Diagrama que muestra los resultados de la solicitud de 10 elementos con un desplazamiento 10 desde el principio de una lista de 16 elementos cuando el elemento número 16 se agregó al comienzo de la lista.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
Una forma de detectar un cambio en los resultados en el servidor es usar el concepto de un elemento delimitador. Un elemento delimitador es un elemento adicional en la respuesta que no se procesará junto con el resto de los resultados, pero se usa para comparar con los resultados de la siguiente para ver si han variado los mismos elementos. Creación de nuevo en nuestro ejemplo sencillo, si la aplicación usa un tamaño de "ventana de" de 10, establezca el número máximo de elementos para volver a 11 realmente. La aplicación procesa los primeros 10 elementos en la respuesta como de costumbre. Para el último elemento, guarde el identificador del elemento como un delimitador, a continuación, emitir la siguiente solicitud con un desplazamiento de 10. Si no ha cambiado los datos, el primer elemento de la segunda respuesta debe tener un identificador de elemento que coincida con el delimitador. Si no coinciden con los identificadores de elemento, sabrá que los datos se haya eliminado o insertado en los elementos de la lista que haya ya "paginar" a través de.
  
Incluso cuando se sabe que los datos ha cambiado, necesitará decidir cómo reaccionar. O bien no hay una única respuesta a esta pregunta. Sus acciones dependerá de la naturaleza de la aplicación y lo importante que es capturar todos los elementos. Es posible que pasar por alto por completo, reiniciar el proceso desde el principio, o realizar una copia de seguimiento e intente detectar en que se produjo el cambio.
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a>Ejemplo: Realizar una búsqueda paginada mediante el uso de la API administrada de EWS
<a name="bk_PagedSearchEWSMA"> </a>

Paginación es compatible con los siguientes métodos de la API administrada de EWS:
  
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
Si está utilizando la API administrada de EWS, su aplicación configura la paginación con la clase [artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) o [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) y recibe información desde el servidor con respecto a paginación desde el [FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx) o [FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) clase. 
  
En el ejemplo siguiente se recupera todos los elementos de una carpeta mediante una búsqueda paginada que devuelve cinco elementos en cada respuesta. También recupera un elemento adicional para que sirva como un delimitador para detectar cambios en los resultados en el servidor. 
  
En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . 
  
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

## <a name="example-perform-a-paged-search-by-using-ews"></a>Ejemplo: Realizar una búsqueda paginada mediante el uso de EWS
<a name="bk_PagedSearchEWS"> </a>

Paginación es compatible con las siguientes operaciones de EWS:
  
- [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
Si está usando EWS, su aplicación configura la paginación con el elemento [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o el elemento [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) y recibe información desde el servidor con respecto a paginación desde el [() RootFolder FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) el elemento [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) o un elemento. 
  
En este ejemplo de solicitud, se envía una solicitud de **FindItem** para un máximo de seis elementos, comenzando en un desplazamiento de cero desde el principio de la lista de elementos en la Bandeja de entrada del usuario. 
  
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

El servidor devuelve la respuesta siguiente, que contiene seis elementos. La respuesta también indica que no hay un total de ocho elementos en los resultados en el servidor y que el último elemento de la lista de resultados no está presente en esta respuesta.
  
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

En este ejemplo, se envía la solicitud de la misma, pero esta vez, el atributo de **desplazamiento** se cambia a cinco, lo que indica que el servidor debería devolver como máximo seis elementos empezando por el desplazamiento cinco desde el principio. 
  
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

El servidor envía la respuesta siguiente, que contiene tres elementos. La respuesta también indica que el número total de elementos en los resultados en el servidor es ocho aún y que el último elemento de los resultados de la lista se incluye en esta respuesta.
  
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

## <a name="see-also"></a>Vea también


- [Búsqueda y EWS en Exchange](search-and-ews-in-exchange.md)
    
- [ExchangeService.FindFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [Operación FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [EWS limitación en Exchange](ews-throttling-in-exchange.md)
    


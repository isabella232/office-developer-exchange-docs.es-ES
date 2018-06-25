---
title: Realizar una búsqueda AQS mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Averigüe cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o aplicación de EWS.
ms.openlocfilehash: dc859e24fa80cd5627477182979c9cc9527818d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763171"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a>Realizar una búsqueda AQS mediante EWS en Exchange

Averigüe cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o aplicación de EWS.
  
Cadenas de consulta proporcionan una alternativa a los [filtros de búsqueda](how-to-use-search-filters-with-ews-in-exchange.md) para expresar los criterios de búsqueda. La mayor ventaja de usar cadenas de consulta es que no es necesario especificar una sola propiedad para buscar. Sólo puede proporcionar un valor, y la búsqueda se aplicará a todos los campos usados con más frecuencia en los elementos. También puede restringir la búsqueda mediante el uso de sintaxis de consulta avanzada (AQS) en lugar de un valor simple. Sin embargo, las cadenas de consulta tienen las siguientes limitaciones que deben tenerse en cuenta antes de agregar al cuadro de herramientas: 
  
- **Capacidad limitada para buscar propiedades específicas.** Al buscar con un valor simple en una cadena de consulta, la búsqueda se realiza en todas las propiedades indizadas. Puede restringir la búsqueda a propiedades específicas, pero las propiedades disponibles para su uso en una cadena AQS están limitadas. Si la propiedad que desea buscar no es una de las propiedades que están disponibles para AQS, considere el uso de un filtro de búsqueda. 
    
- **No se buscan en las propiedades personalizadas.** Las búsquedas de cadena de consulta se llevan a cabo con un índice, y las propiedades personalizadas no se incluyen en ese índice. Si necesita las propiedades personalizadas de búsqueda, utilice en su lugar un filtro de búsqueda. 
    
- **Busca un control limitado de cadena.** Búsquedas de cadenas de consulta siempre entre mayúsculas y minúsculas y siempre son búsquedas de subcadenas. Si desea hacer entre mayúsculas y minúsculas, prefijo o las búsquedas de coincidencia exacta, utilice un filtro de búsqueda. 
    
- **No está disponible para las carpetas o las carpetas de búsqueda.** Las operaciones de EWS para la búsqueda de las carpetas no admiten el uso de una cadena de consulta. Además, las carpetas de búsqueda no admiten cadenas de consulta. En ambos casos, un filtro de búsqueda es la única opción. 
    
## <a name="creating-a-query-string"></a>Creación de una cadena de consulta
<a name="bk_CreateQueryString"> </a>

Cadenas de consulta en la API administrada de EWS y EWS se interpretan como un subconjunto de la sintaxis AQS. Cadenas AQS se componen de los valores o los pares de palabra clave y valor, separados por un carácter de dos puntos (:).
  
`keyword:value`

Cuando se especifica un valor sin una palabra clave, se buscan todas las propiedades indizadas para el valor. Si una palabra clave se corresponde con un valor, la palabra clave especifica una propiedad para buscar el valor correspondiente.
  
**La tabla 1. Palabras clave AQS compatibles**

|**Palabra clave**|**Tipo de valor**|**Ejemplo**|
|:-----|:-----|:-----|
|subject  <br/> |Cadena  <br/> |Asunto: proyecto  <br/> |
|cuerpo  <br/> |Cadena  <br/> |cifras de ventas de cuerpo:  <br/> |
|datos adjuntos  <br/> |Cadena  <br/> |datos adjuntos: informe  <br/> |
|a  <br/> |Cadena  <br/> |para: "Sadie Daniels"  <br/> |
|from  <br/> |Cadena  <br/> |desde: Esperamos  <br/> |
|cc  <br/> |Cadena  <br/> |cc: "Ronnie Sturgis"  <br/> |
|bcc  <br/> |Cadena  <br/> |BCC:Mack  <br/> |
|participants  <br/> |Cadena  <br/> |los participantes: sadie  <br/> |
|.  <br/> |String  <br/> |categoría: proyecto  <br/> |
|importance  <br/> |Cadena  <br/> |importancia: alta  <br/> |
|tipo  <br/> |Tipo de elemento  <br/> |tipo: reuniones  <br/> |
|enviado  <br/> |Fecha  <br/> |enviado: 10/12/2013  <br/> |
|recibido  <br/> |Fecha  <br/> |recibido: ayer  <br/> |
|HasAttachment  <br/> |Boolean  <br/> |Tiene datos adjuntos: true  <br/> |
|estámarcado  <br/> |Boolean  <br/> |isflagged:true  <br/> |
|estáleído  <br/> |Boolean  <br/> |isread:False  <br/> |
|size  <br/> |Número  <br/> |tamaño:\>5000  <br/> |
   
Vamos a echar un vistazo a cómo funcionan los tipos de valores diferentes.
  
### <a name="using-a-string-value-type"></a>Uso de un tipo de valor de cadena

Tipos de valor de cadena son buscado como búsquedas de subcadenas de prefijo que no distinguen mayúsculas de minúsculas de forma predeterminada. Eso significa que busca asunto: proyecto coincidirá con cualquiera de los siguientes temas: 
  
- Notas de las reuniones de proyecto
    
- ¿Tiene los planes del proyecto?
    
- Previsiones de ventas de diciembre
    
Puede cambiar la búsqueda para exigir la palabra completa en lugar de coincidencia de prefijos por encerrar la cadena entre comillas. Buscar asunto: "proyecto" eliminaría el valor "Diciembre las previsiones de ventas" de la lista de coincidencias. Tenga en cuenta que el valor sea aún no distingue mayúsculas de minúsculas. 
  
Si usa varias palabras en una cadena de consulta, se requiere una coincidencia que ambas palabras aparecen en los campos de búsqueda. Por ejemplo, busca el plan del proyecto: asunto coincidirá con cualquiera de los siguientes temas: 
  
- Plan del proyecto
    
- ¿Tiene los planes del proyecto?
    
- Envíeme el plan para nuestro proyecto
    
- Planeación de los hitos del proyecto
    
Si escriba varias palabras entre comillas, se tratan como una sola frase. Buscar asunto: "plan del proyecto" sólo coincidirá con el asunto "Plan del proyecto" de la lista anterior. 
  
### <a name="using-an-item-type-value-type"></a>Uso de un tipo de valor de tipo de elemento

Puede usar los siguientes valores de tipo de elemento con la palabra clave de **tipo** para limitar los resultados de búsqueda a solo un tipo específico de elemento, como correo electrónico o las convocatorias de reunión: 
  
- contactos    
- documentos    
- email    
- faxes    
- mensajería instantánea (corresponde a los mensajes instantáneos)    
- diarios    
- las reuniones (corresponde a las citas y convocatorias de reunión)    
- notas    
- posts    
- rssfeeds    
- tasks    
- correo de voz
    
### <a name="using-a-date-value-type"></a>Uso de un tipo de valor de fecha

Puede buscar los tipos de valor de fecha en un número de formas diferentes. Es el más simple buscar una fecha específica. Buscar con recibido: 11/12/2013 devolverá todos los elementos recibidos en el 11 de diciembre de 2013. Sin embargo, también puede ser menos específico. Buscar con recibido: 12/11 devolverá todos los elementos que se recibe en el 11 de diciembre del año actual. 
  
Otra opción consiste en usar los nombres de mes. Puede buscar con recibido: 11 de diciembre de 2013 o el 11 de diciembre para obtener los mismos resultados recibidos: 11/12/2013 y recibido: 12/11, respectivamente. También puede buscar con recibido: diciembre para obtener todos los elementos recibidos en el mes de diciembre, en el año actual. 
  
También es una opción con los nombres de los días de la semana. Buscar con recibido: el martes devolverá todos los elementos recibidos el martes de la semana actual. 
  
Tipos de valor de fecha también admiten un conjunto de palabras clave para las búsquedas con respecto a la hora actual. Se admiten las siguientes palabras clave:
  
- hoy  
- tomorrow
- yesterday
- this week    
- La semana pasada    
- próximo mes    
- mes pasado    
- año siguiente
    
Tipos de valor de fecha también se pueden comparar con operadores relacionales como mayor o menor que, o se ha especificado como un rango con el operador de intervalo **.**. Por ejemplo, recibido:\>30/11/2013, envía:\>= ayer, y received:12/1/2013..today son todas las cadenas de consulta válida. 
  
### <a name="using-a-boolean-value-type"></a>Uso de un tipo de valor booleano

Tipos de valor de tipo Boolean pueden ser "true" o "false". Los valores no distinguen mayúsculas de minúsculas, por lo que isread:false generarán los mismos resultados que isread:FALSE.
  
### <a name="using-a-number-value-type"></a>Uso de un tipo de valor numérico

Se pueden buscar en los tipos de valor numéricos como coincidencias exactas, pero también se pueden buscar con operadores relacionales como mayor o menor que. Por ejemplo, tamaño: 10000 devolverá sólo los elementos que tienen un tamaño de exactamente 10000 bytes, pero tamaño:\>= 10000 devolverá los elementos que tienen un tamaño mayor o igual a 10000 bytes. También puede especificar un intervalo mediante el operador de rango ( **.**). Por ejemplo, tamaño: 7000..8000 devolverá los elementos que tienen un tamaño de entre 7000 y 8000. 
  
### <a name="using-logical-operators"></a>Usar operadores lógicos

Cadenas de consulta admiten los siguientes operadores lógicos.
  
**Tabla 2. Operadores lógicos compatibles**

|**Operador**|**Ejemplos**|
|:-----|:-----|
|AND  <br/> |proyecto y desde: "Sadie Daniels"  <br/> Asunto:(project AND plan)  <br/> |
|O  <br/> |Asunto: reunión o desde: "Espero bruto"  <br/> desde: ("Sadie Daniels" o "Espero bruto")  <br/> |
|NOT  <br/> |NO desde: "Ronnie Sturgis"  <br/> recibido: no hoy mismo  <br/> |
   
Tenga en cuenta que puede utilizar estos operadores para unir varios criterios o para unir varios valores dentro de un par de palabra clave y valor único. Sin embargo, al unirse a varios valores en un par de palabra clave y valor único, debe usar paréntesis para delimitar los valores de varios. Para comprender por qué, considere la posibilidad de búsqueda con desde: "Sadie Daniels" o "Espero bruto". Esta búsqueda realmente se interpreta como los siguientes criterios:
  
- El elemento es de Sadie Daniels, OR
    
- El elemento tiene la frase "Espero bruto" en cualquiera de sus propiedades indizadas.
    
Por el contrario, desde: ("Sadie Daniels" o "Espero bruto") se interpreta como: 
  
- El elemento es de Sadie Daniels, OR
    
- El elemento es de espero bruto
    
Es el operador de forma predeterminada cuando se especifican varios criterios, pero no se incluye ningún operador lógico AND. Por ejemplo, tiene datos adjuntos: true asunto: proyecto es equivalente a tiene: true: los datos adjuntos y asunto: project.
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a>Ejemplo: Buscar elementos mediante el uso de una cadena de consulta y la API administrada de EWS
<a name="bk_ExampleEWSMA"> </a>

En este ejemplo, se define un método denominado **SearchWithQueryString** . Toma un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , un objeto [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y un objeto **string** que representa la cadena de consulta como parámetros. En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void SearchWithQueryString(ExchangeService service, WellKnownFolderName folder, string queryString)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       ItemSchema.Size,
                                       ItemSchema.Importance,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Execute the search based on the query string.
        // Example: "subject:project plan"
        FindItemsResults<Item> results = service.FindItems(folder, queryString, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Received: {0}", item.DateTimeReceived.ToString());
            Console.WriteLine("Size: {0}", item.Size.ToString());
            Console.WriteLine("Importance: {0}", item.Importance.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

Puede usar este método para buscar todos los elementos con la frase "plan del proyecto" en el asunto, tal como se muestra en este ejemplo.
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a>Ejemplo: Buscar elementos mediante el uso de una cadena de consulta y EWS
<a name="bk_ExampleEWS"> </a>

En este ejemplo, una solicitud SOAP [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) busca todos los elementos en la Bandeja de entrada con la frase "plan del proyecto" en el asunto. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="item:Size" />
          <t:FieldURI FieldURI="item:Importance" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:"project plan"</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta del servidor con los resultados de búsqueda.
  
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
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>project plan</t:Subject>
                <t:DateTimeReceived>2013-12-11T15:42:02Z</t:DateTimeReceived>
                <t:Size>7406</t:Size>
                <t:Importance>Normal</t:Importance>
                <t:IsRead>false</t:IsRead>
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
- [Use los filtros de búsqueda con EWS en Exchange](how-to-use-search-filters-with-ews-in-exchange.md)    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    


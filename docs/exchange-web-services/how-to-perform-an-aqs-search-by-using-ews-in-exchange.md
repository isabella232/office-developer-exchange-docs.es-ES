---
title: Realizar una búsqueda AQS con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Descubra cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o en la aplicación EWS.
localization_priority: Priority
ms.openlocfilehash: 9f611a8d90c6baf0f307897735c6366c82bb63c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455719"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a>Realizar una búsqueda AQS con EWS en Exchange

Descubra cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o en la aplicación EWS.
  
Las cadenas de consulta proporcionan una alternativa a los [filtros de búsqueda](how-to-use-search-filters-with-ews-in-exchange.md) para expresar criterios de búsqueda. La mayor ventaja de usar las cadenas de consulta es que no es necesario especificar una única propiedad para buscar. Solo puede proporcionar un valor y la búsqueda se aplicará a todos los campos de los elementos que se usen con frecuencia. También puede refinar la búsqueda con la sintaxis de consulta avanzada (AQS) en lugar de un valor sencillo. Sin embargo, las cadenas de consulta tienen las siguientes limitaciones que debe tener en cuenta antes de agregarlas al cuadro de herramientas: 
  
- **Capacidad limitada para buscar propiedades específicas.** Cuando se realiza una búsqueda con un valor simple en una cadena de consulta, la búsqueda se realiza en todas las propiedades indizadas. Puede restringir la búsqueda a propiedades específicas, pero las propiedades disponibles para usarlas en una cadena AQS son limitadas. Si la propiedad que quieres buscar no es una de las propiedades que están disponibles para AQS, considera la posibilidad de usar un filtro de búsqueda. 
    
- **Las propiedades personalizadas no se buscan.** Las búsquedas de cadenas de consulta se realizan en un índice, y las propiedades personalizadas no se incluyen en ese índice. Si necesita buscar propiedades personalizadas, use un filtro de búsqueda en su lugar. 
    
- **Control limitado para las búsquedas de cadena.** Las búsquedas de cadenas de consulta siempre omiten mayúsculas y minúsculas y son siempre búsquedas de subcadenas. Si desea realizar búsquedas con distinción de mayúsculas y minúsculas, prefijos o de coincidencia exacta, use un filtro de búsqueda. 
    
- **No disponible para carpetas o carpetas de búsqueda.** Las operaciones de EWS para buscar carpetas no admiten el uso de una cadena de consulta. Además, las carpetas de búsqueda no admiten cadenas de consulta. En ambos casos, un filtro de búsqueda es la única opción. 
    
## <a name="creating-a-query-string"></a>Creación de una cadena de consulta
<a name="bk_CreateQueryString"> </a>

Las cadenas de consulta en la API administrada de EWS y EWS se interpretan como un subconjunto de la sintaxis de AQS. Las cadenas AQS se componen de valores o pares de palabra clave y valor, separados por dos puntos (:).
  
`keyword:value`

Cuando se especifica un valor sin una palabra clave, se busca el valor en todas las propiedades indizadas. Si una palabra clave está emparejada con un valor, la palabra clave especifica una propiedad para buscar el valor correspondiente.
  
**Tabla 1. Palabras clave de AQS admitidas**

|**Palabra clave**|**Tipo de valor**|**Ejemplo**|
|:-----|:-----|:-----|
|subject  <br/> |String  <br/> |asunto: proyecto  <br/> |
|body  <br/> |Cadena  <br/> |cuerpo: cifras de ventas  <br/> |
|datos adjuntos  <br/> |Cadena  <br/> |datos adjuntos: informe  <br/> |
|a  <br/> |Cadena  <br/> |para: "Sadie Daniels"  <br/> |
|from  <br/> |Cadena  <br/> |de: espero  <br/> |
|cc  <br/> |Cadena  <br/> |CC: "Ronnie Sturgis"  <br/> |
|cco  <br/> |Cadena  <br/> |CCO: Mack  <br/> |
|participants  <br/> |Cadena  <br/> |participantes: Sadie  <br/> |
|categoría  <br/> |Cadena  <br/> |Categoría: proyecto  <br/> |
|importance  <br/> |Cadena  <br/> |importance:alta  <br/> |
|kind  <br/> |Tipo de elemento  <br/> |tipo: reuniones  <br/> |
|sent  <br/> |Fecha  <br/> |Enviado el: 12/10/2013  <br/> |
|received  <br/> |Fecha  <br/> |recibido: ayer  <br/> |
|hasattachment  <br/> |Boolean  <br/> |Tiene datos adjuntos: true  <br/> |
|isflagged  <br/> |Boolean  <br/> |isflagged: true  <br/> |
|isread  <br/> |Boolean  <br/> |isread: false  <br/> |
|size  <br/> |Número  <br/> |tamaño: \> 5000  <br/> |
   
Echemos un vistazo a cómo funcionan los distintos tipos de valor.
  
### <a name="using-a-string-value-type"></a>Uso de un tipo de valor de cadena

De forma predeterminada, los tipos de valor de cadena se buscan como búsquedas de subcadena de prefijo que no distinguen mayúsculas de minúsculas. Eso significa que la búsqueda de asunto: Project coincidirá con cualquiera de los siguientes asuntos: 
  
- Notas de la reunión del proyecto
    
- ¿Tiene planes de proyecto?
    
- Proyecciones de ventas de diciembre
    
Puede cambiar la búsqueda para que requiera la palabra completa en lugar de que los prefijos coincidan encerrando la cadena entre comillas. Buscar asunto: "Project" eliminará el valor "proyecto de ventas de diciembre" de la lista de coincidencias. Tenga en cuenta que el valor todavía no distingue mayúsculas de minúsculas. 
  
Si usa varias palabras en una cadena de consulta, una coincidencia requiere que ambas palabras aparezcan en los campos buscados. Por ejemplo, la búsqueda de asunto: el plan del proyecto coincidiría con cualquiera de los siguientes asuntos: 
  
- Plan del proyecto
    
- ¿Tiene planes de proyecto?
    
- Envíeme el plan de nuestro proyecto.
    
- Planeación de hitos de proyecto
    
Si escribe varias palabras entre comillas, se tratarán como una sola frase. La búsqueda del asunto: "plan del proyecto" solo coincidirá con el asunto "plan del proyecto" de la lista anterior. 
  
### <a name="using-an-item-type-value-type"></a>Usar un tipo de valor de tipo de elemento

Puede usar los siguientes valores de tipo de elemento con la palabra clave **Kind** para limitar los resultados de la búsqueda a un tipo específico de elemento, como correo electrónico o convocatorias de reunión: 
  
- contactos    
- documentos    
- correo electrónico    
- faxes    
- mi (corresponde a mensajes instantáneos)    
- diarios    
- reuniones (corresponde a citas y convocatorias de reunión)    
- notas    
- entradas    
- fuentes rss    
- tareas    
- correo de voz
    
### <a name="using-a-date-value-type"></a>Uso de un tipo de valor de fecha

Los tipos de valores de fecha se pueden buscar de varias formas. La más sencilla es buscar una fecha específica. La búsqueda con Received: 12/11/2013 devolverá todos los elementos recibidos el 11 de diciembre de 2013. Sin embargo, también puede ser menos específico. La búsqueda con Received: 12/11 devolverá todos los elementos que se hayan recibido el 11 de diciembre del año actual. 
  
Otra opción es usar los nombres de los meses. Puede buscar con Received: 11 de diciembre de 2013 o 11 de diciembre para obtener los mismos resultados que los recibidos: 12/11/2013 y recibidos: 12/11, respectivamente. También puede buscar con Received: December para obtener todos los elementos recibidos en el mes de diciembre en el año actual. 
  
El uso de los nombres de los días de la semana también es una opción. La búsqueda con Received: Tuesday devolverá todos los elementos que se reciben el martes de la semana actual. 
  
Los tipos de valores de fecha también admiten un conjunto de palabras clave para las búsquedas relativas a la hora actual. Se admiten las siguientes palabras clave:
  
- hoy  
- tomorrow
- yesterday
- this week    
- La semana pasada    
- próximo mes    
- último mes    
- año próximo
    
Los tipos de valores de fecha también se pueden comparar con operadores relacionales como mayor o menor que, o especificarse como un rango con el operador de rango **..**. Por ejemplo, Received: \> 11/30/2013, Sent: \> = ayer y Received: 12/1/2013.. hoy son cadenas de consulta válidas. 
  
### <a name="using-a-boolean-value-type"></a>Uso de un tipo de valor booleano

Los tipos de valores booleanos pueden ser "true" o "false". Los valores no distinguen entre mayúsculas y minúsculas, por lo que isread: false generarán los mismos resultados que isread: FALSE.
  
### <a name="using-a-number-value-type"></a>Uso de un tipo de valor de número

Los tipos de valores de número se pueden buscar como coincidencias exactas, pero también se pueden buscar mediante operadores relacionales como mayor o menor que. Por ejemplo, size: 10000 devolverá solo los elementos que tengan un tamaño exacto de 10000 bytes, pero Size: \> = 10000 devolverá los elementos que tengan un tamaño mayor o igual que 10000 bytes. También puede especificar un intervalo mediante el operador de intervalo ( **..**). Por ejemplo, size: 7000.. 8000 devolverá los elementos que tengan un tamaño entre 7000 y 8000. 
  
### <a name="using-logical-operators"></a>Uso de operadores lógicos

Las cadenas de consulta admiten los siguientes operadores lógicos.
  
**Tabla 2. Operadores lógicos admitidos**

|**Operator**|**Ejemplos**|
|:-----|:-----|
|Y  <br/> |Project y de: "Sadie Daniels"  <br/> asunto: (proyecto y plan)  <br/> |
|O  <br/> |asunto: reunión o de: "Esperamos bruta"  <br/> From:("Sadie Daniels" o "esperanza bruto")  <br/> |
|NO  <br/> |NO de: "Ronnie Sturgis"  <br/> recibido: no hoy  <br/> |
   
Tenga en cuenta que puede usar estos operadores para unir varios criterios de forma conjunta o para combinar varios valores en un solo par de palabra clave y valor. Sin embargo, al combinar varios valores en un par de palabra clave y valor único, debe usar paréntesis para incluir los varios valores. Para comprender por qué, considere la posibilidad de buscar con from: "Sadie Daniels" o "esperanza bruta". En realidad, esta búsqueda se interpreta como los siguientes criterios:
  
- El elemento es de Sadie Daniels o
    
- El elemento tiene la frase "Esperamos bruta" en cualquiera de sus propiedades indizadas.
    
Por el contrario, del:("Sadie Daniels" o "esperanza bruto") se interpreta como: 
  
- El elemento es de Sadie Daniels o
    
- El elemento es de esperanza bruta
    
El operador predeterminado cuando se especifican varios criterios, pero no se incluye ningún operador lógico y. Por ejemplo, tiene datos adjuntos: verdadero asunto: Project equivale a: Attachment: true y Subject: Project.
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a>Ejemplo: buscar elementos mediante una cadena de consulta y la API administrada EWS
<a name="bk_ExampleEWSMA"> </a>

En este ejemplo, se define un método denominado **SearchWithQueryString** . Toma un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , un objeto [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y un objeto **String** que representa la cadena de consulta como parámetros. En este ejemplo se supone que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . 
  
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

Puede usar este método para buscar todos los elementos que contengan la frase "plan de proyecto" en el asunto, tal como se muestra en este ejemplo.
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a>Ejemplo: buscar elementos mediante una cadena de consulta y EWS
<a name="bk_ExampleEWS"> </a>

En este ejemplo, una solicitud [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) de SOAP busca todos los elementos de la bandeja de entrada con la frase "plan del proyecto" en el asunto. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

En el ejemplo siguiente se muestra la respuesta del servidor con los resultados de la búsqueda.
  
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
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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
- [Usar filtros de búsqueda con EWS en Exchange](how-to-use-search-filters-with-ews-in-exchange.md)    
- [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    


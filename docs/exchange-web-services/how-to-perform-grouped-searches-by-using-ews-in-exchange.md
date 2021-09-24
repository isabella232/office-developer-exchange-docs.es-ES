---
title: Realizar búsquedas agrupadas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 55de92eb-8e8b-4156-8ad9-dd3828024242
description: Descubra cómo realizar búsquedas agrupadas en la API administrada ews o la aplicación EWS dirigidas a Exchange.
ms.openlocfilehash: 6142dccc0be6d81167004964562ad2877e0187f5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513209"
---
# <a name="perform-grouped-searches-by-using-ews-in-exchange"></a>Realizar búsquedas agrupadas mediante EWS en Exchange

Descubra cómo realizar búsquedas agrupadas en la API administrada ews o la aplicación EWS dirigidas a Exchange.
  
Las búsquedas agrupadas son útiles, ya que le dan control sobre cómo se organizan los resultados de la búsqueda. Los resultados de búsqueda organizados pueden facilitar que la aplicación procese los resultados o los muestre a un usuario final de una forma fácil de administrar.
  
La agrupación funciona colocando todos los elementos dentro del conjunto de resultados que tienen el mismo valor de un campo específico en un grupo. Por ejemplo, puede agrupar los resultados por el remitente y todos los elementos de la misma persona estarán en un grupo independiente y los elementos de cada grupo se ordenarán según el orden que especifique en la vista. Los propios grupos se ordenan por un valor agregado en función del campo que elija.
  
**Tabla 1. Métodos de LA API administrada ews y operaciones ews para organizar los resultados de búsqueda**

|**Si quiere...**|**En la API administrada de EWS, use…**|**En EWS, use…**|
|:-----|:-----|:-----|
|Organizar los elementos con el mismo valor en una propiedad específica de los resultados en grupos  <br/> |[Grouping.GroupOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.groupon%28v=exchg.80%29.aspx) <br/> |[Elemento FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) como elemento secundario del [elemento GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx)  <br/> |
|Ordenar los elementos de cada grupo por el valor de una propiedad específica  <br/> |[ItemView.OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) <br/> |[Elemento SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)  <br/> |
|Ordenar los grupos  <br/> |[Grouping.AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) <br/><br/> [Grouping.AggregateType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) <br/><br/> [Grouping.SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) <br/> |**Elemento FieldURI** como elemento secundario del [elemento AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx)<br/><br/> **Atributo Aggregate** en el **elemento AggregateOn**<br/><br/>**Atributo Order** en el **elemento GroupBy**  <br/> |
   
Vamos a ir paso a paso.
  
## <a name="group-results-by-a-specific-property"></a>Agrupar resultados por una propiedad específica
<a name="bk_GroupResults"> </a>

El primer paso para usar la agrupación es seleccionar una propiedad o atributo en los elementos del almacén Exchange, para agrupar por. La API administrada ews las expone como propiedades de clase en las clases correspondientes, mientras que EWS las expone como elementos XML. Puede elegir cualquier propiedad, incluidas las propiedades personalizadas o extendidas, pero resulta útil comprender cómo se agrupan los elementos en función del valor de la propiedad que elija. 

Todos los elementos que tengan el mismo valor en la propiedad por la que elija agrupar se agruparán. Esto puede parecer obvio, pero es un detalle importante. Tenga en cuenta lo que sucede si agrupa por una propiedad de fecha y hora, como [Item.DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) en la API administrada ews o el elemento [DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) en EWS. La intención puede ser organizar los resultados en grupos, con cada grupo que contenga elementos del mismo día. Sin embargo, la agrupación examina todo el valor, que incluye la hora. 

El resultado final es que los elementos se agruparán para que los elementos recibidos al mismo tiempo, hasta el segundo, estén en sus propios grupos. Lo más probable es que los resultados se ordenen en un gran número de grupos con un número reducido de elementos en cada grupo. 
  
Para obtener un conjunto de resultados con un número menor de grupos y un número mayor de elementos en cada grupo, elija una propiedad que probablemente tenga un número menor de valores, como [EmailMessage.From](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) o [Item.Categories](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) en la API administrada ews, o [From](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) o [Categories](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) en EWS. En la siguiente figura se muestra una lista de correos electrónicos que aparecen en una Bandeja de entrada. 
  
**Figura 1. Mensajes en una Bandeja de entrada**

![Muestra de una lista de mensajes en la bandeja de entrada de un usuario.](media/Ex15_GroupedSearch_MsgList.png)
  
Si agrupa los elementos de la figura 1 por la propiedad **EmailMessage.From,** el resultado será dos grupos, uno para los mensajes enviados por Hope Gross y otro para los mensajes enviados por Sadie Daniels. 
  
**Figura 2. Mensajes separados en grupos basados en la propiedad From**

![Una imagen que muestra mensajes ordenados en dos listas por la propiedad De.](media/Ex15_GroupedSearch_SeparateGroups.png)
  
## <a name="sort-the-items-within-groups"></a>Ordenar los elementos dentro de grupos
<a name="bk_SortItems"> </a>

Puede controlar cómo se ordenan los elementos dentro de cada grupo mediante la [propiedad ItemView.OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) en la API administrada ews o el [elemento SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) en EWS. El mismo orden se aplica a cada grupo. Por ejemplo, si ordena los elementos de la figura 1 por la **propiedad Item.DateTimeReceived,** en orden descendente, el elemento recibido más recientemente de Hope Gross será el primero en el grupo Hope Gross y el elemento recibido más recientemente de Sadie Daniels será el primero en el grupo Sadie Daniels. Convenientemente, los grupos de la figura 2 ya están ordenados de esta manera. 
  
## <a name="sort-the-groups"></a>Ordenar los grupos
<a name="bk_SortGroups"> </a>

Ahora que ya tiene los grupos resueltos, el paso final es ordenar los propios grupos. Dado que los propios grupos no tienen valores específicos, el proceso de agrupación debe asignar un valor de ordenación a cada grupo. Esto se realiza agregando los valores de una propiedad específica dentro de cada grupo, especificada por la [propiedad Grouping.AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) en la API administrada ews o el elemento [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) como elemento secundario del [elemento AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) en EWS. La [propiedad Grouping.AggregateType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) de la API administrada ews (o el atributo **Aggregate** del elemento **AggregateOn** en EWS) especifica qué valor de los elementos de cada grupo se asigna al valor de ordenación del grupo, ya sea el valor más grande o el valor más pequeño. Por último, la propiedad [Grouping.SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) de la API administrada ews o el atributo **Order** del elemento [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) de EWS especifican el criterio de ordenación (ascendente o descendente). 
  
Por ejemplo, si los grupos de la figura 2 se ordenan agregando en la propiedad **Item.DateTimeReceived,** usando el valor más pequeño y ordenando en orden descendente, los elementos se devuelven en el orden que se muestra en la figura 3. 
  
**Figura 3. Resultados de búsqueda agrupados con los grupos ordenados por la propiedad DateTimeReceived**

![Una imagen que muestra una lista ordenada de mensajes, agrupados por la propiedad De, con los grupos ordenados por la fecha y hora de recepción más antigua.](media/Ex15_GroupedSearch_Results.png)
  
En las secciones siguientes se muestra cómo puede agrupar y ordenar en el código.
  
## <a name="example-perform-a-grouped-search-by-using-the-ews-managed-api"></a>Ejemplo: Realizar una búsqueda agrupada mediante la API administrada de EWS
<a name="bk_GroupSearchEWSMA"> </a>

Los siguientes métodos de API administrada ews pueden usar la agrupación:
  
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
En el ejemplo siguiente se usa **el método ExchangeService.FindItems;** sin embargo, las mismas reglas y conceptos se aplican al **método Folder.FindItems.** En este ejemplo, se define un **método denominado GroupItemsByFrom.** Toma un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) y un [objeto WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) como parámetros. Solicita los primeros 50 elementos de la carpeta, agrupados por la propiedad **EmailMessage.From,** ordenados por la **propiedad Item.DateTimeReceived** en orden descendente. Los propios grupos se ordenan por el valor de la propiedad **Item.DateTimeReceived** más pequeño de sus elementos, en orden descendente. 
  
En este ejemplo se asume que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx). 
  
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

## <a name="example-perform-a-grouped-search-by-using-ews"></a>Ejemplo: realizar una búsqueda agrupada mediante EWS
<a name="bk_GroupSearchEWS"> </a>

En el siguiente ejemplo de solicitud se muestra una solicitud de operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para los primeros 50 elementos de la carpeta, agrupados por el **elemento From,** ordenados por el elemento **DateTimeReceived** en orden descendente. Los propios grupos se ordenan por el valor del **elemento DateTimeReceived** más pequeño de sus elementos, en orden descendente. 
  
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

El servidor devuelve la siguiente respuesta.
  
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

## <a name="version-differences"></a>Diferencias de versión
<a name="bk_VersionDiffs"> </a>

Las versiones de Exchange a partir de la versión principal 15 y terminando con la compilación 15.0.775.38 devuelven elementos **Group** (del tipo **GroupedItemsType**) en lugar de [elementos GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) en la respuesta SOAP. Si usa la API administrada ews, esto hará que la colección [GroupedFindItemsResults.ItemGroups](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx) contenga 0 objetos. Si usa EWS, los **elementos Group** deben controlarse como **elementos GroupedItems.** 
  
Las versiones Exchange a partir de la versión principal 15 devuelven elementos **Group** o **GroupedItems** adicionales con el atributo **xsi:nil** establecido en **true** en la respuesta SOAP. Si usa la API administrada ews, estos elementos adicionales provocarán que [se inicie una excepción ServiceXmlDeserializationException.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) Si usa EWS, estos elementos adicionales deben omitirse. 
  
## <a name="see-also"></a>Vea también

- [Búsqueda y EWS en Exchange](search-and-ews-in-exchange.md)    
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)   
- [Clase de agrupación](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping%28v=exchg.80%29.aspx)    
- [Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    


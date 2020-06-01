---
title: AggregateOn
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AggregateOn
api_type:
- schema
ms.assetid: 9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb
description: El elemento AggregateOn representa la propiedad que se usa para determinar el orden de los elementos agrupados de un conjunto de resultados FindItem agrupados.
ms.openlocfilehash: 04359c187ef11538d64f8f0d3ea2fe84bc3d048b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463569"
---
# <a name="aggregateon"></a>AggregateOn

El elemento **AggregateOn** representa la propiedad que se usa para determinar el orden de los elementos agrupados de un conjunto de resultados FindItem agrupados. 
  
- [FindItem](finditem.md)  
- [GroupBy](groupby.md)
- [AggregateOn](aggregateon.md)
  
```xml
<AggregateOn>
   <FieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <IndexedFieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <ExtendedFieldURI/>
</AggregateOn>
```
 
**AggregateOnType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Aggregate** <br/> | Indica el valor máximo o mínimo de la propiedad identificada por el elemento [FieldURI](fielduri.md) que se usa para ordenar los grupos de elementos.<br/><br/>Los valores posibles son los siguientes:  <br/><br/>-Mínimo  <br/>-Máximo  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI extendidas para obtener, establecer o crear.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GroupBy](groupby.md) <br/> |Especifica agrupaciones arbitrarias para consultas FindItem.  <br/> La siguiente es la expresión XPath a este elemento:`/FindItem/GroupBy` <br/> |
   
## <a name="remarks"></a>Comentarios

La [operación FindItem](finditem-operation.md) puede devolver resultados agrupados. Dentro de los resultados agrupados, todos los elementos que tienen el mismo valor para una determinada propiedad de agrupación se reúnen y presentan como elementos secundarios de ese grupo. Por ejemplo, si agrupa por remitente, todos los mensajes de correo electrónico se organizan en grupos separados en función de si son del remitente A, del remitente B, etc. Estos grupos son elementos secundarios del grupo de remitentes. 
  
Cada uno de los grupos dentro del grupo de remitentes contiene una colección de elementos, como los correos electrónicos reales que provienen de cada remitente. Puede usar el elemento [SortOrder](sortorder.md) para ordenar los elementos dentro de un grupo. Sin embargo, para ordenar los grupos según los valores de propiedad de un elemento, debe usar agregación. 
  
Con agregación, el orden de los grupos se basa en una propiedad específica de los elementos dentro del grupo. Cuando se usa la agregación para ordenar elementos dentro de un grupo, se debe identificar una propiedad representativa mediante la que se ordenan los grupos. Puede usar el elemento **AggregateOn** para especificar la propiedad Representative. 
  
Cuando se identifica una propiedad representativa, se utiliza el atributo **Aggregate** para indicar si los grupos se ordenan según el valor máximo o mínimo de la propiedad identificada. Si el atributo **Aggregate** se establece en Maximum, los grupos se ordenan comenzando por el valor mayor de la propiedad **AggregateOn** . Si el atributo **Aggregate** se establece en Minimum, los grupos se ordenan comenzando por el valor menor de la propiedad **AggregateOn** . 
  
Por ejemplo, si desea emitir una consulta agrupada de FindItem, agrupando por remitente, pero desea ordenar los grupos para que el grupo con el mensaje de correo electrónico más reciente esté en la parte superior, puede agrupar por remitente y agregado por fecha y hora recibidas con un atributo **agregado** de máximo. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se muestra una solicitud FindItem y una respuesta agrupadas. En el ejemplo se muestra una solicitud para devolver los elementos agrupados por la propiedad **ConversationTopic** . Dos grupos, A y B, se devuelven en orden descendente según el valor máximo de la propiedad [DateTimeReceived](datetimereceived.md) . 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="message:ConversationTopic"/>
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AdditionalProperties>    
      </ItemShape>
      <IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="20" Offset="0"/>
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="message:ConversationTopic"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
<!-- EXAMPLE RESPONSE -->
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>B</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAH=" ChangeKey="CQAAABY" />
                    <t:DateTimeReceived>2006-09-14T23:59:18Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnAHR=" ChangeKey="CQAAAw" />
                    <t:DateTimeReceived>2006-09-15T00:00:24Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnA==" ChangeKey="CQAAJXT" />
                    <t:DateTimeReceived>2006-09-15T00:22:45Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>A</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAAA==" ChangeKey="CQCJNe" />
                    <t:DateTimeReceived>2006-09-14T23:56:12Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQWgAA==" ChangeKey="CQAACJV6" />
                    <t:DateTimeReceived>2006-09-14T23:57:33Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAAA==" ChangeKey="CQA6CJXw" />
                    <t:DateTimeReceived>2006-09-15T00:23:31Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

Para ordenar los elementos de un grupo, use el elemento [SortOrder](sortorder.md) . 
  
> [!NOTE]
> Los identificadores de elemento y las claves de cambio se han abreviado para preservar la legibilidad. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindItem](finditem-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)


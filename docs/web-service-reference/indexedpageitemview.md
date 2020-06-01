---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: El elemento IndexedPageItemView describe la forma en que se devuelve la información de la conversación paginada o del elemento para una operación FindItem o una solicitud de operación FindConversation.
ms.openlocfilehash: 0a66f17855fd425082e3651886d3eeec4f217ac4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456916"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

El elemento **IndexedPageItemView** describe la forma en que se devuelve la información de la conversación paginada o del elemento para una [operación FindItem](finditem-operation.md) o una solicitud de [operación FindConversation](findconversation-operation.md) . 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de elementos o conversaciones que se devolverá en la respuesta. Este atributo es opcional.  <br/> |
|**Offset** <br/> |Describe el desplazamiento desde **BasePoint**. Si **BasePoint** es igual al principio, el desplazamiento es positivo. Si **BasePoint** es igual a end, el desplazamiento se trata como si fuera negativo. Esto identifica qué elemento o conversación será el primero que se entregará en la respuesta. Este atributo es obligatorio.  <br/> |
|**BasePoint** <br/> |Describe si la página de elementos o conversaciones se iniciará desde el principio o el final del conjunto de elementos o conversaciones que se encuentren mediante los criterios de búsqueda. Buscar desde el final siempre busca hacia atrás. Este atributo es obligatorio.  <br/> |
   
#### <a name="basepoint-attribute"></a>Atributo BasePoint

|**Valor**|**Descripción**|
|:-----|:-----|
|Empezar  <br/> |La vista paginada comienza al principio de la conversación encontrada o del conjunto de elementos.  <br/> |
|End  <br/> |La vista paginada comienza al final de la conversación encontrada o del conjunto de elementos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Define una solicitud para buscar conversaciones en un buzón.  <br/> |
   
## <a name="remarks"></a>Comentarios

Buscar desde el final implica moverse al origen identificado por el desplazamiento. Además, el puntero se mueve hacia atrás el número de registros solicitados. Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda se inicia desde 75. Si se devuelven 10 registros, el puntero se mueve hacia atrás unos 10 registros adicionales a 65 y devuelve los registros 65 a 75. El siguiente índice es 64. El siguiente desplazamiento desde el final de una página es 100 menos 64, que es igual a 36. 36 es el valor para el siguiente desplazamiento desde el final para obtener la siguiente página indizada.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se muestra una solicitud de [operación FindItem](finditem-operation.md) . Cada elemento se devuelve con su identificador y asunto. En la respuesta se devuelven un máximo de seis elementos, como se especifica en el atributo **MaxEntriesReturned** . Los elementos se enumeran en orden ascendente agrupados por importancia. Los elementos de un grupo se agregan por asunto. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <IndexedPageItemView MaxEntriesReturned="6" BasePoint="Beginning" Offset="0" />
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)
  
[Operación FindConversation](findconversation-operation.md)


[Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)


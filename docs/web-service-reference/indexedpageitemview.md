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
description: El elemento IndexedPageItemView describe cómo paginada conversación o elemento se devuelve información para una operación FindItem o una solicitud de operación FindConversation.
ms.openlocfilehash: f1743e22087158c1889977f03774fccbc5577390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835919"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

El elemento **IndexedPageItemView** describe cómo paginada conversación o elemento se devuelve información para una solicitud de [operación de FindItem](finditem-operation.md) o [FindConversation](findconversation-operation.md) . 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de elementos o conversaciones para devolver en la respuesta. Este atributo es opcional.  <br/> |
|**Offset** <br/> |Describe el desplazamiento desde el **punto base**. Si el **punto base** es igual al principio, el desplazamiento es positivo. Si el **punto base** es igual a End, el desplazamiento se administra como si fuese negativo. Esto identifica qué elemento o conversación será la primera entregar en la respuesta. Este atributo es necesario.  <br/> |
|**Punto base** <br/> |Describe si la página de elementos o las conversaciones se iniciará desde el principio o al final del conjunto de elementos o las conversaciones que se encuentran mediante el uso de los criterios de búsqueda. Buscar desde el final siempre busca hacia atrás. Este atributo es necesario.  <br/> |
   
#### <a name="basepoint-attribute"></a>Atributo de punto base

|**Valor**|**Descripción**|
|:-----|:-----|
|Principio  <br/> |La vista de página comienza al principio del conjunto de conversación o elemento que se encuentra.  <br/> |
|End  <br/> |Se inicia la vista de página al final del conjunto de conversación o elemento que se encuentra.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Define una solicitud para buscar las conversaciones en un buzón de correo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Buscar desde el final implica mover para el origen identificado por el desplazamiento. Además, el puntero se mueve de nuevo el número de registros solicitados. Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda comienza desde 75. Si se devuelven 10 registros, el puntero se mueve hacia atrás un 10 adicionales a 65 de registros y devuelve los registros 65 a través de 75. El siguiente índice es 64. El desplazamiento desde el final de una página siguiente es 100 menos 64 que es igual a 36. 36 es el valor para el desvío siguiente desde el final para obtener la siguiente página indizada.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una solicitud de [operación FindItem](finditem-operation.md) . Cada elemento se devuelve con su identificador y el asunto. Un máximo de seis artículos se devuelven en la respuesta, tal como se especifica mediante el atributo **MaxEntriesReturned** . Los elementos se muestran en orden ascendente agrupados por importancia. Elementos de un grupo se agregan por asunto. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)
  
[Operación de FindConversation](findconversation-operation.md)


[Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)


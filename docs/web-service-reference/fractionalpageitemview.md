---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: El elemento FractionalPageItemView describe dónde se inicia la vista paginada y el número máximo de elementos que se devuelven en una solicitud FindItem.
ms.openlocfilehash: cbf45838558873dc5846823c2d1b26cf2c8af514
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461313"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

El elemento **FractionalPageItemView** describe dónde se inicia la vista paginada y el número máximo de elementos que se devuelven en una solicitud [FindItem](finditem.md) . 
  
[FindItem](finditem.md)
  
[FractionalPageItemView](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Identifica el número máximo de resultados que se devolverá en la respuesta [FindItem](finditem.md) . Este atributo es opcional. Si no se especifica este atributo, la llamada devolverá todos los elementos disponibles.  <br/> |
|**Numera** <br/> |Representa el numerador del desplazamiento fraccionario desde el inicio del conjunto de resultados. Este atributo es obligatorio. El numerador debe ser igual o menor que el denominador. Este atributo debe representar un valor integral que sea igual o mayor que cero.  <br/> Para obtener más información, vea las notas más adelante en este tema.  <br/> |
|**Denominador** <br/> |Representa el denominador del desplazamiento fraccionario desde el principio del número total de elementos del conjunto de resultados. Este atributo es obligatorio. Este atributo debe representar un valor integral que sea mayor que uno.  <br/> Para obtener más información, vea las notas más adelante en este tema.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El desplazamiento de la vista paginada desde el principio del conjunto de elementos encontrados se describe mediante una fracción. La fracción, definida por los atributos **numerador** y **denominador** , describe dónde comienza la página de información. Por ejemplo, si el **numerador** es igual a cuatro y el **denominador** es cinco, la página de la información devuelta comienza en una entrada que se encuentra cuatro-quintos de la forma en el conjunto de resultados. 
  
Si la fracción da como resultado cero, indica el inicio del conjunto de resultados. Si la fracción da como resultado una, que indica el final del conjunto de resultados.
  
> [!NOTE]
> La fracción representa el punto de inicio de la página, no el número de resultados que se devolverán en el conjunto de resultados. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una solicitud [FindItem](finditem.md) . La solicitud devuelve elementos de los resultados de búsqueda que se inician después del segundo tercio de todos los elementos del conjunto de resultados. 
  
```
<?xml version="1.0" encoding="utf-8"?>
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
      <FractionalPageItemView MaxEntriesReturned="12" Numerator="2" Denominator="3"/>
      <GroupBy Order="Descending">
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

Por ejemplo, si el conjunto de resultados contiene nueve elementos, la vista paginada devolverá hasta 12 elementos, a partir del elemento encontrados dos tercios de la forma en el conjunto de resultados. En este caso, la página comienza en el séptimo elemento. La página contendrá el séptimo, octavo y noveno elemento. Si el numerador se establece en cero, la vista de página devolverá todos los elementos del conjunto de resultados siempre que el número sea menor que el atributo **MaxEntriesReturned** . 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)


[Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)


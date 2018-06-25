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
description: El elemento FractionalPageItemView describe donde se inicia la vista de página y el número máximo de elementos devueltos en una solicitud de FindItem.
ms.openlocfilehash: 38c35d2b68dabfca1a43ab034deaf72c47b0ea66
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764708"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

El elemento **FractionalPageItemView** describe donde se inicia la vista de página y el número máximo de elementos devueltos en una solicitud de [FindItem](finditem.md) . 
  
[FindItem](finditem.md)
  
[FractionalPageItemView](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Identifica el número máximo de resultados a devolver en la respuesta [FindItem](finditem.md) . Este atributo es opcional. Si no se especifica este atributo, la llamada devolverá todos los elementos disponibles.  <br/> |
|**Numerador** <br/> |Representa el numerador de la fraccionario desplazamiento desde el comienzo del conjunto de resultados. Este atributo es necesario. El numerador debe ser igual o menor que el denominador. Este atributo debe representar un valor entero que es igual o mayor que cero.  <br/> Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
|**Denominador** <br/> |Representa el denominador de la fraccionario desplazamiento desde el comienzo del número total de elementos en el conjunto de resultados. Este atributo es necesario. Este atributo debe representar un valor entero que es mayor que uno.  <br/> Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

Se describe el desplazamiento de la vista de página desde el comienzo del conjunto de elementos encontrados por una fracción. La fracción, que se define mediante los atributos **numerador** y **denominador** , describe donde se inicia la página de información. Por ejemplo, si **numerador** es igual a cuatro y **denominador** es igual a cinco, la página de información devuelta que comienza en una entrada que encuentra cuatro quintos de la forma en el conjunto de resultados. 
  
Si el argumento de fracción se evalúa como cero, indica el inicio del conjunto de resultados. Si el argumento de fracción se evalúa como uno, indica el final del conjunto de resultados.
  
> [!NOTE]
> La fracción representa el punto inicial de la página, se devolverán resultados no cuántos en el conjunto de resultados. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una solicitud [FindItem](finditem.md) . La solicitud devuelve los elementos de los resultados de búsqueda que se inician después del segundo en tercer lugar de todos los elementos en el conjunto de resultados. 
  
```
<?xml version="1.0" encoding="utf-8"?>
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

Por ejemplo, si el conjunto de resultados contiene nueve elementos, la vista de página devolverá hasta 12 elementos, empezando por el elemento que se encuentra dos tercios de la forma en el conjunto de resultados. En este caso, la página comienza en el séptimo elemento. La página contendrá el séptimo, octavo y noveno elementos. Si el numerador se establece en cero, la vista de la página devolverá todos los elementos en el conjunto siempre y cuando el número es menor que el atributo **MaxEntriesReturned** de resultados. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)


[Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)


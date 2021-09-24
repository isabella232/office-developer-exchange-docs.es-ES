---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: El elemento FractionalPageItemView describe dónde se inicia la vista paginada y el número máximo de elementos devueltos en una solicitud FindItem.
ms.openlocfilehash: 0d948bad0ba24c4a105be32daa645d1864cb4f3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530249"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

El **elemento FractionalPageItemView** describe dónde se inicia la vista paginada y el número máximo de elementos devueltos en una [solicitud FindItem.](finditem.md) 
  
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
|**MaxEntriesReturned** <br/> |Identifica el número máximo de resultados que se devolverán en la [respuesta FindItem.](finditem.md) Este atributo es opcional. Si no se especifica este atributo, la llamada devolverá todos los elementos disponibles.  <br/> |
|**Numerador** <br/> |Representa el numerador del desplazamiento fraccional desde el inicio del conjunto de resultados. Este atributo es obligatorio. El numerador debe ser igual o menor que el denominador. Este atributo debe representar un valor integral igual o mayor que cero.  <br/> Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
|**Denominador** <br/> |Representa el denominador del desplazamiento fraccional desde el inicio del número total de elementos del conjunto de resultados. Este atributo es obligatorio. Este atributo debe representar un valor integral mayor que uno.  <br/> Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El desplazamiento de vista paginada desde el inicio del conjunto de elementos encontrados se describe mediante una fracción. La fracción, definida por los atributos **Numerador** y **Denominador,** describe dónde comienza la página de información. Por ejemplo, si **Numerador** es igual a cuatro y **Denominador** es igual a cinco, la página de información devuelta comienza en una entrada ubicada cuatro quintas partes del camino en el conjunto de resultados. 
  
Si la fracción se evalúa en cero, esto indica el inicio del conjunto de resultados. Si la fracción se evalúa en uno, esto indica el final del conjunto de resultados.
  
> [!NOTE]
> La fracción representa el punto inicial de la página, no cuántos resultados se devolverán en el conjunto de resultados. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una [solicitud FindItem.](finditem.md) La solicitud devuelve elementos de los resultados de búsqueda que comienzan después del segundo tercio de todos los elementos del conjunto de resultados. 
  
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

Por ejemplo, si el conjunto de resultados contiene nueve elementos, la vista paginada devolverá hasta 12 elementos, empezando por el elemento encontrado dos tercios del camino en el conjunto de resultados. En este caso, la página comienza en el séptimo elemento. La página contendrá los elementos séptimo, octavo y noveno. Si el numerador se establece en cero, la vista de página devolverá todos los elementos del conjunto de resultados siempre que el número sea menor que el **atributo MaxEntriesReturned.** 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindItem](finditem-operation.md)


[Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)


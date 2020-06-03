---
title: QueryString (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: El elemento QueryString contiene una cadena de consulta de buzón basada en la sintaxis de consulta avanzada (AQS).
localization_priority: Priority
ms.openlocfilehash: eafbbab6de8d191197fb4b80e2b8e3cea80ab800
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459191"
---
# <a name="querystring-querystringtype"></a>QueryString (QueryStringType)

El elemento **QueryString** contiene una cadena de consulta de buzón basada en la sintaxis de consulta avanzada (AQS). 
  
```XML
<QueryString/>
```

 **QueryStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|ResetCache  <br/> |Indica que se debe restablecer la memoria caché.  <br/> |
|ReturnDeletedItems  <br/> |Indica que se deben devolver los elementos eliminados.  <br/> |
|ReturnHighlightTerms  <br/> |Indica que deben devolverse los términos resaltados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> La siguiente es la expresión XPath a este elemento:/FindItem.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **QueryString** representa una consulta de buzón que se realiza mediante un subconjunto de la [Sintaxis de consulta avanzada (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx). Vea la sección Comentarios para obtener información sobre las opciones de sintaxis admitidas para las cadenas de consulta.
  
## <a name="remarks"></a>Comentarios

En Exchange Server 2010, este elemento es un tipo de cadena de esquema XML. En las versiones de Exchange a partir de Exchange Server 2013, incluido Exchange Online, el tipo de este elemento es **QueryStringType**. Este cambio no rompe los clientes existentes porque agrega tres nuevos atributos opcionales. 
  
El elemento **QueryString** excluye el uso de restricciones de EWS. AQS en EWS admite tres tipos de restricciones: restricción de fase de Word, restricción de intervalo de fechas y restricción de tipo de mensaje. En las tablas siguientes se enumeran las propiedades de búsqueda admitidas para cada tipo de restricción. 
  
**Restricción de fase de Word**

|**Propiedad**|**Ejemplo**|**Función**|
|:-----|:-----|:-----|
|from  <br/> |De: Dean  <br/> De: "Dean Halstead"  <br/> |Buscar elementos enviados desde Dean.  <br/> Buscar elementos enviados desde Dean Halstead. El remitente debe ser exactamente "Dean Halstead".  <br/> |
|a  <br/> |Para: Dean  <br/> |Buscar elementos enviados a Dean.  <br/> |
|cc  <br/> |CC: Dean  <br/> |Busque los elementos con Dean en la línea CC.  <br/> |
|cco  <br/> |CCO: Dean  <br/> |Busque los elementos con Dean en la línea CCO.  <br/> |
|Participantes  <br/> |Participantes: Dean  <br/> |Busca elementos con Dean en los campos to, CC o BCC.  <br/> |
|Subject  <br/> |Asunto: producto  <br/> Asunto: (desarrollo de producto)  <br/> Asunto: "desarrollo de producto"  <br/> |Busca elementos con producto en el asunto.  <br/> Busca elementos con producto y desarrollo en el asunto.  <br/> |
|Cuerpo  <br/> Contenido  <br/> |Cuerpo: progreso  <br/> Contenido: progreso  <br/> |Busca elementos con progreso en el cuerpo.  <br/> |
|Datos adjuntos  <br/> |Datos adjuntos: informe  <br/> |Busca elementos con informe en el nombre del archivo adjunto o en el cuerpo del archivo.  <br/> |
|(no se especifica la propiedad)  <br/> |Desarrollo de productos  <br/> |Busque elementos que contengan el producto y el desarrollo en todas las propiedades de la fase de Word.  <br/> |
   
La coincidencia de restricción de fase de Word siempre no distingue mayúsculas de minúsculas. La restricción de fase de Word admite dos tipos de coincidencia: coincidencia de prefijo o coincidencia exacta. La coincidencia de prefijo es el comportamiento predeterminado de la coincidencia. Si desea que la coincidencia sea exacta, use comillas dobles. Por ejemplo, asunto: "Product" coincide con "Product", pero no con "Production" en el asunto. Varias palabras en comillas dobles restringen ambas fases de Word y su orden. Por ejemplo, "el producto de" gana "coincide solamente con" producto Win ", no con" Win95 Product "ni" Product of Win ". Puede usar un asterisco ( \* ) para definir una coincidencia de prefijo con Order Restricted. Por ejemplo, "producto Win" \* coincide con "Win95 Product", "Windows Production line" pero no con "Windows New Product" ni "Product of Win". Puede buscar en todos los mensajes enviados desde o hacia un dominio. Por ejemplo, from: "@hotmail. com" devuelve todos los mensajes enviados desde hotmail.com.
  
En la tabla siguiente se describen las restricciones del intervalo de fechas.
  
**Restricción de intervalo de fechas**

|**Propiedad**|**Ejemplo**|**Función**|
|:-----|:-----|:-----|
|Sent  <br/> |Enviado: última semana  <br/> Enviado el: 01/01/2001  <br/> Enviado el: 01/01/2001.. 01/15/2001  <br/> |Elementos de búsqueda enviados la semana pasada.  <br/> Buscar los elementos enviados el 1 de enero de 2001.  <br/> Buscar los elementos enviados entre el 1 de enero de 2001 y el 15 de enero de 2001.  <br/> |
|Cantidad.Recibida  <br/> |Recibido: hoy  <br/> Recibido: 01/01/2001  <br/> |Elementos de búsqueda recibidos hoy.  <br/> Buscar los elementos recibidos el 1 de enero de 2001.  <br/> |
   
Los dos puntos (..) es un operador de rango. Se puede usar para definir un intervalo con una fecha de inicio y una fecha de finalización. Para especificar una fecha, puede usar fechas relativas. Se admiten las siguientes fechas relativas:
  
- Fechas relativas: hoy, mañana, ayer
    
- Fechas relativas a multiword: esta semana, mes próximo, semana pasada, mes pasado o año próximo
    
- Días: Domingo, lunes, martes, miércoles, jueves, viernes, sábado
    
- Enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre
    
En la tabla siguiente se describen las restricciones de tipo de mensaje. 
  
**Restricción de tipo de mensaje**

|**Propiedad**|**Ejemplo**|**Función**|
|:-----|:-----|:-----|
|Tipo  <br/> |Tipo: tareas  <br/> |Buscar en todos los elementos de tarea.  <br/> |
   
AQS en EWS usa la propiedad **Kind** para especificar el tipo de mensaje. La propiedad Kind se puede usar con los siguientes tipos de elemento: 
  
- email
    
- reuniones
    
- tasks
    
- notas
    
- documentos
    
- diarios
    
- contacts
    
- mensajería instantánea
    
En la siguiente tabla se describen los conectores lógicos de agrupación.
  
**Agrupación de conectores lógicos**

|**Connector**|**Ejemplo**|**Función**|
|:-----|:-----|:-----|
|Y  <br/> |Asunto: producto y asunto: desarrollo  <br/> Asunto: (Product y Development)  <br/> Asunto: (desarrollo de producto)  <br/> |Buscar elementos con el producto y el desarrollo en el asunto.  <br/> |
|O  <br/> |Cuerpo: proyecto o cuerpo: propuesta  <br/> Cuerpo: (proyecto o propuesta)  <br/> |Buscar elementos con el producto o el desarrollo en el cuerpo.  <br/> |
|NO  <br/> |NO cuerpo: propuesta  <br/> Cuerpo: (no propuesta)  <br/> |Buscar mensajes sin propuestas en el cuerpo.  <br/> |
   
Y siempre es el conector predeterminado. Por ejemplo, asunto: proyecto y cuerpo: la propuesta es la misma que el asunto: cuerpo del proyecto: propuesta. Los conectores lógicos distinguen mayúsculas de minúsculas. Por ejemplo, Body: (proyecto o propuesta) busca los mensajes con "Project", "o", y "proposar" en el cuerpo en lugar de "Project" o "proposar". El símbolo más (+) equivale a y. El símbolo de guión (-) equivale a no. Por ejemplo, Body: (Project-Proposal) busca los mensajes con ' Project ' pero sin ' proposar ' en el cuerpo. 
  
La cadena de consulta también puede contener propiedades no indizadas para la búsqueda. Si la cadena de consulta contiene propiedades no indizadas, la búsqueda puede realizar una búsqueda de Exchange en las propiedades indizadas y una búsqueda de almacén en las propiedades no indizadas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se muestra una solicitud para buscar mensajes en la bandeja de entrada con la detección automática en el asunto.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:Autodiscover</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" 
                        TotalItemsInView="5" 
                        IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkADEzOTExYjJkLTYx" ChangeKey="CQAAABY" />
                <t:Subject>How to use Autodiscover</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

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


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


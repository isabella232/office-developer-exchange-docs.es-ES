---
title: QueryString (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: El elemento de cadena de consulta contiene una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).
ms.openlocfilehash: 410405638b3f8628dc589049873cfea1f153310c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836943"
---
# <a name="querystring-querystringtype"></a>QueryString (QueryStringType)

El elemento de **cadena de consulta** contiene una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS). 
  
```XML
<QueryString/>
```

 **QueryStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|ResetCache  <br/> |Indica que se debe restablecer la memoria caché.  <br/> |
|ReturnDeletedItems  <br/> |Indica que se deben devolver los elementos eliminados.  <br/> |
|ReturnHighlightTerms  <br/> |Indica que se deben devolver el resaltado términos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento: /FindItem.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento de **cadena de consulta** representa una consulta de buzón de correo que se realiza mediante el uso de un subconjunto de la [Sintaxis de consulta avanzada (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx). Vea la sección Comentarios para obtener información acerca de las opciones de sintaxis admitida para cadenas de consulta.
  
## <a name="remarks"></a>Notas

En Exchange Server 2010, este elemento es un tipo de cadena de esquema XML. En las versiones de Exchange Server 2013 a partir de Exchange, incluido Exchange Online, el tipo de este elemento es **QueryStringType**. Este cambio no interrumpen a los clientes existentes ya que agrega tres nuevos atributos opcionales. 
  
El elemento **QueryString** excluye el uso de restricciones de EWS. AQS en EWS admite tres tipos de restricciones: restricción de fase, restricción de intervalo de fecha y restricción de tipo de mensaje de word. Las siguientes tablas enumeran las propiedades de búsqueda admitidos para cada tipo de restricción. 
  
**Restricción de la fase de Word**

|**Propiedad**|**Ejemplo**|**Funci�n**|
|:-----|:-----|:-----|
|from  <br/> |Desde: Dean  <br/> De: "Dean Halstead"  <br/> |Buscar artículos enviados desde Dean.  <br/> Buscar artículos enviados desde Dean Halstead. El remitente debe ser exactamente "Dean Halstead".  <br/> |
|a  <br/> |Para: Dean  <br/> |Buscar elementos enviados a Dean.  <br/> |
|cc  <br/> |Cc:Dean  <br/> |Buscar elementos con Dean en la línea Cc.  <br/> |
|bcc  <br/> |BCC:Dean  <br/> |Buscar elementos con Dean en la línea CCO.  <br/> |
|Participantes  <br/> |Los participantes: Dean  <br/> |Buscar elementos con Dean en para, Cc o CCO campos.  <br/> |
|Subject  <br/> |Asunto: producto  <br/> Asunto:(product development)  <br/> Asunto: "desarrollo de productos"  <br/> |Buscar elementos con el producto en el asunto.  <br/> Buscar elementos con productos y desarrollo en el asunto.  <br/> |
|Cuerpo  <br/> Contenido  <br/> |Cuerpo: progreso  <br/> Contenido: progreso  <br/> |Buscar elementos con el progreso en el cuerpo.  <br/> |
|Datos adjuntos  <br/> |Datos adjuntos: informe  <br/> |Buscar elementos con el informe en el cuerpo de archivo o nombre de archivo de datos adjuntos.  <br/> |
|(no se especifica la propiedad)  <br/> |Desarrollo de productos  <br/> |Buscar elementos que contienen productos y desarrollo en todas las propiedades de fase de word.  <br/> |
   
Coincidencia de restricción de la fase de Word siempre distingue mayúsculas de minúsculas. Restricción de la fase de Word admite dos tipos de coincidencia: coincidencia de prefijo o coincidencia exacta. Coincidencia de prefijo es el comportamiento predeterminado de coincidencia. Si desea que la coincidencia exacta, utilice comillas dobles. Por ejemplo, subject: "product" coincide con 'producto' pero no 'producción' en el asunto. Varias palabras dobles restringen las fases de word y su orden. Por ejemplo "win del producto" coincide con sólo 'win del producto', no 'producto Windows 95' o 'producto de win'. Puede usar un asterisco (\*) para definir una coincidencia de prefijo con orden restringido. Por ejemplo, "win del producto"\* coincide con 'producto Windows 95', 'línea de producción de windows' pero no 'nuevo producto de windows' o 'producto de win'. Puede buscar todos los mensajes enviados desde o a un dominio. Por ejemplo, from:"@hotmail.com" devuelve todos los mensajes enviados desde hotmail.com.
  
En la siguiente tabla se describe las restricciones de intervalo de fecha.
  
**Restricción de intervalo de fecha**

|**Propiedad**|**Ejemplo**|**Funci�n**|
|:-----|:-----|:-----|
|Enviado  <br/> |Enviado: última semana  <br/> Enviado: 01/01/2001  <br/> Sent:01/01/2001..01/15/2001  <br/> |Buscar artículos envían última semana.  <br/> Buscar elementos enviados en 1 de enero de 2001.  <br/> Buscar artículos enviados entre el 1 de enero de 2001 y el 15 de enero de 2001.  <br/> |
|Cantidad.Recibida  <br/> |Recibido: hoy mismo  <br/> Recibido: 01/01/2001  <br/> |Buscar elementos recibidos hoy.  <br/> Buscar elementos recibidos en 1 de enero de 2001.  <br/> |
   
Los dos puntos (.) es un operador de rango. Se puede usar para definir un intervalo con un inicio y una fecha de finalización. Para especificar una fecha, puede usar fechas relativas. Se admiten las fechas relativas siguientes:
  
- Fechas relativas: hoy, mañana, ayer
    
- Fechas relativas varias palabras: esta semana, mes siguiente, la última semana, más allá de mes o año siguiente
    
- Días: Domingo, el lunes, el martes, el miércoles, el jueves, el viernes, sábado
    
- Enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre
    
En la siguiente tabla se describe las restricciones de tipo de mensaje. 
  
**Restricción del tipo de mensaje**

|**Propiedad**|**Ejemplo**|**Funci�n**|
|:-----|:-----|:-----|
|Tipo  <br/> |Tipo: tareas  <br/> |Buscar todos los elementos de tarea.  <br/> |
   
AQS en EWS usa la propiedad **Kind** para especificar el tipo de mensaje. La propiedad Kind se puede usar con los siguientes tipos de elemento: 
  
- email
    
- reuniones
    
- tasks
    
- notas
    
- documentos
    
- diarios
    
- contactos
    
- mensajería instantánea
    
En la siguiente tabla se describe los conectores de la lógicos de agrupación.
  
**Conectores de agrupación lógicos**

|**Connector**|**Ejemplo**|**Funci�n**|
|:-----|:-----|:-----|
|AND  <br/> |Asunto: producto y asunto: desarrollo  <br/> Asunto:(product AND development)  <br/> Asunto:(product development)  <br/> |Buscar elementos con productos y desarrollo en el asunto.  <br/> |
|O  <br/> |Cuerpo: proyecto o cuerpo: propuesta  <br/> Cuerpo de:(project OR proposal)  <br/> |Buscar elementos con el producto o desarrollo en el cuerpo.  <br/> |
|NOT  <br/> |NO: propuesta de cuerpo  <br/> Cuerpo:(NOT proposal)  <br/> |Buscar mensajes sin propuesta en el cuerpo.  <br/> |
   
Y siempre es el conector de forma predeterminada. Por ejemplo, asunto: project AND cuerpo: propuesta es el mismo que el cuerpo: propuesta de asunto: proyecto. Conectores lógicos distinguen mayúsculas de minúsculas. Por ejemplo, body:(project Or proposal) busca los mensajes con 'proyecto', 'o' y 'propuesta' en el cuerpo en lugar de 'proyecto' o 'propuesta'. El signo más (+) es equivalente a and. El símbolo de guión (-) es equivalente a NOT. Por ejemplo, body:(project-proposal) busca mensajes con 'project' pero sin 'propuesta' en el cuerpo. 
  
La cadena de consulta también puede contener propiedades no indizadas para la búsqueda. Si la cadena de consulta contiene propiedades no indizadas, la búsqueda puede realizar una búsqueda de Exchange en las propiedades indizadas y una búsqueda de almacenamiento en las propiedades no indizadas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una solicitud para buscar mensajes en la Bandeja de entrada con detección automática en el asunto.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindItem](finditem-operation.md)
  
[Operación de FindConversation](findconversation-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


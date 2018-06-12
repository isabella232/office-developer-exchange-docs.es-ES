---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: El elemento MimeContentUTF8 contiene la secuencia de UTF-8 MIME de un objeto que se representa en formato base64Binary y admite internalización de dirección de correo electrónico y [RFC6530].
ms.openlocfilehash: 47599b6634738fd488e5b020f69e36d5fcf550a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836466"
---
# <a name="mimecontentutf8"></a>MimeContentUTF8

El elemento **MimeContentUTF8** contiene la secuencia de UTF-8 MIME de un objeto que se representa en formato base64Binary y admite internalización de dirección de correo electrónico y [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Conjunto de caracteres** <br/> |Si se establece, el valor para este atributo se omite el servidor.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[CalendarItem](calendaritem.md) | [contacto](contact.md) | [DistributionList](distributionlist.md) | [elemento](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [ MeetingResponse](meetingresponse.md) | [mensaje](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto que representa una secuencia MIME base64binary es necesario si se usa este elemento.
  
## <a name="remarks"></a>Notas

El contenido del mensaje circula a través de los tres niveles siguientes de codificación antes de que se almacene en el valor de **MimeContentUTF8** : 
  
1. Texto del mensaje: este es el cuerpo de la codificación, como iso-2022-jp para caracteres en japonés.
    
2. Secuencia MIME: se trata de la codificación UTF8 del texto del mensaje para el elemento de **MimeContentUTF8** o la codificación ASCII del texto del mensaje para el elemento [MimeContent](mimecontent.md) . 
    
3. Documento XML — siempre es la secuencia de ASCII con codificación base64 de la secuencia MIME, donde caracteres como '\<', que son significativas para XML, están ocultos de los analizadores XML.
    
Cada nivel es independiente del nivel que le precede.
  
El elemento **MimeContentUTF8** podría contener los mismos datos que contienen otras propiedades que se devuelven con un elemento. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
### <a name="version-differences"></a>Diferencias de versión

Este elemento está disponible en las versiones de Exchange a partir de compilación 15.00.0986.00.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


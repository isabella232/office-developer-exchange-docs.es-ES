---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: El elemento MimeContent contiene la secuencia ASCII MIME de un objeto que se representa en formato base64Binary y es compatible con [RFC2045].
ms.openlocfilehash: 60f2d42f09347611559137c494d93036f1192829
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836465"
---
# <a name="mimecontent"></a>MimeContent

El elemento **MimeContent** contiene la secuencia ASCII MIME de un objeto que se representa en formato base64Binary y es compatible con [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).
  
```xml
<MimeContent CharacterSet="" />
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

Un valor de texto que representa una secuencia MIME base64Binary es necesario si se usa este elemento.
  
## <a name="remarks"></a>Comentarios

El contenido del mensaje circula a través de los tres niveles siguientes de codificación antes de que se almacene en el valor de **MimeContent** : 
  
1. Texto del mensaje: este es el cuerpo de la codificación, como iso-2022-jp para caracteres en japonés.
    
2. Secuencia MIME: se trata de la codificación ASCII del texto del mensaje para el elemento de **MimeContent** o la codificación UTF8 del texto del mensaje para el elemento [MimeContentUTF8](mimecontentutf8.md) . 
    
3. Documento XML — siempre es la secuencia de ASCII con codificación base64 de la secuencia MIME, donde caracteres como '\<', que son significativas para XML, están ocultos de los analizadores XML.
    
Cada nivel es independiente del nivel que le precede.
  
El elemento **MimeContent** podría contener los mismos datos que contienen otras propiedades que se devuelven con un elemento. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


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
description: El elemento MimeContent contiene la secuencia MIME ASCII de un objeto representado en formato base64Binary y compatible con [RFC2045].
ms.openlocfilehash: 039ef1245d48e4cf13141970921dd210f4bd7d06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530439"
---
# <a name="mimecontent"></a>MimeContent

El elemento **MimeContent** contiene la secuencia MIME ASCII de un objeto representado en formato base64Binary y compatible con [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).
  
```xml
<MimeContent CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**CharacterSet** <br/> |Si se establece, el valor de este atributo es ignorado por el servidor.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[CalendarItem](calendaritem.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)  |  [Elemento](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  Propiedad [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se necesita un valor de texto que represente una secuencia MIME base64Binary.
  
## <a name="remarks"></a>Comentarios

El contenido del mensaje pasa por los tres niveles siguientes de codificación antes de almacenarse en el valor **MimeContent** : 
  
1. Texto del mensaje: esta es la codificación del cuerpo, como ISO-2022-JP para caracteres japoneses.
    
2. Secuencia MIME: es la codificación ASCII del texto del mensaje para el elemento **MimeContent** , o la codificación UTF8 del texto del mensaje para el elemento [MimeContentUTF8](mimecontentutf8.md) . 
    
3. Documento XML: siempre es la secuencia ASCII codificada en Base64 de la secuencia MIME, donde los caracteres como ' \< ', que son significativos para XML, están ocultos a los analizadores XML.
    
Cada nivel es independiente del nivel que le precede.
  
El elemento **MimeContent** puede contener los mismos datos que contienen otras propiedades que se devuelven con un elemento. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


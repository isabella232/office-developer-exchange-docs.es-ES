---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: El elemento MimeContentUTF8 contiene la secuencia MIME UTF-8 de un objeto representado en formato base64Binary y admite la internacionalización de direcciones de correo electrónico y [RFC6530].
ms.openlocfilehash: f0ab38368d3a18be38f63c86183a238e2fd0a474
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540758"
---
# <a name="mimecontentutf8"></a>MimeContentUTF8

El **elemento MimeContentUTF8** contiene la secuencia MIME UTF-8 de un objeto que se representa en formato base64Binary y admite la internacionalización de direcciones de correo electrónico y [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**CharacterSet** <br/> |Si se establece, el servidor omite el valor de este atributo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[CalendarItem](calendaritem.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)  |  [Elemento](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Mensaje](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto que representa una secuencia MIME base64binary.
  
## <a name="remarks"></a>Comentarios

El contenido del mensaje pasa por los tres niveles siguientes de codificación antes de almacenarlo en el **valor MimeContentUTF8:** 
  
1. Texto del mensaje: esta es la codificación del cuerpo, como iso-2022-jp para caracteres japoneses.
    
2. Secuencia MIME: se trata de la codificación UTF8 del texto del mensaje para el **elemento MimeContentUTF8** o la codificación ASCII del texto del mensaje [para el elemento MimeContent.](mimecontent.md) 
    
3. Documento XML: siempre es la secuencia ASCII codificada en base64 de la secuencia MIME, donde los caracteres como ' ', que son significativos para XML, se ocultan de los analizadores \< XML.
    
Cada nivel es independiente del nivel que le precede.
  
El **elemento MimeContentUTF8** puede contener los mismos datos que otras propiedades que se devuelven con un elemento. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
### <a name="version-differences"></a>Diferencias de versión

Este elemento está disponible en versiones de Exchange a partir de la compilación 15.00.0986.00.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: El elemento AttachmentShape identifica propiedades adicionales que se van a devolver en una respuesta a una solicitud GetAttachment.
ms.openlocfilehash: e70fbaad0f649c5afdc151b777efef0f8927ba1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529668"
---
# <a name="attachmentshape"></a>AttachmentShape

El elemento **AttachmentShape** identifica propiedades adicionales que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) . 
  
- [GetAttachment](getattachment.md)
  
- [AttachmentShape](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 **AttachmentResponseShapeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[IncludeMimeContent](includemimecontent.md) <br/> |Especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos en la respuesta. Este elemento es opcional.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifica cómo se aplica formato al texto del cuerpo en la respuesta. Este elemento es opcional.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Especifica si se filtra contenido HTML potencialmente no seguro de datos adjuntos. Este elemento es opcional.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica las propiedades adicionales que se devolverán en una respuesta. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |Elemento que define una solicitud para obtener datos adjuntos de un buzón de correo en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetAttachment](getattachment-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


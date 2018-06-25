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
description: El elemento AttachmentShape identifica propiedades adicionales para devolver en una respuesta a una solicitud de GetAttachment.
ms.openlocfilehash: dc6769faa5fd28ce31b796f86c507aec54abff7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763571"
---
# <a name="attachmentshape"></a>AttachmentShape

El elemento **AttachmentShape** identifica propiedades adicionales para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) . 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[IncludeMimeContent](includemimecontent.md) <br/> |Especifica si el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos se devuelve en la respuesta. Este elemento es opcional.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifica cómo se da el formato de texto del cuerpo en la respuesta. Este elemento es opcional.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Especifica si el contenido HTML potencialmente no segura se filtra desde un archivo adjunto. Este elemento es opcional.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica las propiedades adicionales para devolver en una respuesta. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |El elemento que define una solicitud para obtener datos adjuntos de un buzón en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetAttachment](getattachment-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


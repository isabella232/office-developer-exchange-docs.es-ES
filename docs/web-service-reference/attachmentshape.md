---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: El elemento AttachmentShape identifica propiedades adicionales para devolver en una respuesta a una solicitud GetAttachment.
ms.openlocfilehash: 2c7ceb25f481ec07577117e46e26537e657e18c7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520041"
---
# <a name="attachmentshape"></a>AttachmentShape

El **elemento AttachmentShape** identifica propiedades adicionales para devolver en una respuesta a una [solicitud GetAttachment.](getattachment.md) 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[IncludeMimeContent](includemimecontent.md) <br/> |Especifica si el contenido de extensiones de correo de Internet multipropósito (MIME) de un elemento o datos adjuntos se devuelve en la respuesta. Este elemento es opcional.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifica cómo se formatea el texto del cuerpo en la respuesta. Este elemento es opcional.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Especifica si el contenido HTML potencialmente no seguro se filtra desde datos adjuntos. Este elemento es opcional.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica propiedades adicionales para devolver en una respuesta. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |Elemento que define una solicitud para obtener datos adjuntos de un buzón en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetAttachment](getattachment-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


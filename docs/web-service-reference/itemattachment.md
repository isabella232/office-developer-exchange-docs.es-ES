---
title: ItemAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemAttachment
api_type:
- schema
ms.assetid: 089ee599-f45e-46f5-a18a-5cfb3d2851ff
description: El elemento ItemAttachment representa un elemento de Exchange que está vinculado a otro elemento de Exchange.
ms.openlocfilehash: 87e0331664f1fdf8857afc78500014d138f05401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836137"
---
# <a name="itemattachment"></a>ItemAttachment

El elemento **ItemAttachment** representa un elemento de Exchange que está vinculado a otro elemento de Exchange. 
  
```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Item/>
</ItemAttachment>
```

 **ItemAttachmentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifica los datos adjuntos.  <br/> |
|[Nombre (AttachmentType)](name-attachmenttype.md) <br/> |Representa el nombre de los datos adjuntos.  <br/> |
|[ContentType](contenttype.md) <br/> |Describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de los datos adjuntos.  <br/> |
|[ContentId](contentid.md) <br/> |Representa un identificador para el contenido de los datos adjuntos. [ContentId](contentid.md) se puede establecer en cualquier valor de cadena. Las aplicaciones pueden usar [ContentId](contentid.md) para implementar sus propios mecanismos de identificación.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.  <br/> |
|[Size](size.md) <br/> |Representa el tamaño en bytes del archivo adjunto.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Representa cuando se modificó por última vez los datos adjuntos.  <br/> |
|[IsInline](isinline.md) <br/> |Representa si el archivo adjunto aparece en línea dentro de un elemento.  <br/> |
|[Item](item.md) <br/> |Representa los datos adjuntos un elemento genérico de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa los datos adjuntos un mensaje de correo electrónico de Exchange.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa los datos adjuntos un elemento de calendario de Exchange.  <br/> |
|[Contact](contact.md) <br/> |Representa datos adjuntos del elemento de contacto de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa datos adjuntos de tareas de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos que están adjuntos a un elemento en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

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


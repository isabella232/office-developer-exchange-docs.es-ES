---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: El elemento FileAttachment representa un archivo que se adjunta a un elemento en el almacén de Exchange.
ms.openlocfilehash: 5ce7aef753313aa9430f640bb3c26f652b8c1c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764600"
---
# <a name="fileattachment"></a>FileAttachment

El elemento **FileAttachment** representa un archivo que se adjunta a un elemento en el almacén de Exchange. 
  
```XML
<FileAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <IsContactPhoto/>
   <Content/>
</FileAttachment>
```

 **FileAttachmentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifica el archivo adjunto.  <br/> |
|[Nombre (AttachmentType)](name-attachmenttype.md) <br/> |Representa el nombre de los datos adjuntos.  <br/> |
|[ContentType](contenttype.md) <br/> |Describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de los datos adjuntos.  <br/> |
|[ContentId](contentid.md) <br/> |Representa un identificador para el contenido de los datos adjuntos. [ContentId](contentid.md) se puede establecer en cualquier valor de cadena. Las aplicaciones pueden usar [ContentId](contentid.md) para implementar sus propios mecanismos de identificación.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.  <br/> |
|[Size](size.md) <br/> |Representa el tamaño en bytes del archivo adjunto.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Representa cuando se modificó por última vez el archivo adjunto.  <br/> |
|[IsInline](isinline.md) <br/> |Representa si el archivo adjunto aparece en línea dentro de un elemento.  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |Indica si el archivo adjunto es una imagen del contacto.  <br/> |
|[Contenido](content.md) <br/> |Contiene el contenido con codificación Base64 de los datos adjuntos del archivo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.  <br/> |
   
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


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
description: El elemento FileAttachment representa un archivo que está adjunto a un elemento en el almacén de Exchange.
ms.openlocfilehash: db9b541fb2527ae3c09cbdb33bedea7fb215bd30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461019"
---
# <a name="fileattachment"></a>FileAttachment

El elemento **FileAttachment** representa un archivo que está adjunto a un elemento en el almacén de Exchange. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifica los datos adjuntos del archivo.  <br/> |
|[Nombre (AttachmentType)](name-attachmenttype.md) <br/> |Representa el nombre de los datos adjuntos.  <br/> |
|[ContentType](contenttype.md) <br/> |Describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de datos adjuntos.  <br/> |
|[ContentId](contentid.md) <br/> |Representa un identificador para el contenido de un dato adjunto. [Contentid](contentid.md) se puede establecer en cualquier valor de cadena. Las aplicaciones pueden usar [contentid](contentid.md) para implementar sus propios mecanismos de identificación.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.  <br/> |
|[Tamaño](size.md) <br/> |Representa el tamaño en bytes de los datos adjuntos del archivo.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Representa el momento en que se modificó por última vez el archivo adjunto.  <br/> |
|[IsInline](isinline.md) <br/> |Indica si los datos adjuntos aparecen en línea dentro de un elemento.  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |Indica si el archivo adjunto es una imagen de contacto.  <br/> |
|[Content](content.md) <br/> |Contiene el contenido codificado en base64 del archivo de datos adjuntos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

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


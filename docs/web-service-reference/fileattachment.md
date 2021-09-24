---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: El elemento FileAttachment representa un archivo adjunto a un elemento del Exchange almacén.
ms.openlocfilehash: 66424fefafd2084bf0b6f45881089448593e621d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518501"
---
# <a name="fileattachment"></a>FileAttachment

El **elemento FileAttachment** representa un archivo adjunto a un elemento del Exchange almacén. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifica los datos adjuntos del archivo.  <br/> |
|[Name (AttachmentType)](name-attachmenttype.md) <br/> |Representa el nombre de los datos adjuntos.  <br/> |
|[ContentType](contenttype.md) <br/> |Describe el tipo Multipurpose Internet Mail Extensions (MIME) del contenido de datos adjuntos.  <br/> |
|[ContentId](contentid.md) <br/> |Representa un identificador del contenido de los datos adjuntos. [ContentId](contentid.md) se puede establecer en cualquier valor de cadena. Las aplicaciones pueden usar [ContentId](contentid.md) para implementar sus propios mecanismos de identificación.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.  <br/> |
|[Tamaño](size.md) <br/> |Representa el tamaño en bytes de los datos adjuntos del archivo.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Representa cuándo se modificaron por última vez los datos adjuntos del archivo.  <br/> |
|[IsInline](isinline.md) <br/> |Representa si los datos adjuntos aparecen en línea dentro de un elemento.  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |Indica si los datos adjuntos del archivo son una imagen de contacto.  <br/> |
|[Contenido](content.md) <br/> |Contiene el contenido codificado en Base64 de los datos adjuntos del archivo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos adjuntos a un elemento del Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: El elemento AttachmentId identifica un elemento o datos adjuntos de archivo. Este elemento se usa en las respuestas CreateAttachment.
ms.openlocfilehash: a6363fad4e7ef9f0c21377f2c1ea8c19c494cdef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522022"
---
# <a name="attachmentid"></a>AttachmentId

El **elemento AttachmentId** identifica un elemento o datos adjuntos de archivo. Este elemento se usa en las respuestas CreateAttachment. 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 **AttachmentIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identifica el identificador único de los datos adjuntos.  <br/> |
|**RootItemId** <br/> |Identifica el identificador único del elemento de almacén raíz al que se adjuntan los datos adjuntos.  <br/> |
|**RootItemChangeKey** <br/> |Identifica la clave de cambio del elemento de almacén raíz al que se adjuntan los datos adjuntos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Representa un Exchange que se adjunta a otro Exchange elemento.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Representa un archivo adjunto a un elemento del Exchange almacén.  <br/> |
   
## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que cuando se crea un dato adjunto, se modifica la clave de cambio del elemento raíz.
  
El [elemento AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) se usa en las solicitudes DeleteAttachment y GetAttachment. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


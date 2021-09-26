---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: El elemento GetAttachment es el elemento raíz de una solicitud para obtener datos adjuntos del Exchange almacén.
ms.openlocfilehash: 057b42e78845f583cf1e52804e0108f335ef951c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546374"
---
# <a name="getattachment"></a>GetAttachment

El **elemento GetAttachment** es el elemento raíz de una solicitud para obtener datos adjuntos del Exchange almacén. 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 **GetAttachmentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |Identifica propiedades de elementos extendidas adicionales para devolver en una respuesta a una [solicitud GetAttachment.](getattachment.md) Este elemento es opcional.  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |Contiene una matriz de identificadores de datos adjuntos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El [elemento AttachmentShape](attachmentshape.md) no es necesario para identificar las propiedades devueltas en la respuesta. La [operación GetAttachment](getattachment-operation.md) devuelve las propiedades Name, ContentType, ContentId, ContentLocation y Content para datos adjuntos de archivos. Para los datos adjuntos de elementos, las propiedades devueltas son Name, ContentType, ContentId, ContentLocation y todas las propiedades del elemento adjunto. Esto equivale a usar la forma base AllProperties en una [solicitud GetItem.](getitem.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación GetAttachment](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)


---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: El elemento GetAttachment es el elemento raíz de una solicitud para obtener datos adjuntos del almacén de Exchange.
ms.openlocfilehash: d03d086ff443db87b0104a2ec83599eb9eaea6b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463982"
---
# <a name="getattachment"></a>GetAttachment

El elemento **GetAttachment** es el elemento raíz de una solicitud para obtener datos adjuntos del almacén de Exchange. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |Identifica las propiedades adicionales de elementos extendidos que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) . Este elemento es opcional.  <br/> |
|[Identificadores](attachmentids.md) <br/> |Contiene una matriz de identificadores de datos adjuntos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El elemento [AttachmentShape](attachmentshape.md) no es necesario para identificar las propiedades devueltas en la respuesta. La [operación GetAttachment](getattachment-operation.md) devuelve el nombre, ContentType, contentid, ContentLocation y las propiedades de contenido de los datos adjuntos de archivo. Para los datos adjuntos de elementos, las propiedades devueltas son el nombre, ContentType, ContentId, ContentLocation y todas las propiedades del elemento adjunto. Esto equivale a usar la forma base AllProperties en una solicitud [GetItem](getitem.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetAttachment](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)


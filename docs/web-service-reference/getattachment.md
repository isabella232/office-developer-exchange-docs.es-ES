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
description: El elemento de GetAttachment es el elemento raíz en una solicitud para obtener datos adjuntos desde el almacén de Exchange.
ms.openlocfilehash: fb639c86a0654e8f9e9601310f7c2f5b0fc7d729
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764756"
---
# <a name="getattachment"></a>GetAttachment

El elemento de **GetAttachment** es el elemento raíz en una solicitud para obtener datos adjuntos desde el almacén de Exchange. 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 **GetAttachmentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |Identifica las propiedades de elemento extendido adicional para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) . Este elemento es opcional.  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |Contiene una matriz de identificadores de los datos adjuntos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El elemento [AttachmentShape](attachmentshape.md) no es necesario para identificar las propiedades devueltas en la respuesta. La [operación GetAttachment](getattachment-operation.md) devuelve el nombre, ContentType, ContentId, ContentLocation y las propiedades de contenido para datos adjuntos de archivo. Los datos adjuntos de elemento, las propiedades devueltas son el nombre, ContentType, ContentId, ContentLocation y las propiedades de todos los adjuntos del elemento. Esto es equivalente al uso de la forma base AllProperties en una solicitud [GetItem](getitem.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetAttachment](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)


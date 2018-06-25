---
title: CreateAttachmentResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachmentResponse
api_type:
- schema
ms.assetid: cf6bd8bb-5317-4a03-bd75-297dd359b5da
description: El elemento CreateAttachmentResponse define una respuesta a una solicitud de CreateAttachment.
ms.openlocfilehash: dfc86516c5737296bc32330583fa63c36e9e63a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763914"
---
# <a name="createattachmentresponse"></a>CreateAttachmentResponse

El elemento **CreateAttachmentResponse** define una respuesta a una solicitud de CreateAttachment. 
  
```xml
<CreateAttachmentResponse>
   <ResponseMessages/>
</CreateAttachmentResponse>
```

 **CreateAttachmentResponseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación CreateAttachment](createattachment-operation.md)
  
[CreateAttachment](createattachment.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


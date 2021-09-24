---
title: AttachmentIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: El elemento AttachmentIds contiene una matriz de identificadores de datos adjuntos.
ms.openlocfilehash: a631edbd1b82f3bbf7b99014d623fbb0072bb0c8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525137"
---
# <a name="attachmentids"></a>AttachmentIds

El **elemento AttachmentIds** contiene una matriz de identificadores de datos adjuntos. 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 **NonEmptyArrayOfRequestAttachmentIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) <br/> |Elemento que identifica un único dato adjunto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DeleteAttachment](deleteattachment.md) <br/> |Elemento que define una solicitud para eliminar datos adjuntos del Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/DeleteAttachment` <br/> |
|[GetAttachment](getattachment.md) <br/> |Elemento que define una solicitud para obtener datos adjuntos del Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación DeleteAttachment](deleteattachment-operation.md)
- [Operación GetAttachment](getattachment-operation.md)


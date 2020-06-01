---
title: Identificadores
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: El elemento identificadores contiene una matriz de identificadores de datos adjuntos.
ms.openlocfilehash: cff1cb5658690fd6dd2c6a7812e1f600a4c80e29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464255"
---
# <a name="attachmentids"></a>Identificadores

El elemento **identificadores** contiene una matriz de identificadores de datos adjuntos. 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 **NonEmptyArrayOfRequestAttachmentIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) <br/> |Elemento que identifica un solo dato adjunto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DeleteAttachment](deleteattachment.md) <br/> |Elemento que define una solicitud para eliminar datos adjuntos del almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/DeleteAttachment` <br/> |
|[GetAttachment](getattachment.md) <br/> |Elemento que define una solicitud para obtener datos adjuntos del almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación DeleteAttachment](deleteattachment-operation.md)
- [Operación GetAttachment](getattachment-operation.md)


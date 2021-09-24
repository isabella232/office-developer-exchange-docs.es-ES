---
title: RemoveDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RemoveDelegateResponse
api_type:
- schema
ms.assetid: eef56c53-d0a7-4342-9ce6-4dbb6b1a1369
description: El elemento RemoveDelegateResponse contiene el estado y el resultado de una solicitud de operación RemoveDelegate.
ms.openlocfilehash: f00c7d7d83476d4b4d7b035a5567a7d9417ff75a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517976"
---
# <a name="removedelegateresponse"></a>RemoveDelegateResponse

El **elemento RemoveDelegateResponse** contiene el estado y el resultado de una solicitud de operación [RemoveDelegate.](removedelegate-operation.md) 
  
```xml
<RemoveDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RemoveDelegateResponse>
```

 **RemoveDelegateResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages (ArrayOfDelegateUserResponseMessageType)](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |Contiene los mensajes de respuesta de una Exchange delegada de servicios web.  <br/> |
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que encontró la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información adicional de respuesta a errores.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación RemoveDelegate](removedelegate-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


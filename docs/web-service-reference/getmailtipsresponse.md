---
title: GetMailTipsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTipsResponse
api_type:
- schema
ms.assetid: fe270e34-566e-4f9e-9e73-fbf38e06436d
description: El elemento GetMailTipsResponse representa el mensaje de respuesta para una operación de GetMailTips.
ms.openlocfilehash: 2c0dcfe4e2deddcf9a6f4bb9d68d59115c171796
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458610"
---
# <a name="getmailtipsresponse"></a>GetMailTipsResponse

El elemento **GetMailTipsResponse** representa el mensaje de respuesta para una [operación de GetMailTips](getmailtips-operation.md).
  
```XML
<GetMailTipsResponse>
   <ResponseMessages/>
</GetMailTipsResponse>
```

 **GetMailTipsResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages (ArrayOfMailTipsResponseMessageType)](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |Representa una lista de los mensajes de respuesta de sugerencias de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetMailTips](getmailtips-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


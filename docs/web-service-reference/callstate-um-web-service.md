---
title: CallState (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: El elemento CallState contiene un valor que indica el estado de una llamada.
ms.openlocfilehash: 9435124e98cfb75beab5917c1e832096ca193e0c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519971"
---
# <a name="callstate-um-web-service"></a>CallState (servicio web de mensajería unificada)

El **elemento CallState** contiene un valor que indica el estado de una llamada. 
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[CallState (servicio web de mensajería unificada)](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 **UMCallState**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md) <br/> |Define una respuesta a una [operación GetCallInfo (servicio web de mensajería unificada).](getcallinfo-operation-um-web-service.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son los siguientes:
  
- Inactivo
    
- Conectando
    
- Alertado
    
- Conectados
    
- Desconectado
    
- Entrante
    
- Transferencia
    
- Reenvío
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)


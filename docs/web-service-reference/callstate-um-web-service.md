---
title: CallState (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: El elemento CallState contiene un valor que indica el estado de una llamada.
ms.openlocfilehash: e751c2e38783c6634a44d8e1b830a9224cdf300a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763721"
---
# <a name="callstate-um-web-service"></a>CallState (servicio web de mensajería unificada)

El elemento **CallState** contiene un valor que indica el estado de una llamada. 
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[CallState (servicio web de mensajería unificada)](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 **UMCallState**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md) <br/> |Define una respuesta a una [operación de GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md).  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son:
  
- Inactividad
    
- Conectando
    
- Una alerta
    
- Conectado
    
- Desconectado
    
- Entrante
    
- Transferir
    
- Desvío de llamadas
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)


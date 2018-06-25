---
title: EventCause (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: El elemento EventCause contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud de GetCallInfo operación (servicio web de mensajería unificada).
ms.openlocfilehash: dd73d93527bebb3b522ad0a6cdae5b9faee1a6a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764451"
---
# <a name="eventcause-um-web-service"></a>EventCause (servicio web de mensajería unificada)

El elemento **EventCause** contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud de [operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) . 
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[EventCause (servicio web de mensajería unificada)](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMEventCause**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md) <br/> |Define una respuesta a una solicitud de [operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son:
  
- None
    
- UserBusy
    
- NoAnswer
    
- Otro
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)


---
title: EventCause (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: El elemento EventCause contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud de operación GetCallInfo (servicio web de mensajería unificada).
ms.openlocfilehash: 203cefa1a70294bec4d6f4b41aa157da6e639fce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546577"
---
# <a name="eventcause-um-web-service"></a>EventCause (servicio web de mensajería unificada)

El **elemento EventCause** contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud de operación [GetCallInfo (servicio web de](getcallinfo-operation-um-web-service.md) mensajería unificada). 
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[EventCause (servicio web de mensajería unificada)](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMEventCause**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md) <br/> |Define una respuesta a una [solicitud de operación GetCallInfo (servicio web de](getcallinfo-operation-um-web-service.md) mensajería unificada).  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son los siguientes:
  
- Ninguno
    
- UserBusy
    
- NoAnswer
    
- Otro
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)


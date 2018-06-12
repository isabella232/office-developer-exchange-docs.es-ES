---
title: GetCallInfoResponse (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: El elemento GetCallInfoResponse define una respuesta a una solicitud de GetCallInfo operación (servicio web de mensajería unificada).
ms.openlocfilehash: d9658dd9cb47f925e05dc21a8651c98dce1f0a2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764769"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse (servicio web de mensajería unificada)

El elemento **GetCallInfoResponse** define una respuesta a una solicitud de [operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) . 
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMCallInfo**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|CallState  <br/> |Contiene un valor que indica el estado de una llamada para que la [operación de GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) solicita información.  <br/> |
|EventCause  <br/> |Contiene un valor que indica la causa de un evento para una llamada para que la [operación de GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) solicita información.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[CallState (servicio web de mensajería unificada)](callstate-um-web-service.md)
  
[EventCause (servicio web de mensajería unificada)](eventcause-um-web-service.md)


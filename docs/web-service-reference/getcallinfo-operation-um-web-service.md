---
title: Operación GetCallInfo (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfo
api_type:
- schema
ms.assetid: 6bccd418-caf7-4eb9-8a6f-410e56a635c3
description: La operación GetCallInfo devuelve el estado de la llamada de salida que se especifica mediante CallId (servicio web de mensajería unificada).
ms.openlocfilehash: 36f9cba3690520ebb457a4cb2bfbcde3fea4b8dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764765"
---
# <a name="getcallinfo-operation-um-web-service"></a>Operación GetCallInfo (servicio web de mensajería unificada)

La operación GetCallInfo devuelve el estado de la llamada de salida que se especifica mediante [CallId (servicio web de mensajería unificada)](callid-um-web-service.md).
  
## <a name="getcallinfo-request-example"></a>Ejemplo de solicitud de GetCallInfo

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de GetCallInfo muestra cómo formar una solicitud para obtener información acerca de una llamada de salida especificada.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a>Ejemplo de respuesta correcta de GetCallInfo

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta GetCallInfo muestra una respuesta a una solicitud de GetCallInfo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[GetCallInfo (servicio web de mensajería unificada)](getcallinfo-um-web-service.md)
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[CallId (servicio web de mensajería unificada)](callid-um-web-service.md)
  
[CallState (servicio web de mensajería unificada)](callstate-um-web-service.md)
  
[EventCause (servicio web de mensajería unificada)](eventcause-um-web-service.md)


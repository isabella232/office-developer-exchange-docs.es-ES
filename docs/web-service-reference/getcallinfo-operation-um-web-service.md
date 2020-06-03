---
title: Operación GetCallInfo (servicio Web de mensajería unificada)
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
description: La operación GetCallInfo devuelve el estado de la llamada saliente especificada por CallId (servicio Web de mensajería unificada).
ms.openlocfilehash: 6b5664dfe16f9c74cc7175098145141b815a6355
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461243"
---
# <a name="getcallinfo-operation-um-web-service"></a>Operación GetCallInfo (servicio Web de mensajería unificada)

La operación GetCallInfo devuelve el estado de la llamada saliente especificada por [CallId (servicio Web de mensajería unificada)](callid-um-web-service.md).
  
## <a name="getcallinfo-request-example"></a>Ejemplo de solicitud GetCallInfo

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud GetCallInfo muestra cómo crear una solicitud para obtener información sobre una llamada saliente especificada.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a>Ejemplo de respuesta GetCallInfo correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de GetCallInfo muestra una respuesta a una solicitud de GetCallInfo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-um-web-service.md)
  
[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[CallId (servicio Web de mensajería unificada)](callid-um-web-service.md)
  
[CallState (servicio Web de mensajería unificada)](callstate-um-web-service.md)
  
[EventCause (servicio Web de mensajería unificada)](eventcause-um-web-service.md)


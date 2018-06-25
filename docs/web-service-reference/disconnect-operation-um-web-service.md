---
title: (Servicio web de mensajería unificada) de la operación de desconexión
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: La operación de desconexión termina la llamada que se identifica con el CallId especificado (servicio web de mensajería unificada).
ms.openlocfilehash: 1e04e65fa1951a6aa46e2c8b6dd5fe524c84a8fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764192"
---
# <a name="disconnect-operation-um-web-service"></a>(Servicio web de mensajería unificada) de la operación de desconexión

La operación de desconexión termina la llamada que se identifica con el especificado [CallId (servicio web de mensajería unificada)](callid-um-web-service.md).
  
## <a name="disconnect-request-example"></a>Ejemplo de solicitud de desconexión

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de desconexión muestra cómo formar una solicitud para desconectar la llamada.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a>Ejemplo de respuesta correcta de desconexión

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta de desconexión muestra una respuesta a la solicitud de desconexión.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también

- [Desconectar (servicio web de mensajería unificada)](disconnect-um-web-service.md) 
- [DisconnectResponse (servicio web de mensajería unificada)](disconnectresponse-um-web-service.md) 
- [CallId (servicio web de mensajería unificada)](callid-um-web-service.md)


---
title: Operación Disconnect (servicio Web de mensajería unificada)
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
description: La operación de desconexión finaliza la llamada identificada por el CallId (servicio Web de mensajería unificada) especificado.
ms.openlocfilehash: a1268f9ea3d879f472e019bf1847fc13d65d1819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529073"
---
# <a name="disconnect-operation-um-web-service"></a>Operación Disconnect (servicio Web de mensajería unificada)

La operación de desconexión finaliza la llamada identificada por el [CallId (servicio Web de mensajería unificada)](callid-um-web-service.md)especificado.
  
## <a name="disconnect-request-example"></a>Ejemplo de solicitud Disconnect

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud de desconexión muestra cómo crear una solicitud para desconectar una llamada.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a>Ejemplo de respuesta de desconexión correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de desconexión muestra una respuesta a la solicitud de desconexión.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también

- [Disconnect (servicio Web de mensajería unificada)](disconnect-um-web-service.md) 
- [DisconnectResponse (servicio Web de mensajería unificada)](disconnectresponse-um-web-service.md) 
- [CallId (servicio Web de mensajería unificada)](callid-um-web-service.md)


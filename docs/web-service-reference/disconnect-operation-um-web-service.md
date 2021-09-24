---
title: Operación Disconnect (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: La operación Disconnect termina la llamada identificada por el CallId (servicio web de mensajería unificada) especificado.
ms.openlocfilehash: 42e069233fbfc255d43983571c0bb28475a1fe90
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522015"
---
# <a name="disconnect-operation-um-web-service"></a>Operación Disconnect (servicio web de mensajería unificada)

La operación Disconnect termina la llamada identificada por el [CallId especificado (servicio web de mensajería unificada).](callid-um-web-service.md)
  
## <a name="disconnect-request-example"></a>Ejemplo de solicitud disconnect

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud Disconnect se muestra cómo formar una solicitud para desconectar una llamada.
  
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

## <a name="successful-disconnect-response-example"></a>Ejemplo de respuesta disconnect correcta

### <a name="description"></a>Description

En el siguiente ejemplo de una respuesta Disconnect se muestra una respuesta a la solicitud Disconnect.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también

- [Disconnect (servicio web de mensajería unificada)](disconnect-um-web-service.md) 
- [DisconnectResponse (servicio web de mensajería unificada)](disconnectresponse-um-web-service.md) 
- [CallId (servicio web de mensajería unificada)](callid-um-web-service.md)


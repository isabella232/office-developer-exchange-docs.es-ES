---
title: Operación PlayOnPhone (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: La operación PlayOnPhone realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono que es especificado por el elemento DialString.
ms.openlocfilehash: b55bb45d6654f57503879f33e1cd5013ddb69a2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836818"
---
# <a name="playonphone-operation-um-web-service"></a>Operación PlayOnPhone (servicio web de mensajería unificada)

La operación PlayOnPhone realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono que es especificado por el elemento **DialString** . 
  
## <a name="playonphone-request-example"></a>Ejemplo de solicitud de PlayOnPhone

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud PlayOnPhone muestra cómo formar una solicitud para realizar una llamada saliente y reproducir un mensaje.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphone-response-example"></a>Ejemplo de respuesta correcta de PlayOnPhone

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta PlayOnPhone muestra una respuesta a la solicitud de PlayOnPhone.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[PlayOnPhone (servicio web de mensajería unificada)](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse (servicio web de mensajería unificada)](playonphoneresponse-um-web-service.md)
  
[Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)


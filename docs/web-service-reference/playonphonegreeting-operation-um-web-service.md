---
title: Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: La operación PlayOnPhoneGreeting realiza una llamada saliente y reproduce uno de los dos mensajes de saludo en el teléfono.
ms.openlocfilehash: 540cd44d35e70e2588446996aec19aeab17f83e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543138"
---
# <a name="playonphonegreeting-operation-um-web-service"></a>Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)

La operación PlayOnPhoneGreeting realiza una llamada saliente y reproduce uno de los dos mensajes de saludo en el teléfono.
  
## <a name="playonphonegreeting-request-example"></a>Ejemplo de solicitud PlayOnPhoneGreeting

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud PlayOnPhoneGreeting se muestra cómo formar una solicitud para realizar una llamada saliente y reproducir el mensaje de saludo normal en un teléfono.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphonegreeting-response-example"></a>Ejemplo de respuesta PlayOnPhoneGreeting correcto

### <a name="description"></a>Description

En el siguiente ejemplo de una respuesta PlayOnPhoneGreeting se muestra una respuesta a la solicitud PlayOnPhoneGreeting.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Consulte también



[PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse (servicio web de mensajería unificada)](playonphonegreetingresponse-um-web-service.md)
  
[GreetingType (servicio web de mensajería unificada)](greetingtype-um-web-service.md)
  
[dialString (servicio web de mensajería unificada)](dialstring-um-web-service.md)


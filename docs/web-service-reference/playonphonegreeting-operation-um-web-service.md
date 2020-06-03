---
title: Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: La operación PlayOnPhoneGreeting realiza una llamada saliente y reproduce uno de los dos mensajes de saludo en el teléfono.
ms.openlocfilehash: 3af120b9ac8d7a368742fad2850c924228488662
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528898"
---
# <a name="playonphonegreeting-operation-um-web-service"></a>Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)

La operación PlayOnPhoneGreeting realiza una llamada saliente y reproduce uno de los dos mensajes de saludo en el teléfono.
  
## <a name="playonphonegreeting-request-example"></a>Ejemplo de solicitud PlayOnPhoneGreeting

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud de PlayOnPhoneGreeting muestra cómo crear una solicitud para realizar una llamada saliente y reproducir el mensaje de saludo normal en un teléfono.
  
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

## <a name="successful-playonphonegreeting-response-example"></a>Ejemplo de respuesta PlayOnPhoneGreeting correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de PlayOnPhoneGreeting muestra una respuesta a la solicitud PlayOnPhoneGreeting.
  
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

## <a name="see-also"></a>Vea también



[PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse (servicio Web de mensajería unificada)](playonphonegreetingresponse-um-web-service.md)
  
[GreetingType (servicio Web de mensajería unificada)](greetingtype-um-web-service.md)
  
[dialString (servicio Web de mensajería unificada)](dialstring-um-web-service.md)


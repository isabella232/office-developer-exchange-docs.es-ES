---
title: Operación reproducir (servicio Web de mensajería unificada)
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
description: La operación reproducir realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono especificado por el elemento DialString.
ms.openlocfilehash: c5ff82bcd822aa2c659d1782ea4a1349d198bc80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466237"
---
# <a name="playonphone-operation-um-web-service"></a>Operación reproducir (servicio Web de mensajería unificada)

La operación reproducir realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono especificado por el elemento **DialString** . 
  
## <a name="playonphone-request-example"></a>Ejemplo de solicitud reproducir

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud reproducir muestra cómo crear una solicitud para realizar una llamada saliente y reproducir un mensaje.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphone-response-example"></a>Ejemplo de respuesta reproducir correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de reproducir muestra una respuesta a la solicitud reproducir.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[Reproducir (servicio Web de mensajería unificada)](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse (servicio Web de mensajería unificada)](playonphoneresponse-um-web-service.md)
  
[Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)


---
title: Operación PlayOnPhone (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: La operación PlayOnPhone realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono especificado por el elemento DialString.
ms.openlocfilehash: 4d18727da18c36e6410c3cc6ab3bbf873993be72
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516569"
---
# <a name="playonphone-operation-um-web-service"></a>Operación PlayOnPhone (servicio web de mensajería unificada)

La operación PlayOnPhone realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono especificado por el **elemento DialString.** 
  
## <a name="playonphone-request-example"></a>Ejemplo de solicitud de PlayOnPhone

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud de PlayOnPhone se muestra cómo formar una solicitud para realizar una llamada saliente y reproducir un mensaje.
  
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

## <a name="successful-playonphone-response-example"></a>Ejemplo de respuesta correcta de PlayOnPhone

### <a name="description"></a>Descripción

En el siguiente ejemplo de una respuesta de PlayOnPhone se muestra una respuesta a la solicitud PlayOnPhone.
  
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

## <a name="see-also"></a>Ver también



[PlayOnPhone (servicio web de mensajería unificada)](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse (servicio web de mensajería unificada)](playonphoneresponse-um-web-service.md)
  
[Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)


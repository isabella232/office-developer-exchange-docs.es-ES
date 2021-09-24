---
title: Operación SetMissedCallNotificationEnabled (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.
ms.openlocfilehash: 31f59887041aac02e5876b596931902373870203
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521420"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>Operación SetMissedCallNotificationEnabled (servicio web de mensajería unificada)

La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.
  
## <a name="setmissedcallnotificationenabled-request-example"></a>Ejemplo de solicitud SetMissedCallNotificationEnabled

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud SetMissedCallNotificationEnabled se muestra cómo formar una solicitud para habilitar las notificaciones de llamadas perdidas.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a>Ejemplo de respuesta SetMissedCallNotificationEnabled correcto

### <a name="description"></a>Description

En el siguiente ejemplo de una respuesta PlayOnPhoneGreeting se muestra una respuesta a la solicitud SetMissedCallNotificationEnabled.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[SetMissedCallNotificationEnabled (servicio web de mensajería unificada)](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse (servicio web de mensajería unificada)](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Status (servicio web de mensajería unificada: SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)


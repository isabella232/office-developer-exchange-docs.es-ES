---
title: Operación SetMissedCallNotificationEnabled (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.
ms.openlocfilehash: be9479d6ed2c5238ed19c3d22e028fca62b8deed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837434"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>Operación SetMissedCallNotificationEnabled (servicio web de mensajería unificada)

La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.
  
## <a name="setmissedcallnotificationenabled-request-example"></a>Ejemplo de solicitud de SetMissedCallNotificationEnabled

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de SetMissedCallNotificationEnabled muestra cómo formar una solicitud para habilitar las notificaciones de llamadas perdidas.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a>Ejemplo de respuesta correcta de SetMissedCallNotificationEnabled

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta PlayOnPhoneGreeting muestra una respuesta a la solicitud de SetMissedCallNotificationEnabled.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[SetMissedCallNotificationEnabled (servicio web de mensajería unificada)](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse (servicio web de mensajería unificada)](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Estado (servicio web de mensajería unificada - SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)


---
title: Operación SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)
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
ms.openlocfilehash: ca4942942a81bc187e8e18a5e6f003f8587f79d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467399"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>Operación SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)

La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.
  
## <a name="setmissedcallnotificationenabled-request-example"></a>Ejemplo de solicitud SetMissedCallNotificationEnabled

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud SetMissedCallNotificationEnabled muestra cómo crear una solicitud para habilitar las notificaciones de llamadas perdidas.
  
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

## <a name="successful-setmissedcallnotificationenabled-response-example"></a>Ejemplo de respuesta SetMissedCallNotificationEnabled correcta

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta de PlayOnPhoneGreeting muestra una respuesta a la solicitud SetMissedCallNotificationEnabled.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse (servicio Web de mensajería unificada)](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Estado (servicio Web de mensajería unificada-SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)


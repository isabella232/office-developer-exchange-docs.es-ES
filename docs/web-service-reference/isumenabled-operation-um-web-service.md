---
title: Operación IsUMEnabled (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: La operación IsUMEnabled determina si un buzón de correo está habilitado para mensajería unificada.
ms.openlocfilehash: 9d94a359d6b11e41762d21aa2fe5501bd9f7b577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836107"
---
# <a name="isumenabled-operation-um-web-service"></a>Operación IsUMEnabled (servicio web de mensajería unificada)

La operación IsUMEnabled determina si un buzón de correo está habilitado para mensajería unificada.
  
## <a name="isumenabled-request-example"></a>Ejemplo de solicitud de IsUMEnabled

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de IsUMEnabled muestra cómo formar una solicitud para determinar si un buzón de correo está habilitado para mensajería unificada.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a>Ejemplo de respuesta correcta de IsUMEnabled

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta a una solicitud IsUMEnabled correcta.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[IsUMEnabled (servicio web de mensajería unificada)](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse (servicio web de mensajería unificada)](isumenabledresponse-um-web-service.md)


[Elementos XML de servicio de web de Unified Messaging para Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)


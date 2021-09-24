---
title: Operación IsUMEnabled (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: La operación IsUMEnabled determina si un buzón está habilitado para la mensajería unificada.
ms.openlocfilehash: 2c637711fc34a1d1ccc484b14be3199632aaaaa3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514462"
---
# <a name="isumenabled-operation-um-web-service"></a>Operación IsUMEnabled (servicio web de mensajería unificada)

La operación IsUMEnabled determina si un buzón está habilitado para la mensajería unificada.
  
## <a name="isumenabled-request-example"></a>Ejemplo de solicitud IsUMEnabled

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud IsUMEnabled se muestra cómo formar una solicitud para determinar si un buzón está habilitado para la mensajería unificada.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a>Ejemplo de respuesta de IsUMEnabled correcto

### <a name="description"></a>Descripción

En el siguiente ejemplo se muestra una respuesta correcta a una solicitud IsUMEnabled.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[IsUMEnabled (servicio web de mensajería unificada)](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse (servicio web de mensajería unificada)](isumenabledresponse-um-web-service.md)


[Elementos XML del servicio web de mensajería unificada para Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)


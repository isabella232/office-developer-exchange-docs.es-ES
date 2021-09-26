---
title: Operación SetOofStatus (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: La operación SetOofStatus establece un valor que indica si el saludo fuera de Office (OOF) debe reproducirse para el usuario que realiza la solicitud.
ms.openlocfilehash: ce736e7d7bea39f65843923187af3ae616ae1c86
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544755"
---
# <a name="setoofstatus-operation-um-web-service"></a>Operación SetOofStatus (servicio web de mensajería unificada)

La operación SetOofStatus establece un valor que indica si el saludo fuera de Office (OOF) debe reproducirse para el usuario que realiza la solicitud.
  
## <a name="setoofstatus-request-example"></a>Ejemplo de solicitud SetOofStatus

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud SetOofStatus se muestra cómo formar una solicitud para habilitar el saludo de salida de Office para un buzón.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a>Ejemplo de respuesta SetOofStatus correcto

### <a name="description"></a>Description

En el siguiente ejemplo de una respuesta SetOofStatus se muestra una respuesta a la solicitud SetOofStatus.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Consulte también



[SetOofStatus (servicio web de mensajería unificada)](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse (servicio web de mensajería unificada)](setoofstatusresponse-um-web-service.md)
  
[Status (servicio web de mensajería unificada: SetOofStatus)](status-um-web-servicesetoofstatus.md)


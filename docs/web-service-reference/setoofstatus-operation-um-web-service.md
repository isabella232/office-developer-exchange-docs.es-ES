---
title: Operación SetOofStatus (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de oficina (OOF) del usuario que realiza la solicitud.
ms.openlocfilehash: 2bb1deeec8ddb5be56979bfb2fae3396672298a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837445"
---
# <a name="setoofstatus-operation-um-web-service"></a>Operación SetOofStatus (servicio web de mensajería unificada)

La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de oficina (OOF) del usuario que realiza la solicitud.
  
## <a name="setoofstatus-request-example"></a>Ejemplo de solicitud de SetOofStatus

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de SetOofStatus muestra cómo formar una solicitud para habilitar el saludo de fuera de la oficina para un buzón de correo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a>Ejemplo de respuesta correcta de SetOofStatus

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta SetOofStatus muestra una respuesta a la solicitud de SetOofStatus.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[SetOofStatus (servicio web de mensajería unificada)](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse (servicio web de mensajería unificada)](setoofstatusresponse-um-web-service.md)
  
[Estado (servicio web de mensajería unificada - SetOofStatus)](status-um-web-servicesetoofstatus.md)


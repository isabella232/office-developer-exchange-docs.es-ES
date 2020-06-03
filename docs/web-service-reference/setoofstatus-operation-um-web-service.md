---
title: Operación SetOofStatus (servicio Web de mensajería unificada)
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
description: La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de la oficina (OOF) para el usuario que realiza la solicitud.
ms.openlocfilehash: 2311b6137ac25d15ad3d06668450c1d0f7ec1fad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467357"
---
# <a name="setoofstatus-operation-um-web-service"></a>Operación SetOofStatus (servicio Web de mensajería unificada)

La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de la oficina (OOF) para el usuario que realiza la solicitud.
  
## <a name="setoofstatus-request-example"></a>Ejemplo de solicitud SetOofStatus

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud SetOofStatus muestra cómo crear una solicitud para habilitar el saludo de fuera de la oficina para un buzón.
  
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

## <a name="successful-setoofstatus-response-example"></a>Ejemplo de respuesta SetOofStatus correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de SetOofStatus muestra una respuesta a la solicitud SetOofStatus.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[SetOofStatus (servicio Web de mensajería unificada)](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse (servicio Web de mensajería unificada)](setoofstatusresponse-um-web-service.md)
  
[Estado (servicio Web de mensajería unificada-SetOofStatus)](status-um-web-servicesetoofstatus.md)


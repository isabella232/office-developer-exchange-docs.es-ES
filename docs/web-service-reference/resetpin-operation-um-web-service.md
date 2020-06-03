---
title: Operación ResetPIN (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: La operación ResetPIN cambia el PIN (TUI contraseña) a un nuevo valor aleatorio.
ms.openlocfilehash: 8de64ce7a47e9c426f8eb9298e1ca00508fb616c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465495"
---
# <a name="resetpin-operation-um-web-service"></a>Operación ResetPIN (servicio Web de mensajería unificada)

La operación ResetPIN cambia el PIN (TUI contraseña) a un nuevo valor aleatorio.
  
## <a name="remarks"></a>Comentarios

La operación ResetPIN crea un nuevo PIN en función de las directivas de PIN. Si la operación se realiza correctamente, se envía un mensaje de correo electrónico que contiene el nuevo PIN al buzón del usuario. Si se produce un error en la operación, se producirá una excepción que contiene información sobre el error.
  
## <a name="resetpin-request-example"></a>Ejemplo de solicitud ResetPIN

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud ResetPIN muestra cómo crear una solicitud para restablecer el PIN de un buzón.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>Ejemplo de respuesta ResetPIN correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de ResetPIN muestra una respuesta a la solicitud ResetPIN.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[ResetPIN (servicio Web de mensajería unificada)](resetpin-um-web-service.md)
  
[ResetPINResponse (servicio Web de mensajería unificada)](resetpinresponse-um-web-service.md)


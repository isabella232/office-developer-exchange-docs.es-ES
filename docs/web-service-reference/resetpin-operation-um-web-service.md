---
title: Operación ResetPIN (servicio web de mensajería unificada)
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
description: La operación ResetPIN cambia el PIN (contraseña TUI) a un nuevo valor aleatorio.
ms.openlocfilehash: e6417b86ce17c0d34fe857cf1209a18972cbef63
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837146"
---
# <a name="resetpin-operation-um-web-service"></a>Operación ResetPIN (servicio web de mensajería unificada)

La operación ResetPIN cambia el PIN (contraseña TUI) a un nuevo valor aleatorio.
  
## <a name="remarks"></a>Notas

La operación ResetPIN crea un nuevo NIP en función de las directivas de PIN. Si la operación se realiza correctamente, se envía un mensaje de correo electrónico que contiene el nuevo NIP para el buzón de correo del usuario. Si se produce un error en la operación, producirá una excepción que contiene información sobre el error.
  
## <a name="resetpin-request-example"></a>Ejemplo de solicitud de ResetPIN

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de ResetPIN muestra cómo formar una solicitud para restablecer el NIP de un buzón de correo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>Ejemplo de respuesta correcta de ResetPIN

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta ResetPIN muestra una respuesta a la solicitud de ResetPIN.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[ResetPIN (servicio web de mensajería unificada)](resetpin-um-web-service.md)
  
[ResetPINResponse (servicio web de mensajería unificada)](resetpinresponse-um-web-service.md)


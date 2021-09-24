---
title: Operación ResetPIN (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: La operación ResetPIN cambia el PIN (contraseña de TUI) a un nuevo valor aleatorio.
ms.openlocfilehash: 12f1e5719184df84f6c29ab3d02cc362f87abc76
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539111"
---
# <a name="resetpin-operation-um-web-service"></a>Operación ResetPIN (servicio web de mensajería unificada)

La operación ResetPIN cambia el PIN (contraseña de TUI) a un nuevo valor aleatorio.
  
## <a name="remarks"></a>Comentarios

La operación ResetPIN crea un NUEVO PIN basado en las directivas de PIN. Si la operación se realiza correctamente, se envía un mensaje de correo electrónico que contiene el nuevo PIN al buzón del usuario. Si se produce un error en la operación, se producirá una excepción que contenga información sobre el error.
  
## <a name="resetpin-request-example"></a>Ejemplo de solicitud ResetPIN

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud ResetPIN se muestra cómo formar una solicitud para restablecer el PIN de un buzón.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>Ejemplo de respuesta resetPIN correcta

### <a name="description"></a>Description

En el siguiente ejemplo de una respuesta ResetPIN se muestra una respuesta a la solicitud ResetPIN.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[ResetPIN (servicio web de mensajería unificada)](resetpin-um-web-service.md)
  
[ResetPINResponse (servicio web de mensajería unificada)](resetpinresponse-um-web-service.md)


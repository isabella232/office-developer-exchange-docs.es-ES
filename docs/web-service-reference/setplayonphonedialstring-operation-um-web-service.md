---
title: Operación SetPlayOnPhoneDialString (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: La operación SetPlayOnPhoneDialString establece la cadena de marcado que se usará como predeterminada para la operación reproducir (servicio Web de mensajería unificada) y la operación PlayOnPhoneGreeting (servicio Web de mensajería unificada).
ms.openlocfilehash: 7df806eedc2d6d037394f31ec4ccbfe28aaf3372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458645"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>Operación SetPlayOnPhoneDialString (servicio Web de mensajería unificada)

La operación SetPlayOnPhoneDialString establece la cadena de marcado que se usará como predeterminada para la [operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) y la [operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md).
  
## <a name="setplayonphonedialstring-request-example"></a>Ejemplo de solicitud SetPlayOnPhoneDialString

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud SetPlayOnPhoneDialString muestra cómo crear una solicitud para establecer la cadena de marcado predeterminada para un buzón de correo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a>Ejemplo de respuesta SetPlayOnPhoneDialString correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de SetPlayOnePhoneDialString muestra una respuesta a la solicitud SetPlayOnPhoneDialString.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[SetPlayOnPhoneDialString (servicio Web de mensajería unificada)](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse (servicio Web de mensajería unificada)](setplayonphonedialstringresponse-um-web-service.md)
  
[dialString (servicio Web de mensajería unificada)](dialstring-um-web-service.md)


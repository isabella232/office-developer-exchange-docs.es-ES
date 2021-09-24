---
title: Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: La operación SetPlayOnPhoneDialString establece la cadena de marcado que se usará como predeterminada para la operación PlayOnPhone (servicio web de mensajería unificada) y la operación PlayOnPhoneGreeting (servicio web de mensajería unificada).
ms.openlocfilehash: 89f83d7b0a1d56cb0adeccbf4fa0bb67f1197253
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531912"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)

La operación SetPlayOnPhoneDialString establece la cadena de marcado que se usará como valor predeterminado para la operación [PlayOnPhone (servicio web](playonphone-operation-um-web-service.md) de mensajería unificada) y la operación [PlayOnPhoneGreeting (servicio web](playonphonegreeting-operation-um-web-service.md)de mensajería unificada).
  
## <a name="setplayonphonedialstring-request-example"></a>Ejemplo de solicitud SetPlayOnPhoneDialString

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud SetPlayOnPhoneDialString se muestra cómo formar una solicitud para establecer la cadena de marcado predeterminada para un buzón.
  
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

## <a name="successful-setplayonphonedialstring-response-example"></a>Ejemplo de respuesta SetPlayOnPhoneDialString correcto

### <a name="description"></a>Description

En el siguiente ejemplo de una respuesta SetPlayOnePhoneDialString se muestra una respuesta a la solicitud SetPlayOnPhoneDialString.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[SetPlayOnPhoneDialString (servicio web de mensajería unificada)](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse (servicio web de mensajería unificada)](setplayonphonedialstringresponse-um-web-service.md)
  
[dialString (servicio web de mensajería unificada)](dialstring-um-web-service.md)


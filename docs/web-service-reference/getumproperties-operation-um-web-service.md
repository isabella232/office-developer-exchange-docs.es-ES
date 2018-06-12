---
title: Operación GetUMProperties (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMProperties
api_type:
- schema
ms.assetid: 301fb9a3-67df-44c4-8ffe-0600237fc344
description: La operación GetUMProperties Obtiene todas las propiedades de mensajería unificada para el buzón del usuario que realiza la solicitud.
ms.openlocfilehash: 8878099bbd907fe0648f7d64dde3cd9600c2c45f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835678"
---
# <a name="getumproperties-operation-um-web-service"></a>Operación GetUMProperties (servicio web de mensajería unificada)

La operación GetUMProperties Obtiene todas las propiedades de mensajería unificada para el buzón del usuario que realiza la solicitud.
  
## <a name="getumproperties-request-example"></a>Ejemplo de solicitud de GetUMProperties

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de GetUMProperties muestra cómo formar una solicitud para obtener las propiedades de mensajería unificada de un buzón de correo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a>Ejemplo de respuesta correcta de GetUMProperties

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta GetUMProperties muestra una respuesta a la solicitud de GetUMProperties.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetUMPropertiesResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetUMPropertiesResponse>
        <OofStatus>false</OofStatus> 
        <MissedCallNotificationEnabled>true</MissedCallNotificationEnabled> 
        <PlayOnPhoneDialString>12345</PlayOnPhoneDialString> 
        <TelephoneAccessNumbers>54321</TelephoneAccessNumbers> 
        <TelephoneAccessFolderEmail>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</TelephoneAccessFolderEmail> 
      </GetUMPropertiesResponse>
    </GetUMPropertiesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[GetUMProperties (servicio web de mensajería unificada)](getumproperties-um-web-service.md)
  
[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)


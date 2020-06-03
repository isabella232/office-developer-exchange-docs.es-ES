---
title: Operación GetUMProperties (servicio Web de mensajería unificada)
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
description: La operación GetUMProperties obtiene todas las propiedades de mensajería unificada del buzón de correo del usuario que realiza la solicitud.
ms.openlocfilehash: 42176d9cd0288af6515aeea616a4f216a419410c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462475"
---
# <a name="getumproperties-operation-um-web-service"></a>Operación GetUMProperties (servicio Web de mensajería unificada)

La operación GetUMProperties obtiene todas las propiedades de mensajería unificada del buzón de correo del usuario que realiza la solicitud.
  
## <a name="getumproperties-request-example"></a>Ejemplo de solicitud GetUMProperties

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud GetUMProperties muestra cómo crear una solicitud para obtener las propiedades de mensajería unificada de un buzón.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a>Ejemplo de respuesta GetUMProperties correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de GetUMProperties muestra una respuesta a la solicitud GetUMProperties.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetUMPropertiesResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="see-also"></a>Vea también



[GetUMProperties (servicio Web de mensajería unificada)](getumproperties-um-web-service.md)
  
[GetUMPropertiesResponse (servicio Web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)


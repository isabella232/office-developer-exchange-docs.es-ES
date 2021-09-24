---
title: Operación GetUMProperties (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetUMProperties
api_type:
- schema
ms.assetid: 301fb9a3-67df-44c4-8ffe-0600237fc344
description: La operación GetUMProperties obtiene todas las propiedades de mensajería unificada para el buzón del usuario que realiza la solicitud.
ms.openlocfilehash: 8d051196e83e1f927692b517e1ab3e95bb0060db
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515820"
---
# <a name="getumproperties-operation-um-web-service"></a>Operación GetUMProperties (servicio web de mensajería unificada)

La operación GetUMProperties obtiene todas las propiedades de mensajería unificada para el buzón del usuario que realiza la solicitud.
  
## <a name="getumproperties-request-example"></a>Ejemplo de solicitud GetUMProperties

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud GetUMProperties se muestra cómo formar una solicitud para obtener las propiedades de mensajería unificada de un buzón.
  
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

### <a name="description"></a>Descripción

En el siguiente ejemplo de una respuesta GetUMProperties se muestra una respuesta a la solicitud GetUMProperties.
  
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

## <a name="see-also"></a>Ver también



[GetUMProperties (servicio web de mensajería unificada)](getumproperties-um-web-service.md)
  
[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)


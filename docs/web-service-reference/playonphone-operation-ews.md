---
title: Operación PlayOnPhone (EWS)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 70e6ef33-2046-4eb8-9987-e106009be04b
description: La operación PlayOnPhone inicia una llamada saliente y reproduce un mensaje a través del teléfono.
ms.openlocfilehash: ec77720c69862e210316d61975b0d58c9530a40c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836819"
---
# <a name="playonphone-operation-ews"></a>Operación PlayOnPhone (EWS)

La operación **PlayOnPhone** inicia una llamada saliente y reproduce un mensaje a través del teléfono. 
  
## <a name="playonphone-request-example"></a>Ejemplo de solicitud de PlayOnPhone

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud **PlayOnPhone** muestra cómo formar una solicitud para reproducir un mensaje en un teléfono. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:PlayOnPhone>
      <m:ItemId Id="AkAjzQTbY/i="/>
      <m:DialString>5555551212</m:DialString>
    </m:PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="playonphone-response-example"></a>Ejemplo de respuesta PlayOnPhone

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **PlayOnPhone** . 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PlayOnPhoneResponse ResponseClass="Success" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <PhoneCallId Id="ZWMtWYtMY29t"/>
    </PlayOnPhoneResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


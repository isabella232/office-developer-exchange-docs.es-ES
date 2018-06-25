---
title: Cancelar la operación de suscripción
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 994a9d2b-1501-4804-90f0-12bd914496ec
description: La operación de cancelación de la suscripción se utiliza para finalizar una suscripción de extracción de notificación. Use esta operación, en lugar de permitir que un tiempo de espera de suscripción. Esta operación sólo es válida para las notificaciones de extracción.
ms.openlocfilehash: 64514a718d473f0fd7d0320bd1ccecddb1940ac8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840797"
---
# <a name="unsubscribe-operation"></a>Cancelar la operación de suscripción

La operación de cancelación de la suscripción se utiliza para finalizar una suscripción de extracción de notificación. Use esta operación, en lugar de permitir que un tiempo de espera de suscripción. Esta operación sólo es válida para las notificaciones de extracción.
  
## <a name="unsubscribe-request-example"></a>Ejemplo de solicitud de cancelación de suscripción

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra el mensaje SOAP XML que se envía al cancelar su suscripción de un cliente desde el servicio de notificación.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Unsubscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>e6fbf5c1-7e26-4bc6-a5f2-882063d5e34e</SubscriptionId>  
    </Unsubscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-request-elements"></a>Elementos de solicitud de cancelación de suscripción

En la solicitud se usan los siguientes elementos:
  
- [Anular la suscripción](unsubscribe.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
## <a name="successful-unsubscribe-response-example"></a>Ejemplo de respuesta de cancelación de suscripción correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta a una solicitud de cancelación de suscripción correcta.
  
### <a name="code"></a>Código

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-response-elements"></a>Elementos de respuesta de cancelación de suscripción

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [Anular la suscripción](unsubscribe.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UnsubscribeResponseMessage](unsubscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="unsubscribe-error-response-example"></a>Ejemplo de respuesta de Error de cancelación de suscripción

### <a name="description"></a>Descripción

El ejemplo siguiente de una respuesta de error de cancelación de suscripción se produce en respuesta a un intento de cancelar la suscripción mediante el uso de un identificador de suscripción que no se encuentra en el almacén de Exchange.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>The specified subscription was not found.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-error-response-elements"></a>Elementos de respuesta de Error de cancelación de suscripción

En la respuesta de error, se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UnsubscribeResponse](unsubscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UnsubscribeResponseMessage](unsubscriberesponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Operación de suscripción](subscribe-operation.md)
- [Operación GetEvents](getevents-operation.md)
- [Uso de las suscripciones de extracción](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)


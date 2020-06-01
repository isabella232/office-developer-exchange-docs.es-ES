---
title: Operación SetUserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettings
api_type:
- schema
ms.assetid: 36277ef0-18ee-4b35-9e6e-8c321d8f5433
description: El método Web SetUserOofSettings establece un mensaje y una configuración de fuera de la oficina (OOF) de un usuario de buzón.
ms.openlocfilehash: 88b5475dd2f0fe6d334bad51a0fe8d0beb767634
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463156"
---
# <a name="setuseroofsettings-operation"></a>Operación SetUserOofSettings

El método Web **SetUserOofSettings** establece un mensaje y una configuración de fuera de la oficina (OOF) de un usuario de buzón. 
  
## <a name="soap-headers"></a>Encabezados SOAP

La operación **SetUserOofSettings** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
   
## <a name="setuseroofsettings-request-example"></a>Ejemplo de solicitud SetUserOofSettings

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud **SetUserOofSettings** establece un valor OOF para 10 días. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>User1</Name>
        <Address>user1@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-10-05T00:00:00</StartTime>
          <EndTime>2006-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
    
- [Buzón de correo (disponibilidad)](mailbox-availability.md)
    
- [Nombre (EmailAddress)](name-emailaddress.md)
    
- [Address (cadena)](address-string.md)
    
- [RoutingType (EmailAddress)](routingtype-emailaddress.md)
    
- [UserOofSettings](useroofsettings.md)
    
- [OofState](oofstate.md)
    
- [ExternalAudience](externalaudience.md)
    
- [Duración (UserOofSettings)](duration-useroofsettings.md)
    
- [StartTime](starttime.md)
    
- [EndTime](endtime.md)
    
- [InternalReply](internalreply.md)
    
- [Mensaje (disponibilidad)](message-availability.md)
    
- [ExternalReply](externalreply.md)
    
## <a name="successful-setuseroofsettings-response-example"></a>Ejemplo de respuesta SetUserOofSettings correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **SetUserOofSettings** . 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" /> 
  </soap:Header>
  <soap:Body>
    <SetUserOofSettingsResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode> 
      </ResponseMessage>
    </SetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elementos Response correcto

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SetUserOofSettingsResponse](setuseroofsettingsresponse.md)
    
- [ResponseMessage](responsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


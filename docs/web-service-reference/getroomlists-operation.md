---
title: Operación GetRoomLists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetRoomLists
api_type:
- schema
ms.assetid: 55d451f9-547f-44ac-872e-9cb220ea7b7c
description: La operación GetRoomLists obtiene las listas de salas que están disponibles en la Exchange organización.
ms.openlocfilehash: 017936dd7d36ffc4c69183380f95e14f7a529913
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521945"
---
# <a name="getroomlists-operation"></a>Operación GetRoomLists

La **operación GetRoomLists** obtiene las listas de salas que están disponibles en la Exchange organización. 
  
## <a name="soap-headers"></a>Encabezados SOAP

La **operación GetRoomLists** puede usar los encabezados SOAP que se enumeran y se describen en la tabla siguiente. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural RFC3066 que se usará para tener acceso al buzón.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
   
## <a name="getroomlists-request-example"></a>Ejemplo de solicitud GetRoomLists

### <a name="description"></a>Description

A continuación se muestra un ejemplo de una **solicitud GetRoomLists** que devuelve las listas de salas que están disponibles en el servidor. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>Elementos Request

En la solicitud se usa el siguiente elemento:
  
- [GetRoomLists](getroomlists.md)
    
## <a name="successful-getroomlists-response-example"></a>Ejemplo de respuesta GetRoomLists correcto

### <a name="description"></a>Description

A continuación se muestra un ejemplo de una respuesta a una **solicitud GetRoomLists.** Esta respuesta muestra una lista de sala en el servidor. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Address xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Name>Room List</t:Name>
          <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-getroomlists-response-elements"></a>Elementos de respuesta GetRoomLists correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetRoomListsResponse](getroomlistsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [RoomLists](roomlists.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddress)](routingtype-emailaddress.md)
    
- [MailboxType](mailboxtype.md)
    
### <a name="getroomlists-error-response-example"></a>Ejemplo de respuesta de error GetRoomLists

#### <a name="description"></a>Description

En el ejemplo siguiente se muestra la respuesta a un intento de obtener listas de sala de un servidor que no tiene definida ninguna lista de sala.
  
#### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"/>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

#### <a name="getroomlists-error-response-elements"></a>Elementos de respuesta de error GetRoomLists

En la respuesta de error se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetRoomListsResponse](getroomlistsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [RoomLists](roomlists.md)
    
## <a name="see-also"></a>Ver también



[Operaciones ews en Exchange](ews-operations-in-exchange.md)
  
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


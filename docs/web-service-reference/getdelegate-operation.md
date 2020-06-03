---
title: Operación GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 849b2c9e-4685-4bd1-9adb-aba0fcc52650
description: La operación GetDelegate recupera la configuración de delegado de un buzón especificado.
ms.openlocfilehash: 400bf5d1cafcbb789aaa749c62c7a908622d4ddb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461068"
---
# <a name="getdelegate-operation"></a>Operación GetDelegate

La operación **GetDelegate** recupera la configuración de delegado de un buzón especificado. 
  
## <a name="soap-headers"></a>Encabezados SOAP

La operación **GetDelegate** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
   
## <a name="getdelegate-request-example"></a>Ejemplo de solicitud GetDelegate

### <a name="description"></a>Description

En el ejemplo de código siguiente se muestra cómo recuperar la configuración de delegado para todos los delegados que se establecen en el buzón de user3's. Todos los permisos para cada usuario se devuelven en la respuesta.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <GetDelegate xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                 IncludePermissions="true">
      <Mailbox>
        <t:EmailAddress>user3@example.com</t:EmailAddress>
      </Mailbox>
    </GetDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Puede usar el elemento [userid](userid.md) para especificar usuarios individuales en lugar de devolver todos los usuarios que tienen permisos de acceso delegado en el buzón. 
  
> [!NOTE]
> Los servicios web Exchange (EWS) no admiten la administración de delegados de grupo. EWS devolverá un error si se llama a la operación **GetDelegate** para una entidad de seguridad que tenga un delegado de grupo de seguridad. 
  
## <a name="getdelegate-response-example"></a>Ejemplo de respuesta GetDelegate

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de **GetDelegate** muestra una respuesta correcta a una solicitud de **GetDelegate** . La respuesta contiene información sobre los permisos de acceso delegado, si el delegado puede ver elementos privados, si el delegado recibe copias de los mensajes de reunión y a quién se entregaron las convocatorias de reunión. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" 
                         MinorVersion="1" 
                         MajorBuildNumber="206" 
                         MinorBuildNumber="0" 
                         Version="Exchange2007_SP1" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:GetDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           ResponseClass="Success" 
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
              <t:UserId>
                <t:SID>S-1-5-21-1333220396-2200287332-232816053-1116</t:SID>
                <t:PrimarySmtpAddress>User1@example.com</t:PrimarySmtpAddress>
                <t:DisplayName>User1</t:DisplayName>
              </t:UserId>
              <t:DelegatePermissions>
                <t:CalendarFolderPermissionLevel>Author</t:CalendarFolderPermissionLevel>
                <t:ContactsFolderPermissionLevel>Reviewer</t:ContactsFolderPermissionLevel>
              </t:DelegatePermissions>
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
          </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      <m:DeliverMeetingRequests>DelegatesAndMe</m:DeliverMeetingRequests>
      </m:GetDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


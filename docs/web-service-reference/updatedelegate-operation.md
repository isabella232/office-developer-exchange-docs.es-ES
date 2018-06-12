---
title: Operación UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: 03f618ac-ad1a-4772-9b81-c5bb0f12d6ab
description: La operación UpdateDelegate actualiza delegar permisos de buzón de correo de una entidad de seguridad.
ms.openlocfilehash: 9f69d784617d10d8902a260bbf6639703dd33b6d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840805"
---
# <a name="updatedelegate-operation"></a>Operación UpdateDelegate

La operación **UpdateDelegate** actualiza delegar permisos de buzón de correo de una entidad de seguridad. 
  
## <a name="soap-headers"></a>Encabezados SOAP

La operación de **UpdateDelegate** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente. 
  
|**Header**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud.  <br/> |
   
## <a name="updatedelegate-request-example"></a>Ejemplo de solicitud de UpdateDelegate

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **UpdateDelegate** muestra cómo actualizar los permisos de delegado en la cuenta de Usuario1. El usuario 2 se concede ninguna permiso de nivel de la carpeta tareas y se le concede permiso para ver elementos privados. User3 se conceden permisos de revisor para la carpeta diario. Las convocatorias de reunión se envían a los delegados y obtener información acerca de la solicitud se envía al Usuario1. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <UpdateDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>user1@example.com</t:EmailAddress>
      </Mailbox>
      <DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user2@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ViewPrivateItems>true</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user3@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:JournalFolderPermissionLevel>Reviewer</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
        </t:DelegateUser>
      </DelegateUsers>
      <DeliverMeetingRequests>DelegatesAndSendInformationToMe</DeliverMeetingRequests>
    </UpdateDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

La solicitud [UpdateDelegate](updatedelegate.md) no requiere que las actualizaciones se aplica a los delegados. Los clientes pueden cambiar únicamente la configuración de **DeliverMeetingMessage** . 
  
## <a name="updatedelegate-response-example"></a>Ejemplo de respuesta UpdateDelegate

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta para una operación de **UpdateDelegate** . 
  
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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:UpdateDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1117</t:SID>
              <t:PrimarySmtpAddress>User2@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User2</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>true</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1118</t:SID>
              <t:PrimarySmtpAddress>User3@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User3</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="updatedelegate-error-response-example"></a>Ejemplo de respuesta de UpdateDelegate Error

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **UpdateDelegate** . Se generó el error porque el delegado no existe en la lista de delegados de la entidad de seguridad. 
  
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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:UpdateDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              ResponseClass="Success" 
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is not a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorNotDelegate</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


---
title: Operación GetUserSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 758d965c-ef63-4de4-9120-e293abf14ff8
description: La operación GetUserSettings contiene una consulta para la configuración de acceso de cliente de los usuarios.
ms.openlocfilehash: 79e9d5827cbcc4885c99cf5a497868284dda4494
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547410"
---
# <a name="getusersettings-operation-soap"></a>Operación GetUserSettings (SOAP)

La **operación GetUserSettings** contiene una consulta para la configuración de acceso de cliente de los usuarios. 
  
## <a name="getusersettings-request-example"></a>Ejemplo de solicitud GetUserSettings

### <a name="description"></a>Description

En el siguiente ejemplo XML se muestra un cuerpo de solicitud de detección automática que solicita el nombre para mostrar, el nombre distintivo, el identificador de implementación, el servidor de buzones de correo, el nombre distintivo del buzón, el servidor de Active Directory, la versión del servidor de acceso de cliente y los esquemas de servicios web Exchange compatibles.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"      
               xmlns:wsa="http://www.w3.org/2005/08/addressing" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"      
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://myserver.contoso.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>UserName@domain.contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>Elementos Request

Los siguientes elementos se usan en el cuerpo de la solicitud:
  
- [GetUserSettingsRequestMessage (SOAP)](getusersettingsrequestmessage-soap.md)
    
- [Mailbox (SOAP)](mailbox-soap.md)
    
- [Request (SOAP)](request-soap.md)
    
- [RequestedServerVersion (SOAP)](requestedserverversion-soap.md)
    
- [RequestedSettings (SOAP)](requestedsettings-soap.md)
    
- [Setting (SOAP)](setting-soap.md)
    
- [User (SOAP)](user-soap.md)
    
- [Users (SOAP)](users-soap.md)
    
## <a name="getusersettings-response-example"></a>Ejemplo de respuesta GetUserSettings

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta **GetUserSettings** correcta. 
  
### <a name="code"></a>Código

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
  </s:Header>
  <s:Body>
  <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>UserDisplayName</Name>
                <Value>UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Recipients/cn=UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>a40E2742-21c6-4050-8Ed2-d41f100c22b8</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>14.00.0478.000</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007,  Exchange2010</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Configuration/cn=Servers/cn=server/cn=Contoso Pri MDB</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

### <a name="response-elements"></a>Elementos de respuesta

Los siguientes elementos se usan en el cuerpo de la respuesta:
  
- [ErrorCode (SOAP)](errorcode-soap.md)
    
- [ErrorMessage (SOAP)](errormessage-soap.md)
    
- [GetUserSettingsResponseMessage (SOAP)](getusersettingsresponsemessage-soap.md)
    
- [Name (SOAP)](name-soap.md)
    
- [RedirectTarget (SOAP)](redirecttarget-soap.md)
    
- [Response (SOAP)](response-soap.md)
    
- [UserResponse (SOAP)](userresponse-soap.md)
    
- [UserResponses (SOAP)](userresponses-soap.md)
    
- [UserSetting (SOAP)](usersetting-soap.md)
    
- [UserSettingErrors (SOAP)](usersettingerrors-soap.md)
    
- [UserSettings (SOAP)](usersettings-soap.md)
    
- [Value (SOAP)](value-soap.md)
    
## <a name="see-also"></a>Consulte también



[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)


[Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)


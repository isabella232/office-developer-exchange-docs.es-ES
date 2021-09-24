---
title: Operación GetDomainSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a6f4a53d-d7f6-4ad1-8afb-78745c500eaa
description: La operación GetDomainSettings recupera la configuración especificada del dominio para el usuario. Detección automática devuelve los dominios que se van a detectar y la configuración solicitada de esos dominios.
ms.openlocfilehash: 7f52ea840bd7f46198d95ba5f0c07894873cf6e5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525053"
---
# <a name="getdomainsettings-operation-soap"></a>Operación GetDomainSettings (SOAP)

La **operación GetDomainSettings** recupera la configuración especificada del dominio para el usuario. Detección automática devuelve los dominios que se van a detectar y la configuración solicitada de esos dominios. 
  
## <a name="getdomainsettings-request-example"></a>Ejemplo de solicitud GetDomainSettings

### <a name="description"></a>Description

En el siguiente ejemplo de una **solicitud GetDomainSettings** se muestra una solicitud para la configuración del dominio **ExternalEWSUrl** de un usuario. El cliente envía esta solicitud al servidor. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soap:Header> 
        <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
        <wsa:Action>https://schemas.microsoft.com/exchange/2010/
            Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
        <wsa:To>
            https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc
        </wsa:To>
    </soap:Header> 
    <soap:Body> 
        <a:GetDomainSettingsRequestMessage xmlns:a="https://schemas.microsoft.com
            /exchange/2010/Autodiscover"> 
            <a:Request> 
                <a:Domains> 
                    <a:Domain>contoso.com<</a:Domain> 
                </a:Domains> 
                <a:RequestedSettings> 
                    <a:Setting>ExternalEwsUrl</a:Setting> 
                </a:RequestedSettings> 
            </a:Request> 
        </a:GetDomainSettingsRequestMessage> 
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [GetDomainSettingsRequestMessage (SOAP)](getdomainsettingsrequestmessage-soap.md)
    
- [Request (SOAP)](request-soap.md)
    
- [Domains (SOAP)](domains-soap.md)
    
- [Domain (SOAP)](domain-soap.md)
    
- [RequestedSettings (SOAP)](requestedsettings-soap.md)
    
- [Setting (SOAP)](setting-soap.md)
    
## <a name="getdomainsettings-response-example"></a>Ejemplo de respuesta GetDomainSettings

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta correcta a la **solicitud GetDomainSettings** que el servidor envía al cliente. 
  
### <a name="code"></a>Código

```XML
//www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/ 
            Autodiscover/Autodiscover/GetDomainSettingsResponse
        </a:Action> 
        <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
            xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
        <h:MajorVersion>14</h:MajorVersion> 
        <h:MinorVersion>0</h:MinorVersion> 
        <h:MajorBuildNumber>639</h:MajorBuildNumber> 
        <h:MinorBuildNumber>20</h:MinorBuildNumber> 
        <h:Version>Exchange2010</h:Version> 
        </h:ServerVersionInfo>
    </s:Header> 
    <s:Body> 
        <GetDomainSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage /> 
                <DomainResponses> 
                    <DomainResponse> 
                        <ErrorCode>NoError</ErrorCode> 
                        <ErrorMessage>No error.</ErrorMessage> 
                        <DomainSettingErrors /> 
                        <DomainSettings> 
                            <DomainSetting i:type="DomainStringSetting"> 
                                <Name>ExternalEwsUrl</Name> 
                                <Value>https://emea.mail.microsoft.com/EWS/Exchange.asmx</Value> 
                            </DomainSetting> 
                        </DomainSettings> 
                        <RedirectTarget i:nil="true" /> 
                    </DomainResponse> 
                </DomainResponses> 
            </Response> 
        </GetDomainSettingsResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a>Elementos de respuesta

En la respuesta se usan los siguientes elementos:
  
- [GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md)
    
- [Response (SOAP)](response-soap.md)
    
- [ErrorCode (SOAP)](errorcode-soap.md)
    
- [ErrorMessage (SOAP)](errormessage-soap.md)
    
- [DomainResponses (SOAP)](domainresponses-soap.md)
    
- [DomainResponse (SOAP)](domainresponse-soap.md)
    
- [DomainSettingErrors (SOAP)](domainsettingerrors-soap.md)
    
- [DomainSettings (SOAP)](domainsettings-soap.md)
    
- [DomainSetting (SOAP)](domainsetting-soap.md)
    
- [Name (SOAP)](name-soap.md)
    
- [Value (SOAP)](value-soap.md)
    
- [RedirectTarget (SOAP)](redirecttarget-soap.md)
    
## <a name="see-also"></a>Ver también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)


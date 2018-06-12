---
title: Operación GetFederationInformation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6666a42-a18f-4e4b-beb6-b25ff62cfcc5
description: La operación GetFederationInformation proporciona información sobre el estado de federación de la organización, como el identificador URI que se usará al solicitar tokens que van dirigidos a esta organización y el resto de los dominios que la organización tiene también de destino federados.
ms.openlocfilehash: bf38b2f2b3db3e38b9b0157d1677efe4fc274e1b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764850"
---
# <a name="getfederationinformation-operation-soap"></a>Operación GetFederationInformation (SOAP)

La operación **GetFederationInformation** proporciona información sobre el estado de federación de la organización, como el destino de URI que se utilizará al solicitar tokens que van dirigidas a esta organización y los demás dominios que la organización También se ha federados. 
  
Sólo las organizaciones federadas pueden compartir calendario, contactos y mensajes a los usuarios externos.
  
## <a name="getfederationinformation-request-example"></a>Ejemplo de solicitud de GetFederationInformation

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **GetFederationInformation** muestra una solicitud de información de la federación de un usuario. El cliente envía esta solicitud al servidor. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="http://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="http://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">http://schemas.microsoft.com/
            exchange/2010/Autodiscover/Autodiscover/GetFederationInformation
        </a:Action> 
        <a:To soap:mustUnderstand="1">https://autodiscover.byfcxu-
            dom.extest.microsoft.com/autodiscover/autodiscover.svc</a:To> 
        <a:ReplyTo>
            <a:Address>http://www.w3.org/2005/08/addressing/anonymous</a:Address> 
        </a:ReplyTo> 
    </soap:Header> 
    <soap:Body> 
        <GetFederationInformationRequestMessage 
            xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Request> 
                <Domain>contoso.com</Domain> 
            </Request> 
        </GetFederationInformationRequestMessage>
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [GetFederationInformationRequestMessage (SOAP)](getfederationinformationrequestmessage-soap.md)
    
- [Solicitud (SOAP)](request-soap.md)
    
- [Dominio (SOAP)](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a>Ejemplo de respuesta GetFederationInformation

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **GetFederationInformation** que el servidor envía al cliente. 
  
### <a name="code"></a>Código

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage/> 
                <ApplicationUri>BYFCXU-DOM.EXTEST.MICROSOFT.COM</ApplicationUri> 
                <Domains> 
                    <Domain>contoso.com</Domain> 
                    <Domain>europe.contoso.com</Domain> 
                    <Domain>americas.contoso.com</Domain> 
                    <Domain>contosolive.com</Domain> 
                </Domains> 
            </Response> 
        </GetFederationInformationResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a>Elementos de respuesta

En la respuesta se usan los siguientes elementos:
  
- [GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md)
    
- [Respuesta (SOAP)](response-soap.md)
    
- [ErrorCode (SOAP)](errorcode-soap.md)
    
- [ErrorMessage (SOAP)](errormessage-soap.md)
    
- [ApplicationUri (SOAP)](applicationuri-soap.md)
    
- [Dominios (SOAP)](domains-soap.md)
    
- [Dominio (SOAP)](domain-soap.md)
    
## <a name="see-also"></a>Ver también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)


---
title: Operación GetClientAccessToken
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 086876cc-e22c-4e89-89f9-19e78af51217
description: Busque información sobre la EWS GetClientAccessToken operación.
ms.openlocfilehash: afa9a315a8421f31c345c9547a5d80bed41e9fbc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764771"
---
# <a name="getclientaccesstoken-operation"></a>Operación GetClientAccessToken

Obtenga información acerca de la operación de EWS **GetClientAccessToken** . 
  
La operación **GetClientAccessToken** obtiene acceso de cliente de un símbolo (token) para una aplicación de correo para Outlook. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getclientaccesstoken-operation"></a>Mediante la operación GetClientAccessToken

La solicitud de operación **GetClientAccessToken** toma dos argumentos necesarios: el identificador de la aplicación y el tipo de token. Puede usar la [operación de GetAppManifests](getappmanifests-operation.md) para solicitar el identificador de la aplicación. 
  
### <a name="getclientaccesstoken-operation-soap-headers"></a>Encabezados SOAP de operación de GetClientAccessToken

La operación de **GetClientAccessToken** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getclientaccesstoken-operation-request-example-get-a-caller-identity-token"></a>Ejemplo de solicitud de operación de GetClientAccessToken: obtener una identidad del autor de la llamada símbolo (token)

El siguiente ejemplo de una solicitud de operación **GetClientAccessToken** muestra cómo obtener una identidad del autor de la llamada símbolo (token) para una aplicación. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetClientAccessToken>
         <m:TokenRequests>
            <t:TokenRequest>
               <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
               <t:TokenType>CallerIdentity</t:TokenType>
            </t:TokenRequest>
         </m:TokenRequests>
      </m:GetClientAccessToken>
   </soap:Body>
</soap:Envelope>

```

La solicitud SOAP body contiene los siguientes elementos:
  
- [GetClientAccessToken](getclientaccesstoken.md)
    
- [TokenRequests](tokenrequests.md)
    
- [TokenRequest](tokenrequest.md)
    
- [Identificador (cadena)](id-string.md)
    
- [TokenType en](tokentype.md)
    
## <a name="successful-getclientaccesstoken-operation-response"></a>Respuesta es correcta de operación GetClientAccessToken

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetClientAccessToken** para obtener una identidad del autor de la llamada símbolo (token) para una aplicación. 
  
> [!NOTE]
> Los valores del token en este artículo se han abreviado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Token>
                  <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
                  <t:TokenType>CallerIdentity</t:TokenType>
                  <t:TokenValue>eyJ0eXAmv0QitaJg</t:TokenValue>
                  <t:TTL>479</t:TTL>
               </m:Token>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>

```

La respuesta SOAP body contiene los siguientes elementos:
  
- [GetClientAccessTokenResponse](getclientaccesstokenresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetClientAccessTokenResponseMessage](getclientaccesstokenresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Símbolo (token) (ClientAccessTokenType)](token-clientaccesstokentype.md)
    
- [Identificador (cadena)](id-string.md)
    
- [TokenType en (ClientAccessTokenType)](tokentype-clientaccesstokentype.md)
    
- [TokenValue](tokenvalue.md)
    
- [TTL (ClientAccessTokenTypeType)](ttl-clientaccesstokentypetype.md)
    
## <a name="getclientaccesstoken-operation-error-response"></a>Respuesta de error de la operación de GetClientAccessToken

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetClientAccessToken** . Esta es una respuesta a una solicitud para obtener una devolución de llamada de extensión token sin los permisos adecuados. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Error">
               <m:MessageText>The caller does not have enough permission for this token request.</m:MessageText>
               <m:ResponseCode>ErrorInvalidClientAccessTokenRequest</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>
```

La respuesta de error SOAP body contiene los siguientes elementos:
  
- [GetClientAccessTokenResponse](getclientaccesstokenresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetClientAccessTokenResponseMessage](getclientaccesstokenresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetAppManifests](getappmanifests-operation.md)
    
- [Complementos de Outlook](http://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    


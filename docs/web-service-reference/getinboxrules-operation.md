---
title: Operación GetInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: b4b2701a-4a23-4acc-8c75-19f7955ad7ae
description: La operación GetInboxRules usa servicios Web de Exchange para recuperar las reglas de bandeja de entrada en el buzón del usuario identificado.
ms.openlocfilehash: f8a5068b1f189cc6fd5feef6dfec29204a0b8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764872"
---
# <a name="getinboxrules-operation"></a>Operación GetInboxRules

La operación **GetInboxRules** usa servicios Web de Exchange para recuperar las reglas de bandeja de entrada en el buzón del usuario identificado. 
  
## <a name="getinboxrules-request-example"></a>Ejemplo de solicitud de GetInboxRules

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra la solicitud XML que el cliente envía al servidor. La solicitud identifica al usuario en el elemento [MailboxSmtpAddress](mailboxsmtpaddress.md) . Todas las reglas de bandeja de entrada para el usuario identificado están que se devuelve en la respuesta. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetInboxRules>
      <m:MailboxSmtpAddress>User1@Contoso.com</m:MailboxSmtpAddress>
    </m:GetInboxRules>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos de solicitud

La solicitud incluye el elemento opcional siguiente:
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a>Ejemplo de respuesta correcta de GetInboxRules

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **GetInboxRules** . En este ejemplo, la respuesta incluye una regla. 
  
> [!NOTE]
> Los valores del **identificador** y los atributos **ChangeKey** del elemento [FolderId](folderid.md) se han abreviado para conservar la legibilidad. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
        MinorVersion="1" MajorBuildNumber="139"
        MinorBuildNumber="0"
        Version="Exchange2010_SP1"
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetInboxRulesResponse ResponseClass="Success"
        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <OutlookRuleBlobExists>true</OutlookRuleBlobExists>
      <InboxRules>
        <Rule xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <RuleId>dCsAAABjzvA=</RuleId>
          <DisplayName>MoveInterestingToJunk</DisplayName>
          <Priority>1</Priority>
          <IsEnabled>true</IsEnabled>
          <Conditions>
            <ContainsSubjectStrings>
              <String>Interesting</String>
            </ContainsSubjectStrings>
          </Conditions>
          <Actions>
            <MoveToFolder>
              <FolderId ChangeKey="AQAAAA==" Id="AAMkAGYzZjZm" />
            </MoveToFolder>
          </Actions>
        </Rule>
      </InboxRules>
    </GetInboxRulesResponse>
  </s:Body>
</s:Envelope>
```

### <a name="response-elements"></a>Elementos de respuesta

En la respuesta se incluyen los siguientes elementos:
  
- [GetInboxRulesResponse](getinboxrulesresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [OutlookRuleBlobExists](outlookruleblobexists.md)
    
- [InboxRules](inboxrules.md)
    
## <a name="see-also"></a>Ver también



[Operación de UpdateInboxRules](updateinboxrules-operation.md)


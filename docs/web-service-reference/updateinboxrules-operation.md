---
title: Operación UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: f982a237-471e-45c5-a2b5-468cfc53150b
description: La operación UpdateInboxRules actualiza las reglas de bandeja de entrada del usuario autenticado mediante la aplicación de las operaciones especificadas. UpdateInboxRules se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada, o para eliminar una regla de bandeja de entrada.
ms.openlocfilehash: 6e979421d619fed6625fe05db86c1f8c6a7418c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840831"
---
# <a name="updateinboxrules-operation"></a>Operación UpdateInboxRules

La operación UpdateInboxRules actualiza las reglas de bandeja de entrada del usuario autenticado mediante la aplicación de las operaciones especificadas. **UpdateInboxRules** se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada, o para eliminar una regla de bandeja de entrada. 
  
Cuando se usa la operación **UpdateInboxRules** , servicios Web de Exchange elimina las reglas de envío del cliente. Reglas de envío del cliente se almacenan en el cliente en la regla de mensaje de la carpeta asociada información (FAI) y en ningún otro lugar. EWS elimina esta regla mensaje FAI de forma predeterminada, basándose en la expectativa que Outlook volverá a crearlo. Sin embargo, Outlook no puede volver a crear las reglas que no existen también como una regla extendida, y no existen reglas de envío del cliente como reglas extendidas. Como resultado, estas reglas se pierden. Es recomendable que considere la posibilidad de esto al diseñar la solución. 
  
## <a name="updateinboxrules-create-rule-request-example"></a>Ejemplo de solicitud de UpdateInboxRules (Crear regla)

Puede usar servicios Web de Exchange para crear una regla de bandeja de entrada en el buzón de un usuario en el almacén de Exchange. Use el elemento [UpdateInboxRules](updateinboxrules.md) junto con el elemento [CreateRuleOperation](createruleoperation.md) para crear una regla. 
  
### <a name="description"></a>Descripción

El cliente construye la solicitud XML y envía al servidor.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:CreateRuleOperation>
            <t:Rule>
              <t:DisplayName>MoveInterestingToJunk</t:DisplayName>
              <t:Priority>1</t:Priority>
              <t:IsEnabled>true</t:IsEnabled>
              <t:Conditions>
                <t:ContainsSubjectStrings>
                  <t:String>Interesting</t:String>
                </t:ContainsSubjectStrings>
              </t:Conditions>
              <t:Exceptions />
              <t:Actions>
                <t:MoveToFolder>
                  <t:DistinguishedFolderId Id="junkemail" />
                </t:MoveToFolder>
              </t:Actions>
            </t:Rule>
          </t:CreateRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a>Comentarios

En este ejemplo se crea una regla que se va a mover un mensaje de correo electrónico a la carpeta correo electrónico no deseado si el asunto de correo electrónico contiene una cadena que es igual a "Interesante".
  
### <a name="request-elements"></a>Elementos de solicitud

La solicitud de **UpdateInboxRules** incluye los siguientes elementos: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
El elemento de [operaciones](operations.md) contiene el elemento [CreateRuleOperation](createruleoperation.md) para crear una regla. 
  
## <a name="updateinboxrules-create-rule-response-example"></a>Ejemplo de respuesta UpdateInboxRules (Crear regla)

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **UpdateInboxRules** que crea una regla. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a>Ejemplo de solicitud de UpdateInboxRules (regla de conjunto)

Puede usar los servicios Web de Exchange para modificar una regla de bandeja de entrada en el buzón del usuario en el almacén de Exchange. Use el elemento [UpdateInboxRules](updateinboxrules.md) junto con el elemento [SetRuleOperation](setruleoperation.md) para modificar una regla. 
  
### <a name="description"></a>Descripción

El cliente construye la solicitud XML y envía al servidor.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <Rule>
              <RuleId>Nh8AAAAwW/w=</RuleId>
              <DisplayName>(Modified) This is Junk</DisplayName>
              <Priority>1</Priority>
              <IsEnabled>true</IsEnabled>
              <Conditions>
                <ContainsSubjectStrings>
                  <String>Interesting</String>
                </ContainsSubjectStrings>
              </Conditions>
              <Actions>
                <MoveToFolder>
                  <FolderId Id="AAMkADQ1YTE1" ChangeKey="AQAAAA==" />
                </MoveToFolder>
              </Actions>
            </Rule>
          </SetRuleOperation>
        </Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a>Comentarios

En este ejemplo se cambia el nombre para mostrar "(modificado) es no deseado".
  
> [!NOTE]
> Los valores del **identificador** y **ChangeKey** atributos del elemento [FolderId](folderid.md) se han abreviado para mejorar la legibilidad. 
  
### <a name="request-elements"></a>Elementos de solicitud

La solicitud de **UpdateInboxRules** incluye los siguientes elementos: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
El elemento de [operaciones](operations.md) contiene el elemento [SetRuleOperation](setruleoperation.md) para modificar una regla. 
  
## <a name="updateinboxrules-set-rule-response-example"></a>Ejemplo de respuesta UpdateInboxRules (regla de conjunto)

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **UpdateInboxRules** que modifica una regla. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a>Ejemplo de solicitud de UpdateInboxRules (Eliminar regla)

Puede usar los servicios Web de Exchange para eliminar una regla de bandeja de entrada en el buzón del usuario en el almacén de Exchange. Para eliminar una regla, use la [UpdateInboxRules](updateinboxrules.md) junto con el elemento [DeleteRuleOperation](deleteruleoperation.md) . 
  
### <a name="description"></a>Descripción

El cliente construye la solicitud XML y envía al servidor.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:DeleteRuleOperation>
            <t:RuleId>Nh8AAAAwW/U=</t:RuleId>
          </t:DeleteRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a>Comentarios

En este ejemplo se elimina la regla identificada existente.
  
### <a name="request-elements"></a>Elementos de solicitud

La solicitud de **UpdateInboxRules** incluye los siguientes elementos: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
El elemento de [operaciones](operations.md) contiene el elemento [DeleteRuleOperation](deleteruleoperation.md) para eliminar una regla. 
  
## <a name="updateinboxrules-delete-rule-response-example"></a>Ejemplo de respuesta UpdateInboxRules (Eliminar regla)

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **UpdateInboxRules** que se elimina una regla. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="see-also"></a>Vea también



[Operación de GetInboxRules](getinboxrules-operation.md)


---
title: Operación UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: f982a237-471e-45c5-a2b5-468cfc53150b
description: La operación UpdateInboxRules actualiza las reglas de la Bandeja de entrada del usuario autenticado aplicando las operaciones especificadas. UpdateInboxRules se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada o para eliminar una regla de bandeja de entrada.
ms.openlocfilehash: 08f46219bcb01f5f1c9d69cfaa8b4934e82ff5bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510718"
---
# <a name="updateinboxrules-operation"></a>Operación UpdateInboxRules

La operación UpdateInboxRules actualiza las reglas de la Bandeja de entrada del usuario autenticado aplicando las operaciones especificadas. **UpdateInboxRules** se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada o para eliminar una regla de bandeja de entrada. 
  
Cuando se usa la **operación UpdateInboxRules,** Exchange Web Services elimina las reglas de envío del lado cliente. Las reglas de envío del lado cliente se almacenan en el cliente en el Mensaje de información asociada de carpetas (FAI) de la regla y en ningún otro lugar. EWS elimina este mensaje FAI de la regla de manera predeterminada, basándose en la expectativa de que Outlook volverá a crearlo. En cambio, Outlook no puede volver a crear reglas que tampoco existen como una regla extendida, y las reglas de envío del lado cliente no existen como reglas extendidas. Como resultado, estas reglas se pierden. Le sugerimos que considere esta posibilidad al diseñar su solución. 
  
## <a name="updateinboxrules-create-rule-request-example"></a>Ejemplo de solicitud UpdateInboxRules (Crear regla)

Puede usar Exchange Web Services para crear una regla de bandeja de entrada en el buzón de un usuario en el Exchange almacén. Use el [elemento UpdateInboxRules](updateinboxrules.md) junto con el [elemento CreateRuleOperation](createruleoperation.md) para crear una regla. 
  
### <a name="description"></a>Descripción

El cliente construye el XML de solicitud y lo envía al servidor.
  
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

En este ejemplo se crea una regla que moverá un mensaje de correo electrónico a la carpeta correo no deseado si el asunto del correo electrónico contiene una cadena que es igual a "Interesante".
  
### <a name="request-elements"></a>Elementos Request

La **solicitud UpdateInboxRules** incluye los siguientes elementos: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
El [elemento Operations](operations.md) contiene el elemento [CreateRuleOperation](createruleoperation.md) para crear una regla. 
  
## <a name="updateinboxrules-create-rule-response-example"></a>Ejemplo de respuesta UpdateInboxRules (Crear regla)

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **UpdateInboxRules** que crea una regla. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a>Ejemplo de solicitud UpdateInboxRules (Establecer regla)

Puede usar Exchange Web Services para modificar una regla de bandeja de entrada en el buzón de un usuario en el Exchange almacén. Use el [elemento UpdateInboxRules](updateinboxrules.md) junto con el [elemento SetRuleOperation](setruleoperation.md) para modificar una regla. 
  
### <a name="description"></a>Descripción

El cliente construye el XML de solicitud y lo envía al servidor.
  
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
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

En este ejemplo se cambia el nombre para mostrar a "(Modified) This is Junk".
  
> [!NOTE]
> Los valores de los **atributos Id** y **ChangeKey** del [elemento FolderId](folderid.md) se han acortado para mejorar la legibilidad. 
  
### <a name="request-elements"></a>Elementos Request

La **solicitud UpdateInboxRules** incluye los siguientes elementos: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
El [elemento Operations](operations.md) contiene el elemento [SetRuleOperation](setruleoperation.md) para modificar una regla. 
  
## <a name="updateinboxrules-set-rule-response-example"></a>Ejemplo de respuesta UpdateInboxRules (Set Rule)

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **UpdateInboxRules** que modifica una regla. 
  
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
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a>Ejemplo de solicitud UpdateInboxRules (Eliminar regla)

Puede usar Exchange Web Services para eliminar una regla de bandeja de entrada en el buzón de un usuario en el Exchange almacén. Use [UpdateInboxRules](updateinboxrules.md) junto con el [elemento DeleteRuleOperation](deleteruleoperation.md) para eliminar una regla. 
  
### <a name="description"></a>Descripción

El cliente construye el XML de solicitud y lo envía al servidor.
  
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
  
### <a name="request-elements"></a>Elementos Request

La **solicitud UpdateInboxRules** incluye los siguientes elementos: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
El [elemento Operations](operations.md) contiene el elemento [DeleteRuleOperation](deleteruleoperation.md) para eliminar una regla. 
  
## <a name="updateinboxrules-delete-rule-response-example"></a>Ejemplo de respuesta UpdateInboxRules (Eliminar regla)

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **UpdateInboxRules** que elimina una regla. 
  
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
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="see-also"></a>Ver también



[Operación de GetInboxRules](getinboxrules-operation.md)


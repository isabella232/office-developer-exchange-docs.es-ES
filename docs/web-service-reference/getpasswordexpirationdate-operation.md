---
title: Operación GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: La operación GetPasswordExpirationDate proporciona la fecha de expiración de la contraseña de la cuenta de correo electrónico para el usuario actual.
ms.openlocfilehash: 07928fd3e6fca410a292d6cd74f1240d8e81c42f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524241"
---
# <a name="getpasswordexpirationdate-operation"></a>Operación GetPasswordExpirationDate

La **operación GetPasswordExpirationDate** proporciona la fecha de expiración de la contraseña de la cuenta de correo electrónico para el usuario actual. 
  
Esta operación se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>Encabezados SOAP de la operación GetPasswordExpirationDate

La **operación GetPasswordExpirationDate** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Esto es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica el esquema de la solicitud de operación. Esto es aplicable a una solicitud. Esto es aplicable a una solicitud.  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>Ejemplo de solicitud de operación GetPasswordExpirationDate

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud de **operación GetPasswordExpirationDate** se muestra cómo obtener la fecha de expiración de contraseña para una cuenta de correo electrónico. 
  
### <a name="code"></a>Código

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [GetPasswordExpirationDate](getpasswordexpirationdate.md)
    
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>Respuesta de operación GetPasswordExpirationDate correcta

En la respuesta se usan los siguientes elementos:
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    


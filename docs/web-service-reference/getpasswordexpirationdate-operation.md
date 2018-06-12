---
title: Operación GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: La operación GetPasswordExpirationDate proporciona la fecha de caducidad de contraseña de cuenta de correo electrónico para el usuario actual.
ms.openlocfilehash: c57942c88b09a910e2d529a12ea279bb2da5d693
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764932"
---
# <a name="getpasswordexpirationdate-operation"></a>Operación GetPasswordExpirationDate

La operación **GetPasswordExpirationDate** proporciona la fecha de caducidad de contraseña de cuenta de correo electrónico para el usuario actual. 
  
Esta operación se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>Encabezados SOAP de operación de GetPasswordExpirationDate

La operación de **GetPasswordExpirationDate** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Header**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Esto es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica el esquema de la solicitud de la operación. Esto es aplicable a una solicitud. Esto es aplicable a una solicitud.  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>Ejemplo de solicitud de operación de GetPasswordExpirationDate

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de operación **GetPasswordExpirationDate** muestra cómo obtener la fecha de caducidad de contraseña para una cuenta de correo electrónico. 
  
### <a name="code"></a>Código

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [GetPasswordExpirationDate](getpasswordexpirationdate.md)
    
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>Respuesta es correcta de operación GetPasswordExpirationDate

En la respuesta se usan los siguientes elementos:
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    


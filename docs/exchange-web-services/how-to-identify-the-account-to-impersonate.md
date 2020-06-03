---
title: Identificación de la cuenta que se va a suplantar
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: c7749f12-b97f-48d9-88e5-a545e108efb0
description: Obtenga información sobre cómo la aplicación de servicio usa EWS para identificar al usuario que se va a suplantar.
localization_priority: Priority
ms.openlocfilehash: 7159707abe96632aba2ed70dc0057417e087349f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527995"
---
# <a name="identify-the-account-to-impersonate"></a>Identificación de la cuenta que se va a suplantar

Obtenga información sobre cómo la aplicación de servicio usa EWS para identificar al usuario que se va a suplantar.
  
La aplicación de servicio identifica la cuenta de usuario que se va a suplantar mediante uno de los tres identificadores siguientes:
  
- La dirección SMTP principal.
    
- El nombre principal del usuario (UPN).
    
- Identificador de seguridad (SID).
    
El identificador que se usa depende, por supuesto, de la información que la aplicación tiene disponible.
  
## <a name="identifying-the-user-account-to-impersonate"></a>Identificación de la cuenta de usuario que se va a suplantar

La aplicación puede usar la API administrada de EWS o las solicitudes SOAP de EWS para identificar la cuenta de usuario que se va a suplantar. La API administrada de EWS usa la propiedad [ExchangeService. ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) para identificar al usuario suplantado. EWS usa el elemento [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) , como se muestra en el siguiente fragmento XML. 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

En cada una de las siguientes secciones se muestra cómo usar uno de los identificadores. Para obtener un ejemplo que muestre el identificador de suplantación en acción, vea [Agregar citas mediante la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md).
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a>Usar la dirección de correo electrónico SMTP para identificar la cuenta de usuario

La dirección de correo electrónico SMTP es la dirección de correo electrónico principal asociada a una cuenta de usuario.
  
En una aplicación de la API administrada de EWS, especifique la dirección de correo electrónico SMTP junto con el valor de enumeración [ConnectingIdType. SMTP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) . 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

En una solicitud SOAP de EWS, el elemento [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) contiene la dirección de correo electrónico de la cuenta de usuario. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a>Usar el UPN para identificar la cuenta de usuario

El UPN contiene el nombre de dominio completo (FQDN) para la ubicación de la cuenta de usuario. No es necesariamente el dominio del buzón de correo del usuario. El atributo **UserPrincipalName** debe establecerse correctamente en la cuenta de usuario en servicios de dominio de Active Directory (AD DS) para que la búsqueda de usuario se realice correctamente. 
  
En una aplicación de la API administrada de EWS, especifique el UPN junto con el valor de enumeración [ConnectingIdType. PrincipalName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) . 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipalName, "alias@billing.contoso.com");
```

En una solicitud SOAP de EWS, el elemento [PrincipalName (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md) contiene el UPN de la cuenta de usuario. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a>Usar el SID para identificar la cuenta de usuario

El SID es el identificador de la cuenta que se va a suplantar en el formato de lenguaje de definición de descriptores de seguridad (SDDL).
  
En una aplicación de la API administrada de EWS, especifique el SID junto con el valor de enumeración [ConnectingIdType. SID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) . 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

En una solicitud SOAP de EWS, el elemento [SID](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) contiene el SID de la cuenta de usuario. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a>Vea también


- [Suplantación y EWS en Exchange](impersonation-and-ews-in-exchange.md)
    
- [Adición de citas mediante la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [Clase ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    


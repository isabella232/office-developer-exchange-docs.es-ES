---
title: Identificación de la cuenta para suplantar a
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c7749f12-b97f-48d9-88e5-a545e108efb0
description: Obtenga información sobre cómo utiliza su aplicación de servicio EWS para identificar al usuario para suplantar.
ms.openlocfilehash: 78df4b511a9947d4d815b2802a53ab178b14622b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763073"
---
# <a name="identify-the-account-to-impersonate"></a>Identificación de la cuenta para suplantar a

Obtenga información sobre cómo utiliza su aplicación de servicio EWS para identificar al usuario para suplantar.
  
La aplicación de servicio identifica la cuenta de usuario para suplantar mediante uno de los identificadores de tres siguientes:
  
- La dirección SMTP principal.
    
- El nombre de principal de usuario (UPN).
    
- El identificador de seguridad (SID).
    
El identificador que utilice depende, por supuesto, la información que la aplicación tenga disponibles.
  
## <a name="identifying-the-user-account-to-impersonate"></a>Identificación de la cuenta de usuario para suplantar a

La aplicación puede utilizar las solicitudes de la API administrada de EWS o EWS SOAP para identificar la cuenta de usuario que está realizando la suplantación. La API administrada de EWS, se utiliza la propiedad [ExchangeService.ImpersonatedUserId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) para identificar el usuario suplantado. EWS usa el elemento [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) , tal como se muestra en el siguiente fragmento XML. 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

Cada una de las siguientes secciones muestra cómo usar uno de los identificadores. Para obtener un ejemplo que muestra el identificador de suplantación en acción, vea [Agregar citas mediante el uso de la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md).
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a>Use la dirección de correo electrónico SMTP para identificar la cuenta de usuario

La dirección de correo electrónico SMTP es la dirección de correo electrónico principal que está asociada con una cuenta de usuario.
  
En una aplicación de API administrada de EWS, especifique la dirección de correo electrónico SMTP junto con el valor de la enumeración [ConnectingIdType.SMTP](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) . 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

En una solicitud de EWS SOAP, el elemento [PrimarySmtpAddress](http://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) contiene la dirección de correo electrónico para la cuenta de usuario. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a>Use el UPN para identificar la cuenta de usuario

El UPN contiene el nombre de dominio completo (FQDN) para la ubicación de la cuenta de usuario. Esto no es necesariamente dominio de buzón de correo del usuario. El atributo **UserPrincipleName** debe establecerse correctamente en la cuenta de usuario en servicios de dominio de Active Directory (AD DS) para que la búsqueda de usuarios se realice correctamente. 
  
En una aplicación de API administrada de EWS, especifique el UPN junto con el valor de la enumeración [ConnectingIdType.PrincipleName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) . 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipleName, "alias@billing.contoso.com");
```

En una solicitud SOAP de EWS, el [elemento PrincipalName (ConnectingSIDType complexType) (EWS)](http://msdn.microsoft.com/library/6aac5388-c971-817b-b0bb-095a2639c6de%28Office.15%29.aspx) elemento contiene el UPN de la cuenta de usuario. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a>Use el SID para identificar la cuenta de usuario

El SID es el identificador de la cuenta para acceder al formulario de idioma (SDDL) de definición de descriptor de seguridad.
  
En una aplicación de API administrada de EWS, especifique al SID junto con el valor de la enumeración [ConnectingIdType.SID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) . 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

En una solicitud de EWS SOAP, el elemento de [SID](http://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) contiene al SID para la cuenta de usuario. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a>Ver también


- [Suplantación y EWS en Exchange](impersonation-and-ews-in-exchange.md)
    
- [Agregar citas mediante el uso de la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [Clase ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    


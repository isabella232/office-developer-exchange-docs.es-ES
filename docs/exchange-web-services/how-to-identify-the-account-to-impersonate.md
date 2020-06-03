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
# <a name="identify-the-account-to-impersonate"></a><span data-ttu-id="dbad6-103">Identificación de la cuenta que se va a suplantar</span><span class="sxs-lookup"><span data-stu-id="dbad6-103">Identify the account to impersonate</span></span>

<span data-ttu-id="dbad6-104">Obtenga información sobre cómo la aplicación de servicio usa EWS para identificar al usuario que se va a suplantar.</span><span class="sxs-lookup"><span data-stu-id="dbad6-104">Learn how your service application uses EWS to identify the user to impersonate.</span></span>
  
<span data-ttu-id="dbad6-105">La aplicación de servicio identifica la cuenta de usuario que se va a suplantar mediante uno de los tres identificadores siguientes:</span><span class="sxs-lookup"><span data-stu-id="dbad6-105">Your service application identifies the user account to impersonate by using one of the following three identifiers:</span></span>
  
- <span data-ttu-id="dbad6-106">La dirección SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="dbad6-106">The primary SMTP address.</span></span>
    
- <span data-ttu-id="dbad6-107">El nombre principal del usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="dbad6-107">The user principal name (UPN).</span></span>
    
- <span data-ttu-id="dbad6-108">Identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="dbad6-108">The security identifier (SID).</span></span>
    
<span data-ttu-id="dbad6-109">El identificador que se usa depende, por supuesto, de la información que la aplicación tiene disponible.</span><span class="sxs-lookup"><span data-stu-id="dbad6-109">The identifier that you use depends, of course, on the information that your application has available.</span></span>
  
## <a name="identifying-the-user-account-to-impersonate"></a><span data-ttu-id="dbad6-110">Identificación de la cuenta de usuario que se va a suplantar</span><span class="sxs-lookup"><span data-stu-id="dbad6-110">Identifying the user account to impersonate</span></span>

<span data-ttu-id="dbad6-111">La aplicación puede usar la API administrada de EWS o las solicitudes SOAP de EWS para identificar la cuenta de usuario que se va a suplantar.</span><span class="sxs-lookup"><span data-stu-id="dbad6-111">Your application can use either the EWS Managed API or EWS SOAP requests to identify the user account that it is impersonating.</span></span> <span data-ttu-id="dbad6-112">La API administrada de EWS usa la propiedad [ExchangeService. ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) para identificar al usuario suplantado.</span><span class="sxs-lookup"><span data-stu-id="dbad6-112">The EWS Managed API uses the [ExchangeService.ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property to identify the impersonated user.</span></span> <span data-ttu-id="dbad6-113">EWS usa el elemento [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) , como se muestra en el siguiente fragmento XML.</span><span class="sxs-lookup"><span data-stu-id="dbad6-113">EWS uses the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) element, as shown in the following XML fragment.</span></span> 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

<span data-ttu-id="dbad6-114">En cada una de las siguientes secciones se muestra cómo usar uno de los identificadores.</span><span class="sxs-lookup"><span data-stu-id="dbad6-114">Each of the following sections shows how to use one of the identifiers.</span></span> <span data-ttu-id="dbad6-115">Para obtener un ejemplo que muestre el identificador de suplantación en acción, vea [Agregar citas mediante la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md).</span><span class="sxs-lookup"><span data-stu-id="dbad6-115">For an example that shows the impersonation identifier in action, see [Add appointments by using Exchange impersonation](how-to-add-appointments-by-using-exchange-impersonation.md).</span></span>
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a><span data-ttu-id="dbad6-116">Usar la dirección de correo electrónico SMTP para identificar la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="dbad6-116">Use the SMTP email address to identify the user account</span></span>

<span data-ttu-id="dbad6-117">La dirección de correo electrónico SMTP es la dirección de correo electrónico principal asociada a una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="dbad6-117">The SMTP email address is the primary email address that is associated with a user account.</span></span>
  
<span data-ttu-id="dbad6-118">En una aplicación de la API administrada de EWS, especifique la dirección de correo electrónico SMTP junto con el valor de enumeración [ConnectingIdType. SMTP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dbad6-118">In an EWS Managed API application, you specify the SMTP email address along with the [ConnectingIdType.SMTP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

<span data-ttu-id="dbad6-119">En una solicitud SOAP de EWS, el elemento [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) contiene la dirección de correo electrónico de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="dbad6-119">In an EWS SOAP request, the [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) element contains the email address for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a><span data-ttu-id="dbad6-120">Usar el UPN para identificar la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="dbad6-120">Use the UPN to identify the user account</span></span>

<span data-ttu-id="dbad6-121">El UPN contiene el nombre de dominio completo (FQDN) para la ubicación de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="dbad6-121">The UPN contains the fully qualified domain name (FQDN) for the location of the user account.</span></span> <span data-ttu-id="dbad6-122">No es necesariamente el dominio del buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="dbad6-122">This is not necessarily the user's mailbox domain.</span></span> <span data-ttu-id="dbad6-123">El atributo **UserPrincipalName** debe establecerse correctamente en la cuenta de usuario en servicios de dominio de Active Directory (AD DS) para que la búsqueda de usuario se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="dbad6-123">The **UserPrincipalName** attribute must be set correctly on the user account in Active Directory Domain Services (AD DS) for the user lookup to succeed.</span></span> 
  
<span data-ttu-id="dbad6-124">En una aplicación de la API administrada de EWS, especifique el UPN junto con el valor de enumeración [ConnectingIdType. PrincipalName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dbad6-124">In an EWS Managed API application, you specify the UPN along with the [ConnectingIdType.PrincipalName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipalName, "alias@billing.contoso.com");
```

<span data-ttu-id="dbad6-125">En una solicitud SOAP de EWS, el elemento [PrincipalName (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md) contiene el UPN de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="dbad6-125">In an EWS SOAP request, the [PrincipalName element (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md) element contains the UPN for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a><span data-ttu-id="dbad6-126">Usar el SID para identificar la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="dbad6-126">Use the SID to identify the user account</span></span>

<span data-ttu-id="dbad6-127">El SID es el identificador de la cuenta que se va a suplantar en el formato de lenguaje de definición de descriptores de seguridad (SDDL).</span><span class="sxs-lookup"><span data-stu-id="dbad6-127">The SID is the identifier of the account to be impersonated in security descriptor definition language (SDDL) form.</span></span>
  
<span data-ttu-id="dbad6-128">En una aplicación de la API administrada de EWS, especifique el SID junto con el valor de enumeración [ConnectingIdType. SID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dbad6-128">In an EWS Managed API application, you specify the SID along with the [ConnectingIdType.SID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

<span data-ttu-id="dbad6-129">En una solicitud SOAP de EWS, el elemento [SID](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) contiene el SID de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="dbad6-129">In an EWS SOAP request, the [SID](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) element contains the SID for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a><span data-ttu-id="dbad6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbad6-130">See also</span></span>


- [<span data-ttu-id="dbad6-131">Suplantación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dbad6-131">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="dbad6-132">Adición de citas mediante la suplantación de Exchange</span><span class="sxs-lookup"><span data-stu-id="dbad6-132">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [<span data-ttu-id="dbad6-133">Clase ExchangeService</span><span class="sxs-lookup"><span data-stu-id="dbad6-133">ExchangeService class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [<span data-ttu-id="dbad6-134">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="dbad6-134">ExchangeImpersonation</span></span>](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    


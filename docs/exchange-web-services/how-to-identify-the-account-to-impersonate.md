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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763073"
---
# <a name="identify-the-account-to-impersonate"></a><span data-ttu-id="f74fc-103">Identificación de la cuenta para suplantar a</span><span class="sxs-lookup"><span data-stu-id="f74fc-103">Identify the account to impersonate</span></span>

<span data-ttu-id="f74fc-104">Obtenga información sobre cómo utiliza su aplicación de servicio EWS para identificar al usuario para suplantar.</span><span class="sxs-lookup"><span data-stu-id="f74fc-104">Learn how your service application uses EWS to identify the user to impersonate.</span></span>
  
<span data-ttu-id="f74fc-105">La aplicación de servicio identifica la cuenta de usuario para suplantar mediante uno de los identificadores de tres siguientes:</span><span class="sxs-lookup"><span data-stu-id="f74fc-105">Your service application identifies the user account to impersonate by using one of the following three identifiers:</span></span>
  
- <span data-ttu-id="f74fc-106">La dirección SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="f74fc-106">The primary SMTP address.</span></span>
    
- <span data-ttu-id="f74fc-107">El nombre de principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="f74fc-107">The user principle name (UPN).</span></span>
    
- <span data-ttu-id="f74fc-108">El identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="f74fc-108">The security identifier (SID).</span></span>
    
<span data-ttu-id="f74fc-109">El identificador que utilice depende, por supuesto, la información que la aplicación tenga disponibles.</span><span class="sxs-lookup"><span data-stu-id="f74fc-109">The identifier that you use depends, of course, on the information that your application has available.</span></span>
  
## <a name="identifying-the-user-account-to-impersonate"></a><span data-ttu-id="f74fc-110">Identificación de la cuenta de usuario para suplantar a</span><span class="sxs-lookup"><span data-stu-id="f74fc-110">Identifying the user account to impersonate</span></span>

<span data-ttu-id="f74fc-111">La aplicación puede utilizar las solicitudes de la API administrada de EWS o EWS SOAP para identificar la cuenta de usuario que está realizando la suplantación.</span><span class="sxs-lookup"><span data-stu-id="f74fc-111">Your application can use either the EWS Managed API or EWS SOAP requests to identify the user account that it is impersonating.</span></span> <span data-ttu-id="f74fc-112">La API administrada de EWS, se utiliza la propiedad [ExchangeService.ImpersonatedUserId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) para identificar el usuario suplantado.</span><span class="sxs-lookup"><span data-stu-id="f74fc-112">The EWS Managed API uses the [ExchangeService.ImpersonatedUserId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property to identify the impersonated user.</span></span> <span data-ttu-id="f74fc-113">EWS usa el elemento [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) , tal como se muestra en el siguiente fragmento XML.</span><span class="sxs-lookup"><span data-stu-id="f74fc-113">EWS uses the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) element, as shown in the following XML fragment.</span></span> 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

<span data-ttu-id="f74fc-114">Cada una de las siguientes secciones muestra cómo usar uno de los identificadores.</span><span class="sxs-lookup"><span data-stu-id="f74fc-114">Each of the following sections shows how to use one of the identifiers.</span></span> <span data-ttu-id="f74fc-115">Para obtener un ejemplo que muestra el identificador de suplantación en acción, vea [Agregar citas mediante el uso de la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md).</span><span class="sxs-lookup"><span data-stu-id="f74fc-115">For an example that shows the impersonation identifier in action, see [Add appointments by using Exchange impersonation](how-to-add-appointments-by-using-exchange-impersonation.md).</span></span>
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a><span data-ttu-id="f74fc-116">Use la dirección de correo electrónico SMTP para identificar la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="f74fc-116">Use the SMTP email address to identify the user account</span></span>

<span data-ttu-id="f74fc-117">La dirección de correo electrónico SMTP es la dirección de correo electrónico principal que está asociada con una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f74fc-117">The SMTP email address is the primary email address that is associated with a user account.</span></span>
  
<span data-ttu-id="f74fc-118">En una aplicación de API administrada de EWS, especifique la dirección de correo electrónico SMTP junto con el valor de la enumeración [ConnectingIdType.SMTP](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f74fc-118">In an EWS Managed API application, you specify the SMTP email address along with the [ConnectingIdType.SMTP](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

<span data-ttu-id="f74fc-119">En una solicitud de EWS SOAP, el elemento [PrimarySmtpAddress](http://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) contiene la dirección de correo electrónico para la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f74fc-119">In an EWS SOAP request, the [PrimarySmtpAddress](http://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) element contains the email address for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a><span data-ttu-id="f74fc-120">Use el UPN para identificar la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="f74fc-120">Use the UPN to identify the user account</span></span>

<span data-ttu-id="f74fc-121">El UPN contiene el nombre de dominio completo (FQDN) para la ubicación de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f74fc-121">The UPN contains the fully qualified domain name (FQDN) for the location of the user account.</span></span> <span data-ttu-id="f74fc-122">Esto no es necesariamente dominio de buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f74fc-122">This is not necessarily the user's mailbox domain.</span></span> <span data-ttu-id="f74fc-123">El atributo **UserPrincipleName** debe establecerse correctamente en la cuenta de usuario en servicios de dominio de Active Directory (AD DS) para que la búsqueda de usuarios se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="f74fc-123">The **UserPrincipleName** attribute must be set correctly on the user account in Active Directory Domain Services (AD DS) for the user lookup to succeed.</span></span> 
  
<span data-ttu-id="f74fc-124">En una aplicación de API administrada de EWS, especifique el UPN junto con el valor de la enumeración [ConnectingIdType.PrincipleName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f74fc-124">In an EWS Managed API application, you specify the UPN along with the [ConnectingIdType.PrincipleName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipleName, "alias@billing.contoso.com");
```

<span data-ttu-id="f74fc-125">En una solicitud SOAP de EWS, el [elemento PrincipalName (ConnectingSIDType complexType) (EWS)](http://msdn.microsoft.com/library/6aac5388-c971-817b-b0bb-095a2639c6de%28Office.15%29.aspx) elemento contiene el UPN de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f74fc-125">In an EWS SOAP request, the [PrincipalName element (ConnectingSIDType complexType) (EWS)](http://msdn.microsoft.com/library/6aac5388-c971-817b-b0bb-095a2639c6de%28Office.15%29.aspx) element contains the UPN for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a><span data-ttu-id="f74fc-126">Use el SID para identificar la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="f74fc-126">Use the SID to identify the user account</span></span>

<span data-ttu-id="f74fc-127">El SID es el identificador de la cuenta para acceder al formulario de idioma (SDDL) de definición de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f74fc-127">The SID is the identifier of the account to be impersonated in security descriptor definition language (SDDL) form.</span></span>
  
<span data-ttu-id="f74fc-128">En una aplicación de API administrada de EWS, especifique al SID junto con el valor de la enumeración [ConnectingIdType.SID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f74fc-128">In an EWS Managed API application, you specify the SID along with the [ConnectingIdType.SID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

<span data-ttu-id="f74fc-129">En una solicitud de EWS SOAP, el elemento de [SID](http://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) contiene al SID para la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f74fc-129">In an EWS SOAP request, the [SID](http://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) element contains the SID for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a><span data-ttu-id="f74fc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f74fc-130">See also</span></span>


- [<span data-ttu-id="f74fc-131">Suplantación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f74fc-131">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f74fc-132">Agregar citas mediante el uso de la suplantación de Exchange</span><span class="sxs-lookup"><span data-stu-id="f74fc-132">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [<span data-ttu-id="f74fc-133">Clase ExchangeService</span><span class="sxs-lookup"><span data-stu-id="f74fc-133">ExchangeService class</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [<span data-ttu-id="f74fc-134">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f74fc-134">ExchangeImpersonation</span></span>](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    


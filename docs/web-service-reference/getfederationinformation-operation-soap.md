---
title: Operación GetFederationInformation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6666a42-a18f-4e4b-beb6-b25ff62cfcc5
description: La operación GetFederationInformation proporciona información sobre el estado de Federación de la organización, como el URI de destino que se va a usar al solicitar tokens destinados a esta organización, y los otros dominios que la organización también ha federado.
ms.openlocfilehash: 533b2f6d282e3287f4945df56b169f5bc93ff445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455628"
---
# <a name="getfederationinformation-operation-soap"></a><span data-ttu-id="23ebc-103">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-103">GetFederationInformation operation (SOAP)</span></span>

<span data-ttu-id="23ebc-104">La operación **GetFederationInformation** proporciona información sobre el estado de Federación de la organización, como el URI de destino que se va a usar al solicitar tokens destinados a esta organización, y los otros dominios que la organización también ha federado.</span><span class="sxs-lookup"><span data-stu-id="23ebc-104">The **GetFederationInformation** operation provides information about the federation status of the organization, such as the target URI to be used when requesting tokens that are targeted at this organization, and the other domains that the organization has also federated.</span></span> 
  
<span data-ttu-id="23ebc-105">Solo las organizaciones federadas pueden compartir el calendario, los contactos y los mensajes con los usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="23ebc-105">Only federated organizations can share calendar, contacts, and messages to external users.</span></span>
  
## <a name="getfederationinformation-request-example"></a><span data-ttu-id="23ebc-106">Ejemplo de solicitud GetFederationInformation</span><span class="sxs-lookup"><span data-stu-id="23ebc-106">GetFederationInformation request example</span></span>

### <a name="description"></a><span data-ttu-id="23ebc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="23ebc-107">Description</span></span>

<span data-ttu-id="23ebc-108">El siguiente ejemplo de una solicitud **GetFederationInformation** muestra una solicitud de información de Federación de un usuario.</span><span class="sxs-lookup"><span data-stu-id="23ebc-108">The following example of a **GetFederationInformation** request shows a request for a user's federation information.</span></span> <span data-ttu-id="23ebc-109">El cliente envía esta solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="23ebc-109">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="23ebc-110">Código</span><span class="sxs-lookup"><span data-stu-id="23ebc-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="https://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="https://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">https://schemas.microsoft.com/
            exchange/2010/Autodiscover/Autodiscover/GetFederationInformation
        </a:Action> 
        <a:To soap:mustUnderstand="1">https://autodiscover.byfcxu-
            dom.extest.microsoft.com/autodiscover/autodiscover.svc</a:To> 
        <a:ReplyTo>
            <a:Address>http://www.w3.org/2005/08/addressing/anonymous</a:Address> 
        </a:ReplyTo> 
    </soap:Header> 
    <soap:Body> 
        <GetFederationInformationRequestMessage 
            xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Request> 
                <Domain>contoso.com</Domain> 
            </Request> 
        </GetFederationInformationRequestMessage>
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="23ebc-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="23ebc-111">Request elements</span></span>

<span data-ttu-id="23ebc-112">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="23ebc-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="23ebc-113">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-113">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md)
    
- [<span data-ttu-id="23ebc-114">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-114">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="23ebc-115">Dominio (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-115">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a><span data-ttu-id="23ebc-116">Ejemplo de respuesta GetFederationInformation</span><span class="sxs-lookup"><span data-stu-id="23ebc-116">GetFederationInformation response example</span></span>

### <a name="description"></a><span data-ttu-id="23ebc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="23ebc-117">Description</span></span>

<span data-ttu-id="23ebc-118">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **GetFederationInformation** que el servidor envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="23ebc-118">The following example shows a successful response to the **GetFederationInformation** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="23ebc-119">Código</span><span class="sxs-lookup"><span data-stu-id="23ebc-119">Code</span></span>

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage/> 
                <ApplicationUri>BYFCXU-DOM.EXTEST.MICROSOFT.COM</ApplicationUri> 
                <Domains> 
                    <Domain>contoso.com</Domain> 
                    <Domain>europe.contoso.com</Domain> 
                    <Domain>americas.contoso.com</Domain> 
                    <Domain>contosolive.com</Domain> 
                </Domains> 
            </Response> 
        </GetFederationInformationResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="23ebc-120">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="23ebc-120">Response elements</span></span>

<span data-ttu-id="23ebc-121">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="23ebc-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="23ebc-122">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-122">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md)
    
- [<span data-ttu-id="23ebc-123">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-123">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="23ebc-124">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-124">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="23ebc-125">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-125">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="23ebc-126">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-126">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md)
    
- [<span data-ttu-id="23ebc-127">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-127">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="23ebc-128">Dominio (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-128">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="23ebc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="23ebc-129">See also</span></span>

- [<span data-ttu-id="23ebc-130">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="23ebc-131">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="23ebc-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)


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
description: La operación GetFederationInformation proporciona información sobre el estado de federación de la organización, como el identificador URI que se usará al solicitar tokens que van dirigidos a esta organización y el resto de los dominios que la organización tiene también de destino federados.
ms.openlocfilehash: bf38b2f2b3db3e38b9b0157d1677efe4fc274e1b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764850"
---
# <a name="getfederationinformation-operation-soap"></a><span data-ttu-id="fa339-103">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-103">GetFederationInformation operation (SOAP)</span></span>

<span data-ttu-id="fa339-104">La operación **GetFederationInformation** proporciona información sobre el estado de federación de la organización, como el destino de URI que se utilizará al solicitar tokens que van dirigidas a esta organización y los demás dominios que la organización También se ha federados.</span><span class="sxs-lookup"><span data-stu-id="fa339-104">The **GetFederationInformation** operation provides information about the federation status of the organization, such as the target URI to be used when requesting tokens that are targeted at this organization, and the other domains that the organization has also federated.</span></span> 
  
<span data-ttu-id="fa339-105">Sólo las organizaciones federadas pueden compartir calendario, contactos y mensajes a los usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="fa339-105">Only federated organizations can share calendar, contacts, and messages to external users.</span></span>
  
## <a name="getfederationinformation-request-example"></a><span data-ttu-id="fa339-106">Ejemplo de solicitud de GetFederationInformation</span><span class="sxs-lookup"><span data-stu-id="fa339-106">GetFederationInformation request example</span></span>

### <a name="description"></a><span data-ttu-id="fa339-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa339-107">Description</span></span>

<span data-ttu-id="fa339-108">El siguiente ejemplo de una solicitud de **GetFederationInformation** muestra una solicitud de información de la federación de un usuario.</span><span class="sxs-lookup"><span data-stu-id="fa339-108">The following example of a **GetFederationInformation** request shows a request for a user's federation information.</span></span> <span data-ttu-id="fa339-109">El cliente envía esta solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="fa339-109">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="fa339-110">Código</span><span class="sxs-lookup"><span data-stu-id="fa339-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="http://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="http://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">http://schemas.microsoft.com/
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
            xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Request> 
                <Domain>contoso.com</Domain> 
            </Request> 
        </GetFederationInformationRequestMessage>
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="fa339-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="fa339-111">Request elements</span></span>

<span data-ttu-id="fa339-112">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fa339-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="fa339-113">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-113">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md)
    
- [<span data-ttu-id="fa339-114">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-114">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="fa339-115">Dominio (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-115">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a><span data-ttu-id="fa339-116">Ejemplo de respuesta GetFederationInformation</span><span class="sxs-lookup"><span data-stu-id="fa339-116">GetFederationInformation response example</span></span>

### <a name="description"></a><span data-ttu-id="fa339-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa339-117">Description</span></span>

<span data-ttu-id="fa339-118">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **GetFederationInformation** que el servidor envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="fa339-118">The following example shows a successful response to the **GetFederationInformation** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="fa339-119">Código</span><span class="sxs-lookup"><span data-stu-id="fa339-119">Code</span></span>

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
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

### <a name="response-elements"></a><span data-ttu-id="fa339-120">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="fa339-120">Response elements</span></span>

<span data-ttu-id="fa339-121">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fa339-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="fa339-122">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-122">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md)
    
- [<span data-ttu-id="fa339-123">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-123">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="fa339-124">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-124">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="fa339-125">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-125">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="fa339-126">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-126">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md)
    
- [<span data-ttu-id="fa339-127">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-127">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="fa339-128">Dominio (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-128">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="fa339-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa339-129">See also</span></span>

- [<span data-ttu-id="fa339-130">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="fa339-131">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fa339-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)


---
title: Operación GetDomainSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a6f4a53d-d7f6-4ad1-8afb-78745c500eaa
description: La operación GetDomainSettings recupera la configuración especificada del dominio para el usuario. Detección automática devuelve los dominios que se van a detectar y la configuración solicitada de esos dominios.
ms.openlocfilehash: fd655e088b73372bc1dd68a740ebc2b516d1804a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460970"
---
# <a name="getdomainsettings-operation-soap"></a><span data-ttu-id="e52f8-104">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-104">GetDomainSettings operation (SOAP)</span></span>

<span data-ttu-id="e52f8-105">La operación **GetDomainSettings** recupera la configuración especificada del dominio para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e52f8-105">The **GetDomainSettings** operation retrieves the specified settings of the domain for the user.</span></span> <span data-ttu-id="e52f8-106">Detección automática devuelve los dominios que se van a detectar y la configuración solicitada de esos dominios.</span><span class="sxs-lookup"><span data-stu-id="e52f8-106">Autodiscover returns the domains that are to be discovered and the requested settings of those domains.</span></span> 
  
## <a name="getdomainsettings-request-example"></a><span data-ttu-id="e52f8-107">Ejemplo de solicitud GetDomainSettings</span><span class="sxs-lookup"><span data-stu-id="e52f8-107">GetDomainSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="e52f8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e52f8-108">Description</span></span>

<span data-ttu-id="e52f8-109">El siguiente ejemplo de una solicitud de **GetDomainSettings** muestra una solicitud para la configuración de dominio de **ExternalEWSUrl** de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e52f8-109">The following example of a **GetDomainSettings** request shows a request for a user's **ExternalEWSUrl** domain settings.</span></span> <span data-ttu-id="e52f8-110">El cliente envía esta solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="e52f8-110">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e52f8-111">Código</span><span class="sxs-lookup"><span data-stu-id="e52f8-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soap:Header> 
        <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
        <wsa:Action>https://schemas.microsoft.com/exchange/2010/
            Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
        <wsa:To>
            https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc
        </wsa:To>
    </soap:Header> 
    <soap:Body> 
        <a:GetDomainSettingsRequestMessage xmlns:a="https://schemas.microsoft.com
            /exchange/2010/Autodiscover"> 
            <a:Request> 
                <a:Domains> 
                    <a:Domain>contoso.com<</a:Domain> 
                </a:Domains> 
                <a:RequestedSettings> 
                    <a:Setting>ExternalEwsUrl</a:Setting> 
                </a:RequestedSettings> 
            </a:Request> 
        </a:GetDomainSettingsRequestMessage> 
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="e52f8-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="e52f8-112">Request elements</span></span>

<span data-ttu-id="e52f8-113">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="e52f8-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e52f8-114">GetDomainSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-114">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md)
    
- [<span data-ttu-id="e52f8-115">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-115">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="e52f8-116">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-116">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="e52f8-117">Dominio (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-117">Domain (SOAP)</span></span>](domain-soap.md)
    
- [<span data-ttu-id="e52f8-118">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-118">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md)
    
- [<span data-ttu-id="e52f8-119">Configuración (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-119">Setting (SOAP)</span></span>](setting-soap.md)
    
## <a name="getdomainsettings-response-example"></a><span data-ttu-id="e52f8-120">Ejemplo de respuesta GetDomainSettings</span><span class="sxs-lookup"><span data-stu-id="e52f8-120">GetDomainSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="e52f8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e52f8-121">Description</span></span>

<span data-ttu-id="e52f8-122">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **GetDomainSettings** que el servidor envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="e52f8-122">The following example shows a successful response to the **GetDomainSettings** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e52f8-123">Código</span><span class="sxs-lookup"><span data-stu-id="e52f8-123">Code</span></span>

```XML
//www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/ 
            Autodiscover/Autodiscover/GetDomainSettingsResponse
        </a:Action> 
        <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
            xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
        <h:MajorVersion>14</h:MajorVersion> 
        <h:MinorVersion>0</h:MinorVersion> 
        <h:MajorBuildNumber>639</h:MajorBuildNumber> 
        <h:MinorBuildNumber>20</h:MinorBuildNumber> 
        <h:Version>Exchange2010</h:Version> 
        </h:ServerVersionInfo>
    </s:Header> 
    <s:Body> 
        <GetDomainSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage /> 
                <DomainResponses> 
                    <DomainResponse> 
                        <ErrorCode>NoError</ErrorCode> 
                        <ErrorMessage>No error.</ErrorMessage> 
                        <DomainSettingErrors /> 
                        <DomainSettings> 
                            <DomainSetting i:type="DomainStringSetting"> 
                                <Name>ExternalEwsUrl</Name> 
                                <Value>https://emea.mail.microsoft.com/EWS/Exchange.asmx</Value> 
                            </DomainSetting> 
                        </DomainSettings> 
                        <RedirectTarget i:nil="true" /> 
                    </DomainResponse> 
                </DomainResponses> 
            </Response> 
        </GetDomainSettingsResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="e52f8-124">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="e52f8-124">Response elements</span></span>

<span data-ttu-id="e52f8-125">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e52f8-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e52f8-126">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-126">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md)
    
- [<span data-ttu-id="e52f8-127">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-127">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="e52f8-128">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-128">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="e52f8-129">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-129">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="e52f8-130">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md)
    
- [<span data-ttu-id="e52f8-131">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-131">DomainResponse (SOAP)</span></span>](domainresponse-soap.md)
    
- [<span data-ttu-id="e52f8-132">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-132">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md)
    
- [<span data-ttu-id="e52f8-133">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-133">DomainSettings (SOAP)</span></span>](domainsettings-soap.md)
    
- [<span data-ttu-id="e52f8-134">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-134">DomainSetting (SOAP)</span></span>](domainsetting-soap.md)
    
- [<span data-ttu-id="e52f8-135">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-135">Name (SOAP)</span></span>](name-soap.md)
    
- [<span data-ttu-id="e52f8-136">Valor (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-136">Value (SOAP)</span></span>](value-soap.md)
    
- [<span data-ttu-id="e52f8-137">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-137">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="e52f8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e52f8-138">See also</span></span>



[<span data-ttu-id="e52f8-139">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="e52f8-140">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e52f8-140">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)


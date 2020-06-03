---
title: Operación GetPhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformation
api_type:
- schema
ms.assetid: 418bd6ca-39d9-49a9-841e-7a71ede1fa51
description: La operación GetPhoneCallInformation devuelve información sobre la llamada telefónica especificada.
ms.openlocfilehash: 231b160713526f44433188e2b1e3bd98012370b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458316"
---
# <a name="getphonecallinformation-operation"></a><span data-ttu-id="0c8cc-103">Operación GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="0c8cc-103">GetPhoneCallInformation operation</span></span>

<span data-ttu-id="0c8cc-104">La operación **GetPhoneCallInformation** devuelve información sobre la llamada telefónica especificada.</span><span class="sxs-lookup"><span data-stu-id="0c8cc-104">The **GetPhoneCallInformation** operation returns information about the specified telephone call.</span></span> 
  
## <a name="getphonecallinformation-request-example"></a><span data-ttu-id="0c8cc-105">Ejemplo de solicitud GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="0c8cc-105">GetPhoneCallInformation request example</span></span>

### <a name="description"></a><span data-ttu-id="0c8cc-106">Description</span><span class="sxs-lookup"><span data-stu-id="0c8cc-106">Description</span></span>

<span data-ttu-id="0c8cc-107">El siguiente ejemplo de una solicitud **GetPhoneCallInformation** muestra cómo crear una solicitud para obtener información sobre una llamada telefónica específica.</span><span class="sxs-lookup"><span data-stu-id="0c8cc-107">The following example of a **GetPhoneCallInformation** request shows how to form a request to get information about a specific telephone call.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0c8cc-108">Código</span><span class="sxs-lookup"><span data-stu-id="0c8cc-108">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetPhoneCallInformation>
      <m:PhoneCallId Id="NDDY5uY29y9t"/>
    </m:GetPhoneCallInformation>
  </soap:Body>
</soap:Envelope>
```

## <a name="getphonecallinformation-response-example"></a><span data-ttu-id="0c8cc-109">Ejemplo de respuesta GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="0c8cc-109">GetPhoneCallInformation response example</span></span>

### <a name="description"></a><span data-ttu-id="0c8cc-110">Description</span><span class="sxs-lookup"><span data-stu-id="0c8cc-110">Description</span></span>

<span data-ttu-id="0c8cc-111">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **GetPhoneCallInformation** .</span><span class="sxs-lookup"><span data-stu-id="0c8cc-111">The following example shows a successful response to the **GetPhoneCallInformation** request.</span></span> <span data-ttu-id="0c8cc-112">La respuesta representa una llamada telefónica que está conectada actualmente.</span><span class="sxs-lookup"><span data-stu-id="0c8cc-112">The response represents a telephone call that is currently connected.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0c8cc-113">Código</span><span class="sxs-lookup"><span data-stu-id="0c8cc-113">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetPhoneCallInformationResponse ResponseClass="Success" 
                                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:PhoneCallInformation xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:PhoneCallState xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">Connected</t:PhoneCallState>
        <t:ConnectionFailureCause xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">None</t:ConnectionFailureCause>
      </m:PhoneCallInformation>
    </GetPhoneCallInformationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="0c8cc-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c8cc-114">See also</span></span>

- [<span data-ttu-id="0c8cc-115">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0c8cc-115">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="0c8cc-116">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0c8cc-116">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


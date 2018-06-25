---
title: Operación PlayOnPhone (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: La operación PlayOnPhone realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono que es especificado por el elemento DialString.
ms.openlocfilehash: b55bb45d6654f57503879f33e1cd5013ddb69a2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836818"
---
# <a name="playonphone-operation-um-web-service"></a><span data-ttu-id="40b7e-103">Operación PlayOnPhone (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="40b7e-103">PlayOnPhone operation (UM web service)</span></span>

<span data-ttu-id="40b7e-104">La operación PlayOnPhone realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono que es especificado por el elemento **DialString** .</span><span class="sxs-lookup"><span data-stu-id="40b7e-104">The PlayOnPhone operation makes an outbound call and plays a specified message over the telephone that is specified by the **DialString** element.</span></span> 
  
## <a name="playonphone-request-example"></a><span data-ttu-id="40b7e-105">Ejemplo de solicitud de PlayOnPhone</span><span class="sxs-lookup"><span data-stu-id="40b7e-105">PlayOnPhone request example</span></span>

### <a name="description"></a><span data-ttu-id="40b7e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="40b7e-106">Description</span></span>

<span data-ttu-id="40b7e-107">El siguiente ejemplo de una solicitud PlayOnPhone muestra cómo formar una solicitud para realizar una llamada saliente y reproducir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="40b7e-107">The following example of a PlayOnPhone request shows how to form a request to make an outbound call and play a message.</span></span>
  
### <a name="code"></a><span data-ttu-id="40b7e-108">Código</span><span class="sxs-lookup"><span data-stu-id="40b7e-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphone-response-example"></a><span data-ttu-id="40b7e-109">Ejemplo de respuesta correcta de PlayOnPhone</span><span class="sxs-lookup"><span data-stu-id="40b7e-109">Successful PlayOnPhone response example</span></span>

### <a name="description"></a><span data-ttu-id="40b7e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40b7e-110">Description</span></span>

<span data-ttu-id="40b7e-111">El siguiente ejemplo de una respuesta PlayOnPhone muestra una respuesta a la solicitud de PlayOnPhone.</span><span class="sxs-lookup"><span data-stu-id="40b7e-111">The following example of a PlayOnPhone response shows a response to the PlayOnPhone request.</span></span>
  
### <a name="code"></a><span data-ttu-id="40b7e-112">Código</span><span class="sxs-lookup"><span data-stu-id="40b7e-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="40b7e-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="40b7e-113">See also</span></span>



[<span data-ttu-id="40b7e-114">PlayOnPhone (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="40b7e-114">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md)
  
[<span data-ttu-id="40b7e-115">PlayOnPhoneResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="40b7e-115">PlayOnPhoneResponse (UM web service)</span></span>](playonphoneresponse-um-web-service.md)
  
[<span data-ttu-id="40b7e-116">Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="40b7e-116">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)


---
title: Operación reproducir (servicio Web de mensajería unificada)
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
description: La operación reproducir realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono especificado por el elemento DialString.
ms.openlocfilehash: c5ff82bcd822aa2c659d1782ea4a1349d198bc80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466237"
---
# <a name="playonphone-operation-um-web-service"></a><span data-ttu-id="17546-103">Operación reproducir (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17546-103">PlayOnPhone operation (UM web service)</span></span>

<span data-ttu-id="17546-104">La operación reproducir realiza una llamada saliente y reproduce un mensaje especificado a través del teléfono especificado por el elemento **DialString** .</span><span class="sxs-lookup"><span data-stu-id="17546-104">The PlayOnPhone operation makes an outbound call and plays a specified message over the telephone that is specified by the **DialString** element.</span></span> 
  
## <a name="playonphone-request-example"></a><span data-ttu-id="17546-105">Ejemplo de solicitud reproducir</span><span class="sxs-lookup"><span data-stu-id="17546-105">PlayOnPhone request example</span></span>

### <a name="description"></a><span data-ttu-id="17546-106">Description</span><span class="sxs-lookup"><span data-stu-id="17546-106">Description</span></span>

<span data-ttu-id="17546-107">El siguiente ejemplo de una solicitud reproducir muestra cómo crear una solicitud para realizar una llamada saliente y reproducir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="17546-107">The following example of a PlayOnPhone request shows how to form a request to make an outbound call and play a message.</span></span>
  
### <a name="code"></a><span data-ttu-id="17546-108">Código</span><span class="sxs-lookup"><span data-stu-id="17546-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphone-response-example"></a><span data-ttu-id="17546-109">Ejemplo de respuesta reproducir correcta</span><span class="sxs-lookup"><span data-stu-id="17546-109">Successful PlayOnPhone response example</span></span>

### <a name="description"></a><span data-ttu-id="17546-110">Description</span><span class="sxs-lookup"><span data-stu-id="17546-110">Description</span></span>

<span data-ttu-id="17546-111">El siguiente ejemplo de una respuesta de reproducir muestra una respuesta a la solicitud reproducir.</span><span class="sxs-lookup"><span data-stu-id="17546-111">The following example of a PlayOnPhone response shows a response to the PlayOnPhone request.</span></span>
  
### <a name="code"></a><span data-ttu-id="17546-112">Código</span><span class="sxs-lookup"><span data-stu-id="17546-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="17546-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="17546-113">See also</span></span>



[<span data-ttu-id="17546-114">Reproducir (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17546-114">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md)
  
[<span data-ttu-id="17546-115">PlayOnPhoneResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17546-115">PlayOnPhoneResponse (UM web service)</span></span>](playonphoneresponse-um-web-service.md)
  
[<span data-ttu-id="17546-116">Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17546-116">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)


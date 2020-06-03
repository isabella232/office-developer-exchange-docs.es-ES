---
title: Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: La operación PlayOnPhoneGreeting realiza una llamada saliente y reproduce uno de los dos mensajes de saludo en el teléfono.
ms.openlocfilehash: 3af120b9ac8d7a368742fad2850c924228488662
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528898"
---
# <a name="playonphonegreeting-operation-um-web-service"></a><span data-ttu-id="f5fcd-103">Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="f5fcd-103">PlayOnPhoneGreeting operation (UM web service)</span></span>

<span data-ttu-id="f5fcd-104">La operación PlayOnPhoneGreeting realiza una llamada saliente y reproduce uno de los dos mensajes de saludo en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="f5fcd-104">The PlayOnPhoneGreeting operation makes an outbound call and plays one of the two greeting messages on the telephone.</span></span>
  
## <a name="playonphonegreeting-request-example"></a><span data-ttu-id="f5fcd-105">Ejemplo de solicitud PlayOnPhoneGreeting</span><span class="sxs-lookup"><span data-stu-id="f5fcd-105">PlayOnPhoneGreeting request example</span></span>

### <a name="description"></a><span data-ttu-id="f5fcd-106">Description</span><span class="sxs-lookup"><span data-stu-id="f5fcd-106">Description</span></span>

<span data-ttu-id="f5fcd-107">El siguiente ejemplo de una solicitud de PlayOnPhoneGreeting muestra cómo crear una solicitud para realizar una llamada saliente y reproducir el mensaje de saludo normal en un teléfono.</span><span class="sxs-lookup"><span data-stu-id="f5fcd-107">The following example of a PlayOnPhoneGreeting request shows how to form a request to make an outbound call and play the normal greeting message on a telephone.</span></span>
  
### <a name="code"></a><span data-ttu-id="f5fcd-108">Código</span><span class="sxs-lookup"><span data-stu-id="f5fcd-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphonegreeting-response-example"></a><span data-ttu-id="f5fcd-109">Ejemplo de respuesta PlayOnPhoneGreeting correcta</span><span class="sxs-lookup"><span data-stu-id="f5fcd-109">Successful PlayOnPhoneGreeting response example</span></span>

### <a name="description"></a><span data-ttu-id="f5fcd-110">Description</span><span class="sxs-lookup"><span data-stu-id="f5fcd-110">Description</span></span>

<span data-ttu-id="f5fcd-111">El siguiente ejemplo de una respuesta de PlayOnPhoneGreeting muestra una respuesta a la solicitud PlayOnPhoneGreeting.</span><span class="sxs-lookup"><span data-stu-id="f5fcd-111">The following example of a PlayOnPhoneGreeting response shows a response to the PlayOnPhoneGreeting request.</span></span>
  
### <a name="code"></a><span data-ttu-id="f5fcd-112">Código</span><span class="sxs-lookup"><span data-stu-id="f5fcd-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="f5fcd-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5fcd-113">See also</span></span>



[<span data-ttu-id="f5fcd-114">PlayOnPhoneGreeting (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="f5fcd-114">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)
  
[<span data-ttu-id="f5fcd-115">PlayOnPhoneGreetingResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="f5fcd-115">PlayOnPhoneGreetingResponse (UM web service)</span></span>](playonphonegreetingresponse-um-web-service.md)
  
[<span data-ttu-id="f5fcd-116">GreetingType (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="f5fcd-116">GreetingType (UM web service)</span></span>](greetingtype-um-web-service.md)
  
[<span data-ttu-id="f5fcd-117">dialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="f5fcd-117">dialString (UM web service)</span></span>](dialstring-um-web-service.md)


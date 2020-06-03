---
title: Operación Disconnect (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: La operación de desconexión finaliza la llamada identificada por el CallId (servicio Web de mensajería unificada) especificado.
ms.openlocfilehash: a1268f9ea3d879f472e019bf1847fc13d65d1819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529073"
---
# <a name="disconnect-operation-um-web-service"></a><span data-ttu-id="dfd31-103">Operación Disconnect (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="dfd31-103">Disconnect operation (UM web service)</span></span>

<span data-ttu-id="dfd31-104">La operación de desconexión finaliza la llamada identificada por el [CallId (servicio Web de mensajería unificada)](callid-um-web-service.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="dfd31-104">The Disconnect operation terminates the call that is identified by the specified [CallId (UM web service)](callid-um-web-service.md).</span></span>
  
## <a name="disconnect-request-example"></a><span data-ttu-id="dfd31-105">Ejemplo de solicitud Disconnect</span><span class="sxs-lookup"><span data-stu-id="dfd31-105">Disconnect request example</span></span>

### <a name="description"></a><span data-ttu-id="dfd31-106">Description</span><span class="sxs-lookup"><span data-stu-id="dfd31-106">Description</span></span>

<span data-ttu-id="dfd31-107">El siguiente ejemplo de una solicitud de desconexión muestra cómo crear una solicitud para desconectar una llamada.</span><span class="sxs-lookup"><span data-stu-id="dfd31-107">The following example of a Disconnect request shows how to form a request to disconnect a call.</span></span>
  
### <a name="code"></a><span data-ttu-id="dfd31-108">Código</span><span class="sxs-lookup"><span data-stu-id="dfd31-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a><span data-ttu-id="dfd31-109">Ejemplo de respuesta de desconexión correcta</span><span class="sxs-lookup"><span data-stu-id="dfd31-109">Successful Disconnect response example</span></span>

### <a name="description"></a><span data-ttu-id="dfd31-110">Description</span><span class="sxs-lookup"><span data-stu-id="dfd31-110">Description</span></span>

<span data-ttu-id="dfd31-111">El siguiente ejemplo de una respuesta de desconexión muestra una respuesta a la solicitud de desconexión.</span><span class="sxs-lookup"><span data-stu-id="dfd31-111">The following example of a Disconnect response shows a response to the Disconnect request.</span></span>
  
### <a name="code"></a><span data-ttu-id="dfd31-112">Código</span><span class="sxs-lookup"><span data-stu-id="dfd31-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="dfd31-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfd31-113">See also</span></span>

- [<span data-ttu-id="dfd31-114">Disconnect (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="dfd31-114">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md) 
- [<span data-ttu-id="dfd31-115">DisconnectResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="dfd31-115">DisconnectResponse (UM web service)</span></span>](disconnectresponse-um-web-service.md) 
- [<span data-ttu-id="dfd31-116">CallId (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="dfd31-116">CallId (UM web service)</span></span>](callid-um-web-service.md)


---
title: Operación SetOofStatus (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de oficina (OOF) del usuario que realiza la solicitud.
ms.openlocfilehash: 2bb1deeec8ddb5be56979bfb2fae3396672298a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837445"
---
# <a name="setoofstatus-operation-um-web-service"></a><span data-ttu-id="5f670-103">Operación SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5f670-103">SetOofStatus operation (UM web service)</span></span>

<span data-ttu-id="5f670-104">La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de oficina (OOF) del usuario que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f670-104">The SetOofStatus operation sets a value that indicates whether the Out of Office (OOF) greeting should be played for the user who makes the request.</span></span>
  
## <a name="setoofstatus-request-example"></a><span data-ttu-id="5f670-105">Ejemplo de solicitud de SetOofStatus</span><span class="sxs-lookup"><span data-stu-id="5f670-105">SetOofStatus request example</span></span>

### <a name="description"></a><span data-ttu-id="5f670-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f670-106">Description</span></span>

<span data-ttu-id="5f670-107">El siguiente ejemplo de una solicitud de SetOofStatus muestra cómo formar una solicitud para habilitar el saludo de fuera de la oficina para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5f670-107">The following example of a SetOofStatus request shows how to form a request to enable the Out of Office greeting for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f670-108">Código</span><span class="sxs-lookup"><span data-stu-id="5f670-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a><span data-ttu-id="5f670-109">Ejemplo de respuesta correcta de SetOofStatus</span><span class="sxs-lookup"><span data-stu-id="5f670-109">Successful SetOofStatus response example</span></span>

### <a name="description"></a><span data-ttu-id="5f670-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f670-110">Description</span></span>

<span data-ttu-id="5f670-111">El siguiente ejemplo de una respuesta SetOofStatus muestra una respuesta a la solicitud de SetOofStatus.</span><span class="sxs-lookup"><span data-stu-id="5f670-111">The following example of a SetOofStatus response shows a response to the SetOofStatus request.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f670-112">Código</span><span class="sxs-lookup"><span data-stu-id="5f670-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="5f670-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="5f670-113">See also</span></span>



[<span data-ttu-id="5f670-114">SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5f670-114">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="5f670-115">SetOofStatusResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5f670-115">SetOofStatusResponse (UM web service)</span></span>](setoofstatusresponse-um-web-service.md)
  
[<span data-ttu-id="5f670-116">Estado (servicio web de mensajería unificada - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="5f670-116">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)


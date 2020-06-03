---
title: Operación SetOofStatus (servicio Web de mensajería unificada)
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
description: La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de la oficina (OOF) para el usuario que realiza la solicitud.
ms.openlocfilehash: 2311b6137ac25d15ad3d06668450c1d0f7ec1fad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467357"
---
# <a name="setoofstatus-operation-um-web-service"></a><span data-ttu-id="73531-103">Operación SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="73531-103">SetOofStatus operation (UM web service)</span></span>

<span data-ttu-id="73531-104">La operación SetOofStatus establece un valor que indica si se debe reproducir el saludo de fuera de la oficina (OOF) para el usuario que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73531-104">The SetOofStatus operation sets a value that indicates whether the Out of Office (OOF) greeting should be played for the user who makes the request.</span></span>
  
## <a name="setoofstatus-request-example"></a><span data-ttu-id="73531-105">Ejemplo de solicitud SetOofStatus</span><span class="sxs-lookup"><span data-stu-id="73531-105">SetOofStatus request example</span></span>

### <a name="description"></a><span data-ttu-id="73531-106">Description</span><span class="sxs-lookup"><span data-stu-id="73531-106">Description</span></span>

<span data-ttu-id="73531-107">El siguiente ejemplo de una solicitud SetOofStatus muestra cómo crear una solicitud para habilitar el saludo de fuera de la oficina para un buzón.</span><span class="sxs-lookup"><span data-stu-id="73531-107">The following example of a SetOofStatus request shows how to form a request to enable the Out of Office greeting for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="73531-108">Código</span><span class="sxs-lookup"><span data-stu-id="73531-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a><span data-ttu-id="73531-109">Ejemplo de respuesta SetOofStatus correcta</span><span class="sxs-lookup"><span data-stu-id="73531-109">Successful SetOofStatus response example</span></span>

### <a name="description"></a><span data-ttu-id="73531-110">Description</span><span class="sxs-lookup"><span data-stu-id="73531-110">Description</span></span>

<span data-ttu-id="73531-111">El siguiente ejemplo de una respuesta de SetOofStatus muestra una respuesta a la solicitud SetOofStatus.</span><span class="sxs-lookup"><span data-stu-id="73531-111">The following example of a SetOofStatus response shows a response to the SetOofStatus request.</span></span>
  
### <a name="code"></a><span data-ttu-id="73531-112">Código</span><span class="sxs-lookup"><span data-stu-id="73531-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="73531-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="73531-113">See also</span></span>



[<span data-ttu-id="73531-114">SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="73531-114">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="73531-115">SetOofStatusResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="73531-115">SetOofStatusResponse (UM web service)</span></span>](setoofstatusresponse-um-web-service.md)
  
[<span data-ttu-id="73531-116">Estado (servicio Web de mensajería unificada-SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="73531-116">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)


---
title: Operación SetMissedCallNotificationEnabled (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.
ms.openlocfilehash: be9479d6ed2c5238ed19c3d22e028fca62b8deed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837434"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a><span data-ttu-id="b59eb-103">Operación SetMissedCallNotificationEnabled (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b59eb-103">SetMissedCallNotificationEnabled operation (UM web service)</span></span>

<span data-ttu-id="b59eb-104">La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="b59eb-104">The SetMissedCallNotificationEnabled operation enables or disables missed call notifications.</span></span>
  
## <a name="setmissedcallnotificationenabled-request-example"></a><span data-ttu-id="b59eb-105">Ejemplo de solicitud de SetMissedCallNotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="b59eb-105">SetMissedCallNotificationEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="b59eb-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b59eb-106">Description</span></span>

<span data-ttu-id="b59eb-107">El siguiente ejemplo de una solicitud de SetMissedCallNotificationEnabled muestra cómo formar una solicitud para habilitar las notificaciones de llamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="b59eb-107">The following example of a SetMissedCallNotificationEnabled request shows how to form a request to enable missed call notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="b59eb-108">Código</span><span class="sxs-lookup"><span data-stu-id="b59eb-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a><span data-ttu-id="b59eb-109">Ejemplo de respuesta correcta de SetMissedCallNotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="b59eb-109">Successful SetMissedCallNotificationEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="b59eb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b59eb-110">Description</span></span>

<span data-ttu-id="b59eb-111">El siguiente ejemplo de una respuesta PlayOnPhoneGreeting muestra una respuesta a la solicitud de SetMissedCallNotificationEnabled.</span><span class="sxs-lookup"><span data-stu-id="b59eb-111">The following example of a PlayOnPhoneGreeting response shows a response to the SetMissedCallNotificationEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b59eb-112">Código</span><span class="sxs-lookup"><span data-stu-id="b59eb-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="b59eb-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="b59eb-113">See also</span></span>



[<span data-ttu-id="b59eb-114">SetMissedCallNotificationEnabled (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b59eb-114">SetMissedCallNotificationEnabled (UM web service)</span></span>](setmissedcallnotificationenabled-um-web-service.md)
  
[<span data-ttu-id="b59eb-115">SetMissedCallNotificationEnabledResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b59eb-115">SetMissedCallNotificationEnabledResponse (UM web service)</span></span>](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[<span data-ttu-id="b59eb-116">Estado (servicio web de mensajería unificada - SetMissedCallNotificationEnabled)</span><span class="sxs-lookup"><span data-stu-id="b59eb-116">Status (UM web service - SetMissedCallNotificationEnabled)</span></span>](status-um-web-servicesetmissedcallnotificationenabled.md)


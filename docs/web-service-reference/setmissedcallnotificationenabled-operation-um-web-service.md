---
title: Operación SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)
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
ms.openlocfilehash: ca4942942a81bc187e8e18a5e6f003f8587f79d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467399"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a><span data-ttu-id="0a821-103">Operación SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="0a821-103">SetMissedCallNotificationEnabled operation (UM web service)</span></span>

<span data-ttu-id="0a821-104">La operación SetMissedCallNotificationEnabled habilita o deshabilita las notificaciones de llamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="0a821-104">The SetMissedCallNotificationEnabled operation enables or disables missed call notifications.</span></span>
  
## <a name="setmissedcallnotificationenabled-request-example"></a><span data-ttu-id="0a821-105">Ejemplo de solicitud SetMissedCallNotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="0a821-105">SetMissedCallNotificationEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="0a821-106">Description</span><span class="sxs-lookup"><span data-stu-id="0a821-106">Description</span></span>

<span data-ttu-id="0a821-107">El siguiente ejemplo de una solicitud SetMissedCallNotificationEnabled muestra cómo crear una solicitud para habilitar las notificaciones de llamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="0a821-107">The following example of a SetMissedCallNotificationEnabled request shows how to form a request to enable missed call notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="0a821-108">Código</span><span class="sxs-lookup"><span data-stu-id="0a821-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a><span data-ttu-id="0a821-109">Ejemplo de respuesta SetMissedCallNotificationEnabled correcta</span><span class="sxs-lookup"><span data-stu-id="0a821-109">Successful SetMissedCallNotificationEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="0a821-110">Description</span><span class="sxs-lookup"><span data-stu-id="0a821-110">Description</span></span>

<span data-ttu-id="0a821-111">El siguiente ejemplo de una respuesta de PlayOnPhoneGreeting muestra una respuesta a la solicitud SetMissedCallNotificationEnabled.</span><span class="sxs-lookup"><span data-stu-id="0a821-111">The following example of a PlayOnPhoneGreeting response shows a response to the SetMissedCallNotificationEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="0a821-112">Código</span><span class="sxs-lookup"><span data-stu-id="0a821-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="0a821-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a821-113">See also</span></span>



[<span data-ttu-id="0a821-114">SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="0a821-114">SetMissedCallNotificationEnabled (UM web service)</span></span>](setmissedcallnotificationenabled-um-web-service.md)
  
[<span data-ttu-id="0a821-115">SetMissedCallNotificationEnabledResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="0a821-115">SetMissedCallNotificationEnabledResponse (UM web service)</span></span>](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[<span data-ttu-id="0a821-116">Estado (servicio Web de mensajería unificada-SetMissedCallNotificationEnabled)</span><span class="sxs-lookup"><span data-stu-id="0a821-116">Status (UM web service - SetMissedCallNotificationEnabled)</span></span>](status-um-web-servicesetmissedcallnotificationenabled.md)


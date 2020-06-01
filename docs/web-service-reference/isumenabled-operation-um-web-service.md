---
title: Operación IsUMEnabled (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: La operación IsUMEnabled determina si un buzón de correo está habilitado para mensajería unificada.
ms.openlocfilehash: b1478f5a113059251fe1b036ac7d77e5a4ab4f50
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458239"
---
# <a name="isumenabled-operation-um-web-service"></a><span data-ttu-id="b766e-103">Operación IsUMEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b766e-103">IsUMEnabled operation (UM web service)</span></span>

<span data-ttu-id="b766e-104">La operación IsUMEnabled determina si un buzón de correo está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="b766e-104">The IsUMEnabled operation determines whether a mailbox is enabled for Unified Messaging.</span></span>
  
## <a name="isumenabled-request-example"></a><span data-ttu-id="b766e-105">Ejemplo de solicitud IsUMEnabled</span><span class="sxs-lookup"><span data-stu-id="b766e-105">IsUMEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="b766e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b766e-106">Description</span></span>

<span data-ttu-id="b766e-107">El siguiente ejemplo de una solicitud IsUMEnabled muestra cómo crear una solicitud para determinar si un buzón está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="b766e-107">The following example of an IsUMEnabled request shows how to form a request to determine whether a mailbox is enabled for Unified Messaging.</span></span>
  
### <a name="code"></a><span data-ttu-id="b766e-108">Código</span><span class="sxs-lookup"><span data-stu-id="b766e-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a><span data-ttu-id="b766e-109">Ejemplo de respuesta IsUMEnabled correcta</span><span class="sxs-lookup"><span data-stu-id="b766e-109">Successful IsUMEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="b766e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b766e-110">Description</span></span>

<span data-ttu-id="b766e-111">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud IsUMEnabled.</span><span class="sxs-lookup"><span data-stu-id="b766e-111">The following example shows a successful response to an IsUMEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b766e-112">Código</span><span class="sxs-lookup"><span data-stu-id="b766e-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="b766e-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="b766e-113">See also</span></span>



[<span data-ttu-id="b766e-114">IsUMEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b766e-114">IsUMEnabled (UM web service)</span></span>](isumenabled-um-web-service.md)
  
[<span data-ttu-id="b766e-115">IsUMEnabledResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b766e-115">IsUMEnabledResponse (UM web service)</span></span>](isumenabledresponse-um-web-service.md)


[<span data-ttu-id="b766e-116">Elementos XML de servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="b766e-116">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)


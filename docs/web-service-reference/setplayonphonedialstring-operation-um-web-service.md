---
title: Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: La operación SetPlayOnPhoneDialString establece la cadena de marcado para usar como el valor predeterminado para la operación de PlayOnPhone (servicio web de mensajería unificada) y la operación de PlayOnPhoneGreeting (servicio web de mensajería unificada).
ms.openlocfilehash: 0d1a879784740777e5eab0cbd5f85e59a6479461
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837446"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a><span data-ttu-id="a5cf3-103">Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a5cf3-103">SetPlayOnPhoneDialString operation (UM web service)</span></span>

<span data-ttu-id="a5cf3-104">La operación SetPlayOnPhoneDialString establece la cadena de marcado para usar como el valor predeterminado para la [operación de PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) y la [operación de PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="a5cf3-104">The SetPlayOnPhoneDialString operation sets the dial string to use as the default for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and the [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>
  
## <a name="setplayonphonedialstring-request-example"></a><span data-ttu-id="a5cf3-105">Ejemplo de solicitud de SetPlayOnPhoneDialString</span><span class="sxs-lookup"><span data-stu-id="a5cf3-105">SetPlayOnPhoneDialString request example</span></span>

### <a name="description"></a><span data-ttu-id="a5cf3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5cf3-106">Description</span></span>

<span data-ttu-id="a5cf3-107">El siguiente ejemplo de una solicitud de SetPlayOnPhoneDialString muestra cómo formar una solicitud para establecer la cadena de marcado predeterminado para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a5cf3-107">The following example of a SetPlayOnPhoneDialString request shows how to form a request to set the default dial string for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="a5cf3-108">Código</span><span class="sxs-lookup"><span data-stu-id="a5cf3-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a><span data-ttu-id="a5cf3-109">Ejemplo de respuesta correcta de SetPlayOnPhoneDialString</span><span class="sxs-lookup"><span data-stu-id="a5cf3-109">Successful SetPlayOnPhoneDialString response example</span></span>

### <a name="description"></a><span data-ttu-id="a5cf3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5cf3-110">Description</span></span>

<span data-ttu-id="a5cf3-111">El siguiente ejemplo de una respuesta SetPlayOnePhoneDialString muestra una respuesta a la solicitud de SetPlayOnPhoneDialString.</span><span class="sxs-lookup"><span data-stu-id="a5cf3-111">The following example of a SetPlayOnePhoneDialString response shows a response to the SetPlayOnPhoneDialString request.</span></span>
  
### <a name="code"></a><span data-ttu-id="a5cf3-112">Código</span><span class="sxs-lookup"><span data-stu-id="a5cf3-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="a5cf3-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="a5cf3-113">See also</span></span>



[<span data-ttu-id="a5cf3-114">SetPlayOnPhoneDialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a5cf3-114">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
[<span data-ttu-id="a5cf3-115">SetPlayOnPhoneDialStringResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a5cf3-115">SetPlayOnPhoneDialStringResponse (UM web service)</span></span>](setplayonphonedialstringresponse-um-web-service.md)
  
[<span data-ttu-id="a5cf3-116">dialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a5cf3-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md)


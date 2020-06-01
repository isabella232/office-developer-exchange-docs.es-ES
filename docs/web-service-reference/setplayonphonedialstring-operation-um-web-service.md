---
title: Operación SetPlayOnPhoneDialString (servicio Web de mensajería unificada)
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
description: La operación SetPlayOnPhoneDialString establece la cadena de marcado que se usará como predeterminada para la operación reproducir (servicio Web de mensajería unificada) y la operación PlayOnPhoneGreeting (servicio Web de mensajería unificada).
ms.openlocfilehash: 7df806eedc2d6d037394f31ec4ccbfe28aaf3372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458645"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a><span data-ttu-id="330e3-103">Operación SetPlayOnPhoneDialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="330e3-103">SetPlayOnPhoneDialString operation (UM web service)</span></span>

<span data-ttu-id="330e3-104">La operación SetPlayOnPhoneDialString establece la cadena de marcado que se usará como predeterminada para la [operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) y la [operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="330e3-104">The SetPlayOnPhoneDialString operation sets the dial string to use as the default for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and the [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>
  
## <a name="setplayonphonedialstring-request-example"></a><span data-ttu-id="330e3-105">Ejemplo de solicitud SetPlayOnPhoneDialString</span><span class="sxs-lookup"><span data-stu-id="330e3-105">SetPlayOnPhoneDialString request example</span></span>

### <a name="description"></a><span data-ttu-id="330e3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="330e3-106">Description</span></span>

<span data-ttu-id="330e3-107">El siguiente ejemplo de una solicitud SetPlayOnPhoneDialString muestra cómo crear una solicitud para establecer la cadena de marcado predeterminada para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="330e3-107">The following example of a SetPlayOnPhoneDialString request shows how to form a request to set the default dial string for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="330e3-108">Código</span><span class="sxs-lookup"><span data-stu-id="330e3-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a><span data-ttu-id="330e3-109">Ejemplo de respuesta SetPlayOnPhoneDialString correcta</span><span class="sxs-lookup"><span data-stu-id="330e3-109">Successful SetPlayOnPhoneDialString response example</span></span>

### <a name="description"></a><span data-ttu-id="330e3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="330e3-110">Description</span></span>

<span data-ttu-id="330e3-111">El siguiente ejemplo de una respuesta de SetPlayOnePhoneDialString muestra una respuesta a la solicitud SetPlayOnPhoneDialString.</span><span class="sxs-lookup"><span data-stu-id="330e3-111">The following example of a SetPlayOnePhoneDialString response shows a response to the SetPlayOnPhoneDialString request.</span></span>
  
### <a name="code"></a><span data-ttu-id="330e3-112">Código</span><span class="sxs-lookup"><span data-stu-id="330e3-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="330e3-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="330e3-113">See also</span></span>



[<span data-ttu-id="330e3-114">SetPlayOnPhoneDialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="330e3-114">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
[<span data-ttu-id="330e3-115">SetPlayOnPhoneDialStringResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="330e3-115">SetPlayOnPhoneDialStringResponse (UM web service)</span></span>](setplayonphonedialstringresponse-um-web-service.md)
  
[<span data-ttu-id="330e3-116">dialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="330e3-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md)


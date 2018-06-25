---
title: Cancelar la operación de suscripción
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 994a9d2b-1501-4804-90f0-12bd914496ec
description: La operación de cancelación de la suscripción se utiliza para finalizar una suscripción de extracción de notificación. Use esta operación, en lugar de permitir que un tiempo de espera de suscripción. Esta operación sólo es válida para las notificaciones de extracción.
ms.openlocfilehash: 64514a718d473f0fd7d0320bd1ccecddb1940ac8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840797"
---
# <a name="unsubscribe-operation"></a><span data-ttu-id="84c4c-105">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-105">Unsubscribe operation</span></span>

<span data-ttu-id="84c4c-106">La operación de cancelación de la suscripción se utiliza para finalizar una suscripción de extracción de notificación.</span><span class="sxs-lookup"><span data-stu-id="84c4c-106">The Unsubscribe operation is used to end a pull notification subscription.</span></span> <span data-ttu-id="84c4c-107">Use esta operación, en lugar de permitir que un tiempo de espera de suscripción.</span><span class="sxs-lookup"><span data-stu-id="84c4c-107">Use this operation rather than letting a subscription timeout.</span></span> <span data-ttu-id="84c4c-108">Esta operación sólo es válida para las notificaciones de extracción.</span><span class="sxs-lookup"><span data-stu-id="84c4c-108">This operation is only valid for pull notifications.</span></span>
  
## <a name="unsubscribe-request-example"></a><span data-ttu-id="84c4c-109">Ejemplo de solicitud de cancelación de suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-109">Unsubscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="84c4c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-110">Description</span></span>

<span data-ttu-id="84c4c-111">En el ejemplo siguiente se muestra el mensaje SOAP XML que se envía al cancelar su suscripción de un cliente desde el servicio de notificación.</span><span class="sxs-lookup"><span data-stu-id="84c4c-111">The following example shows the SOAP XML message that is sent to unsubscribe a client from the Notification service.</span></span>
  
### <a name="code"></a><span data-ttu-id="84c4c-112">Código</span><span class="sxs-lookup"><span data-stu-id="84c4c-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Unsubscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>e6fbf5c1-7e26-4bc6-a5f2-882063d5e34e</SubscriptionId>  
    </Unsubscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-request-elements"></a><span data-ttu-id="84c4c-113">Elementos de solicitud de cancelación de suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-113">Unsubscribe request elements</span></span>

<span data-ttu-id="84c4c-114">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="84c4c-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="84c4c-115">Anular la suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-115">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="84c4c-116">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="84c4c-116">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
## <a name="successful-unsubscribe-response-example"></a><span data-ttu-id="84c4c-117">Ejemplo de respuesta de cancelación de suscripción correcta</span><span class="sxs-lookup"><span data-stu-id="84c4c-117">Successful Unsubscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="84c4c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-118">Description</span></span>

<span data-ttu-id="84c4c-119">En el ejemplo siguiente se muestra una respuesta a una solicitud de cancelación de suscripción correcta.</span><span class="sxs-lookup"><span data-stu-id="84c4c-119">The following example shows a successful response to an Unsubscribe request.</span></span>
  
### <a name="code"></a><span data-ttu-id="84c4c-120">Código</span><span class="sxs-lookup"><span data-stu-id="84c4c-120">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-response-elements"></a><span data-ttu-id="84c4c-121">Elementos de respuesta de cancelación de suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-121">Unsubscribe response elements</span></span>

<span data-ttu-id="84c4c-122">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="84c4c-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="84c4c-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="84c4c-123">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="84c4c-124">Anular la suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-124">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="84c4c-125">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="84c4c-125">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="84c4c-126">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="84c4c-126">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="84c4c-127">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="84c4c-127">ResponseCode</span></span>](responsecode.md)
    
## <a name="unsubscribe-error-response-example"></a><span data-ttu-id="84c4c-128">Ejemplo de respuesta de Error de cancelación de suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-128">Unsubscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="84c4c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-129">Description</span></span>

<span data-ttu-id="84c4c-130">El ejemplo siguiente de una respuesta de error de cancelación de suscripción se produce en respuesta a un intento de cancelar la suscripción mediante el uso de un identificador de suscripción que no se encuentra en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="84c4c-130">The following example of an Unsubscribe error response occurs in response to an attempt to unsubscribe by using a subscription identifier that cannot be located in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="84c4c-131">Código</span><span class="sxs-lookup"><span data-stu-id="84c4c-131">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>The specified subscription was not found.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-error-response-elements"></a><span data-ttu-id="84c4c-132">Elementos de respuesta de Error de cancelación de suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-132">Unsubscribe Error response elements</span></span>

<span data-ttu-id="84c4c-133">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="84c4c-133">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="84c4c-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="84c4c-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="84c4c-135">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="84c4c-135">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
    
- [<span data-ttu-id="84c4c-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="84c4c-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="84c4c-137">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="84c4c-137">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="84c4c-138">MessageText</span><span class="sxs-lookup"><span data-stu-id="84c4c-138">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="84c4c-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="84c4c-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="84c4c-140">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="84c4c-140">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="84c4c-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="84c4c-141">See also</span></span>

- [<span data-ttu-id="84c4c-142">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="84c4c-142">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="84c4c-143">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="84c4c-143">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="84c4c-144">Uso de las suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="84c4c-144">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)


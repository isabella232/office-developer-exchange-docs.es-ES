---
title: Operación subscribe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: f17c3d08-c79e-41f1-ba31-6e41e7aafd87
description: La operación subscribe se usa para suscribir las aplicaciones cliente a las notificaciones de inserción o extracción. Es importante tener en cuenta que la estructura de los mensajes y respuestas de la solicitud es diferente en función del tipo de notificación de eventos.
ms.openlocfilehash: c40e0e434f698c6535ff5d03fd4d45a453959dd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467049"
---
# <a name="subscribe-operation"></a><span data-ttu-id="bbbc3-104">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="bbbc3-104">Subscribe operation</span></span>

<span data-ttu-id="bbbc3-105">La operación subscribe se usa para suscribir las aplicaciones cliente a las notificaciones de inserción o extracción.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-105">The Subscribe operation is used to subscribe client applications to either push or pull notifications.</span></span> <span data-ttu-id="bbbc3-106">Es importante tener en cuenta que la estructura de los mensajes y respuestas de la solicitud es diferente en función del tipo de notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-106">It is important to be aware that the structure of the request messages and responses is different depending on the type of event notification.</span></span> 
  
## <a name="pull-subscription-subscribe-request-example"></a><span data-ttu-id="bbbc3-107">Ejemplo de solicitud subscribe de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-107">Pull Subscription Subscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="bbbc3-108">Description</span><span class="sxs-lookup"><span data-stu-id="bbbc3-108">Description</span></span>

<span data-ttu-id="bbbc3-109">En el ejemplo de código siguiente se muestra cómo suscribirse a una suscripción de notificación de evento de extracción.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-109">The following code example shows how to subscribe to a pull event notification subscription.</span></span> <span data-ttu-id="bbbc3-110">La suscripción informa a la aplicación cliente si se agrega correo nuevo a la bandeja de entrada y si un elemento se elimina de la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-110">The subscription informs the client application if new mail is added to the Inbox and if an item is deleted from the Inbox.</span></span> <span data-ttu-id="bbbc3-111">Se agotará el tiempo de espera de la suscripción si el cliente no solicita información sobre los eventos en 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-111">The subscription will time out if the client does not request information about events within ten minutes.</span></span> <span data-ttu-id="bbbc3-112">Si la suscripción expira, se debe establecer una nueva suscripción para seguir solicitando notificaciones.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-112">If the subscription expires, a new subscription must be established to continue to request notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="bbbc3-113">Código</span><span class="sxs-lookup"><span data-stu-id="bbbc3-113">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PullSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox"/>
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
          <t:EventType>DeletedEvent</t:EventType>
        </t:EventTypes>
        <t:Timeout>10</t:Timeout>
      </PullSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-request-elements"></a><span data-ttu-id="bbbc3-114">Elementos de solicitud subscribe de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-114">Pull Subscription Subscribe Request Elements</span></span>

<span data-ttu-id="bbbc3-115">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="bbbc3-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="bbbc3-116">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="bbbc3-116">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="bbbc3-117">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="bbbc3-117">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
    
- [<span data-ttu-id="bbbc3-118">FolderIds</span><span class="sxs-lookup"><span data-stu-id="bbbc3-118">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="bbbc3-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="bbbc3-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="bbbc3-120">EventTypes</span><span class="sxs-lookup"><span data-stu-id="bbbc3-120">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="bbbc3-121">EventType</span><span class="sxs-lookup"><span data-stu-id="bbbc3-121">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="bbbc3-122">Timeout</span><span class="sxs-lookup"><span data-stu-id="bbbc3-122">Timeout</span></span>](timeout.md)
    
<span data-ttu-id="bbbc3-123">Para buscar otras opciones para el mensaje de solicitud de la operación de suscripción, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-123">To find other options for the request message of the Subscribe operation, explore the schema hierarchy.</span></span> <span data-ttu-id="bbbc3-124">Empiece en el elemento [PullSubscriptionRequest](pullsubscriptionrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="bbbc3-124">Start at the [PullSubscriptionRequest](pullsubscriptionrequest.md) element.</span></span> 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a><span data-ttu-id="bbbc3-125">Ejemplo de respuesta de suscripción de suscripción de extracción correcta</span><span class="sxs-lookup"><span data-stu-id="bbbc3-125">Successful Pull Subscription Subscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="bbbc3-126">Description</span><span class="sxs-lookup"><span data-stu-id="bbbc3-126">Description</span></span>

<span data-ttu-id="bbbc3-127">En el ejemplo siguiente se muestra una respuesta de suscripción de extracción correcta.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-127">The following example shows a successful pull subscription response.</span></span> <span data-ttu-id="bbbc3-128">La respuesta contiene el identificador y la marca de agua de la suscripción que se usa para obtener la matriz de eventos asociados a una suscripción.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-128">The response contains the subscription identifier and watermark that is used to get the array of events that are associated with a subscription.</span></span> <span data-ttu-id="bbbc3-129">El identificador de suscripción también se usa para cancelar la suscripción de un cliente desde una suscripción.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-129">The subscription identifier is also used to unsubscribe a client from a subscription.</span></span>
  
### <a name="code"></a><span data-ttu-id="bbbc3-130">Código</span><span class="sxs-lookup"><span data-stu-id="bbbc3-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>39ea5d0f-f062-455e-a1e9-89c0304390f4</m:SubscriptionId>
          <m:Watermark>AAAAAHgGAAAAAAAAAQ==</m:Watermark>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-response-elements"></a><span data-ttu-id="bbbc3-131">Elementos de respuesta subscribe de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-131">Pull Subscription Subscribe response elements</span></span>

<span data-ttu-id="bbbc3-132">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bbbc3-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="bbbc3-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bbbc3-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bbbc3-134">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="bbbc3-134">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="bbbc3-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bbbc3-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bbbc3-136">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bbbc3-136">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="bbbc3-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bbbc3-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bbbc3-138">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="bbbc3-138">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="bbbc3-139">Watermark</span><span class="sxs-lookup"><span data-stu-id="bbbc3-139">Watermark</span></span>](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a><span data-ttu-id="bbbc3-140">Ejemplo de respuesta de error suscribirse a suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-140">Pull Subscription Subscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="bbbc3-141">Description</span><span class="sxs-lookup"><span data-stu-id="bbbc3-141">Description</span></span>

<span data-ttu-id="bbbc3-142">En el ejemplo siguiente se muestra una respuesta de error a una solicitud subscribe.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-142">The following example shows an error response to a Subscribe request.</span></span> <span data-ttu-id="bbbc3-143">El error se produce al intentar suscribirse a las notificaciones mediante el acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-143">The error is caused by an attempt to subscribe to notifications by using delegate access.</span></span>
  
### <a name="code"></a><span data-ttu-id="bbbc3-144">Código</span><span class="sxs-lookup"><span data-stu-id="bbbc3-144">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>Subscriptions are not supported for delegate user access.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionDelegateAccessNotSupported</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-error-response-elements"></a><span data-ttu-id="bbbc3-145">Elementos de respuesta de error de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-145">Pull Subscription Error response elements</span></span>

<span data-ttu-id="bbbc3-146">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="bbbc3-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="bbbc3-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bbbc3-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bbbc3-148">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="bbbc3-148">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="bbbc3-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bbbc3-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bbbc3-150">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bbbc3-150">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="bbbc3-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="bbbc3-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="bbbc3-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bbbc3-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bbbc3-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bbbc3-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a><span data-ttu-id="bbbc3-154">Ejemplo de solicitud de suscripción de inserción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-154">Push Subscription request example</span></span>

### <a name="description"></a><span data-ttu-id="bbbc3-155">Description</span><span class="sxs-lookup"><span data-stu-id="bbbc3-155">Description</span></span>

<span data-ttu-id="bbbc3-156">En el ejemplo de código siguiente se muestra cómo suscribirse a una suscripción de notificación de evento de inserción.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-156">The following code example shows how to subscribe to a push event notification subscription.</span></span> <span data-ttu-id="bbbc3-157">La solicitud identifica las carpetas que se van a supervisar, los tipos de eventos que se van a supervisar, la frecuencia de las notificaciones de estado y la dirección URL del servicio Web de cliente que escucha las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-157">The request identifies the folders to monitor, the types of events to monitor, the frequency of status notifications, and the URL of the client Web service that listens for the push notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="bbbc3-158">Código</span><span class="sxs-lookup"><span data-stu-id="bbbc3-158">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="https://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="https://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="bbbc3-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bbbc3-159">Comments</span></span>

<span data-ttu-id="bbbc3-160">El servicio Web de cliente debe estar configurado antes de que se envíe la solicitud subscribe de notificaciones de inserción; de lo contrario, la primera notificación no se enviará a un extremo válido y se producirá un error en la notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-160">The client Web service must be set up before the push notification subscribe request is sent; otherwise, the first notification will not be sent to a valid endpoint and the push notification will fail.</span></span> <span data-ttu-id="bbbc3-161">Para obtener más información, vea [aplicación de ejemplo de notificación de inserción](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bbbc3-161">For more information, see [Push Notification Sample Application](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="bbbc3-162">Se crea un nuevo [SubscriptionId (GetEvents)](subscriptionid-getevents.md) cuando se resuscribe.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-162">A new [SubscriptionId (GetEvents)](subscriptionid-getevents.md) is created when you resubscribe.</span></span> <span data-ttu-id="bbbc3-163">Use la marca de agua de una suscripción anterior para resuscribirse en el punto en el que finalizó la suscripción anterior.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-163">Use the watermark of a previous subscription to resubscribe at the point where the previous subscription ended.</span></span> 
  
### <a name="push-subscription-request-elements"></a><span data-ttu-id="bbbc3-164">Elementos de solicitud de suscripción de inserción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-164">Push Subscription Request Elements</span></span>

<span data-ttu-id="bbbc3-165">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="bbbc3-165">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="bbbc3-166">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="bbbc3-166">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="bbbc3-167">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="bbbc3-167">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
    
- [<span data-ttu-id="bbbc3-168">FolderIds</span><span class="sxs-lookup"><span data-stu-id="bbbc3-168">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="bbbc3-169">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="bbbc3-169">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="bbbc3-170">EventTypes</span><span class="sxs-lookup"><span data-stu-id="bbbc3-170">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="bbbc3-171">EventType</span><span class="sxs-lookup"><span data-stu-id="bbbc3-171">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="bbbc3-172">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="bbbc3-172">StatusFrequency</span></span>](statusfrequency.md)
    
- [<span data-ttu-id="bbbc3-173">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="bbbc3-173">Url </span></span>](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a><span data-ttu-id="bbbc3-174">Ejemplo de respuesta de suscripción de inserción correcta</span><span class="sxs-lookup"><span data-stu-id="bbbc3-174">Successful Push Subscription response example</span></span>

### <a name="description"></a><span data-ttu-id="bbbc3-175">Description</span><span class="sxs-lookup"><span data-stu-id="bbbc3-175">Description</span></span>

<span data-ttu-id="bbbc3-176">En el ejemplo siguiente se muestra una respuesta de suscripción de inserción correcta.</span><span class="sxs-lookup"><span data-stu-id="bbbc3-176">The following example shows a successful push subscription response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bbbc3-177">Código</span><span class="sxs-lookup"><span data-stu-id="bbbc3-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <SubscribeResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <SubscriptionId>83826921-afdf-48be-b469-628cc02b5f49</SubscriptionId>
          <Watermark>AQAAAOpvG0LURVdOhQkPOWZLPcI8EgAAAAAAAAE=</Watermark>
        </SubscribeResponseMessage>
      </ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="push-subscription-response-elements"></a><span data-ttu-id="bbbc3-178">Elementos de respuesta de suscripción de inserción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-178">Push Subscription response elements</span></span>

<span data-ttu-id="bbbc3-179">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bbbc3-179">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="bbbc3-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bbbc3-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bbbc3-181">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="bbbc3-181">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="bbbc3-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bbbc3-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bbbc3-183">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bbbc3-183">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="bbbc3-184">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bbbc3-184">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bbbc3-185">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="bbbc3-185">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="bbbc3-186">Watermark</span><span class="sxs-lookup"><span data-stu-id="bbbc3-186">Watermark</span></span>](watermark.md)
    
## <a name="see-also"></a><span data-ttu-id="bbbc3-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbbc3-187">See also</span></span>



[<span data-ttu-id="bbbc3-188">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="bbbc3-188">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="bbbc3-189">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="bbbc3-189">GetEvents operation</span></span>](getevents-operation.md)


[<span data-ttu-id="bbbc3-190">Uso de suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-190">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="bbbc3-191">Aplicación de ejemplo de notificación de inserción</span><span class="sxs-lookup"><span data-stu-id="bbbc3-191">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)


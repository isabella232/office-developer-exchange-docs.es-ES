---
title: Operación de suscripción
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
description: Se usa la operación de suscribirse para suscribirse a las notificaciones de inserción o de extracción las aplicaciones cliente. Es importante tener en cuenta que la estructura de los mensajes de solicitud y las respuestas es diferente según el tipo de notificación de eventos.
ms.openlocfilehash: f6cacab80c8ca2e505ab63a162a161fcf5de8585
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837619"
---
# <a name="subscribe-operation"></a><span data-ttu-id="fb98e-104">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-104">Subscribe operation</span></span>

<span data-ttu-id="fb98e-105">Se usa la operación de suscribirse para suscribirse a las notificaciones de inserción o de extracción las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="fb98e-105">The Subscribe operation is used to subscribe client applications to either push or pull notifications.</span></span> <span data-ttu-id="fb98e-106">Es importante tener en cuenta que la estructura de los mensajes de solicitud y las respuestas es diferente según el tipo de notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="fb98e-106">It is important to be aware that the structure of the request messages and responses is different depending on the type of event notification.</span></span> 
  
## <a name="pull-subscription-subscribe-request-example"></a><span data-ttu-id="fb98e-107">Ejemplo de solicitud de suscripción de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="fb98e-107">Pull Subscription Subscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="fb98e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-108">Description</span></span>

<span data-ttu-id="fb98e-109">En el ejemplo de código siguiente se muestra cómo suscribirse a una suscripción de notificación de evento de extracción.</span><span class="sxs-lookup"><span data-stu-id="fb98e-109">The following code example shows how to subscribe to a pull event notification subscription.</span></span> <span data-ttu-id="fb98e-110">La suscripción informa a la aplicación cliente si el correo nuevo se agrega a la Bandeja de entrada y si se elimina un elemento de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb98e-110">The subscription informs the client application if new mail is added to the Inbox and if an item is deleted from the Inbox.</span></span> <span data-ttu-id="fb98e-111">La suscripción será el tiempo de espera si el cliente no solicita información acerca de los eventos dentro de diez minutos.</span><span class="sxs-lookup"><span data-stu-id="fb98e-111">The subscription will time out if the client does not request information about events within ten minutes.</span></span> <span data-ttu-id="fb98e-112">Si caduca la suscripción, se debe establecer una nueva suscripción para continuar solicitar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="fb98e-112">If the subscription expires, a new subscription must be established to continue to request notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="fb98e-113">Código</span><span class="sxs-lookup"><span data-stu-id="fb98e-113">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-subscribe-request-elements"></a><span data-ttu-id="fb98e-114">Suscripción de extracción suscribirse a elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb98e-114">Pull Subscription Subscribe Request Elements</span></span>

<span data-ttu-id="fb98e-115">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fb98e-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="fb98e-116">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="fb98e-116">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="fb98e-117">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="fb98e-117">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
    
- [<span data-ttu-id="fb98e-118">FolderIds</span><span class="sxs-lookup"><span data-stu-id="fb98e-118">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="fb98e-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="fb98e-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="fb98e-120">Debe establecer</span><span class="sxs-lookup"><span data-stu-id="fb98e-120">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="fb98e-121">EventType</span><span class="sxs-lookup"><span data-stu-id="fb98e-121">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="fb98e-122">Timeout</span><span class="sxs-lookup"><span data-stu-id="fb98e-122">Timeout</span></span>](timeout.md)
    
<span data-ttu-id="fb98e-123">Para buscar otras opciones para el mensaje de solicitud de la operación de Subscribe, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="fb98e-123">To find other options for the request message of the Subscribe operation, explore the schema hierarchy.</span></span> <span data-ttu-id="fb98e-124">Comenzar en el elemento de [PullSubscriptionRequest](pullsubscriptionrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="fb98e-124">Start at the [PullSubscriptionRequest](pullsubscriptionrequest.md) element.</span></span> 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a><span data-ttu-id="fb98e-125">Ejemplo de respuesta correcta suscribirse de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="fb98e-125">Successful Pull Subscription Subscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="fb98e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-126">Description</span></span>

<span data-ttu-id="fb98e-127">En el ejemplo siguiente se muestra una respuesta de suscripción de extracción correcta.</span><span class="sxs-lookup"><span data-stu-id="fb98e-127">The following example shows a successful pull subscription response.</span></span> <span data-ttu-id="fb98e-128">La respuesta contiene el identificador de suscripción y la marca de agua que se usa para obtener la matriz de eventos que están asociados con una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="fb98e-128">The response contains the subscription identifier and watermark that is used to get the array of events that are associated with a subscription.</span></span> <span data-ttu-id="fb98e-129">El identificador de suscripción también se usa para cancelar la suscripción de un cliente de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="fb98e-129">The subscription identifier is also used to unsubscribe a client from a subscription.</span></span>
  
### <a name="code"></a><span data-ttu-id="fb98e-130">Código</span><span class="sxs-lookup"><span data-stu-id="fb98e-130">Code</span></span>

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
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-subscribe-response-elements"></a><span data-ttu-id="fb98e-131">Elementos de respuesta suscribirse de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="fb98e-131">Pull Subscription Subscribe response elements</span></span>

<span data-ttu-id="fb98e-132">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fb98e-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="fb98e-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fb98e-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="fb98e-134">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="fb98e-134">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="fb98e-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fb98e-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="fb98e-136">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fb98e-136">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="fb98e-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fb98e-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fb98e-138">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="fb98e-138">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="fb98e-139">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="fb98e-139">Watermark</span></span>](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a><span data-ttu-id="fb98e-140">Ejemplo de respuesta de Error de suscribirse de suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="fb98e-140">Pull Subscription Subscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="fb98e-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-141">Description</span></span>

<span data-ttu-id="fb98e-142">En el ejemplo siguiente se muestra una respuesta de error a una solicitud Subscribe.</span><span class="sxs-lookup"><span data-stu-id="fb98e-142">The following example shows an error response to a Subscribe request.</span></span> <span data-ttu-id="fb98e-143">El error está causado por un intento para suscribirse a las notificaciones mediante el uso de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="fb98e-143">The error is caused by an attempt to subscribe to notifications by using delegate access.</span></span>
  
### <a name="code"></a><span data-ttu-id="fb98e-144">Código</span><span class="sxs-lookup"><span data-stu-id="fb98e-144">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-error-response-elements"></a><span data-ttu-id="fb98e-145">Elementos de respuesta de Error en la suscripción de extracción</span><span class="sxs-lookup"><span data-stu-id="fb98e-145">Pull Subscription Error response elements</span></span>

<span data-ttu-id="fb98e-146">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fb98e-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="fb98e-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fb98e-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="fb98e-148">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="fb98e-148">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="fb98e-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fb98e-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="fb98e-150">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fb98e-150">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="fb98e-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="fb98e-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="fb98e-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fb98e-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fb98e-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fb98e-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a><span data-ttu-id="fb98e-154">Ejemplo de solicitud de suscripción de inserción</span><span class="sxs-lookup"><span data-stu-id="fb98e-154">Push Subscription request example</span></span>

### <a name="description"></a><span data-ttu-id="fb98e-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-155">Description</span></span>

<span data-ttu-id="fb98e-156">En el ejemplo de código siguiente se muestra cómo suscribirse a una suscripción de notificación de evento de inserción.</span><span class="sxs-lookup"><span data-stu-id="fb98e-156">The following code example shows how to subscribe to a push event notification subscription.</span></span> <span data-ttu-id="fb98e-157">La solicitud identifica las carpetas para supervisar, los tipos de eventos para supervisar, la frecuencia de las notificaciones de estado y la dirección URL del servicio Web que atiende las notificaciones de inserción de cliente.</span><span class="sxs-lookup"><span data-stu-id="fb98e-157">The request identifies the folders to monitor, the types of events to monitor, the frequency of status notifications, and the URL of the client Web service that listens for the push notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="fb98e-158">Código</span><span class="sxs-lookup"><span data-stu-id="fb98e-158">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="http://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="http://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="fb98e-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb98e-159">Comments</span></span>

<span data-ttu-id="fb98e-160">Se envía al cliente Web servicio debe configurarse antes de la notificación de inserción suscribirse solicitud; de lo contrario, no se enviará la primera notificación a un extremo válido y se producirá un error en la notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="fb98e-160">The client Web service must be set up before the push notification subscribe request is sent; otherwise, the first notification will not be sent to a valid endpoint and the push notification will fail.</span></span> <span data-ttu-id="fb98e-161">Para obtener más información, vea [Aplicación de ejemplo de notificación de inserción](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb98e-161">For more information, see [Push Notification Sample Application](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="fb98e-162">Cuando se vuelve a suscribir, se crea un nuevo [SubscriptionId (GetEvents)](subscriptionid-getevents.md) .</span><span class="sxs-lookup"><span data-stu-id="fb98e-162">A new [SubscriptionId (GetEvents)](subscriptionid-getevents.md) is created when you resubscribe.</span></span> <span data-ttu-id="fb98e-163">Use la marca de agua de una suscripción anterior debe volver a suscribirse en el punto donde se finalizó la suscripción anterior.</span><span class="sxs-lookup"><span data-stu-id="fb98e-163">Use the watermark of a previous subscription to resubscribe at the point where the previous subscription ended.</span></span> 
  
### <a name="push-subscription-request-elements"></a><span data-ttu-id="fb98e-164">Elementos de la solicitud de suscripción de inserción</span><span class="sxs-lookup"><span data-stu-id="fb98e-164">Push Subscription Request Elements</span></span>

<span data-ttu-id="fb98e-165">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fb98e-165">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="fb98e-166">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="fb98e-166">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="fb98e-167">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="fb98e-167">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
    
- [<span data-ttu-id="fb98e-168">FolderIds</span><span class="sxs-lookup"><span data-stu-id="fb98e-168">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="fb98e-169">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="fb98e-169">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="fb98e-170">Debe establecer</span><span class="sxs-lookup"><span data-stu-id="fb98e-170">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="fb98e-171">EventType</span><span class="sxs-lookup"><span data-stu-id="fb98e-171">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="fb98e-172">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="fb98e-172">StatusFrequency</span></span>](statusfrequency.md)
    
- [<span data-ttu-id="fb98e-173">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="fb98e-173">Url </span></span>](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a><span data-ttu-id="fb98e-174">Ejemplo de respuesta correcta de suscripción de inserción</span><span class="sxs-lookup"><span data-stu-id="fb98e-174">Successful Push Subscription response example</span></span>

### <a name="description"></a><span data-ttu-id="fb98e-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-175">Description</span></span>

<span data-ttu-id="fb98e-176">En el ejemplo siguiente se muestra una respuesta de suscripción de inserción correctas.</span><span class="sxs-lookup"><span data-stu-id="fb98e-176">The following example shows a successful push subscription response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="fb98e-177">Código</span><span class="sxs-lookup"><span data-stu-id="fb98e-177">Code</span></span>

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
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="push-subscription-response-elements"></a><span data-ttu-id="fb98e-178">Inserción de elementos de respuesta de suscripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-178">Push Subscription response elements</span></span>

<span data-ttu-id="fb98e-179">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fb98e-179">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="fb98e-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fb98e-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="fb98e-181">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="fb98e-181">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="fb98e-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fb98e-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="fb98e-183">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fb98e-183">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="fb98e-184">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fb98e-184">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fb98e-185">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="fb98e-185">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="fb98e-186">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="fb98e-186">Watermark</span></span>](watermark.md)
    
## <a name="see-also"></a><span data-ttu-id="fb98e-187">Ver también</span><span class="sxs-lookup"><span data-stu-id="fb98e-187">See also</span></span>



[<span data-ttu-id="fb98e-188">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="fb98e-188">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="fb98e-189">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="fb98e-189">GetEvents operation</span></span>](getevents-operation.md)


[<span data-ttu-id="fb98e-190">Uso de las suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="fb98e-190">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="fb98e-191">Aplicación de ejemplo de notificación de inserción</span><span class="sxs-lookup"><span data-stu-id="fb98e-191">Push Notification Sample Application</span></span>](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)


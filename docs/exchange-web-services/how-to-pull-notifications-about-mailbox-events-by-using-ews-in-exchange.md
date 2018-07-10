---
title: Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: Descubra cómo usar la API administrada de EWS o EWS para suscribirse a las notificaciones de extracción y obtener eventos.
ms.openlocfilehash: 6a04aaf0102c149691a30c2bd2f499e03265bce8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763159"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a><span data-ttu-id="5ec18-103">Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5ec18-103">Pull notifications about mailbox events by using EWS in Exchange</span></span>

<span data-ttu-id="5ec18-104">Descubra cómo usar la API administrada de EWS o EWS para suscribirse a las notificaciones de extracción y obtener eventos.</span><span class="sxs-lookup"><span data-stu-id="5ec18-104">Find out how to use the EWS Managed API or EWS to subscribe to pull notifications and get events.</span></span>
  
<span data-ttu-id="5ec18-105">EWS en Exchange usa las notificaciones de extracción para permitir que los clientes a petición (o pull) notificaciones sobre los cambios realizados en el buzón de correo desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="5ec18-105">EWS in Exchange uses pull notifications to enable clients to request (or pull) notifications about changes to the mailbox from the server to the client.</span></span>
  
<span data-ttu-id="5ec18-106">Si está suscribirse a las notificaciones de extracción mediante el uso de la API administrada de EWS, [suscribirse a y obtener las notificaciones de extracción](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) mediante el método [SubscribeToPullNotifications](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5ec18-106">If you're subscribing to pull notifications by using the EWS Managed API, you [subscribe to and get pull notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) by using the [SubscribeToPullNotifications](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="5ec18-107">A continuación, obtener eventos desde el servidor mediante el método [GetEvents](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5ec18-107">You then get events from the server by using the [GetEvents](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="5ec18-108">Para suscribirse a las notificaciones de extracción mediante el uso de EWS, [Cree una suscripción](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) mediante el uso de la [operación de Subscribe](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), analizar la respuesta y, a continuación, [Obtenga las notificaciones](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mediante el uso de la [operación GetEvents](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ec18-108">To subscribe to pull notifications by using EWS, you [create a subscription](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) by using the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), parse the response, and then [get the notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) by using the [GetEvents operation](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="5ec18-109">Una vez que el cliente recibe notificaciones de los elementos que se han modificado o creados en el servidor, a continuación, puede [sincronizar los cambios](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="5ec18-109">After the client receives notifications of items that are changed or created on the server, it can then [synchronize the changes](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a><span data-ttu-id="5ec18-110">Suscribirse a y obtener las notificaciones de extracción mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="5ec18-110">Subscribe to and get pull notifications by using the EWS Managed API</span></span>
<span data-ttu-id="5ec18-111"><a name="bk_cepullewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="5ec18-111"></span></span>

<span data-ttu-id="5ec18-112">En el ejemplo de código siguiente se muestra cómo usar el método [SubscribeToPullNotifications](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) para suscribirse a las notificaciones de extracción para todos los eventos en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="5ec18-112">The following code example shows how to use the [SubscribeToPullNotifications](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method to subscribe to pull notifications for all events in the Inbox folder.</span></span> <span data-ttu-id="5ec18-113">El ejemplo utiliza el método [GetEvents](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) para recuperar los eventos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="5ec18-113">The example then uses the [GetEvents](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method to retrieve events from the server.</span></span> <span data-ttu-id="5ec18-114">En este ejemplo, se supone que el **servicio** está un enlace [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido.</span><span class="sxs-lookup"><span data-stu-id="5ec18-114">In this example, we assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) binding.</span></span> 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

<span data-ttu-id="5ec18-115">Después de recibir un evento desde el servidor, puede [sincronizar los cambios con el servidor](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="5ec18-115">After you receive an event from the server, you can [synchronize those changes with the server](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="5ec18-116">Use uno de los métodos de cancelación de suscripción especificados en [¿Cómo puedo cancelar la suscripción a las notificaciones?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) para finalizar la suscripción con el servidor cuando ya no sea necesaria la suscripción.</span><span class="sxs-lookup"><span data-stu-id="5ec18-116">Use one of the unsubscribe methods specified in [How do I unsubscribe to notifications?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a><span data-ttu-id="5ec18-117">Suscribirse a las notificaciones de extracción mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="5ec18-117">Subscribe to pull notifications by using EWS</span></span>
<span data-ttu-id="5ec18-118"><a name="bk_cepullews"> </a></span><span class="sxs-lookup"><span data-stu-id="5ec18-118"></span></span>

<span data-ttu-id="5ec18-119">En el ejemplo siguiente se muestra la solicitud XML a enviar al servidor para suscribirse a todos los [debe establecer](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) en la carpeta Bandeja de entrada mediante el uso de la [operación de suscripción](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ec18-119">The following example shows the XML request to send to the server to subscribe to all [EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) in the Inbox folder by using the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx).</span></span> <span data-ttu-id="5ec18-120">También es la solicitud XML que la API administrada de EWS envía al suscribirse a las notificaciones de extracción mediante el método [SubscribeToPullNotifications](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5ec18-120">This is also the XML request that the EWS Managed API sends when subscribing to pull notifications by using the [SubscribeToPullNotifications](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <PullSubscriptionRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <FolderIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
      <DistinguishedFolderId Id="inbox" />
    </FolderIds>
    <EventTypes xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <EventType>NewMailEvent</EventType>
            <EventType>CreatedEvent</EventType>
            <EventType>DeletedEvent</EventType>
            <EventType>ModifiedEvent</EventType>
            <EventType>MovedEvent</EventType>
            <EventType>CopiedEvent</EventType>
            <EventType>FreeBusyChangedEvent</EventType>
    </EventTypes>
    <Timeout xmlns="http://schemas.microsoft.com/exchange/services/2006/types">30</Timeout>
  </PullSubscriptionRequest>
</Subscribe>
```

<span data-ttu-id="5ec18-121">En el ejemplo de XML siguiente se muestra el mensaje [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de operación **Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="5ec18-121">The following XML example shows the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message that is sent from the server to the client in response to the **Subscribe** operation request.</span></span> <span data-ttu-id="5ec18-122">La inclusión del valor para el elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) NoError significa que la suscripción se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5ec18-122">The inclusion of the NoError value for the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element means that the subscription was created successfully.</span></span> <span data-ttu-id="5ec18-123">El elemento [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) identifica de forma única la suscripción de extracción de notificación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5ec18-123">The [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) element uniquely identifies the pull notification subscription on the server.</span></span> <span data-ttu-id="5ec18-124">El elemento de [marca de agua](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) representa un marcador en la cola de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5ec18-124">The [Watermark](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) element represents a bookmark in the mailbox event queue.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<SubscribeResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <SubscribeResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <SubscriptionId>d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
      <Watermark>AAAAAGUhAAAAAAAAAQ==</Watermark>
    </SubscribeResponseMessage>
  </ResponseMessages>
</SubscribeResponse>
```

<span data-ttu-id="5ec18-125">Después de crear la suscripción, ahora puede obtener eventos mediante el uso de **SubscriptionId** que se devuelve en el mensaje **SubscribeResponse** .</span><span class="sxs-lookup"><span data-stu-id="5ec18-125">After creating the subscription, you can now get events by using the **SubscriptionId** that is returned in the **SubscribeResponse** message.</span></span> 
  
## <a name="get-pull-notifications-by-using-ews"></a><span data-ttu-id="5ec18-126">Obtener las notificaciones de extracción mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="5ec18-126">Get pull notifications by using EWS</span></span>
<span data-ttu-id="5ec18-127"><a name="bk_getpull"> </a></span><span class="sxs-lookup"><span data-stu-id="5ec18-127"></span></span>

<span data-ttu-id="5ec18-128">En el ejemplo de XML siguiente se muestra el mensaje de solicitud de [operación GetEvents](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) que se envía desde el cliente al servidor para obtener las notificaciones para el [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) que se devuelve en el mensaje [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5ec18-128">The following XML example shows the [GetEvents operation](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) request message that is sent from the client to the server to get notifications for the [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) that is returned in the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> <span data-ttu-id="5ec18-129">Para la primera solicitud **GetEvents** , use la [marca de agua](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) devuelto en la respuesta de **suscripción** .</span><span class="sxs-lookup"><span data-stu-id="5ec18-129">For the first **GetEvents** request, use the [Watermark](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) returned in the **Subscribe** response.</span></span> <span data-ttu-id="5ec18-130">Para las solicitudes **GetEvents** posteriores, use la última **marca de agua** que se devuelve en la solicitud de **GetEvents** anterior.</span><span class="sxs-lookup"><span data-stu-id="5ec18-130">For subsequent **GetEvents** requests, use the last **Watermark** that was returned in the previous **GetEvents** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

<span data-ttu-id="5ec18-131">En el ejemplo de XML siguiente se muestra el mensaje de respuesta **GetEvents** que se envía desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="5ec18-131">The following XML example shows the **GetEvents** response message that is sent from the server to the client.</span></span> <span data-ttu-id="5ec18-132">Cada respuesta **GetEvents** incluye información acerca de uno o más eventos.</span><span class="sxs-lookup"><span data-stu-id="5ec18-132">Each **GetEvents** response includes information about one or more events.</span></span> <span data-ttu-id="5ec18-133">Una **marca de agua** se devuelve para cada evento.</span><span class="sxs-lookup"><span data-stu-id="5ec18-133">A **Watermark** is returned for each event.</span></span> <span data-ttu-id="5ec18-134">Debe guardar y utilizar en la siguiente solicitud **GetEvents** la última **marca de agua** .</span><span class="sxs-lookup"><span data-stu-id="5ec18-134">The last **Watermark** must be saved and used in the next **GetEvents** request.</span></span> <span data-ttu-id="5ec18-135">Si no hay eventos de almacén se han producido desde la última solicitud **GetEvents** , se devuelve un evento de estado.</span><span class="sxs-lookup"><span data-stu-id="5ec18-135">If no store events have occurred since the last **GetEvents** request, a status event is returned.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEventsResponseType xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <GetEventsResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <Notification>
        <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
        <PreviousWatermark xmlns="http://schemas.microsoft.com/exchange/services/2006/types">AAAAAGUhAAAAAAAAAQ==</PreviousWatermark>
        <MoreEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/types">false</MoreEvents>
        <NewMailEvent xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Watermark>AAAAAHMhAAAAAAAAAQ==</Watermark>
          <TimeStamp>2013-09-15T21:37:01Z</TimeStamp>
          <ItemId Id="AAAtA=" ChangeKey="CQAAAA==" />
          <ParentFolderId Id="AQAtAEFkbWA==" ChangeKey="AQAAAA==" />
        </NewMailEvent>
      </Notification>
    </GetEventsResponseMessage>
  </ResponseMessages>
</GetEventsResponse>
```

Una vez que se recibe un evento desde el servidor, [sincronizar los cambios realizados en el cliente](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). <span data-ttu-id="5ec18-137">Use la [operación de cancelación de suscripción](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) para finalizar la suscripción con el servidor cuando ya no sea necesaria la suscripción.</span><span class="sxs-lookup"><span data-stu-id="5ec18-137">Use the [Unsubscribe operation](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="5ec18-138">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="5ec18-138">Next steps</span></span>
<span data-ttu-id="5ec18-139"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="5ec18-139"></span></span>

<span data-ttu-id="5ec18-140">Una vez que se reciban las notificaciones, puede [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md) o [sincronizar el contenido de la carpeta que ha cambiado](how-to-synchronize-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="5ec18-140">After you're received notifications, you can [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [sync the contents of the folder that changed](how-to-synchronize-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ec18-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ec18-141">See also</span></span>


- [<span data-ttu-id="5ec18-142">Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5ec18-142">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="5ec18-143">Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5ec18-143">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="5ec18-144">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="5ec18-144">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [<span data-ttu-id="5ec18-145">Tratamiento de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5ec18-145">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="5ec18-146">Sincronización de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5ec18-146">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    


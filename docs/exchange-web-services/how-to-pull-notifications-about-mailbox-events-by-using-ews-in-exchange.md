---
title: Extraer notificaciones sobre eventos de buzón de correo mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: Descubra cómo usar la API administrada de EWS o EWS para suscribirse a notificaciones de extracción y obtener eventos.
ms.openlocfilehash: 3d77c0d4efb8fc853eea64ff2429af5c3dbead27
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456757"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a><span data-ttu-id="e42d9-103">Extraer notificaciones sobre eventos de buzón de correo mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e42d9-103">Pull notifications about mailbox events by using EWS in Exchange</span></span>

<span data-ttu-id="e42d9-104">Descubra cómo usar la API administrada de EWS o EWS para suscribirse a notificaciones de extracción y obtener eventos.</span><span class="sxs-lookup"><span data-stu-id="e42d9-104">Find out how to use the EWS Managed API or EWS to subscribe to pull notifications and get events.</span></span>
  
<span data-ttu-id="e42d9-105">EWS en Exchange usa notificaciones de extracción para permitir que los clientes soliciten (o extraigan) notificaciones sobre cambios en el buzón de correo desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="e42d9-105">EWS in Exchange uses pull notifications to enable clients to request (or pull) notifications about changes to the mailbox from the server to the client.</span></span>
  
<span data-ttu-id="e42d9-106">Si se está suscribiendo para extraer notificaciones mediante la API administrada de EWS, puede [suscribirse a las notificaciones de extracción y obtenerlas](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) mediante el método [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e42d9-106">If you're subscribing to pull notifications by using the EWS Managed API, you [subscribe to and get pull notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) by using the [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="e42d9-107">A continuación, se obtienen los eventos del servidor mediante el método [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e42d9-107">You then get events from the server by using the [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="e42d9-108">Para suscribirse a las notificaciones de extracción mediante EWS, se [crea una suscripción](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) mediante la [operación subscribe](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), se analiza la respuesta y, a continuación, se [obtienen las notificaciones](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mediante la [operación GetEvents](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e42d9-108">To subscribe to pull notifications by using EWS, you [create a subscription](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) by using the [Subscribe operation](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), parse the response, and then [get the notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) by using the [GetEvents operation](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="e42d9-109">Una vez que el cliente recibe notificaciones de los elementos que se han cambiado o que se han creado en el servidor, puede [sincronizar los cambios](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="e42d9-109">After the client receives notifications of items that are changed or created on the server, it can then [synchronize the changes](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a><span data-ttu-id="e42d9-110">Suscribirse a y obtener notificaciones de extracción mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e42d9-110">Subscribe to and get pull notifications by using the EWS Managed API</span></span>
<span data-ttu-id="e42d9-111"><a name="bk_cepullewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e42d9-111"><a name="bk_cepullewsma"> </a></span></span>

<span data-ttu-id="e42d9-112">En el ejemplo de código siguiente se muestra cómo usar el método [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) para suscribirse a las notificaciones de extracción para todos los eventos de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="e42d9-112">The following code example shows how to use the [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method to subscribe to pull notifications for all events in the Inbox folder.</span></span> <span data-ttu-id="e42d9-113">A continuación, en el ejemplo se usa el método [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) para recuperar los eventos del servidor.</span><span class="sxs-lookup"><span data-stu-id="e42d9-113">The example then uses the [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method to retrieve events from the server.</span></span> <span data-ttu-id="e42d9-114">En este ejemplo, se supone que el **servicio** es un enlace [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido.</span><span class="sxs-lookup"><span data-stu-id="e42d9-114">In this example, we assume that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) binding.</span></span> 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

<span data-ttu-id="e42d9-115">Después de recibir un evento del servidor, puede [sincronizar esos cambios con el servidor](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="e42d9-115">After you receive an event from the server, you can [synchronize those changes with the server](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="e42d9-116">Use uno de los métodos de cancelación de suscripción especificados en [¿Cómo puedo cancelar la suscripción a las notificaciones?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) para finalizar la suscripción con el servidor cuando la suscripción ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="e42d9-116">Use one of the unsubscribe methods specified in [How do I unsubscribe to notifications?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a><span data-ttu-id="e42d9-117">Suscribirse a notificaciones de extracción mediante EWS</span><span class="sxs-lookup"><span data-stu-id="e42d9-117">Subscribe to pull notifications by using EWS</span></span>
<span data-ttu-id="e42d9-118"><a name="bk_cepullews"> </a></span><span class="sxs-lookup"><span data-stu-id="e42d9-118"><a name="bk_cepullews"> </a></span></span>

<span data-ttu-id="e42d9-119">En el ejemplo siguiente se muestra la solicitud XML que se va a enviar al servidor para suscribirse a todos los [EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) de la carpeta Bandeja de entrada mediante la [operación subscribe](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e42d9-119">The following example shows the XML request to send to the server to subscribe to all [EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) in the Inbox folder by using the [Subscribe operation](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx).</span></span> <span data-ttu-id="e42d9-120">También es la solicitud XML que la API administrada de EWS envía al suscribirse para extraer notificaciones mediante el método [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e42d9-120">This is also the XML request that the EWS Managed API sends when subscribing to pull notifications by using the [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <PullSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
      <DistinguishedFolderId Id="inbox" />
    </FolderIds>
    <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
            <EventType>NewMailEvent</EventType>
            <EventType>CreatedEvent</EventType>
            <EventType>DeletedEvent</EventType>
            <EventType>ModifiedEvent</EventType>
            <EventType>MovedEvent</EventType>
            <EventType>CopiedEvent</EventType>
            <EventType>FreeBusyChangedEvent</EventType>
    </EventTypes>
    <Timeout xmlns="https://schemas.microsoft.com/exchange/services/2006/types">30</Timeout>
  </PullSubscriptionRequest>
</Subscribe>
```

<span data-ttu-id="e42d9-121">El siguiente ejemplo de XML muestra el mensaje [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de operación de **suscripción** .</span><span class="sxs-lookup"><span data-stu-id="e42d9-121">The following XML example shows the [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message that is sent from the server to the client in response to the **Subscribe** operation request.</span></span> <span data-ttu-id="e42d9-122">La inclusión del valor NoError para el elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) significa que la suscripción se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e42d9-122">The inclusion of the NoError value for the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element means that the subscription was created successfully.</span></span> <span data-ttu-id="e42d9-123">El elemento [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) identifica de forma exclusiva la suscripción de notificaciones de extracción en el servidor.</span><span class="sxs-lookup"><span data-stu-id="e42d9-123">The [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) element uniquely identifies the pull notification subscription on the server.</span></span> <span data-ttu-id="e42d9-124">El elemento [marca de agua](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) representa un marcador en la cola de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="e42d9-124">The [Watermark](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) element represents a bookmark in the mailbox event queue.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<SubscribeResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <SubscribeResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <SubscriptionId>d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
      <Watermark>AAAAAGUhAAAAAAAAAQ==</Watermark>
    </SubscribeResponseMessage>
  </ResponseMessages>
</SubscribeResponse>
```

<span data-ttu-id="e42d9-125">Después de crear la suscripción, ahora puede obtener eventos mediante el **SubscriptionId** que se devuelve en el mensaje **SubscribeResponse** .</span><span class="sxs-lookup"><span data-stu-id="e42d9-125">After creating the subscription, you can now get events by using the **SubscriptionId** that is returned in the **SubscribeResponse** message.</span></span> 
  
## <a name="get-pull-notifications-by-using-ews"></a><span data-ttu-id="e42d9-126">Obtener notificaciones de extracción mediante EWS</span><span class="sxs-lookup"><span data-stu-id="e42d9-126">Get pull notifications by using EWS</span></span>
<span data-ttu-id="e42d9-127"><a name="bk_getpull"> </a></span><span class="sxs-lookup"><span data-stu-id="e42d9-127"><a name="bk_getpull"> </a></span></span>

<span data-ttu-id="e42d9-128">El siguiente ejemplo de XML muestra el mensaje de solicitud de [operación GetEvents](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) que se envía desde el cliente al servidor para obtener notificaciones para el [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) que se devuelve en el mensaje [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e42d9-128">The following XML example shows the [GetEvents operation](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) request message that is sent from the client to the server to get notifications for the [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) that is returned in the [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> <span data-ttu-id="e42d9-129">Para la primera solicitud **GetEvents** , use la [marca de agua](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) devuelta en la respuesta de **suscripción** .</span><span class="sxs-lookup"><span data-stu-id="e42d9-129">For the first **GetEvents** request, use the [Watermark](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) returned in the **Subscribe** response.</span></span> <span data-ttu-id="e42d9-130">Para las siguientes solicitudes **GetEvents** , use la última **marca de agua** devuelta en la solicitud **GetEvents** anterior.</span><span class="sxs-lookup"><span data-stu-id="e42d9-130">For subsequent **GetEvents** requests, use the last **Watermark** that was returned in the previous **GetEvents** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

<span data-ttu-id="e42d9-131">El siguiente ejemplo de XML muestra el mensaje de respuesta **GetEvents** que se envía desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="e42d9-131">The following XML example shows the **GetEvents** response message that is sent from the server to the client.</span></span> <span data-ttu-id="e42d9-132">Cada respuesta **GetEvents** incluye información sobre uno o más eventos.</span><span class="sxs-lookup"><span data-stu-id="e42d9-132">Each **GetEvents** response includes information about one or more events.</span></span> <span data-ttu-id="e42d9-133">Se devuelve una **marca de agua** para cada evento.</span><span class="sxs-lookup"><span data-stu-id="e42d9-133">A **Watermark** is returned for each event.</span></span> <span data-ttu-id="e42d9-134">La última **marca de agua** debe guardarse y usarse en la siguiente solicitud **GetEvents** .</span><span class="sxs-lookup"><span data-stu-id="e42d9-134">The last **Watermark** must be saved and used in the next **GetEvents** request.</span></span> <span data-ttu-id="e42d9-135">Si no se han producido eventos de almacenamiento desde la última solicitud **GetEvents** , se devuelve un evento status.</span><span class="sxs-lookup"><span data-stu-id="e42d9-135">If no store events have occurred since the last **GetEvents** request, a status event is returned.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEventsResponseType xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <GetEventsResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <Notification>
        <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
        <PreviousWatermark xmlns="https://schemas.microsoft.com/exchange/services/2006/types">AAAAAGUhAAAAAAAAAQ==</PreviousWatermark>
        <MoreEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/types">false</MoreEvents>
        <NewMailEvent xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

Después de recibir un evento del servidor, [sincronice los cambios en el cliente](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). <span data-ttu-id="e42d9-137">Use la [operación unsubscribe](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) para finalizar la suscripción con el servidor cuando ya no se necesite la suscripción.</span><span class="sxs-lookup"><span data-stu-id="e42d9-137">Use the [Unsubscribe operation](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="e42d9-138">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="e42d9-138">Next steps</span></span>
<span data-ttu-id="e42d9-139"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e42d9-139"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="e42d9-140">Una vez que haya recibido las notificaciones, puede [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md) o [sincronizar el contenido de la carpeta que ha cambiado](how-to-synchronize-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="e42d9-140">After you're received notifications, you can [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [sync the contents of the folder that changed](how-to-synchronize-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e42d9-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e42d9-141">See also</span></span>


- [<span data-ttu-id="e42d9-142">Suscripciones de notificación, eventos de buzón y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e42d9-142">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="e42d9-143">Notificaciones de secuencia sobre eventos de buzón de correo mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e42d9-143">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e42d9-144">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo de Exchange</span><span class="sxs-lookup"><span data-stu-id="e42d9-144">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [<span data-ttu-id="e42d9-145">Control de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e42d9-145">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e42d9-146">Sincronización de buzones de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e42d9-146">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    


---
title: Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe9bde1e-da0e-413c-a109-077f399f67a3
description: Descubra cómo usar la API administrada de EWS o EWS para suscribirse a las notificaciones de transmisión y obtener eventos.
ms.openlocfilehash: aad7604511687d1482914183979e954f79572af9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763170"
---
# <a name="stream-notifications-about-mailbox-events-by-using-ews-in-exchange"></a><span data-ttu-id="32a69-103">Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a69-103">Stream notifications about mailbox events by using EWS in Exchange</span></span>

<span data-ttu-id="32a69-104">Descubra cómo usar la API administrada de EWS o EWS para suscribirse a las notificaciones de transmisión y obtener eventos.</span><span class="sxs-lookup"><span data-stu-id="32a69-104">Find out how to use the EWS Managed API or EWS to subscribe to streaming notifications and get events.</span></span>
  
<span data-ttu-id="32a69-105">EWS en Exchange usa transmisión por secuencias de notificaciones para recibir las notificaciones que se envían por el servidor a través de una conexión que queda abierto para un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="32a69-105">EWS in Exchange uses streaming notifications to receive notifications that are sent by the server through a connection that remains open for a specified period of time.</span></span>
  
<span data-ttu-id="32a69-106">Si está suscribirse a la transmisión por secuencias de notificaciones mediante el uso de la API administrada de EWS, [suscribirse y obtener transmisión por secuencias de notificaciones](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamewsma) mediante el método [SubscribeToStreamingNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a69-106">If you're subscribing to streaming notifications by using the EWS Managed API, you [subscribe and get streaming notifications](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamewsma) by using the [SubscribeToStreamingNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="32a69-107">A continuación, crear una conexión a la suscripción mediante el objeto [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a69-107">You then create a connection to the subscription by using the [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="32a69-108">Para suscribirse a las notificaciones de transmisión por secuencias mediante el uso de EWS, [Cree una suscripción](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamews) mediante el uso de la [operación de Subscribe](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), analizar la respuesta y, a continuación, [Obtenga las notificaciones de transmisión por secuencias](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews) mediante el uso de la [operación de GetStreamingEvents](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) solicitud.</span><span class="sxs-lookup"><span data-stu-id="32a69-108">To subscribe to streaming notifications by using EWS, you [create a subscription](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamews) by using the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), parse the response, and then [get the streaming notifications](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews) by using the [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request.</span></span> 
  
<span data-ttu-id="32a69-109">Una vez que el cliente recibe las notificaciones de elementos ha cambiado o creado en el servidor, el [siguiente paso](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) es sincronizar los cambios.</span><span class="sxs-lookup"><span data-stu-id="32a69-109">After the client receives notifications of items changed or created on the server, the [next step](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) is to synchronize the changes.</span></span> 
  
## <a name="subscribe-to-and-get-streaming-notifications-by-using-the-ews-managed-api"></a><span data-ttu-id="32a69-110">Suscribirse a y obtener la transmisión por secuencias de notificaciones mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="32a69-110">Subscribe to and get streaming notifications by using the EWS Managed API</span></span>
<span data-ttu-id="32a69-111"><a name="bk_cestreamewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="32a69-111"></span></span>

<span data-ttu-id="32a69-112">En el ejemplo de código siguiente se muestra cómo usar el método [SubscribeToStreamingNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx) para suscribirse a la transmisión por secuencias de notificaciones para todos los eventos en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="32a69-112">The following code example shows how to use the [SubscribeToStreamingNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx) method to subscribe to streaming notifications for all events in the Inbox folder.</span></span> <span data-ttu-id="32a69-113">A continuación, se crea una conexión para la suscripción mediante la creación de un objeto [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a69-113">It then creates a connection for the subscription by creating a [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="32a69-114">En este ejemplo, se supone que el **servicio** está un enlace [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido.</span><span class="sxs-lookup"><span data-stu-id="32a69-114">In this example, we assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) binding.</span></span> 
  
```cs
// Subscribe to streaming notifications in the Inbox. 
StreamingSubscription = service.SubscribeToStreamingNotifications(
    new FolderId[] { WellKnownFolderName.Inbox },
    EventType.NewMail,
    EventType.Created,
    EventType.Deleted,
    EventType.Modified,
    EventType.Moved,
    EventType.Copied,
    EventType.FreeBusyChanged);
// Create a streaming connection to the service object, over which events are returned to the client.
// Keep the streaming connection open for 30 minutes.
StreamingSubscriptionConnection connection = new StreamingSubscriptionConnection(service, 30);
connection.AddSubscription(StreamingSubscription);
connection.OnNotificationEvent += OnNotificationEvent;
connection.OnDisconnect += OnDisconnect;
connection.Open();
```

<span data-ttu-id="32a69-115">Después de que ha recibido eventos desde el servidor, el [siguiente paso](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) es para sincronizar los cambios con el servidor.</span><span class="sxs-lookup"><span data-stu-id="32a69-115">After you have received events from the server, the [next step](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) is to synchronize those changes with the server.</span></span> <span data-ttu-id="32a69-116">Use uno de los métodos de cancelación de suscripción que aparecen en la [tabla 4](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) para finalizar la suscripción con el servidor cuando ya no sea necesaria la suscripción.</span><span class="sxs-lookup"><span data-stu-id="32a69-116">Use one of the unsubscribe methods listed in [Table 4](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="subscribe-to-streaming-notifications-by-using-ews"></a><span data-ttu-id="32a69-117">Suscríbase a la transmisión por secuencias de notificaciones mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="32a69-117">Subscribe to streaming notifications by using EWS</span></span>
<span data-ttu-id="32a69-118"><a name="bk_cestreamews"> </a></span><span class="sxs-lookup"><span data-stu-id="32a69-118"></span></span>

<span data-ttu-id="32a69-119">En el ejemplo siguiente se muestra una solicitud XML que se envía por el cliente al servidor cuando el cliente llama a la [operación de suscribirse](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) para suscribirse a todos los [debe establecer](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="32a69-119">The following example shows an XML request that is sent by the client to the server when the client calls the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) to subscribe to all [EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) in the Inbox folder.</span></span> <span data-ttu-id="32a69-120">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método [SubscribeToStreamingNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx) para suscribirse a las notificaciones de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="32a69-120">This is also the XML request that the EWS Managed API sends when you use the [SubscribeToStreamingNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx) method to subscribe to streaming notifications.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
          <t:EventType>CreatedEvent</t:EventType>
          <t:EventType>DeletedEvent</t:EventType>
          <t:EventType>ModifiedEvent</t:EventType>
          <t:EventType>MovedEvent</t:EventType>
          <t:EventType>CopiedEvent</t:EventType>
          <t:EventType>FreeBusyChangedEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="32a69-121">En el ejemplo de XML siguiente se muestra el mensaje de [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud [Subscribe operación](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a69-121">The following XML example shows the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message that is sent from the server to the client in response to the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="32a69-122">La inclusión del valor para el elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) NoError significa que la suscripción se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="32a69-122">The inclusion of the NoError value for the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element means that the subscription was created successfully.</span></span> <span data-ttu-id="32a69-123">El elemento [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) identifica de forma única la suscripción de notificación de transmisión por secuencias en el servidor.</span><span class="sxs-lookup"><span data-stu-id="32a69-123">The [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) element uniquely identifies the streaming notification subscription on the server.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
          <m:SubscribeResponseMessage ResponseClass="Success">
            <m:ResponseCode>NoError</m:ResponseCode>
            <m:SubscriptionId>JgBibjFwcjAzbWIyMDIubmFtcHJkMDMucHJvZC5vdXRsb29rLmNvbRAAAADwXxVesOnHS5BxUHKwAW88SHjwd1iB0Ag=</m:SubscriptionId>
          </m:SubscribeResponseMessage>
        </m:ResponseMessages>
      </m:SubscribeResponse>
    </s:Body>
  </s:Envelope>
```

<span data-ttu-id="32a69-124">Después de crear la suscripción, puede ahora [Obtenga los eventos de transmisión por secuencias](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews) mediante el uso de la [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) devueltas en el mensaje [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a69-124">After creating the subscription, you can now [get the streamed events](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews) by using the [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) returned in the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> 
  
## <a name="get-streaming-events-by-using-ews"></a><span data-ttu-id="32a69-125">Obtener transmisión por secuencias eventos mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="32a69-125">Get streaming events by using EWS</span></span>
<span data-ttu-id="32a69-126"><a name="bk_cegetnotifsews"> </a></span><span class="sxs-lookup"><span data-stu-id="32a69-126"></span></span>

<span data-ttu-id="32a69-127">En el ejemplo de XML siguiente se muestra el mensaje de solicitud de la [operación de GetStreamingEvents](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) que el cliente envía al servidor para obtener las notificaciones para el [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) devueltas en el mensaje de [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a69-127">The following XML example shows the [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request message that the client sends to the server to get notifications for the [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) returned in the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> <span data-ttu-id="32a69-128">La solicitud de [operación GetStreamingEvents](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) indica que la longitud de la conexión es de 30 minutos de tipo long.</span><span class="sxs-lookup"><span data-stu-id="32a69-128">The [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request indicates that the length of the connection is 30 minutes long.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetStreamingEvents>
      <m:SubscriptionIds>
        <t:SubscriptionId>JgBibjFwcjAzbWIyMDIubmFtcHJkMDMucHJvZC5vdXRsb29rLmNvbRAAAADwXxVesOnHS5BxUHKwAW88SHjwd1iB0Ag=</t:SubscriptionId>
      </m:SubscriptionIds>
      <m:ConnectionTimeout>30</m:ConnectionTimeout>
    </m:GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="32a69-129">En el ejemplo de XML siguiente se muestra el mensaje de [GetStreamingEventsResponse](http://msdn.microsoft.com/library/ea1e7e7e-1b19-4e07-ba42-5dbd888c6db2%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de la [operación de GetStreamingEvents](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a69-129">The following XML example shows the [GetStreamingEventsResponse](http://msdn.microsoft.com/library/ea1e7e7e-1b19-4e07-ba42-5dbd888c6db2%28Office.15%29.aspx) message that is sent from the server to the client in response to the [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="32a69-130">Contiene un CreatedEvent y un NewMailEvent para el elemento y un ModifiedEvent para la carpeta, todos los cuales se producen cuando se recibe un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="32a69-130">It contains a CreatedEvent and a NewMailEvent for the item, and a ModifiedEvent for the folder, all of which occur when a new message is received.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <soap:Body xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseMessages>
      <m:GetStreamingEventsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Notifications>
          <m:Notification>
            <t:SubscriptionId>JgBibjFwcjAzbWIyMDIubmFtcHJkMDMucHJvZC5vdXRsb29rLmNvbRAAAADwXxVesOnHS5BxUHKwAW88SHjwd1iB0Ag=</t:SubscriptionId>
            <t:CreatedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:CreatedEvent>
            <t:NewMailEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:ModifiedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:FolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgEJAAAA" ChangeKey="AQAAAA==" />
              <t:UnreadCount>1</t:UnreadCount>
            </t:ModifiedEvent>
          </m:Notification>
        </m:Notifications>
      </m:GetStreamingEventsResponseMessage>
    </m:ResponseMessages>
  </m:GetStreamingEventsResponse>
</soap:Body>
```

Después de que ha recibido eventos desde el servidor, el [siguiente paso](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) es para sincronizar los cambios con el servidor. <span data-ttu-id="32a69-132">Use la [operación de cancelación de suscripción](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) para finalizar la suscripción con el servidor cuando ya no sea necesaria la suscripción.</span><span class="sxs-lookup"><span data-stu-id="32a69-132">Use the [Unsubscribe operation](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="32a69-133">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="32a69-133">Next steps</span></span>
<span data-ttu-id="32a69-134"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="32a69-134"></span></span>

<span data-ttu-id="32a69-135">Una vez haya recibido las notificaciones, puede [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md) o [sincronizar el contenido de la carpeta que ha cambiado](how-to-synchronize-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="32a69-135">After you've received notifications, you can [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [sync the contents of the folder that changed](how-to-synchronize-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32a69-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="32a69-136">See also</span></span>


- [<span data-ttu-id="32a69-137">Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a69-137">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="32a69-138">Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a69-138">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32a69-139">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="32a69-139">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [<span data-ttu-id="32a69-140">Tratamiento de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a69-140">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="32a69-141">Sincronización de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a69-141">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    


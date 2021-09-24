---
title: Notificaciones de extracción de eventos de buzón utilizando EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: Descubra cómo usar la API administrada ews o EWS para suscribirse a las notificaciones de extracción y obtener eventos.
ms.openlocfilehash: eb694eddd16567e42ccc43b2854f0432c54dc6b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513104"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>Notificaciones de extracción de eventos de buzón utilizando EWS en Exchange

Descubra cómo usar la API administrada ews o EWS para suscribirse a las notificaciones de extracción y obtener eventos.
  
EWS en Exchange usa notificaciones de extracción para permitir que los clientes soliciten (o extraigan) notificaciones sobre los cambios realizados en el buzón del servidor al cliente.
  
Si se suscribe a las notificaciones de extracción mediante [](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) la API administrada de EWS, se suscribe y obtiene notificaciones de extracción mediante el método [SubscribeToPullNotifications.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) A continuación, se obtienen eventos del servidor mediante el [método GetEvents.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) 
  
Para suscribirse a las notificaciones de extracción mediante EWS, cree una suscripción [](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mediante la operación [Subscribe](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), analice la respuesta y, [a](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) continuación, obtenga las notificaciones mediante la [operación GetEvents](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).
  
Después de que el cliente recibe notificaciones de elementos que se cambian o crean en el servidor, puede sincronizar [los cambios](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a>Suscribirse y obtener notificaciones de extracción mediante la API administrada ews
<a name="bk_cepullewsma"> </a>

En el siguiente ejemplo de código se muestra cómo usar el método [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) para suscribirse a las notificaciones de extracción de todos los eventos de la carpeta Bandeja de entrada. A continuación, se usa [el método GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) para recuperar eventos del servidor. En este ejemplo, se supone que **el servicio** es un enlace [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido. 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

Después de recibir un evento del servidor, puede [sincronizar esos cambios con el servidor](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). Use uno de los métodos de cancelación de suscripción especificados en ¿Cómo cancelar la suscripción a las [notificaciones?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) para finalizar la suscripción con el servidor cuando la suscripción ya no sea necesaria. 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a>Suscribirse a notificaciones de extracción mediante EWS
<a name="bk_cepullews"> </a>

En el ejemplo siguiente se muestra la solicitud XML para enviar al servidor para suscribirse a todos los [EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) de la carpeta Bandeja de entrada mediante la [operación Subscribe](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx). Esta es también la solicitud XML que la API administrada ews envía al suscribirse a notificaciones de extracción mediante el método [SubscribeToPullNotifications.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) 
  
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

En el siguiente ejemplo XML se muestra el mensaje [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud **de operación Subscribe.** La inclusión del valor NoError para el [elemento ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) significa que la suscripción se creó correctamente. El [elemento SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) identifica de forma única la suscripción de notificación de extracción en el servidor. El [elemento Watermark](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) representa un marcador en la cola de eventos del buzón. 
  
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

Después de crear la suscripción, ahora puede obtener eventos mediante **el SubscriptionId** que se devuelve en el **mensaje SubscribeResponse.** 
  
## <a name="get-pull-notifications-by-using-ews"></a>Obtener notificaciones de extracción mediante EWS
<a name="bk_getpull"> </a>

En el siguiente ejemplo XML se muestra el mensaje de solicitud de operación [GetEvents](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) que se envía desde el cliente al servidor para obtener notificaciones del [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) que se devuelve en el [mensaje SubscribeResponse.](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) Para la primera **solicitud GetEvents,** use la [marca de agua devuelta](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) en la respuesta **Subscribe.** Para las **solicitudes GetEvents** posteriores, use la última **marca de** agua que se devolvió en la solicitud **GetEvents** anterior. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

En el siguiente ejemplo XML se muestra el mensaje de respuesta **GetEvents** que se envía desde el servidor al cliente. Cada **respuesta GetEvents** incluye información sobre uno o varios eventos. Se **devuelve una** marca de agua para cada evento. La última **marca de** agua debe guardarse y usarse en la siguiente **solicitud GetEvents.** Si no se han producido eventos de almacén desde la última **solicitud GetEvents,** se devuelve un evento de estado. 
  
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

Después de recibir un evento del servidor, [sincronice los cambios en el cliente](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). Use la [operación Cancelar suscripción](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) para finalizar la suscripción con el servidor cuando la suscripción ya no sea necesaria. 
  
## <a name="next-steps"></a>Pasos siguientes
<a name="bk_nextsteps"> </a>

Después de recibir notificaciones, puede [](how-to-synchronize-folders-by-using-ews-in-exchange.md) sincronizar la jerarquía de carpetas o sincronizar el contenido [de la carpeta que cambió](how-to-synchronize-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Ver también


- [Suscripciones de notificación, eventos de buzón, y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Notificaciones de transmisión de eventos de buzón usando EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Mantener la afinidad entre un grupo de suscripciones y el servidor del buzón de Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [Manejo de errores relacionados con la notificación en EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Sincronización del buzón y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    


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
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange

Descubra cómo usar la API administrada de EWS o EWS para suscribirse a las notificaciones de extracción y obtener eventos.
  
EWS en Exchange usa las notificaciones de extracción para permitir que los clientes a petición (o pull) notificaciones sobre los cambios realizados en el buzón de correo desde el servidor al cliente.
  
Si está suscribirse a las notificaciones de extracción mediante el uso de la API administrada de EWS, [suscribirse a y obtener las notificaciones de extracción](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) mediante el método [SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) . A continuación, obtener eventos desde el servidor mediante el método [GetEvents](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) . 
  
Para suscribirse a las notificaciones de extracción mediante el uso de EWS, [Cree una suscripción](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) mediante el uso de la [operación de Subscribe](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), analizar la respuesta y, a continuación, [Obtenga las notificaciones](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mediante el uso de la [operación GetEvents](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).
  
Una vez que el cliente recibe notificaciones de los elementos que se han modificado o creados en el servidor, a continuación, puede [sincronizar los cambios](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a>Suscribirse a y obtener las notificaciones de extracción mediante el uso de la API administrada de EWS
<a name="bk_cepullewsma"> </a>

En el ejemplo de código siguiente se muestra cómo usar el método [SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) para suscribirse a las notificaciones de extracción para todos los eventos en la carpeta Bandeja de entrada. El ejemplo utiliza el método [GetEvents](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) para recuperar los eventos desde el servidor. En este ejemplo, se supone que el **servicio** está un enlace [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido. 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

Después de recibir un evento desde el servidor, puede [sincronizar los cambios con el servidor](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). Use uno de los métodos de cancelación de suscripción especificados en [¿Cómo puedo cancelar la suscripción a las notificaciones?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) para finalizar la suscripción con el servidor cuando ya no sea necesaria la suscripción. 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a>Suscribirse a las notificaciones de extracción mediante el uso de EWS
<a name="bk_cepullews"> </a>

En el ejemplo siguiente se muestra la solicitud XML a enviar al servidor para suscribirse a todos los [debe establecer](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) en la carpeta Bandeja de entrada mediante el uso de la [operación de suscripción](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx). También es la solicitud XML que la API administrada de EWS envía al suscribirse a las notificaciones de extracción mediante el método [SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) . 
  
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

En el ejemplo de XML siguiente se muestra el mensaje [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de operación **Subscribe** . La inclusión del valor para el elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) NoError significa que la suscripción se ha creado correctamente. El elemento [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) identifica de forma única la suscripción de extracción de notificación en el servidor. El elemento de [marca de agua](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) representa un marcador en la cola de eventos de buzón de correo. 
  
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

Después de crear la suscripción, ahora puede obtener eventos mediante el uso de **SubscriptionId** que se devuelve en el mensaje **SubscribeResponse** . 
  
## <a name="get-pull-notifications-by-using-ews"></a>Obtener las notificaciones de extracción mediante el uso de EWS
<a name="bk_getpull"> </a>

En el ejemplo de XML siguiente se muestra el mensaje de solicitud de [operación GetEvents](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) que se envía desde el cliente al servidor para obtener las notificaciones para el [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) que se devuelve en el mensaje [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) . Para la primera solicitud **GetEvents** , use la [marca de agua](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) devuelto en la respuesta de **suscripción** . Para las solicitudes **GetEvents** posteriores, use la última **marca de agua** que se devuelve en la solicitud de **GetEvents** anterior. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

En el ejemplo de XML siguiente se muestra el mensaje de respuesta **GetEvents** que se envía desde el servidor al cliente. Cada respuesta **GetEvents** incluye información acerca de uno o más eventos. Una **marca de agua** se devuelve para cada evento. Debe guardar y utilizar en la siguiente solicitud **GetEvents** la última **marca de agua** . Si no hay eventos de almacén se han producido desde la última solicitud **GetEvents** , se devuelve un evento de estado. 
  
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

Una vez que se recibe un evento desde el servidor, [sincronizar los cambios realizados en el cliente](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). Use la [operación de cancelación de suscripción](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) para finalizar la suscripción con el servidor cuando ya no sea necesaria la suscripción. 
  
## <a name="next-steps"></a>Siguientes pasos
<a name="bk_nextsteps"> </a>

Una vez que se reciban las notificaciones, puede [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md) o [sincronizar el contenido de la carpeta que ha cambiado](how-to-synchronize-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Vea también


- [Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [Tratamiento de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Sincronización de buzón de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    


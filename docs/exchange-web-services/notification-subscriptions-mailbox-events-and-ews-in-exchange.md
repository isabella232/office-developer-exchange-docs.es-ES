---
title: Suscripciones de notificación, eventos de buzón, y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 76136f28-0dad-4ecc-9dd7-a45a1861e4b0
description: Descubre las suscripciones de notificación y los eventos de buzón en EWS in Exchange.
localization_priority: Priority
ms.openlocfilehash: 00a0941e615f35a46bb77c00648b75fcd2a45286
ms.sourcegitcommit: 843a2e030a94b12aec70c553ca4e06e39ac02d82
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2020
ms.locfileid: "49603844"
---
# <a name="notification-subscriptions-mailbox-events-and-ews-in-exchange"></a>Suscripciones de notificación, eventos de buzón, y EWS en Exchange

Descubre las suscripciones de notificación y los eventos de buzón en EWS in Exchange.
  
Puedes utilizar tanto la API administrada de EWS como los servicios Web Exchange (EWS) para suscribirte y recibir notificaciones cuando los eventos se produzcan en un buzón de correo, o en una o más de las carpetas de un buzón. Hay tres tipos de suscripción disponibles: notificaciones de transmisión, notificaciones de extracción y notificaciones de inserción. Cada uno de estos tipos de suscripción utiliza diferentes técnicas para recibir o recuperar las notificaciones.
  
## <a name="getting-notifications---what-are-my-options"></a>Recibir notificaciones: ¿qué opciones tengo?
<a name="bk_notiftypes"> </a>

EWS incluye tres tipos de suscripción que funcionan de forma independiente para notificar al cliente los cambios en el servidor. No importa qué tipo de suscripción elijas, al final tendrás acceso a todas las notificaciones de los mismos eventos, sólo depende de cómo se consiguen.
  
**Cuadro 1. Tipos de suscripción**

|**Opción**|**Descripción**|**¿Es adecuado para mí?**|
|:-----|:-----|:-----|
|Notificaciones de transmisión  <br/> |Notificaciones que son enviadas por el servidor a través de una conexión que permanece abierta durante un período de tiempo determinado.  <br/> |Por lo general, se recomiendan las notificaciones de transmisión para la mayoría de las aplicaciones. Son similares a las notificaciones de extracción e inserción, y ofrecen las ventajas de las dos. Después de establecer la suscripción de notificación, la conexión permanece abierta hasta 30 minutos para permitir que el servidor devuelva las notificaciones al cliente. No es necesario solicitar actualizaciones, como lo harías con una suscripción de extracción, y no tienes que crear una aplicación de escucha de servicio web como lo harías con una suscripción de inserción.  <br/> |
|Notificaciones de extracción  <br/> |Notificaciones que son solicitadas (o extraídas) por el cliente.  <br/> |Las notificaciones de extracción son por lo general más apropiadas para los clientes de conexión débil, en los que el cliente no está conectado de forma fiable a la red. Las notificaciones de extracción pueden crear un exceso de tráfico entre el cliente y el servidor porque el cliente está enviando frecuentes solicitudes al servidor para recuperar las notificaciones, y no todas las solicitudes resultan en la recuperación de las notificaciones.  <br/> |
|Notificaciones de inserción   <br/> |Notificaciones que son enviadas (o insertadas) por el servidor a un servicio web por parte del cliente a través de una dirección de devolución de llamada.  <br/> |Por lo general, las notificaciones de inserción  proporcionan una latencia de notificación menor que las notificaciones de extracción y son adecuadas para clientes estrechamente acoplados a los que el servidor tiene un acceso fiable y el cliente es accesible por IP. Sin embargo, las notificaciones de inserción han caído en desuso desde la llegada de las notificaciones de transmisión en Exchange 2010. En la medida de lo posible, te recomendamos que utilices las notificaciones por transmisión en lugar de las notificaciones de inserción en el futuro. Las notificaciones de inserción requieren que escribas una aplicación de escucha, que es donde se insertan las notificaciones. Esto tiene un ligero beneficio sobre las notificaciones de extracción ya que reduce el tráfico en la red, pero añade gastos generales al requerir una aplicación separada.  <br/> |
   
## <a name="what-ews-events-can-i-subscribe-to"></a>¿A qué eventos de EWS puedo suscribirme?
<a name="bk_eventtypes"> </a>

Los tipos de eventos EWS a los que se suscriben los clientes se definen mediante la enumeración [EventType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx) para la API administrada de EWS o el elemento [EventType](https://msdn.microsoft.com/library/04b70f9e-c226-4130-958e-0db0275cf58b%28Office.15%29.aspx) para EWS. Es posible suscribirse a los siguientes eventos de EWS: 
  
- NewMail - Un nuevo mensaje llegó a la bandeja de entrada.
    
- Borrado - Un mensaje fue borrado por completo de la bandeja de entrada. Para obtener más información sobre las notificaciones de elementos eliminados, consulta [Eliminación de elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md) y [Notificaciones de extracción para eventos de buzón de correo relacionados con la eliminación de EWS en Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md).
    
- Modificado: se ha cambiado un elemento o una carpeta.
    
- Trasladado: se ha trasladado un elemento o una carpeta. 
    
- Copiado: se ha copiado un elemento o una carpeta.
    
- Creado: se ha creado un elemento o una carpeta. 
    
- FreeBusyChanged: se ha cambiado la información disponibilidad de un usuario.
    
Otro tipo de evento EWS, el evento Estado, está definido por el elemento [EventType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx) pero no estás suscrito a este evento. En su lugar, es enviado por el servidor para comprobar el estado del cliente para las notificaciones de transmisión e inserción solamente. El cliente tiene que responder a este evento o de lo contrario el cliente se quedará sin tiempo. 
  
Una acción de un solo usuario suele dar lugar a la creación de múltiples notificaciones. Para ilustrar esto, el siguiente gráfico muestra algunos escenarios comunes y las notificaciones creadas para cada uno de ellos. La configuración del cliente tiene un impacto en las notificaciones recibidas, por lo que esta no es una lista exhaustiva de todas las opciones de configuración y notificaciones resultantes.
  
**Gráfico 1. Tipos de eventos devueltos por las suscripciones de notificación** 

![Tabla que muestra las notificaciones enviadas en escenarios de usuario comunes, como recibir nuevo correo, crear una nueva carpeta, mover una carpeta, etc.](media/Exchange2013_Notifications_Events.png)
  
El gráfico 1 simplifica el proceso de notificación. En realidad, se pueden crear múltiples notificaciones (incluso múltiples notificaciones del mismo tipo) para una sola acción del usuario. Por ejemplo, en el caso de una operación de traslado de una carpeta, se crean tres eventos de carpeta: uno para la carpeta que se está modificando, otro para la antigua carpeta principal y otro para la nueva carpeta principal. Dado que se pueden desencadenar numerosos eventos para una sola operación, se recomienda [incorporar un tiempo de espera de unos pocos segundos en las operaciones de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices), de modo que sólo se sincronice cuando la acción se haya completado, en lugar de a mitad de la operación.
  
También es importante tener en cuenta que los ajustes de configuración que cada usuario elija afectarán a las notificaciones que se creen. Por ejemplo, los datos de disponibilidad de algunos usuarios se actualizan automáticamente y el evento FreeBusyChanged se crea cuando se recibe una nueva solicitud de reunión, incluso antes de que hayan leído el artículo. Para otros usuarios, los datos de disponibilidad no se actualizan y el evento FreeBusyChanged no se crea hasta después de que la reunión haya sido aceptada. Estos ajustes pueden tener un impacto considerable en las notificaciones creadas por el servidor.
  
## <a name="how-do-ews-notifications-work"></a>¿Cómo funcionan las notificaciones de EWS?
<a name="bk_howwork"> </a>

Las notificaciones de EWS se administran por suscripción. Normalmente hay una suscripción por buzón, y dentro de la suscripción del buzón puedes suscribirte a algunas o a todas las carpetas. Puedes decidir a qué tipo de notificación suscribirte (de transmisión, de extracción o de inserción) y qué tipo de eventos te gustaría recibir (NewMail, Creado, Eliminado, Modificado, etc.), y luego puedes crear una suscripción. Los eventos de EWS se envían asincrónicamente desde el servidor del buzón al cliente. (Lección de historia: los eventos están sincronizados en Exchange 2007 - y los eventos se almacenan en el servidor de Acceso de Clientes en Exchange 2010, pero ya no).
  
Dependiendo del tipo de suscripción que tengas, las formas en que se envían las notificaciones al cliente pueden variar. En esta sección se describe con más detalle cómo funciona cada tipo de suscripción.
  
### <a name="ews-streaming-notifications"></a>Notificaciones de transmisión EWS
<a name="bk_streamnotif"> </a>

Las notificaciones de transmisión se basan en una solicitud de colgado en el servidor para mantener abierta una conexión de suscripción de transmisión, de modo que cualquier evento que ocurra mientras la conexión está activa se transmita al cliente inmediatamente. Se pueden enviar múltiples notificaciones en el curso de una sola conexión, y la conexión se mantiene abierta hasta que el intervalo caduque, o durante un máximo de 30 minutos. Después de que la conexión caduque, el cliente envía la solicitud de colgado de nuevo. En el gráfico 2 se muestra cómo funcionan las suscripciones y las notificaciones de transmisión.
  
**Figura 2. Descripción general de la notificación de transmisión**

![Ilustración que muestra cómo funcionan las notificaciones de streaming. Para configurar las notificaciones de streaming: 1. Suscribirse, 2. Abrir conexión, 3. Esperar eventos, 4. Recibir eventos, repetir 3 y 4, 5. Cerrar o mantener conexión, 6. Cancelar suscripción o agotar tiempo de espera.](media/Exchange2013_Notifications_StreamSub.png)
  
Para obtener información sobre la creación de notificaciones de transmisión consulta [Notificaciones de transmisión de eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md).
  
### <a name="ews-pull-notifications"></a>Notificaciones de extracción EWS
<a name="bk_pullnotif"> </a>

Las notificaciones de extracción dependen de que el cliente pida las notificaciones en un intervalo de tiempo que el cliente administre. Esto puede dar lugar a respuestas de GetEvents sin notificaciones. En el gráfico 3 se muestra cómo funcionan las suscripciones y las notificaciones de extracción e inserción.
  
**Grafico 3. Descripción general de la notificación de extracción**

![Ilustración que muestra cómo funcionan las notificaciones de extracción. Para configurar las notificaciones de extracción: 1. Suscribirse, 2. Enviar GetEvents, 3. Recibir respuesta, repetir 2 y 3, 4. Cerrar o mantener conexión, 5. Cancelar suscripción o agotar tiempo de espera.](media/Exchange2013_Notifications_PullSub.png)
  
Para obtener información sobre la creación de notificaciones de extracción consulta [Notificaciones de extracción de eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).
  
### <a name="ews-push-notifications"></a>Notificaciones de inserción EWS
<a name="bk_pushnotif"> </a>

Las notificaciones de inserción se basan en que el servidor devuelva las notificaciones al cliente. Sólo hay tráfico si hay una notificación. En el gráfico 4 se muestra cómo funcionan las suscripciones y las notificaciones de inserción.
  
**Grafico 4. Descripción general de la notificación de inserción**

![Ilustración que muestra cómo funcionan las notificaciones de inserción. Para configurar las notificaciones de inserción: 1. Crear agente de escucha, 2. Suscribirse, 3. Esperar eventos, 4. Recibir eventos, 5. Enviar respuesta "OK", repetir 3, 4 y 5, 6. Cancelar suscripción o agotar tiempo de espera.](media/Exchange2013_Notifications_PushSub.png)

Si estás usando [notificaciones de inserción con Exchange 2010](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx) considera la posibilidad de actualizar tu aplicación para usar las [notificaciones de transmisión](https://code.msdn.microsoft.com/exchange/Exchange-2013-Set-push-82738cc5), de modo que no necesites una aplicación separada para recibir los eventos.

  
## <a name="how-do-i-subscribe-to-notifications"></a>¿Cómo me suscribo a las notificaciones?
<a name="bk_notifoperations"> </a>

Según el tipo de suscripción que quieras crear, tienes varias opciones para elegir para suscribirte a las notificaciones.
  
**Cuadro 2. Operaciones y métodos de suscripción a las notificaciones**

|**Tipo de suscripción**|**Operación de EWS**|**Métodos de administración de la API de EWS**|**Lo que hace**|
|:-----|:-----|:-----|:-----|
|Transmisión  <br/> |[Operación de suscripción](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToStreamingNotifications method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToStreamingNotificationsOnAllFolders method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToStreamingNotificationsOnAllFolders method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> |Crea una solicitud para suscribirse a las notificaciones de transmisión  <br/> |
|Extracción  <br/> |[Operación de suscripción](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPullNotifications method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPullNotificationsOnAllFolders method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotifications method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotificationsOnAllFolders method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |Crea una solicitud para suscribirse a las notificaciones de extracción  <br/> |
|Inserción  <br/> |[Operación de suscripción](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPushNotifications overloaded method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPushNotificationsOnAllFolders overload method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPushNotifications overloaded method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPushNotificationsOnAllFolders overloaded method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |Crea una solicitud para suscribirse a las notificaciones de inserción  <br/> |
   
## <a name="how-do-i-get-ews-events"></a>¿Cómo consigo eventos de EWS?
<a name="bk_getevents"> </a>

Una vez creada la suscripción, la forma en que se envían los eventos actuales al cliente depende del tipo de suscripción. 
  
Para las notificaciones de transmisión, debe crearse una conexión de suscripción de transmisión y luego la suscripción se agrega a la conexión. [Puedes leer más sobre este proceso en Notificaciones de transmisión de eventos de buzón usando EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md). 
  
En el caso de las notificaciones de extracción, el objeto de la suscripción se inicializó cuando se creó la suscripción, por lo que sólo hay que llamar al método u operación **GetEvent** para recuperar los eventos del servidor. Puedes leer más acerca de esto en [Notificaciones sobre eventos de buzón de correo usando EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md). 
  
La siguiente tabla enumera las operaciones y clases necesarias para recuperar los eventos. 
  
**Cuadro 3. Elementos y clases para crear una conexión y obtener eventos**

|**Tipo de suscripción**|**Operación de EWS**|**Método de la API administrada de EWS**|**Lo que hace**|
|:-----|:-----|:-----|:-----|
|Transmisión  <br/> |[Operación GetStreamingEvents](https://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) <br/> |[StreamingSubscriptionConnection.AddSubscription method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.addsubscription%28v=exchg.80%29.aspx) <br/> |Crea una solicitud de colgado en el servidor, a la que se responde cuando se producen los eventos.  <br/> |
|Extracción  <br/> |[Operación GetEvents](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) <br/> |[PullSubscription.GetEvents method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) <br/> |Obtiene los eventos de notificación de extracción del servidor.  <br/> |
|Inserción  <br/> |No procede.  <br/> |No procede.  <br/> |Las notificaciones de inserción se envían automáticamente al receptor del servicio web (la URL de devolución de llamada especificada en la solicitud de suscripción). No es necesario recurrir a métodos u operaciones adicionales.  <br/> |
   
## <a name="how-do-i-unsubscribe-to-notifications"></a>¿Cómo puedo darme de baja de las notificaciones?
<a name="bk_notifunsubscribe"> </a>

En el siguiente cuadro se enumeran las formas en que puede darse de baja de cada tipo de suscripción.
  
**Cuadro 4. Operaciones y métodos para dar de baja las notificaciones**

|**Tipo de suscripción**|**EWS**|**API administrada EWS**||
|:-----|:-----|:-----|:-----|
|Transmisión  <br/> |[Operación Darse de baja](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[StreamingSubscription.BeginUnsubscribe method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.EndUnsubscribe method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.Unsubscribe method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|Extracción  <br/> |[Operación Darse de baja](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[PullSubscription.BeginUnsubscribe method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.EndUnsubscribe method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.Unsubscribe method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|Inserción  <br/> |Devolver **Darse de baja** en el elemento[ StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx) del [ SendNotificationResponseMessage](https://msdn.microsoft.com/library/2c6d681b-67ac-4331-bc6b-a2e709b638e3%28Office.15%29.aspx) <br/> |No procede. En vez de eso, deja que la suscripción caduque.  <br/> ||
   
Otra posibilidad es dejar que cada una de las suscripciones caduquen. 
  
**Cuadro 5. Caducidad de las suscripciones**

|**Tipo de suscripción**|**Valor de caducidad en el EWS**|**Valor de caducidad en la API administrada de EWS**|**Gestión de la caducidad**|
|:-----|:-----|:-----|:-----|
|Transmisión  <br/> |[ConnectionTimeout](https://msdn.microsoft.com/library/14da68a0-bcca-4281-a774-47644baa4ee9%28Office.15%29.aspx) elemento   <br/> | *duración* parámetro del [StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx) constructor  <br/> |Para la API administrada de EWS, después de que el valor de caducidad haya terminado el evento [OnDisconnect](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.ondisconnect%28v=exchg.80%29.aspx) se aumenta. Si no se recurre al método [StreamingSubscriptionConnection.Open](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.open%28v=exchg.80%29.aspx)la conexión se cierra.  <br/> Para EWS, después de que el valor de caducidad haya pasado, el mensaje [GetUserConfigurationResponse](https://msdn.microsoft.com/library/5e418c91-c836-4de0-a80d-f0dad0c684d7%28Office.15%29.aspx) devuelve un valor de [ConnectionStatus](https://msdn.microsoft.com/library/4300f9d6-8bf9-48c2-9f07-d80197864e17%28Office.15%29.aspx) de Closed.  <br/> |
|Extracción  <br/> |[Caducidad](https://msdn.microsoft.com/library/c2e1ca5a-6667-4f6f-aac4-89de33bddc54%28Office.15%29.aspx) elemento  <br/> | *caducidad* parámetro del método [SubscribeToPullNotification](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)  <br/> |Una vez que el valor de caducidad haya transcurrido, el servidor borra la suscripción.  <br/> |
|Inserción  <br/> |[StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx) elemento  <br/> | *frecuencia* parámetro de del método [SubscribeToPushNotification](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx)  <br/> |Si el servidor no recibe una respuesta a una notificación de inserción o a un ping de estado, vuelve a intentar enviar la notificación varias veces antes de dejar de enviar las notificaciones. Para obtener más información, vea: [StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)  <br/> |
   
## <a name="can-i-limit-subscriptions"></a>¿Puedo limitar las suscripciones?
<a name="bk_limitsubs"> </a>

En un despliegue local, se puede limitar el número de suscripciones por usuario con el parámetro de limitación de [EwsMaxSubscriptions.](ews-throttling-in-exchange.md) de la directiva de limitación. Esa directiva puede aplicarse a todos los usuarios o sólo a usuarios específicos. La directiva de limitación de **EwsMaxSubscriptions** no es configurable para Exchange Online. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_limitsubs"> </a>

- [Notificaciones de transmisión de eventos de buzón usando EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Notificaciones de extracción de eventos de buzón utilizando EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Mantener la afinidad entre un grupo de suscripciones y el servidor del buzón de Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [Manejo de errores relacionados con la notificación en EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
- [Referencia de servicios web para Exchange](../web-service-reference/web-services-reference-for-exchange.md)
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Sincronización del buzón y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
- [Solicitud de muestra de notificación de inserción](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)
    


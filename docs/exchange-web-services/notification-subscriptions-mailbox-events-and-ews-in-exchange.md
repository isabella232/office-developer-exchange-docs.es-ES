---
title: Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 76136f28-0dad-4ecc-9dd7-a45a1861e4b0
description: Obtenga información acerca de las suscripciones de notificación y eventos de buzón de correo en EWS en Exchange.
ms.openlocfilehash: 4f466c6cc01af410807948a9fec40c2af399c3e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763297"
---
# <a name="notification-subscriptions-mailbox-events-and-ews-in-exchange"></a>Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange

Obtenga información acerca de las suscripciones de notificación y eventos de buzón de correo en EWS en Exchange.
  
Puede usar la API administrada de EWS y la Exchange Web Services (EWS) para suscribirse para recibir notificaciones cuando se producen eventos en un buzón de correo o en una o varias de las carpetas en un buzón de correo. Existen tres tipos de suscripción: transmisión por secuencias de notificaciones, las notificaciones de extracción y notificaciones de inserción. Cada uno de estos tipos de suscripción utiliza diferentes técnicas para recibir o recuperar las notificaciones.
  
## <a name="getting-notifications---what-are-my-options"></a>Introducción a las notificaciones - ¿cuáles son las opciones de mi?
<a name="bk_notiftypes"> </a>

EWS incluye tres tipos de suscripción que funcionan de forma independiente para notificar al cliente de los cambios realizados en el servidor. Sin importar qué tipo de suscripción que elija, que tendrán acceso a todos los mismos eventos de notificación al final - es simplemente una cuestión de cómo obtenerlos.
  
**La tabla 1. Tipos de suscripción**

|**Opción**|**Descripción**|**¿Es adecuada para mí?**|
|:-----|:-----|:-----|
|Notificaciones de transmisión por secuencias  <br/> |Las notificaciones que se envían por el servidor a través de una conexión que queda abierto para un período de tiempo especificado.  <br/> |Por lo general se recomiendan las notificaciones de transmisión por secuencias para la mayoría de las aplicaciones. Son similares a las notificaciones de inserción y extracción y se ofrecen lo mejor de ambos mundos. Después de establecer la suscripción de notificación, la conexión permanece abierta para hasta 30 minutos permitir que al servidor las notificaciones de inserción al cliente. No es necesario para solicitar actualizaciones, como lo haría con una suscripción de extracción, y no tiene que crear una aplicación de agente de escucha de servicio web como lo haría con una suscripción de inserción.  <br/> |
|Notificaciones de extracción  <br/> |Notificaciones que se solicitó (o extraídas) por el cliente.  <br/> |Notificaciones de extracción son generalmente más adecuadas para los clientes de acoplamiento flexible, donde el cliente no confiable conectado a la red. Notificaciones de extracción pueden crear exceso de tráfico entre el cliente y el servidor debido a que el cliente está enviando solicitudes frecuentes en el servidor para recuperar las notificaciones y no todas las solicitudes de resultado en recuperar las notificaciones.  <br/> |
|Notificaciones de inserción  <br/> |Las notificaciones que se envían (o inserta) por el servidor a un cliente web de servicio a través de una dirección de devolución de llamada.  <br/> |Por lo general, las notificaciones de inserción proporcionan para menor latencia de notificación que las notificaciones de extracción y son adecuadas para los clientes acoplados a la que el servidor tiene un acceso confiable y el cliente es IP direccionable. Sin embargo, las notificaciones de inserción han quedado en desuso desde la llegada de transmisión por secuencias notificaciones en Exchange 2010. Si es posible, se recomienda que use las notificaciones de transmisión por secuencias en lugar de las notificaciones de inserción en el futuro. Notificaciones de inserción requieren que escribir una aplicación de agente de escucha, que es donde se envían las notificaciones a. Esto tiene una ligera ventaja sobre las notificaciones de extracción en que reduce el tráfico de cable, pero agrega sobrecarga exigiendo una aplicación independiente.  <br/> |
   
## <a name="what-ews-events-can-i-subscribe-to"></a>¿Qué eventos EWS ¿suscribirse a?
<a name="bk_eventtypes"> </a>

Definen los tipos de eventos EWS que los clientes suscribirse a la enumeración [EventType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx) para la API administrada de EWS o el elemento [EventType](http://msdn.microsoft.com/library/04b70f9e-c226-4130-958e-0db0275cf58b%28Office.15%29.aspx) de EWS. Los siguientes eventos EWS están disponibles para la suscripción: 
  
- NewMail — Llegó un nuevo mensaje en la Bandeja de entrada.
    
- Eliminados: Un mensaje era difícil elimina de la Bandeja de entrada. Para obtener más información acerca de las notificaciones de elementos eliminados, consulte [supresión de elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md) y [extraer las notificaciones de eventos de buzón de correo relacionados con la eliminación de EWS en Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md).
    
- Modificado: Se ha cambiado un elemento o carpeta.
    
- Mover: Un elemento o carpeta se ha movido. 
    
- Copiar: Se ha copiado un elemento o carpeta.
    
- Created: Se creó una carpeta o elemento. 
    
- FreeBusyChanged: Se ha cambiado la información de disponibilidad de un usuario.
    
Otro tipo de evento EWS, el evento de estado, se define mediante el elemento [EventType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx) , pero no suscribirse a este evento. En su lugar, se envía por el servidor para comprobar el estado del cliente para notificaciones de inserción y transmisión por secuencias. El cliente necesita responder a este evento necesidades o el cliente de tiempo de espera. 
  
Una acción de un usuario único a menudo da como resultado la creación de varias notificaciones. Para ilustrar esto, la siguiente ilustración muestra algunos escenarios comunes y las notificaciones que se crean para cada uno de ellos. Configuración de cliente tiene un impacto sobre las notificaciones recibidas, por lo que esto no es una lista exhaustiva de todas las opciones de configuración y notificaciones resultantes.
  
**En la figura 1. Tipos de eventos de suscripciones de notificación**

![Tabla que muestra las notificaciones enviadas en escenarios de usuario comunes, como recibir nuevo correo, crear una nueva carpeta, mover una carpeta, etc.](media/Exchange2013_Notifications_Events.png)
  
En la figura 1 se simplifica el proceso de notificación. En realidad, se pueden crear varias notificaciones (incluso varias notificaciones del mismo tipo) para una acción de usuario único. Por ejemplo, en el caso de una operación de movimiento de carpeta, se crean tres eventos de carpeta: uno para la carpeta que se está modificando, uno para la carpeta principal antigua y otro para la nueva carpeta principal. Debido a que numerosos eventos pueden desencadenarse para una sola operación, se recomienda [crear un tiempo de espera de unos segundos en las operaciones de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices), poder sincronizar solo cuando la acción se haya completado, en lugar de mitad a través de la operación.
  
También es importante tener en cuenta que las opciones de configuración que cada usuario elige afectará a qué notificaciones se crean. Por ejemplo, los datos de disponibilidad gratuita algunos usuarios se actualizan automáticamente y se crea el evento FreeBusyChanged cuando se recibe una nueva convocatoria de reunión, incluso antes de que han leído el elemento. Para otros usuarios, no se actualicen los datos de disponibilidad gratuitos y no se crea el evento FreeBusyChanged hasta después de que se ha aceptado la reunión. Esta configuración puede tener un impacto considerable en las notificaciones creadas por el servidor.
  
## <a name="how-do-ews-notifications-work"></a>¿Cómo funcionan las notificaciones de EWS?
<a name="bk_howwork"> </a>

Notificaciones de EWS se administran según la suscripción. Normalmente, no hay una sola suscripción por buzón de correo y, dentro de la suscripción de buzón de correo puede suscribirse a algunas o todas las carpetas. Decidir qué tipo de notificación para suscribirse a (transmisión por secuencias, extracción o inserción) y qué tipo de eventos que le gustaría recibir (NewMail, creado, Deleted, Modified, etc.) y, a continuación, se crea una suscripción. Los eventos EWS se envían asincrónicamente desde el servidor de buzón de correo para el cliente. (Lección historial: eventos son sincrónicos en Exchange 2007 - y eventos están almacenados en el servidor de acceso de cliente de Exchange 2010, pero no hay más!).
  
Según el tipo de suscripción que tiene, pueden variar las maneras en que las notificaciones se envían al cliente. En esta sección se describe con más detalle cómo funciona cada tipo de suscripción.
  
### <a name="ews-streaming-notifications"></a>Notificaciones de transmisión por secuencias de EWS
<a name="bk_streamnotif"> </a>

Notificaciones de transmisión por secuencias se basan en una francesa solicitud get en el servidor para mantener una conexión de suscripción transmisiones abiertas, para que los eventos que se producen mientras la conexión está activa se transmiten inmediatamente al cliente. Varias notificaciones se pueden enviar en el transcurso de una sola conexión y la conexión se mantiene abierto hasta que expire el intervalo, o para un máximo de 30 minutos. Una vez que expire la conexión, el cliente envía el francesa nuevamente la solicitud get. La figura 2 se muestra cómo funcionan la transmisión por secuencias de suscripciones y transmisión por secuencias de notificaciones.
  
**La figura 2. Introducción a la notificación transmisión por secuencias**

![Ilustración que muestra cómo funcionan las notificaciones de streaming. Para configurar las notificaciones de streaming: 1. Suscribirse, 2. Abrir conexión, 3. Esperar eventos, 4. Recibir eventos, repetir 3 y 4, 5. Cerrar o mantener conexión, 6. Cancelar suscripción o agotar tiempo de espera.](media/Exchange2013_Notifications_StreamSub.png)
  
Para obtener información sobre la creación de notificaciones de transmisión por secuencias, vea [notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md).
  
### <a name="ews-pull-notifications"></a>Notificaciones de extracción EWS
<a name="bk_pullnotif"> </a>

Notificaciones de extracción se basan en el cliente solicitan las notificaciones en un intervalo que administra el cliente. Esto puede producir respuestas GetEvents con ninguna notificación. La figura 3 muestra cómo funcionan las suscripciones de extracción y notificaciones de extracción.
  
**La figura 3. Información general de notificación de extracción**

![Ilustración que muestra cómo funcionan las notificaciones de extracción. Para configurar las notificaciones de extracción: 1. Suscribirse, 2. Enviar GetEvents, 3. Recibir respuesta, repetir 2 y 3, 4. Cerrar o mantener conexión, 5. Cancelar suscripción o agotar tiempo de espera.](media/Exchange2013_Notifications_PullSub.png)
  
Para obtener información sobre la creación de notificaciones de extracción, ven [las notificaciones de extracción acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).
  
### <a name="ews-push-notifications"></a>Notificaciones de inserción EWS
<a name="bk_pushnotif"> </a>

Notificaciones de inserción se basan en el servidor de inserción de las notificaciones de vuelta al cliente. No hay únicamente el tráfico si no hay una notificación. La figura 4 muestra cómo funcionan las suscripciones de inserción y las notificaciones de inserción.
  
**La figura 4. Información general de notificación de inserción**

![Ilustración que muestra cómo funcionan las notificaciones de inserción. Para configurar las notificaciones de inserción: 1. Crear agente de escucha, 2. Suscribirse, 3. Esperar eventos, 4. Recibir eventos, 5. Enviar respuesta "OK", repetir 3, 4 y 5, 6. Cancelar suscripción o agotar tiempo de espera.](media/Exchange2013_Notifications_PushSub.png)
  
Si está utilizando [las notificaciones de inserción con Exchange 2010](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx), considere la posibilidad de actualización de la aplicación para [usar notificaciones de transmisión por secuencias](http://code.msdn.microsoft.com/exchange/Exchange-2013-Set-push-82738cc5), por lo que no necesita una aplicación independiente para recibir los eventos.
  
## <a name="how-do-i-subscribe-to-notifications"></a>¿Cómo suscribirse a las notificaciones?
<a name="bk_notifoperations"> </a>

Según el tipo de suscripción que le gustaría crear, tiene un número de opciones que puede elegir para suscribirse a las notificaciones.
  
**Tabla 2. Operaciones y los métodos para suscribirse a las notificaciones**

|**Tipo de suscripción**|**Operación de EWS**|**Métodos de la API administrada de EWS**|**Para qué sirve**|
|:-----|:-----|:-----|:-----|
|Transmisión por secuencias  <br/> |[Operación de suscripción](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToStreamingNotifications (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToStreamingNotificationsOnAllFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToStreamingNotificationsOnAllFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> |Crea una solicitud para suscribirse a las notificaciones de transmisión.  <br/> |
|Extracción  <br/> |[Operación de suscripción](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPullNotifications (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPullNotificationsOnAllFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotifications (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotificationsOnAllFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |Crea una solicitud para suscribirse a las notificaciones de extracción.  <br/> |
|Inserción  <br/> |[Operación de suscripción](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPushNotifications sobrecargado (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [Sobrecarga de ExchangeService.BeginSubscribeToPushNotificationsOnAllFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPushNotifications sobrecargado (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPushNotificationsOnAllFolders sobrecargado (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |Crea una solicitud para suscribirse a las notificaciones de inserción.  <br/> |
   
## <a name="how-do-i-get-ews-events"></a>¿Cómo se puede obtener eventos EWS?
<a name="bk_getevents"> </a>

Una vez creada la suscripción, la manera en que los eventos reales se envían al cliente depende del tipo de suscripción. 
  
Para la transmisión de las notificaciones, debe crearse una conexión de suscripción de transmisión por secuencias y, a continuación, se agrega la suscripción a la conexión. Puede leer más información acerca de este proceso en [las notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md). 
  
Para las notificaciones de extracción, suscripción se inicializó el objeto cuando se creó la suscripción, por lo que debe llamar a la operación para recuperar los eventos desde el servidor o **GetEvent** (método). Puede leer más información acerca de este en [extraer las notificaciones sobre los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md). 
  
En la siguiente tabla se enumera las operaciones y las clases requeridas para recuperar los eventos. 
  
**Tabla 3. Elementos y clases para crear una conexión y obtención de eventos**

|**Tipo de suscripción**|**Operación de EWS**|**Método de la API administrada de EWS**|**Para qué sirve**|
|:-----|:-----|:-----|:-----|
|Transmisión por secuencias  <br/> |[Operación GetStreamingEvents](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) <br/> |[StreamingSubscriptionConnection.AddSubscription (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.addsubscription%28v=exchg.80%29.aspx) <br/> |Crea un francesa solicitud get en el servidor, que se ha respondido a cuando se produzcan eventos.  <br/> |
|Extracción  <br/> |[Operación GetEvents](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) <br/> |[PullSubscription.GetEvents (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) <br/> |Obtiene los eventos de notificación de extracción desde el servidor.  <br/> |
|Inserción  <br/> |No es aplicable.  <br/> |No es aplicable.  <br/> |Notificaciones de inserción se envían automáticamente a la escucha de servicios web (la URL de devolución de llamada especificada en la solicitud de suscripción). No hay métodos adicionales o las operaciones deben llamarse.  <br/> |
   
## <a name="how-do-i-unsubscribe-to-notifications"></a>¿Cómo puedo cancelar la suscripción a las notificaciones?
<a name="bk_notifunsubscribe"> </a>

En la siguiente tabla se enumera las maneras en que puede cancelar la suscripción a cada tipo de suscripción.
  
**Tabla 4. Operaciones y métodos para anular la suscripción a las notificaciones**

|**Tipo de suscripción**|**EWS**|**API administrada EWS**||
|:-----|:-----|:-----|:-----|
|Transmisión por secuencias  <br/> |[Cancelar la operación de suscripción](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[StreamingSubscription.BeginUnsubscribe (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.EndUnsubscribe (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.Unsubscribe (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|Extracción  <br/> |[Cancelar la operación de suscripción](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[PullSubscription.BeginUnsubscribe (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.EndUnsubscribe (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.Unsubscribe (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|Inserción  <br/> |Devolver la **cancelación de la suscripción** en el elemento [StatusFrequency](http://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx) de la [SendNotificationResponseMessage](http://msdn.microsoft.com/library/2c6d681b-67ac-4331-bc6b-a2e709b638e3%28Office.15%29.aspx) <br/> |No es aplicable. Permitir que el tiempo de espera de suscripción en su lugar.  <br/> ||
   
Como alternativa, puede dejar que cada una de las suscripciones de tiempo de espera. 
  
**Tabla 5. Tiempos de espera de suscripción**

|**Tipo de suscripción**|**Valor de tiempo de espera en EWS**|**Valor de tiempo de espera en la API administrada de EWS**|**Control de tiempo de espera**|
|:-----|:-----|:-----|:-----|
|Transmisión por secuencias  <br/> |Elemento [ConnectionTimeout](http://msdn.microsoft.com/library/14da68a0-bcca-4281-a774-47644baa4ee9%28Office.15%29.aspx)  <br/> | parámetro de *duración* del constructor [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)  <br/> |Para la API administrada de EWS, después transcurre el valor de tiempo de espera, se produce el evento [OnDisconnect](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.ondisconnect%28v=exchg.80%29.aspx) . Si no se llama al método de [StreamingSubscriptionConnection.Open](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.open%28v=exchg.80%29.aspx) , se cierra la conexión.  <br/> Para EWS, después transcurre el valor de tiempo de espera, el mensaje [GetUserConfigurationResponse](http://msdn.microsoft.com/library/5e418c91-c836-4de0-a80d-f0dad0c684d7%28Office.15%29.aspx) devuelve un valor de [ConnectionStatus](http://msdn.microsoft.com/library/4300f9d6-8bf9-48c2-9f07-d80197864e17%28Office.15%29.aspx) de cerrado.  <br/> |
|Extracción  <br/> |[Tiempo de espera de](http://msdn.microsoft.com/library/c2e1ca5a-6667-4f6f-aac4-89de33bddc54%28Office.15%29.aspx) elemento  <br/> | parámetro de *tiempo de espera* del método [SubscribeToPullNotification](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)  <br/> |Una vez transcurrido el valor de tiempo de espera, el servidor elimina la suscripción.  <br/> |
|Inserción  <br/> |Elemento [StatusFrequency](http://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)  <br/> | *frecuencia de* parámetro del método [SubscribeToPushNotification](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx)  <br/> |Si el servidor no recibe una respuesta a una notificación de inserción o ping de estado, vuelve a intentar enviar la notificación de varias veces antes de deje de enviar las notificaciones. Para obtener más información, vea [StatusFrequency](http://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx).  <br/> |
   
## <a name="can-i-limit-subscriptions"></a>¿Puede limitar las suscripciones?
<a name="bk_limitsubs"> </a>

En una implementación local, puede limitar el número de suscripciones por usuario con el [parámetro de limitación de peticiones de EwsMaxSubscriptions](ews-throttling-in-exchange.md) de la directiva de limitación. Que la directiva se puede aplicar a todos los usuarios o sólo determinados usuarios. El **EwsMaxSubscriptions** directiva de limitación no es configurable para Exchange Online. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_limitsubs"> </a>

- [Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [Tratamiento de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Ver también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
- [Referencia de servicios Web de Exchange](../web-service-reference/web-services-reference-for-exchange.md)
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Sincronización de buzón de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
- [Aplicación de ejemplo de notificación de inserción](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)
    


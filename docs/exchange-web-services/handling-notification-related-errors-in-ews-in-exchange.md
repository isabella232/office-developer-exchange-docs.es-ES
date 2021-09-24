---
title: Manejo de errores relacionados con la notificación en EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 519e1e52-5f1f-4f06-931e-8c20a586a563
description: Descubra cómo controlar errores relacionados con notificaciones en aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 7b49a57b7236318e08cb70ac2ac00edc4cf86363
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520216"
---
# <a name="handling-notification-related-errors-in-ews-in-exchange"></a>Manejo de errores relacionados con la notificación en EWS in Exchange

Descubra cómo controlar errores relacionados con notificaciones en aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.

Si la aplicación se suscribe y recibe notificaciones, es posible que tenga que controlar los errores relacionados con las notificaciones. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS.

**Tabla 1. Errores relacionados con notificaciones y cómo controlarlos**

|Error|Se produce cuando se intenta...|Controlarla por...|
|:-----|:-----|:-----|
|**ErrorExceededConnectionCount** |Abra una conexión para obtener eventos cuando la cuenta alcanzó el límite de conexión de las conexiones de streaming abiertas. | <ul><li>Usar [la suplantación](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) para [abrir conexiones](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</li><li>Usar menos conexiones para obtener eventos. Maximice el número de [](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md) suscripciones en cada conexión mediante afinidad y colocando un máximo de [200](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain)identificadores de suscripción en el mismo grupo . A continuación, puede usar la misma conexión para recuperar eventos para todo el grupo, lo que reduce el número de conexiones necesarias.</li><li>  Cambiar el valor de HangingConnectionLimit en el archivo web.config para Exchange local para invalidar el valor predeterminado de tres conexiones abiertas. Exchange Online tiene un valor predeterminado HangingConnectionLimit de 10, que no se puede configurar.</li></ul> |
|**ErrorExceededSubscriptionCount** |Crear demasiadas suscripciones. El parámetro de directiva de limitación [EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) determina el número máximo de suscripciones que puede crear una cuenta. | <ul><li>Usar [la suplantación](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) para [crear suscripciones](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</li><li>Reducción del número de suscripciones.</li></ul> |
|**ErrorInvalidSubscriptionRequest** |Cree suscripciones para varios buzones o varias carpetas desde una sola solicitud.  |Crear una suscripción para una sola carpeta pública o un único buzón en una sola solicitud.|
|**ErrorInvalidWatermark** |Obtener eventos mediante una marca de agua no válida.| <ul><li>Comprobar el identificador de suscripción devuelto en una respuesta anterior.</li><li>Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</li><li>[Creación de una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</li></ul> |
|**ErrorMissedNotificationEvents** |Obtener eventos cuando se han perdido algunos eventos anteriores.   |Comparar las propiedades de carpeta extendida **PR_LOCAL_COMMIT_TIME_MAX** (0x670a) y **PR_DELETED_COUNT_TOTAL** (0x670b) para determinar qué cambios se han perdido y crear una [nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).  |
|**ErrorProxyRequestNotAllowed** |Suscribirse a eventos para un usuario en una solicitud por lotes cuyo buzón se ha movido a otro sitio.   |Usar [Detección automática](autodiscover-for-exchange.md) para redescubrir ExternalEwsUrl o EwsPartnerUrl y crear una nueva suscripción.  |
|**ErrorReadEventsFailed** |Obtener eventos de una suscripción que no se encuentra.  |Usar [Detección automática](autodiscover-for-exchange.md) para redescubrir ExternalEwsUrl o EwsPartnerUrl y crear una nueva suscripción.  |
|**ErrorServerBusy** | Exceder [los límites de limitación.](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) Tenga en cuenta lo siguiente con respecto a la limitación:<ul><li>El límite de limitación [ewsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) identifica el número máximo de suscripciones de notificaciones de inserción, extracción o streaming que pueden estar activas al mismo tiempo. Este es el valor de las suscripciones de buzones de correo, no el número de suscripciones a carpetas individuales en una suscripción de buzón. A partir de las versiones 14.16.0135 y 14.15.0057.000 del buzón de servicio, un buzón hospedado por Exchange Online o Exchange Online como parte de Office 365 puede tener hasta 20 suscripciones y un buzón local de Exchange de destino de 2013 puede tener hasta 5000 suscripciones.</li><li>El límite de limitación [ewsMaxConcurrency](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx) identifica el número máximo de solicitudes activas para las conexiones que no son de streaming y tiene un valor predeterminado de 27.</li><li>El límite predeterminado para las conexiones de streaming abiertas es de diez.</li></ul> |<ul><li>[Teniendo en cuenta](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) las implicaciones de las directivas de limitación relacionadas con la notificación y limitando el número de suscripciones activas y conexiones activas para que la aplicación no se limite.</li><li>Usar menos conexiones para obtener eventos. Maximice el número de suscripciones en cada conexión colocando un máximo de [200](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)identificadores de suscripción en el mismo grupo . A continuación, puede usar la misma conexión para recuperar eventos para todo el grupo, lo que reduce el número de conexiones necesarias.</li><li>Cambiar el valor de HangingConnectionLimit en el archivo web.config para invalidar el valor predeterminado de diez conexiones de streaming abiertas.</li></ul>|
|**ErrorSubscriptionNotFound** |Obtener eventos para una suscripción que no se encuentra. Es posible que la suscripción haya expirado, que se haya reiniciado el proceso ews o que se haya pasado una suscripción no válida. | <ul><li>Comprobar que está usando el mismo identificador de suscripción que se devolvió en una respuesta anterior.</li><li>Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</li><li> [Creación de una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</li></ul> |
|**[ServiceLocalException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |Agregue una suscripción a una nueva carpeta mientras se abre una conexión de suscripción en otra carpeta.  |Cambiar la suscripción para suscribirse a todas las carpetas del buzón, en lugar de una carpeta específica.  |
|**[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |Obtener eventos para una suscripción que no se puede encontrar en el Exchange local.  | <ul><li>Comprobar que está usando el mismo identificador de suscripción que se devolvió en una respuesta anterior.</li><li>Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</li></ul> |

## <a name="recovering-from-lost-subscriptions"></a>Recuperación de suscripciones perdidas
<a name="bk_recover"> </a>

Cuando se pierde una suscripción o ya no se puede acceder a ella, lo mejor es crear una nueva suscripción y no incluir la marca de agua antigua en la nueva suscripción. Volver a suscribirse con la marca de agua antigua provoca un examen lineal de eventos, lo que es costoso. En su lugar, cree una nueva suscripción y compare las propiedades de la carpeta para buscar los cambios de contenido que se produjeron entre la suscripción perdida y la nueva suscripción. Las propiedades de carpeta extendida que  se recomienda comprobar son PR_LOCAL_COMMIT_TIME_MAX (0x670a0040) y **PR_DELETED_COUNT_TOTAL** (0x670b0003). Para ello, cree [una definición de propiedad extendida](properties-and-extended-properties-in-ews-in-exchange.md).

## <a name="see-also"></a>Ver también

- [Suscripciones de notificación, eventos de buzón, y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [Notificaciones de transmisión de eventos de buzón usando EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Notificaciones de extracción de eventos de buzón utilizando EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Mantener la afinidad entre un grupo de suscripciones y el servidor del buzón de Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)



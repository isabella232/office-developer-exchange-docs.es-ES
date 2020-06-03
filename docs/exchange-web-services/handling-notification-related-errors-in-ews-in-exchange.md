---
title: Control de errores relacionados con la notificación en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 519e1e52-5f1f-4f06-931e-8c20a586a563
description: Descubra cómo controlar los errores relacionados con notificaciones en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 60edb1344e6b0499ef6d2ed2aefaebde723b42cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528317"
---
# <a name="handling-notification-related-errors-in-ews-in-exchange"></a>Control de errores relacionados con la notificación en EWS en Exchange

Descubra cómo controlar los errores relacionados con notificaciones en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.

Si la aplicación se suscribe a y recibe notificaciones, es posible que deba controlar los errores relacionados con la notificación. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS.

**Tabla 1. Errores relacionados con la notificación y cómo controlarlos**

|Error|Se produce cuando se intenta...|Controlarla por...|
|:-----|:-----|:-----|
|**ErrorExceededConnectionCount** |Abra una conexión para obtener eventos cuando la cuenta ha alcanzado el límite de conexión de conexiones de transmisión abierta. | <ul><li>Uso de la [suplantación](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) para [abrir conexiones](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</li><li>Uso de menos conexiones para obtener eventos. Maximice el número de suscripciones en cada conexión mediante la [afinidad](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md) y [colocando un máximo de 200 identificadores de suscripción en el mismo grupo](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain). A continuación, puede usar la misma conexión para recuperar eventos para todo el grupo, lo que reduce el número de conexiones necesarias.</li><li>  Cambiar el valor de HangingConnectionLimit en el archivo Web. config de Exchange local para reemplazar el valor predeterminado de tres conexiones abiertas. Exchange Online tiene una HangingConnectionLimit predeterminada de 10, que no se puede configurar.</li></ul> |
|**ErrorExceededSubscriptionCount** |Cree demasiadas suscripciones. El parámetro de la Directiva de limitación [EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) determina el número máximo de suscripciones que puede crear una cuenta. | <ul><li>Uso de la [suplantación](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) para [crear suscripciones](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</li><li>Reducir el número de suscripciones.</li></ul> |
|**ErrorInvalidSubscriptionRequest** |Cree suscripciones para varios buzones o varias carpetas de una sola solicitud.  |Crear una suscripción para una sola carpeta pública o un único buzón de correo en una única solicitud.|
|**ErrorInvalidWatermark** |Obtener eventos con una marca de agua no válida.| <ul><li>Comprobando el identificador de suscripción devuelto en una respuesta anterior.</li><li>Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</li><li>[Crear una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</li></ul> |
|**ErrorMissedNotificationEvents** |Obtener eventos cuando se omitieron algunos eventos anteriores.   |Comparación de las propiedades de la carpeta extendida **PR_LOCAL_COMMIT_TIME_MAX** (0x670a) y **PR_DELETED_COUNT_TOTAL** (0x670b) para determinar qué cambios se han perdido y [crear una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).  |
|**ErrorProxyRequestNotAllowed** |Suscribirse a los eventos de un usuario en una solicitud por lotes cuyo buzón se haya movido a otro sitio.   |Usar la [detección automática](autodiscover-for-exchange.md) para volver a detectar ExternalEwsUrl o EwsPartnerUrl y crear una nueva suscripción.  |
|**ErrorReadEventsFailed** |Obtener eventos de una suscripción que no se encuentra.  |Usar la [detección automática](autodiscover-for-exchange.md) para volver a detectar ExternalEwsUrl o EwsPartnerUrl y crear una nueva suscripción.  |
|**ErrorServerBusy** | Superar los límites de [limitación](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) . Tenga en cuenta lo siguiente con respecto a la limitación:<ul><li>El límite de limitación [EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) identifica el número máximo de suscripciones de notificación de inserción, extracción o transmisión que pueden estar activas al mismo tiempo. Este es el valor de las suscripciones a buzones de correo, no el número de suscripciones de carpeta individual en una suscripción de buzón. A partir de las versiones de buzones de servicio versiones 14.16.0135 y 14.15.0057.000, un buzón de correo hospedado por Exchange online o Exchange online como parte de Office 365 puede tener hasta 20 suscripciones y un buzón local de Exchange 2013 de destino puede tener hasta 5000 suscripciones.</li><li>El límite de limitación [EwsMaxConcurrency](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx) identifica el número máximo de solicitudes activas para conexiones sin transmisión por secuencias y tiene un valor predeterminado de 27.</li><li>El límite predeterminado para las conexiones de streaming abiertas es diez.</li></ul> |<ul><li>Tener en cuenta [las implicaciones de las directivas de limitación relacionadas con notificaciones](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) y limitar el número de suscripciones activas y conexiones activas para que no se limite la aplicación.</li><li>Uso de menos conexiones para obtener eventos. Maximice el número de suscripciones en cada conexión [colocando un máximo de 200 identificadores de suscripción en el mismo grupo](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md). A continuación, puede usar la misma conexión para recuperar eventos para todo el grupo, lo que reduce el número de conexiones necesarias.</li><li>Cambiar el valor de HangingConnectionLimit en el archivo Web. config para invalidar el valor predeterminado de diez conexiones de transmisión por secuencias abiertas.</li></ul>|
|**ErrorSubscriptionNotFound** |Obtener eventos para una suscripción que no se encuentra. Es posible que la suscripción haya expirado, que se haya reiniciado el proceso EWS o que se haya pasado una suscripción no válida. | <ul><li>Comprobando que está usando el mismo identificador de suscripción que se ha devuelto en una respuesta anterior.</li><li>Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</li><li> [Crear una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</li></ul> |
|**[ServiceLocalException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |Agregar una suscripción a una carpeta nueva mientras una conexión de suscripción está abierta en otra carpeta.  |Cambiar la suscripción para suscribirse a todas las carpetas del buzón, en lugar de a una carpeta específica.  |
|**[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |Obtener eventos para una suscripción que no se encuentra en el almacén de Exchange.  | <ul><li>Comprobando que está usando el mismo identificador de suscripción que se ha devuelto en una respuesta anterior.</li><li>Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</li></ul> |

## <a name="recovering-from-lost-subscriptions"></a>Recuperación de suscripciones perdidas
<a name="bk_recover"> </a>

Cuando se pierde una suscripción, o porque ya no se puede obtener acceso a ella, es mejor crear una nueva suscripción y no incluir la antigua marca de agua en la nueva suscripción. Resubscribing con la marca de agua antigua causa un análisis lineal de los eventos, lo que es costoso. En su lugar, cree una nueva suscripción y compare las propiedades de la carpeta para buscar los cambios de contenido que se produjeron entre la suscripción perdida y la nueva suscripción. Las propiedades de carpeta extendida que se recomienda comprobar son **PR_LOCAL_COMMIT_TIME_MAX** (0x670a0040) y **PR_DELETED_COUNT_TOTAL** (0x670b0003). Para ello, [cree una definición de propiedad extendida](properties-and-extended-properties-in-ews-in-exchange.md).

## <a name="see-also"></a>Vea también

- [Suscripciones de notificación, eventos de buzón y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [Notificaciones de secuencia sobre eventos de buzón de correo mediante EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Extraer notificaciones sobre eventos de buzón de correo mediante EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo de Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)



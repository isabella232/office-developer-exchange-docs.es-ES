---
title: Tratamiento de errores relacionados con la notificación en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 519e1e52-5f1f-4f06-931e-8c20a586a563
description: Encuentre información acerca de cómo tratar los errores relacionados con la notificación en aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: cb0c16a74e68b5a16ef0f2011f65b22675950f58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763013"
---
# <a name="handling-notification-related-errors-in-ews-in-exchange"></a><span data-ttu-id="d2363-103">Tratamiento de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2363-103">Handling notification-related errors in EWS in Exchange</span></span>

<span data-ttu-id="d2363-104">Encuentre información acerca de cómo tratar los errores relacionados con la notificación en aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2363-104">Find out how to handle notification-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d2363-105">Si la aplicación se suscribe a y obtiene notificaciones, debe controlar los errores relacionados con la notificación.</span><span class="sxs-lookup"><span data-stu-id="d2363-105">If your application subscribes to and gets notifications, you might have to handle notification-related errors.</span></span> <span data-ttu-id="d2363-106">Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS.</span><span class="sxs-lookup"><span data-stu-id="d2363-106">You can handle these errors at runtime, or while you are developing your EWS application.</span></span>
  
<span data-ttu-id="d2363-107">**La tabla 1. Los errores relacionados con la notificación y cómo controlarlos**</span><span class="sxs-lookup"><span data-stu-id="d2363-107">**Table 1. Notification-related errors and how to handle them**</span></span>

|<span data-ttu-id="d2363-108">Error</span><span class="sxs-lookup"><span data-stu-id="d2363-108">Error</span></span>|<span data-ttu-id="d2363-109">Se produce al intentar...</span><span class="sxs-lookup"><span data-stu-id="d2363-109">Occurs when you try to…</span></span>|<span data-ttu-id="d2363-110">Controlarla por...</span><span class="sxs-lookup"><span data-stu-id="d2363-110">Handle it by…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2363-111">**ErrorExceededConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="d2363-111">**ErrorExceededConnectionCount**</span></span> |<span data-ttu-id="d2363-112">Abrir una conexión para obtener eventos cuando la cuenta alcanza su límite de conexión de abrir conexiones de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="d2363-112">Open a connection to get events when the account reached its connection limit of open streaming connections.</span></span> | <ul><li><span data-ttu-id="d2363-113">Usar [suplantación](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) para [Abrir conexiones](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</span><span class="sxs-lookup"><span data-stu-id="d2363-113">Using [impersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) to [open connections](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</span></span></li><li><span data-ttu-id="d2363-114">Uso de menos conexiones para obtener eventos.</span><span class="sxs-lookup"><span data-stu-id="d2363-114">Using fewer connections to get events.</span></span> <span data-ttu-id="d2363-115">Maximizar el número de suscripciones en cada conexión [con afinidad](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md) y [colocar un máximo de 200 suscripción identificadores en el mismo grupo](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain).</span><span class="sxs-lookup"><span data-stu-id="d2363-115">Maximize the number of subscriptions in each connection by [using affinity](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md) and [placing a maximum of 200 subscription IDs in the same group](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain).</span></span> <span data-ttu-id="d2363-116">A continuación, puede usar la misma conexión para recuperar los eventos para todo el grupo, reduciendo el número de conexiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="d2363-116">You can then use the same connection to retrieve events for the entire group, reducing the number of connections required.</span></span></li><li>  <span data-ttu-id="d2363-117">Cambiar el valor de la HangingConnectionLimit en el archivo web.config para Exchange local para invalidar el valor predeterminado de tres conexiones abiertas.</span><span class="sxs-lookup"><span data-stu-id="d2363-117">Changing the value of the HangingConnectionLimit in the web.config file for Exchange on-premises to override the default value of three open connections.</span></span> <span data-ttu-id="d2363-118">Exchange Online tiene un valor predeterminado de HangingConnectionLimit de 10, lo cual no es configurable.</span><span class="sxs-lookup"><span data-stu-id="d2363-118">Exchange Online has a default HangingConnectionLimit of 10, which is not configurable.</span></span></li></ul> |
|<span data-ttu-id="d2363-119">**ErrorExceededSubscriptionCount**</span><span class="sxs-lookup"><span data-stu-id="d2363-119">**ErrorExceededSubscriptionCount**</span></span> |<span data-ttu-id="d2363-120">Crear demasiadas suscripciones.</span><span class="sxs-lookup"><span data-stu-id="d2363-120">Create too many subscriptions.</span></span> <span data-ttu-id="d2363-121">El [EwsMaxSubscriptions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) parámetro de la directiva de limitación determina el número máximo de suscripciones que puede crear una cuenta.</span><span class="sxs-lookup"><span data-stu-id="d2363-121">The [EwsMaxSubscriptions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) throttling policy parameter determines the maximum number of subscriptions that an account can create.</span></span> | <ul><li><span data-ttu-id="d2363-122">Usar [suplantación](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) para [crear las suscripciones](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</span><span class="sxs-lookup"><span data-stu-id="d2363-122">Using [impersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) to [create subscriptions](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</span></span></li><li><span data-ttu-id="d2363-123">Reducir el número de suscripciones.</span><span class="sxs-lookup"><span data-stu-id="d2363-123">Reducing the number of subscriptions.</span></span></li></ul> |
|<span data-ttu-id="d2363-124">**ErrorInvalidSubscriptionRequest**</span><span class="sxs-lookup"><span data-stu-id="d2363-124">**ErrorInvalidSubscriptionRequest**</span></span> |<span data-ttu-id="d2363-125">Creación de suscripciones para varios buzones de correo o varias carpetas desde una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2363-125">Create subscriptions for multiple mailboxes or multiple folders from a single request.</span></span>  |<span data-ttu-id="d2363-126">Creación de una suscripción para una única carpeta pública o un solo buzón en una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2363-126">Creating a subscription for a single public folder or a single mailbox in a single request.</span></span>| 
|<span data-ttu-id="d2363-127">**ErrorInvalidWatermark**</span><span class="sxs-lookup"><span data-stu-id="d2363-127">**ErrorInvalidWatermark**</span></span> |<span data-ttu-id="d2363-128">Obtener eventos mediante el uso de una marca de agua no válido.</span><span class="sxs-lookup"><span data-stu-id="d2363-128">Get events by using an invalid watermark.</span></span>| <ul><li><span data-ttu-id="d2363-129">El identificador de suscripción de comprobación devueltos en una respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="d2363-129">Checking the subscription ID returned in a previous response.</span></span></li><li><span data-ttu-id="d2363-130">Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</span><span class="sxs-lookup"><span data-stu-id="d2363-130">Ensuring that you're sending the subscription ID for the correct **ExchangeService** object.</span></span></li><li><span data-ttu-id="d2363-131">[Crear una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</span><span class="sxs-lookup"><span data-stu-id="d2363-131">[Creating a new subscription](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</span></span></li></ul> |
|<span data-ttu-id="d2363-132">**ErrorMissedNotificationEvents**</span><span class="sxs-lookup"><span data-stu-id="d2363-132">**ErrorMissedNotificationEvents**</span></span> |<span data-ttu-id="d2363-133">Obtener eventos cuando se hayan perdido algunos eventos anteriores.</span><span class="sxs-lookup"><span data-stu-id="d2363-133">Get events when some previous events were missed.</span></span>   |<span data-ttu-id="d2363-134">Comparación de las propiedades de carpeta extendida **PR_LOCAL_COMMIT_TIME_MAX** (0x670a) y **PR_DELETED_COUNT_TOTAL** (0x670b) para determinar los cambios que no se revisó y [crear una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</span><span class="sxs-lookup"><span data-stu-id="d2363-134">Comparing the extended folder properties **PR_LOCAL_COMMIT_TIME_MAX** (0x670a) and **PR_DELETED_COUNT_TOTAL** (0x670b) to determine what changes were missed, and [creating a new subscription](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</span></span>  |
|<span data-ttu-id="d2363-135">**ErrorProxyRequestNotAllowed**</span><span class="sxs-lookup"><span data-stu-id="d2363-135">**ErrorProxyRequestNotAllowed**</span></span> |<span data-ttu-id="d2363-136">Suscribirse a eventos para un usuario en una solicitud por lotes cuyo buzón de correo se ha movido a otro sitio.</span><span class="sxs-lookup"><span data-stu-id="d2363-136">Subscribe to events for a user in a batched request whose mailbox has moved to another site.</span></span>   |<span data-ttu-id="d2363-137">Uso de [detección automática](autodiscover-for-exchange.md) para volver a descubrir la ExternalEwsUrl o EwsPartnerUrl y crear una nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="d2363-137">Using [Autodiscover](autodiscover-for-exchange.md) to rediscover the ExternalEwsUrl or EwsPartnerUrl, and creating a new subscription.</span></span>  |
|<span data-ttu-id="d2363-138">**ErrorReadEventsFailed**</span><span class="sxs-lookup"><span data-stu-id="d2363-138">**ErrorReadEventsFailed**</span></span> |<span data-ttu-id="d2363-139">Obtener eventos de una suscripción a que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="d2363-139">Get events from a subscription that cannot be found.</span></span>  |<span data-ttu-id="d2363-140">Uso de [detección automática](autodiscover-for-exchange.md) para volver a descubrir la ExternalEwsUrl o EwsPartnerUrl y crear una nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="d2363-140">Using [Autodiscover](autodiscover-for-exchange.md) to rediscover the ExternalEwsUrl or EwsPartnerUrl, and creating a new subscription.</span></span>  |
|<span data-ttu-id="d2363-141">**ErrorServerBusy**</span><span class="sxs-lookup"><span data-stu-id="d2363-141">**ErrorServerBusy**</span></span> | <span data-ttu-id="d2363-142">Superar los límites de [limitación](ews-throttling-in-exchange.md#bk_ThrottlingNotifications) .</span><span class="sxs-lookup"><span data-stu-id="d2363-142">Exceed [throttling](ews-throttling-in-exchange.md#bk_ThrottlingNotifications) limits.</span></span> <span data-ttu-id="d2363-143">Tenga en cuenta de la limitación en cuanto a siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2363-143">Be aware of the following regarding throttling:</span></span><ul><li><span data-ttu-id="d2363-144">El [EwsMaxSubscriptions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) limitación límite identifica el número máximo de inserción, extracción o transmisión por secuencias de suscripciones de notificación que pueden estar activos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d2363-144">The [EwsMaxSubscriptions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) throttling limit identifies the maximum number of push, pull, or streaming notification subscriptions that can be active at one time.</span></span> <span data-ttu-id="d2363-145">Éste es el valor de suscripciones de buzón de correo, no el número de suscripciones de carpeta individuales en una suscripción de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d2363-145">This is the value of mailbox subscriptions, not the number of individual folder subscriptions in a mailbox subscription.</span></span> <span data-ttu-id="d2363-146">A partir de las versiones de buzón de correo de servicio 14.16.0135 y 14.15.0057.000, un buzón de correo alojado en Exchange Online o Exchange Online como parte de Office 365 puede tener un máximo de 20 suscripciones, un destino de Exchange 2013 locales y en buzón de correo puede tener hasta 5000 suscripciones.</span><span class="sxs-lookup"><span data-stu-id="d2363-146">Starting with service mailbox versions 14.16.0135 and 14.15.0057.000, a mailbox hosted by Exchange Online or Exchange Online as part of Office 365 can have up to 20 subscriptions, and a target Exchange 2013 on-premises mailbox can have up to 5000 subscriptions.</span></span></li><li><span data-ttu-id="d2363-147">El [EwsMaxConcurrency](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx) limitación límite identifica el número máximo de solicitudes activas para las conexiones que no sean transmisión por secuencias y tiene un valor predeterminado de 27.</span><span class="sxs-lookup"><span data-stu-id="d2363-147">The [EwsMaxConcurrency](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx) throttling limit identifies the maximum number of active requests for non-streaming connections and has a default value of 27.</span></span></li><li><span data-ttu-id="d2363-148">El límite predeterminado para abrir conexiones de transmisión por secuencias es diez.</span><span class="sxs-lookup"><span data-stu-id="d2363-148">The default limit for open streaming connections is ten.</span></span></li></ul> |<ul><li><span data-ttu-id="d2363-149">[Teniendo en cuenta las implicaciones de las directivas de limitación de peticiones relacionadas con la notificación](ews-throttling-in-exchange.md#bk_ThrottlingNotifications) y limitar el número de suscripciones activas y las conexiones activas de forma que no se limita a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2363-149">[Considering the implications of the notification-related throttling policies](ews-throttling-in-exchange.md#bk_ThrottlingNotifications) and limiting the number of active subscriptions and active connections so that the application is not throttled.</span></span></li><li><span data-ttu-id="d2363-150">Uso de menos conexiones para obtener eventos.</span><span class="sxs-lookup"><span data-stu-id="d2363-150">Using fewer connections to get events.</span></span> <span data-ttu-id="d2363-151">Maximizar el número de suscripciones en cada conexión mediante la [colocación de un máximo de 200 suscripción identificadores en el mismo grupo](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md).</span><span class="sxs-lookup"><span data-stu-id="d2363-151">Maximize the number of subscriptions in each connection by [placing a maximum of 200 subscription IDs in the same group](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md).</span></span> <span data-ttu-id="d2363-152">A continuación, puede usar la misma conexión para recuperar los eventos para todo el grupo, reduciendo el número de conexiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="d2363-152">You can then use the same connection to retrieve events for the entire group, reducing the number of connections required.</span></span></li><li><span data-ttu-id="d2363-153">Cambiar el valor de la HangingConnectionLimit en el archivo web.config para reemplazar el valor predeterminado de diez conexiones abiertas de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="d2363-153">Changing the value of the HangingConnectionLimit in the web.config file to override the default value of ten open streaming connections.</span></span></li></ul>|
|<span data-ttu-id="d2363-154">**ErrorSubscriptionNotFound**</span><span class="sxs-lookup"><span data-stu-id="d2363-154">**ErrorSubscriptionNotFound**</span></span> |<span data-ttu-id="d2363-155">Obtener eventos de una suscripción a que no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="d2363-155">Get events for a subscription that cannot be found.</span></span> <span data-ttu-id="d2363-156">Es posible que haya caducado la suscripción, es posible que se haya reiniciado el proceso de EWS, o se ha pasado una suscripción válida en.</span><span class="sxs-lookup"><span data-stu-id="d2363-156">The subscription might have expired, the EWS process might have been restarted, or an invalid subscription was passed in.</span></span> | <ul><li><span data-ttu-id="d2363-157">Comprobar que se está usando el mismo identificador de suscripción que se devuelve en una respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="d2363-157">Verifying that you're using the same subscription ID that was returned in a previous response.</span></span></li><li><span data-ttu-id="d2363-158">Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</span><span class="sxs-lookup"><span data-stu-id="d2363-158">Ensuring that you're sending the subscription ID for the correct **ExchangeService** object.</span></span></li><li> <span data-ttu-id="d2363-159">[Crear una nueva suscripción](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</span><span class="sxs-lookup"><span data-stu-id="d2363-159">[Creating a new subscription](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</span></span></li></ul> |
|<span data-ttu-id="d2363-160">**[ServiceLocalException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2363-160">**[ServiceLocalException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)**</span></span> |<span data-ttu-id="d2363-161">Agregar una suscripción a una nueva carpeta mientras está abierta una conexión de suscripción en otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="d2363-161">Add a subscription to a new folder while a subscription connection is open on another folder.</span></span>  |<span data-ttu-id="d2363-162">Cambio de su suscripción para suscribirse a todas las carpetas del buzón de correo, en lugar de una carpeta específica.</span><span class="sxs-lookup"><span data-stu-id="d2363-162">Changing your subscription to subscribe to all folders in the mailbox, instead of a specific folder.</span></span>  |
|<span data-ttu-id="d2363-163">**[ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2363-163">**[ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)**</span></span> |<span data-ttu-id="d2363-164">Obtener eventos de una suscripción a que no se encuentra en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2363-164">Get events for a subscription that cannot be located in the Exchange store.</span></span>  | <ul><li><span data-ttu-id="d2363-165">Comprobar que se está usando el mismo identificador de suscripción que se devuelve en una respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="d2363-165">Verifying that you're using the same subscription ID that was returned in a previous response.</span></span></li><li><span data-ttu-id="d2363-166">Asegurarse de que va a enviar el identificador de suscripción para el objeto **ExchangeService** correcto.</span><span class="sxs-lookup"><span data-stu-id="d2363-166">Ensuring that you're sending the subscription ID for the correct **ExchangeService** object.</span></span></li></ul> |
   
## <a name="recovering-from-lost-subscriptions"></a><span data-ttu-id="d2363-167">La recuperación a partir de las suscripciones perdidas</span><span class="sxs-lookup"><span data-stu-id="d2363-167">Recovering from lost subscriptions</span></span>
<span data-ttu-id="d2363-168"><a name="bk_recover"> </a></span><span class="sxs-lookup"><span data-stu-id="d2363-168"></span></span>

<span data-ttu-id="d2363-169">Cuando una suscripción se pierda o ya no es accesible, es mejor crear una nueva suscripción y no incluir la marca de agua antigua en la nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="d2363-169">When a subscription is lost, or is no longer accessible, it is best to create a new subscription and not include the old watermark in the new subscription.</span></span> <span data-ttu-id="d2363-170">Resubscribing con la marca de agua antiguo hace que un examen lineal para eventos, que resulta caro.</span><span class="sxs-lookup"><span data-stu-id="d2363-170">Resubscribing with the old watermark causes a linear scan for events, which is costly.</span></span> <span data-ttu-id="d2363-171">En su lugar, crear una nueva suscripción y comparar propiedades de la carpeta para que busque cambia el contenido que se ha producido entre la suscripción pierden y la nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="d2363-171">Instead, create a new subscription and compare folder properties to look for content changes that occurred between the lost subscription and the new subscription.</span></span> <span data-ttu-id="d2363-172">Las propiedades de carpeta extendida que se recomienda que compruebe son **PR_LOCAL_COMMIT_TIME_MAX** (0x670a0040) y **PR_DELETED_COUNT_TOTAL** (0x670b0003).</span><span class="sxs-lookup"><span data-stu-id="d2363-172">The extended folder properties that we recommend that you check are **PR_LOCAL_COMMIT_TIME_MAX** (0x670a0040) and **PR_DELETED_COUNT_TOTAL** (0x670b0003).</span></span> <span data-ttu-id="d2363-173">Puede hacerlo mediante la [creación de una definición de propiedad extendida](properties-and-extended-properties-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d2363-173">You can do this by [creating an extended property definition](properties-and-extended-properties-in-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2363-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2363-174">See also</span></span>

- [<span data-ttu-id="d2363-175">Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2363-175">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [<span data-ttu-id="d2363-176">Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2363-176">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="d2363-177">Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d2363-177">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="d2363-178">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="d2363-178">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    

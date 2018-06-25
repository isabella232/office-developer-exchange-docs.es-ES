---
title: Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bda4094-88c3-4f61-9219-6ee70f6e81cf
description: Obtenga información acerca de mantener la afinidad entre un grupo de suscripciones y el servidor de buzón de correo.
ms.openlocfilehash: 7cfbfb5cc19e092c37e3d48a7fcc4f27023516e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763088"
---
# <a name="maintain-affinity-between-a-group-of-subscriptions-and-the-mailbox-server-in-exchange"></a><span data-ttu-id="80f46-103">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="80f46-103">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>

<span data-ttu-id="80f46-104">Obtenga información acerca de mantener la afinidad entre un grupo de suscripciones y el servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="80f46-104">Find out about maintaining the affinity between a group of subscriptions and the Mailbox server.</span></span>
  
<span data-ttu-id="80f46-105">La afinidad es la asociación de una secuencia de mensajes de solicitud y respuesta con un determinado servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="80f46-105">Affinity is the association of a sequence of request and response messages with a particular Mailbox server.</span></span> <span data-ttu-id="80f46-106">Para la mayoría de las funciones de Exchange, el servidor controla la afinidad.</span><span class="sxs-lookup"><span data-stu-id="80f46-106">For most functionality in Exchange, affinity is handled by the server.</span></span> <span data-ttu-id="80f46-107">Las notificaciones, sin embargo, son una excepción.</span><span class="sxs-lookup"><span data-stu-id="80f46-107">Notifications, however, are an exception.</span></span> <span data-ttu-id="80f46-108">El cliente es responsable de mantener la afinidad con el servidor de buzón de correo para las suscripciones de notificación.</span><span class="sxs-lookup"><span data-stu-id="80f46-108">The client is responsible for maintaining the affinity with the Mailbox server for notification subscriptions.</span></span> <span data-ttu-id="80f46-109">Esta afinidad permite el equilibrador de carga y servidores de acceso de cliente entre el cliente y el servidor para las suscripciones de notificación de ruta y solicitudes relacionadas en el servidor de buzón de correo que se mantiene la suscripción.</span><span class="sxs-lookup"><span data-stu-id="80f46-109">This affinity enables the load balancer and Client Access servers between the client and the server to route notification subscriptions and related requests to the Mailbox server that maintains the subscription.</span></span> <span data-ttu-id="80f46-110">Sin afinidad, la solicitud es posible que se enrutan a un servidor de buzón de correo diferente que no incluya las suscripciones del cliente, lo que pueden causar un error de [ErrorSubscriptionNotFound](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="80f46-110">Without affinity, the request might get routed to a different Mailbox server that does not include the client's subscriptions, which can cause an [ErrorSubscriptionNotFound](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) error to be returned.</span></span> 
  
## <a name="how-is-affinity-maintained"></a><span data-ttu-id="80f46-111">¿Cómo se mantiene la afinidad?</span><span class="sxs-lookup"><span data-stu-id="80f46-111">How is affinity maintained?</span></span>
<span data-ttu-id="80f46-112"><a name="bk_howmaintained"> </a></span><span class="sxs-lookup"><span data-stu-id="80f46-112"></span></span>

<span data-ttu-id="80f46-113">Afinidad de Exchange es cookie según se indique.</span><span class="sxs-lookup"><span data-stu-id="80f46-113">Affinity in Exchange is cookie based.</span></span> <span data-ttu-id="80f46-114">El cliente desencadena la creación de la cookie mediante la inclusión de los encabezados específicos en la solicitud de suscripción y, a continuación, la respuesta de suscripción contiene la cookie.</span><span class="sxs-lookup"><span data-stu-id="80f46-114">The client triggers the creation of the cookie by including specific headers in the subscription request, and then the subscription response contains the cookie.</span></span> <span data-ttu-id="80f46-115">El cliente envía a continuación, ese cookie en las solicitudes posteriores para asegurarse de que la solicitud se enruta al servidor de buzón de correo correcto.</span><span class="sxs-lookup"><span data-stu-id="80f46-115">The client then sends that cookie in subsequent requests to ensure that the request is routed to the right Mailbox server.</span></span>
  
<span data-ttu-id="80f46-116">Más concretamente, afinidad en Exchange se controla mediante el siguiente:</span><span class="sxs-lookup"><span data-stu-id="80f46-116">More specifically, affinity in Exchange is handled by the following:</span></span> 
  
- <span data-ttu-id="80f46-117">X-AnchorMailbox: Un encabezado que se incluye en la solicitud de suscripción inicial.</span><span class="sxs-lookup"><span data-stu-id="80f46-117">X-AnchorMailbox — An HTTP header that is included in the initial subscription request.</span></span> <span data-ttu-id="80f46-118">Identifica el primer buzón de correo en un grupo de buzones que comparten afinidad con el mismo servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="80f46-118">It identifies the first mailbox in a group of mailboxes that share affinity with the same Mailbox server.</span></span>
    
- <span data-ttu-id="80f46-119">X-PreferServerAffinity: Un encabezado HTTP que se incluye en la solicitud de suscripción inicial con el encabezado X-AnchorMailbox y se establece en true para indicar que el cliente solicita que se mantenga la afinidad con el servidor de buzones.</span><span class="sxs-lookup"><span data-stu-id="80f46-119">X-PreferServerAffinity — An HTTP header that is included in the initial subscription request with the X-AnchorMailbox header and is set to true to indicate that the client is requesting that affinity be maintained with the Mailbox server.</span></span>
    
- <span data-ttu-id="80f46-120">X-BackEndOverrideCookie: Una cookie que se incluye en la respuesta de suscripción inicial y contiene una cookie que el equilibrador de carga y el servidor de acceso de cliente que se usan para enrutar las solicitudes posteriores en el mismo servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="80f46-120">X-BackEndOverrideCookie — A cookie that is included in the initial subscription response and contains a cookie that the load balancer and Client Access server use to route subsequent requests to the same Mailbox server.</span></span>
    
## <a name="how-do-i-maintain-affinity-by-using-the-ews-managed-api-or-ews"></a><span data-ttu-id="80f46-121">¿Cómo se puede mantener la afinidad mediante el uso de la API administrada de EWS o EWS?</span><span class="sxs-lookup"><span data-stu-id="80f46-121">How do I maintain affinity by using the EWS Managed API or EWS?</span></span>
<span data-ttu-id="80f46-122"><a name="bk_howdoimaintain"> </a></span><span class="sxs-lookup"><span data-stu-id="80f46-122"></span></span>

<span data-ttu-id="80f46-123">Puede usar los mismos pasos para mantener la afinidad para varias suscripciones de buzón de correo y sus servidores de buzones de correo, independientemente de si está utilizando la transmisión por secuencias, extracción o notificaciones de inserción, independientemente de si posea un Exchange locales y en servidor o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="80f46-123">You can use the same steps to maintain affinity for multiple mailbox subscriptions and their Mailbox servers, regardless of whether you are using streaming, pull, or push notifications, and regardless of whether you're targeting an Exchange on-premises server or Exchange Online.</span></span>
  
1. <span data-ttu-id="80f46-124">Para cada buzón de correo, [detección automática de llamadas](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) y obtener la configuración de usuario GroupingInformation y ExternalEwsUrl.</span><span class="sxs-lookup"><span data-stu-id="80f46-124">For each mailbox, [call Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and get the GroupingInformation and ExternalEwsUrl user settings.</span></span> <span data-ttu-id="80f46-125">Para la detección automática de SOAP, use el elemento de [configuración](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) y para la detección automática de POX, se utiliza el elemento de [GroupingInformation](http://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="80f46-125">For SOAP Autodiscover, you use the [Setting](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) element, and for POX Autodiscover, you use the [GroupingInformation](http://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) element.</span></span> 
    
2. <span data-ttu-id="80f46-126">Con la configuración de GroupingInformation y ExternalEwsUrl de las respuestas de detección automática, los buzones de correo electrónicos con el mismo ExternalEwsUrl y GroupingInformation concatena el valor en el mismo grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-126">Using the GroupingInformation and ExternalEwsUrl settings from the Autodiscover responses, place mailboxes with the same ExternalEwsUrl and GroupingInformation concatenated value in the same group.</span></span> <span data-ttu-id="80f46-127">Si los grupos tienen más de 200 buzones, desglosar los grupos adicionales para que cada grupo tiene buzones no más de 200.</span><span class="sxs-lookup"><span data-stu-id="80f46-127">If any groups have more than 200 mailboxes, break the groups down further so that each group has no more than 200 mailboxes.</span></span>
    
3. <span data-ttu-id="80f46-128">Crear y usar un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) para el resto del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="80f46-128">Create and use one [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) object for the rest of the procedure.</span></span> <span data-ttu-id="80f46-129">Cuando se usa el mismo **ExchangeService** objeto, cookies y encabezados (cuando se establecen) se mantienen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="80f46-129">When you use the same **ExchangeService** object, cookies and headers (when they are set) are automatically maintained.</span></span> <span data-ttu-id="80f46-130">Tenga en cuenta que si no desea suscripciones de transmisión por secuencias de grupo en una sola conexión, está libre para crear un objeto **ExchangeService** diferente para cada usuario suplantado.</span><span class="sxs-lookup"><span data-stu-id="80f46-130">Note that if you do not intend to group streaming subscriptions into a single connection, you are free to create a different **ExchangeService** object for each impersonated user.</span></span> 
    
4. <span data-ttu-id="80f46-131">[Enviar una suscripción a](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) la solicitud para el usuario cuyo nombre de usuario aparece en primer lugar cuando todos los usuarios en el grupo se ordenan alfabéticamente (nos referiremos a este usuario como el usuario de buzón de correo de anclaje).</span><span class="sxs-lookup"><span data-stu-id="80f46-131">[Send a subscription](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) request for the user whose user name appears first when all users in the group are sorted alphabetically (we'll refer to this user as the anchor mailbox user).</span></span> <span data-ttu-id="80f46-132">Haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="80f46-132">Do the following:</span></span> 
    
  - <span data-ttu-id="80f46-133">Incluir el encabezado X-AnchorMailbox con un valor establecido en la dirección SMTP del usuario de buzón de correo de delimitador.</span><span class="sxs-lookup"><span data-stu-id="80f46-133">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user.</span></span>
    
  - <span data-ttu-id="80f46-134">Incluya el encabezado X-PreferServerAffinity con un valor establecido en true.</span><span class="sxs-lookup"><span data-stu-id="80f46-134">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="80f46-135">Use la función [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) (el tipo [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="80f46-135">Use the [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
5. <span data-ttu-id="80f46-136">En la respuesta de suscripción, obtener el valor de X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="80f46-136">In the subscription response, get the X-BackEndOverrideCookie value.</span></span> <span data-ttu-id="80f46-137">Incluir este valor en cada una de las solicitudes posteriores de suscripción para los usuarios de este grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-137">Include this value in each of the subsequent subscription requests for users in this group.</span></span>
    
6. <span data-ttu-id="80f46-138">Para cada usuario adicional en el grupo, envíe una solicitud de suscripción y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="80f46-138">For each additional user in the group, send a subscription request and do the following:</span></span>
    
  - <span data-ttu-id="80f46-139">Incluir el encabezado X-AnchorMailbox con un valor establecido en la dirección SMTP del usuario de buzón de correo de anclaje para el grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-139">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user for the group.</span></span>
    
  - <span data-ttu-id="80f46-140">Incluya el encabezado X-PreferServerAffinity con un valor establecido en true.</span><span class="sxs-lookup"><span data-stu-id="80f46-140">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="80f46-141">Incluir X-BackEndOverrideCookie que se devuelve en respuesta de suscripción del usuario de buzón de correo de delimitador.</span><span class="sxs-lookup"><span data-stu-id="80f46-141">Include the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response.</span></span>
    
  - <span data-ttu-id="80f46-142">Use la función [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) (el tipo [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="80f46-142">Use the [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
    <span data-ttu-id="80f46-143">Tenga en cuenta que el servidor utiliza los valores de X-PreferServerAffinity y X-BackendOverrideCookie conjuntamente para realizar el enrutamiento para el servidor de buzones.</span><span class="sxs-lookup"><span data-stu-id="80f46-143">Note that the server uses the X-PreferServerAffinity and X-BackendOverrideCookie values together to perform the routing to the mailbox server.</span></span> <span data-ttu-id="80f46-144">El encabezado X-AnchorMailbox también es necesario, pero se omite el servidor si los dos valores son válidos.</span><span class="sxs-lookup"><span data-stu-id="80f46-144">The X-AnchorMailbox header is also required, but is ignored by the server if the other two values are valid.</span></span> <span data-ttu-id="80f46-145">Si X-AnchorMailbox y X-PreferServerAffinity se encuentran en una solicitud y BackendOverrideCookie de X no se incluye, el valor de X-AnchorMailbox se usa para enrutar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80f46-145">If X-AnchorMailbox and X-PreferServerAffinity are in a request and X-BackendOverrideCookie is not included, the X-AnchorMailbox value is used to route the requests.</span></span>
    
    <span data-ttu-id="80f46-146">Debido a que los valores de X-BackendOverrideCookie y X-PreferServerAffinity realizan el enrutamiento, si el buzón de correo de anclaje nunca se mueve a otro servidor o grupo, no cambie la lógica de debido a que la X-BackendOverrideCookie usará para enrutar la solicitud al servidor correcto para el grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-146">Because the X-PreferServerAffinity and X-BackendOverrideCookie values perform the routing, if the anchor mailbox ever moves to another group or server, the logic does not change because the X-BackendOverrideCookie will route the request to the correct server for the group.</span></span>
    
7. <span data-ttu-id="80f46-147">Enviar un único [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) o solicitudes [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) para el grupo y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="80f46-147">Send a single [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) requests for the group, and do the following:</span></span> 
    
  - <span data-ttu-id="80f46-148">Incluir los valores de [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) devueltos en cada una de las respuestas de suscripción individual para los buzones de correo en el grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-148">Include the [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values returned in each of the individual subscription responses for mailboxes in the group.</span></span> 
    
  - <span data-ttu-id="80f46-149">Si existen más de 200 suscripciones para el grupo, crear varias solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80f46-149">If more than 200 subscriptions exist for the group, create multiple requests.</span></span> <span data-ttu-id="80f46-150">El número máximo de valores de [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) para incluir en una solicitud es 200.</span><span class="sxs-lookup"><span data-stu-id="80f46-150">The maximum number of [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values to include in a request is 200.</span></span> 
    
  - <span data-ttu-id="80f46-151">Si necesita más conexiones que están disponibles en el buzón de destino, use la cuenta de servicio para suplantar el buzón de correo de anclaje para el grupo; de lo contrario, no utilice la suplantación.</span><span class="sxs-lookup"><span data-stu-id="80f46-151">If you need more connections than are available to the target mailbox, use the service account to impersonate the anchor mailbox for the group; otherwise, do not use impersonation.</span></span> <span data-ttu-id="80f46-152">Lo ideal es que desee suplantar a un único buzón por solicitud [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) o [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) para evitar que no se produzcan nunca los límites de limitación de peticiones.</span><span class="sxs-lookup"><span data-stu-id="80f46-152">Ideally, you want to impersonate a unique mailbox per [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) request so that you never encounter throttling limits.</span></span> 
    
  - <span data-ttu-id="80f46-153">Usar ApplicationImpersonation si necesita [más conexiones que están disponibles en el buzón de destino](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); de lo contrario, no utilice ApplicationImpersonation.</span><span class="sxs-lookup"><span data-stu-id="80f46-153">Use ApplicationImpersonation if you need [more connections than are available to the target mailbox](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); otherwise, do not use ApplicationImpersonation.</span></span>
    
  - <span data-ttu-id="80f46-154">Incluya el encabezado X-PreferServerAffinity y establézcalo en true.</span><span class="sxs-lookup"><span data-stu-id="80f46-154">Include the X-PreferServerAffinity header and set it to true.</span></span> <span data-ttu-id="80f46-155">Este valor se incluye automáticamente si está utilizando el objeto **ExchangeService** que creó en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="80f46-155">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
  - <span data-ttu-id="80f46-156">Incluir la X-BackEndOverrideCookie para el grupo (la X-BackEndOverrideCookie que se devuelve en respuesta de suscripción del usuario de buzón de correo de anclaje).</span><span class="sxs-lookup"><span data-stu-id="80f46-156">Include the X-BackEndOverrideCookie for the group (the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response).</span></span> <span data-ttu-id="80f46-157">Este valor se incluye automáticamente si está utilizando el objeto **ExchangeService** que creó en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="80f46-157">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
8. <span data-ttu-id="80f46-158">Pase los eventos devueltos a un subproceso independiente para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="80f46-158">Pass the returned events to a separate thread for processing.</span></span>
    
## <a name="what-throttling-values-do-i-need-to-take-into-consideration"></a><span data-ttu-id="80f46-159">¿Qué valores de limitación de peticiones es necesario tener en cuenta?</span><span class="sxs-lookup"><span data-stu-id="80f46-159">What throttling values do I need to take into consideration?</span></span>
<span data-ttu-id="80f46-160"><a name="bk_throttling"> </a></span><span class="sxs-lookup"><span data-stu-id="80f46-160"></span></span>

<span data-ttu-id="80f46-161">Cuando planee la implementación de la notificación, querrá tener dos valores en cuenta: el número de conexiones y el número de suscripciones.</span><span class="sxs-lookup"><span data-stu-id="80f46-161">As you plan your notification implementation, you'll want to take two values into consideration: the number of connections, and the number of subscriptions.</span></span> <span data-ttu-id="80f46-162">En la siguiente tabla se enumera los valores predeterminados para cada opción de [limitación de peticiones](ews-throttling-in-exchange.md) y cómo se usa la configuración.</span><span class="sxs-lookup"><span data-stu-id="80f46-162">The following table lists the default values for each [throttling](ews-throttling-in-exchange.md) setting and how the settings are used.</span></span> <span data-ttu-id="80f46-163">Para cada valor, se asigna el presupuesto en el buzón de destino.</span><span class="sxs-lookup"><span data-stu-id="80f46-163">For each value, the budget is allocated to the target mailbox.</span></span> <span data-ttu-id="80f46-164">Por este motivo, el uso de suplantación para conexiones adicionales de ganancia es un paso necesario en muchos escenarios.</span><span class="sxs-lookup"><span data-stu-id="80f46-164">For this reason, using impersonation to gain additional connections is a required step in many scenarios.</span></span> 
  
<span data-ttu-id="80f46-165">**La tabla 1. Limitación de los valores predeterminados**</span><span class="sxs-lookup"><span data-stu-id="80f46-165">**Table 1. Default throttling values**</span></span>

|<span data-ttu-id="80f46-166">**Área de consideración**</span><span class="sxs-lookup"><span data-stu-id="80f46-166">**Area of consideration**</span></span>|<span data-ttu-id="80f46-167">**Configuración de limitación**</span><span class="sxs-lookup"><span data-stu-id="80f46-167">**Throttling setting**</span></span>|<span data-ttu-id="80f46-168">**Valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="80f46-168">**Default value**</span></span>|<span data-ttu-id="80f46-169">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80f46-169">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80f46-170">Conexiones de transmisión por secuencias</span><span class="sxs-lookup"><span data-stu-id="80f46-170">Streaming connections</span></span>  <br/> |<span data-ttu-id="80f46-171">Predeterminado de sangría límite de conexión</span><span class="sxs-lookup"><span data-stu-id="80f46-171">Default hanging connection limit</span></span>  <br/> |<span data-ttu-id="80f46-172">10 para Exchange Online</span><span class="sxs-lookup"><span data-stu-id="80f46-172">10 for Exchange Online</span></span>  <br/> <span data-ttu-id="80f46-173">3 para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="80f46-173">3 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="80f46-174">El número máximo de conexiones simultáneas de transmisión por secuencias que una cuenta puede tener abiertas a la vez en el servidor.</span><span class="sxs-lookup"><span data-stu-id="80f46-174">The maximum number of concurrent streaming connections that an account can have open on the server at one time.</span></span> <span data-ttu-id="80f46-175">Para que funcione dentro de este límite, utilice una cuenta de servicio con la función ApplicationImpersonation asignada a los buzones de correo de destino y representar al primer usuario en cada grupo de identificador de suscripción cuando Introducción transmitir eventos.</span><span class="sxs-lookup"><span data-stu-id="80f46-175">To work within this limit, use a service account with the ApplicationImpersonation role assigned for the target mailboxes, and impersonate the first user in each subscription ID group when getting streamed events.</span></span>  <br/> |
|<span data-ttu-id="80f46-176">Extracción o inserción de conexiones</span><span class="sxs-lookup"><span data-stu-id="80f46-176">Pull or push connections</span></span>  <br/> |<span data-ttu-id="80f46-177">EWSMaxConcurrency</span><span class="sxs-lookup"><span data-stu-id="80f46-177">EWSMaxConcurrency</span></span>  <br/> |<span data-ttu-id="80f46-178">27</span><span class="sxs-lookup"><span data-stu-id="80f46-178">27</span></span>  <br/> |<span data-ttu-id="80f46-179">El número máximo de conexiones simultáneas de extracción o inserción (las solicitudes que se han recibido pero que aún no se ha respondido a) que una cuenta de a la vez puede tener abiertas en el servidor.</span><span class="sxs-lookup"><span data-stu-id="80f46-179">The maximum number of concurrent pull or push connections (requests that have been received but not yet responded to) that an account can have open on the server at one time.</span></span>  <br/> |
|<span data-ttu-id="80f46-180">Suscripciones</span><span class="sxs-lookup"><span data-stu-id="80f46-180">Subscriptions</span></span>  <br/> |<span data-ttu-id="80f46-181">EWSMaxSubscriptions</span><span class="sxs-lookup"><span data-stu-id="80f46-181">EWSMaxSubscriptions</span></span>  <br/> |<span data-ttu-id="80f46-182">20 para Exchange Online</span><span class="sxs-lookup"><span data-stu-id="80f46-182">20 for Exchange Online</span></span>  <br/> <span data-ttu-id="80f46-183">5000 para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="80f46-183">5000 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="80f46-184">El número máximo de suscripciones nonexpired que una cuenta puede tener al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="80f46-184">The maximum number of nonexpired subscriptions that an account can have at one time.</span></span> <span data-ttu-id="80f46-185">Este valor es disminuye cuando se crea la suscripción en el servidor.</span><span class="sxs-lookup"><span data-stu-id="80f46-185">This value is decremented when the subscription is created on the server.</span></span>  <br/> |
   
<span data-ttu-id="80f46-186">En el ejemplo siguiente se muestra cómo se controlan los presupuestos entre cualquier buzón de correo de destino y la cuenta de servicio que tiene la función [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) asignada a los buzones de correo de destino.</span><span class="sxs-lookup"><span data-stu-id="80f46-186">The following example shows how budgets are handled between any target mailbox and the service account that has the [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) role assigned for the target mailboxes.</span></span> 
  
- <span data-ttu-id="80f46-187">ServiceAccount1 (sa1) suplanta muchos usuarios (m1, m2, m3 y así sucesivamente) y crea suscripciones para cada buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="80f46-187">ServiceAccount1 (sa1) impersonates many users (m1, m2, m3, and so on) and creates subscriptions for each mailbox.</span></span> <span data-ttu-id="80f46-188">Tenga en cuenta que cuando se crean las suscripciones, el propietario de la suscripción es sa1, por lo que cuando sa1 abre una conexión con las suscripciones, EWS exige que las suscripciones pertenecen a sa1.</span><span class="sxs-lookup"><span data-stu-id="80f46-188">Note that when the subscriptions are created, the subscription owner is sa1, so when sa1 opens a connection with the subscriptions, EWS enforces that the subscriptions are owned by sa1.</span></span>
    
- <span data-ttu-id="80f46-189">Sa1 puede abrir la conexión de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="80f46-189">Sa1 can open the connection in the following ways:</span></span>
    
1. <span data-ttu-id="80f46-190">Sin suplantación, lo que la conexión se atribuyen a sa1.</span><span class="sxs-lookup"><span data-stu-id="80f46-190">Without impersonation, so the connection is charged against sa1.</span></span>
    
2. <span data-ttu-id="80f46-191">Mediante la suplantación de cualquiera de los usuarios: m1, por ejemplo, para que la conexión se contabiliza en una copia del presupuesto de m1.</span><span class="sxs-lookup"><span data-stu-id="80f46-191">By impersonating any of the users — m1 for example — so that the connection is charged against a copy of m1's budget.</span></span> <span data-ttu-id="80f46-192">(M1 sí puede abrir diez conexiones mediante el uso de Exchange Online y todas las cuentas de servicio suplantación m1 pueden abrir diez conexiones utilizando el presupuesto copiado.)</span><span class="sxs-lookup"><span data-stu-id="80f46-192">(M1 itself can open ten connections by using Exchange Online, and all service accounts impersonating m1 can open ten connections by using the copied budget.)</span></span>
    
- <span data-ttu-id="80f46-193">Si se alcanza el límite de conexión, están disponibles las siguientes soluciones alternativas:</span><span class="sxs-lookup"><span data-stu-id="80f46-193">If the connection limit is hit, the following workarounds are available:</span></span>
    
  - <span data-ttu-id="80f46-194">Si se usa la opción 1, el administrador puede crear varias cuentas de servicio para suplantar a los usuarios adicionales.</span><span class="sxs-lookup"><span data-stu-id="80f46-194">If option 1 is used, the administrator can create multiple service accounts to impersonate additional users.</span></span>
    
  - <span data-ttu-id="80f46-195">Si se usa la opción 2, el código puede suplantar a otro usuario: m2, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="80f46-195">If option 2 is used, the code can impersonate another user — m2 for example.</span></span>
    
## <a name="example-maintaining-affinity-between-a-group-of-subscriptions-and-the-mailbox-server"></a><span data-ttu-id="80f46-196">Ejemplo: Mantenimiento de afinidad entre un grupo de suscripciones y el servidor de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="80f46-196">Example: Maintaining affinity between a group of subscriptions and the Mailbox server</span></span>
<span data-ttu-id="80f46-197"><a name="bk_ce"> </a></span><span class="sxs-lookup"><span data-stu-id="80f46-197"></span></span>

<span data-ttu-id="80f46-198">Bien, veamos en acción.</span><span class="sxs-lookup"><span data-stu-id="80f46-198">Okay, let's see it in action.</span></span> <span data-ttu-id="80f46-199">En el ejemplo de código siguiente se muestra cómo agrupar los usuarios y usar los encabezados X-AnchorMailbox y X-PreferServerAffinity y la cookie de X-BackendOverrideCookie para mantener la afinidad con el servidor de buzones.</span><span class="sxs-lookup"><span data-stu-id="80f46-199">The following code example shows you how to group users and use the X-AnchorMailbox and X-PreferServerAffinity headers and the X-BackendOverrideCookie cookie to maintain affinity with the Mailbox server.</span></span> <span data-ttu-id="80f46-200">Debido a que los encabezados y la cookie son de importancia principal en la historia de afinidad, en este ejemplo se centra en las solicitudes de EWS XML y respuestas.</span><span class="sxs-lookup"><span data-stu-id="80f46-200">Because the headers and the cookie are of primary importance in the affinity story, this example focuses on the EWS XML requests and responses.</span></span> <span data-ttu-id="80f46-201">Para usar la API administrada de EWS para crear el cuerpo de las respuestas y solicitudes de suscripción, vea [notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) y [extraer las notificaciones sobre los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="80f46-201">To use the EWS Managed API to create the body of the subscription requests and responses, see [Stream notifications about mailbox events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) and [Pull notifications about mailbox events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="80f46-202">En esta sección se incluye particular, pasos adicionales para mantener la afinidad y agregar los encabezados a las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80f46-202">This section includes additional steps particular to maintaining affinity and adding the headers to your requests.</span></span>
  
<span data-ttu-id="80f46-203">Este ejemplo tiene cuatro usuarios: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com y sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="80f46-203">This example has four users: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com, and sadie@contoso.com.</span></span> <span data-ttu-id="80f46-204">La siguiente ilustración muestra la GroupingInformation y ExternalEwsUrl [configuración de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="80f46-204">The following figure shows the GroupingInformation and ExternalEwsUrl [Autodiscover settings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) for the users.</span></span> 
  
<span data-ttu-id="80f46-205">**En la figura 1. Configuración de detección automática usada para los buzones de correo de grupo**</span><span class="sxs-lookup"><span data-stu-id="80f46-205">**Figure 1. Autodiscover settings used to group mailboxes**</span></span>

![Tabla que muestra los valores de GroupingInformation y ExternalEwsUrl para cada uno de los usuarios.](media/Exchange2013_NotificationAffinityAutoDResults.png)
  
<span data-ttu-id="80f46-207">Con la configuración de las respuestas de detección automática, los buzones de correo se agrupan por el valor concatenado de los valores de GroupingInformation y ExternalEwsUrl.</span><span class="sxs-lookup"><span data-stu-id="80f46-207">Using the settings from the Autodiscover responses, the mailboxes are grouped by the concatenated value of the GroupingInformation and ExternalEwsUrl settings.</span></span> <span data-ttu-id="80f46-208">En este ejemplo, Alfred y Sadie tienen los mismos valores, por lo que se encuentran en un grupo y Alisa y Ronnie comparten los mismos valores, por lo que están en otro grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-208">In this example, Alfred and Sadie have the same values, so they are in one group, and Alisa and Ronnie share the same values, so they are in another group.</span></span>
  
<span data-ttu-id="80f46-209">**La figura 2. Creación de grupos de buzón de correo**</span><span class="sxs-lookup"><span data-stu-id="80f46-209">**Figure 2. Creating mailbox groups**</span></span>

![Tabla que muestra cómo se crean los grupos de buzones usando la configuración de Detección automática.](media/Exchange2013_NotificationAffinityGrouping.png)
  
<span data-ttu-id="80f46-211">A efectos de este ejemplo, nos centraremos en grupo A. Se debería usar los mismos pasos para el grupo B, pero se puede usar un valor distinto de X-AnchorMailbox para ese grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-211">For the purpose of this example, we'll focus on Group A. We would use the same steps for group B, but use a different X-AnchorMailbox value for that group.</span></span>
  
<span data-ttu-id="80f46-212">Uso de [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx), crear la solicitud de suscripción para el buzón de correo de anclaje (alfred@contoso.com), con el encabezado X-AnchorMailbox establecido en el su dirección de correo electrónico y un valor de encabezado X-PreferServerAffinity de true.</span><span class="sxs-lookup"><span data-stu-id="80f46-212">Using [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx), create the subscription request for the anchor mailbox (alfred@contoso.com), with the X-AnchorMailbox header set to the their email address and an X-PreferServerAffinity header value of true.</span></span> <span data-ttu-id="80f46-213">Configuración de estos valores de dos encabezado se activará el servidor para crear un BackEndOverrideCookie X para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80f46-213">Setting these two header values will trigger the server to create an X-BackEndOverrideCookie for the response.</span></span>
  
<span data-ttu-id="80f46-214">Si se usa la API administrada de EWS, use el método[Add](http://msdn.microsoft.com/EN-US/library/cy7xta5e) de [cadena](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)para agregar los encabezados de dos a petición de suscripción, tal como se muestra.</span><span class="sxs-lookup"><span data-stu-id="80f46-214">If you're using the EWS Managed API, use the [HttpHeaders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)[Add](http://msdn.microsoft.com/EN-US/library/cy7xta5e) method to add the two headers to your subscription request, as shown.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", Mailbox.SMTPAddress);
service.HttpHeaders.Add("X-PreferServerAffinity", "true");
```

<span data-ttu-id="80f46-215">Por lo tanto solicitudes de suscripción de Alfred tiene este aspecto.</span><span class="sxs-lookup"><span data-stu-id="80f46-215">So Alfred's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="80f46-216">El siguiente mensaje XML es la respuesta a la solicitud de suscripción de Alfred, e incluye la X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="80f46-216">The following XML message is the response to Alfred's subscription request, and it includes the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="80f46-217">Volver a enviar esta cookie para todas las solicitudes posteriores para los usuarios de este grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-217">Resend this cookie for all subsequent requests for users in this group.</span></span> <span data-ttu-id="80f46-218">Tenga en cuenta que la respuesta contiene también las cookies adicionales, como la cookie de exchangecookie utilizada por Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="80f46-218">Notice that the response also contains additional cookies, such as the exchangecookie cookie used by Exchange 2010.</span></span> <span data-ttu-id="80f46-219">Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013, omitir exchangecookie si se incluye en las solicitudes de suscripción subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="80f46-219">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013, ignore exchangecookie if it is included in subsequent subscription requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=ddb8c383aef34c7694132aa679744feb; expires=Thu, 25-Sep-2014 18:42:45 GMT; path=/;
    HttpOnly
Set-Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295; path=/; secure; HttpOnly
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
    expires=Wed, 25-Sep-2013 18:52:49 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
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
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="80f46-220">Uso el X-BackEndOverrideCookie de respuesta de Alfred y el encabezado X-AnchorMailbox, se crea la solicitud de suscripción para Sadie, el otro miembro de la solicitud de suscripción del grupo A. Sadie tiene este aspecto.</span><span class="sxs-lookup"><span data-stu-id="80f46-220">Using the X-BackEndOverrideCookie from Alfred's response and the X-AnchorMailbox header, the subscription request is created for Sadie, the other member of Group A. Sadie's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@consoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@consoso.com </t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="80f46-221">Respuesta de suscripción de Sadie tiene este aspecto.</span><span class="sxs-lookup"><span data-stu-id="80f46-221">Sadie's subscription response looks like this.</span></span> <span data-ttu-id="80f46-222">Tenga en cuenta que no incluye el X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="80f46-222">Note that it does not include the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="80f46-223">El cliente es responsable de almacenamiento en caché que el valor de las solicitudes futuras.</span><span class="sxs-lookup"><span data-stu-id="80f46-223">The client is responsible for caching that value for future requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=640ea858f69d47ff8cce8b44c337f6d9; path=/
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
   expires= Wed, 25-Sep-2013 18:53:06 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
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
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="80f46-224">Con los valores de [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) de las respuestas de suscripción, ha creado una solicitud de operación de [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) para todas las suscripciones en el grupo.</span><span class="sxs-lookup"><span data-stu-id="80f46-224">Using the [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values from the subscription responses, a [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) operation request was created for all the subscriptions in the group.</span></span> <span data-ttu-id="80f46-225">Debido a que hay menos de 200 suscripciones en este grupo, todos se envían en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="80f46-225">Because there are less than 200 subscriptions in this group, they are all sent in one request.</span></span> <span data-ttu-id="80f46-226">El encabezado X-PreferServerAffinity se establece en true y se incluye el X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="80f46-226">The X-PreferServerAffinity header is set to true and the X-BackEndOverrideCookie is included.</span></span> 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:GetStreamingEvents>
      <m:SubscriptionIds>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</t:SubscriptionId>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</t:SubscriptionId>
      </m:SubscriptionIds>
      <m:ConnectionTimeout>10</m:ConnectionTimeout>
    </m:GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="80f46-227">Los eventos devueltos, a continuación, se pasan a un subproceso independiente para el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="80f46-227">The returned events are then passed to a separate thread for processing.</span></span>
  
## <a name="how-has-affinity-changed"></a><span data-ttu-id="80f46-228">¿Cómo ha cambiado la afinidad?</span><span class="sxs-lookup"><span data-stu-id="80f46-228">How has affinity changed?</span></span>
<span data-ttu-id="80f46-229"><a name="bk_howchanged"> </a></span><span class="sxs-lookup"><span data-stu-id="80f46-229"></span></span>

<span data-ttu-id="80f46-230">En Exchange 2010, las suscripciones se mantienen en el servidor acceso de cliente, como se muestra en la figura 3.</span><span class="sxs-lookup"><span data-stu-id="80f46-230">In Exchange 2010, subscriptions are maintained on the Client Access server, as shown in Figure 3.</span></span> <span data-ttu-id="80f46-231">En las versiones de Exchange posterior a Exchange 2010, las suscripciones se mantienen en el servidor de buzón de correo, tal como se muestra en la figura 4.</span><span class="sxs-lookup"><span data-stu-id="80f46-231">In versions of Exchange later than Exchange 2010, subscriptions are maintained on the Mailbox server, as shown in Figure 4.</span></span>
  
<span data-ttu-id="80f46-232">**La figura 3. Proceso para el mantenimiento de la afinidad de Exchange 2010**</span><span class="sxs-lookup"><span data-stu-id="80f46-232">**Figure 3. Process for maintaining affinity in Exchange 2010**</span></span>

![Ilustración que muestra cómo se mantiene la tabla de suscripciones activas en el servidor de acceso de cliente en Exchange 2010.](media/Exchange2013_NoficationAffinity2010.png)
  
<span data-ttu-id="80f46-234">**La figura 4. Proceso para el mantenimiento de afinidad en Exchange Online y Exchange 2013**</span><span class="sxs-lookup"><span data-stu-id="80f46-234">**Figure 4. Process for maintaining affinity in Exchange Online and Exchange 2013**</span></span>

![Ilustración que muestra cómo el equilibrador de carga y el servidor de acceso de cliente enrutan las solicitudes al servidor de buzones que mantiene la tabla de suscripciones activas en Exchange Server y Exchange Online.](media/Exchange2013_NoficationAffinity2013.png)
  
<span data-ttu-id="80f46-236">En Exchange 2010, el cliente sólo sabe la dirección del equilibrador de carga y el exchangecookie que es devuelto por el servidor se asegura de que la solicitud se enruta al servidor de acceso de cliente correcto.</span><span class="sxs-lookup"><span data-stu-id="80f46-236">In Exchange 2010, the client only knows the address of the load balancer, and the exchangecookie that is returned by the server ensures that the request is routed to the right Client Access server.</span></span> <span data-ttu-id="80f46-237">Sin embargo, en versiones posteriores, el equilibrador de carga y las funciones de servidor acceso de cliente tienen que enrutar las solicitudes de forma adecuada antes de que se incluyen en el servidor de buzones.</span><span class="sxs-lookup"><span data-stu-id="80f46-237">However, in later versions, the load balancer and the Client Access server roles both have to route the requests appropriately before they get to the Mailbox server.</span></span> <span data-ttu-id="80f46-238">Para llevar a cabo, que se necesita información adicional, que es la razón por la que se introdujeron las cookies y los nuevos encabezados.</span><span class="sxs-lookup"><span data-stu-id="80f46-238">To do that, additional information is required, which is why the new headers and cookie were introduced.</span></span> <span data-ttu-id="80f46-239">El artículo de [suscripciones de notificación, eventos de buzón de correo y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explica cómo se mantienen las suscripciones en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="80f46-239">The article [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explains how subscriptions are maintained in Exchange 2013.</span></span> 
  
<span data-ttu-id="80f46-240">Es posible que tenga en cuenta que el exchangecookie que usa Exchange 2010 sigue siendo devuelto por versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="80f46-240">You might notice that the exchangecookie that Exchange 2010 uses is still returned by later versions.</span></span> <span data-ttu-id="80f46-241">No hay ningún riesgo en incluidos esta cookie en las solicitudes, pero las versiones posteriores de Exchange pasar por alto.</span><span class="sxs-lookup"><span data-stu-id="80f46-241">There's no harm in including this cookie in requests, but later versions of Exchange ignore it.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="80f46-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="80f46-242">See also</span></span>

- [<span data-ttu-id="80f46-243">Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="80f46-243">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [<span data-ttu-id="80f46-244">Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="80f46-244">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="80f46-245">Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="80f46-245">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="80f46-246">Tratamiento de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="80f46-246">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
- [<span data-ttu-id="80f46-247">Cambios en la administración de afinidad para las suscripciones de EWS...</span><span class="sxs-lookup"><span data-stu-id="80f46-247">Changes in Managing Affinity for EWS Subscriptions…</span></span>](http://blogs.msdn.com/b/mstehle/archive/2013/04/17/changes-in-managing-affinity-for-ews-subscriptions.aspx)
- [<span data-ttu-id="80f46-248">EWS limitación en Exchange</span><span class="sxs-lookup"><span data-stu-id="80f46-248">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    


---
title: Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1bda4094-88c3-4f61-9219-6ee70f6e81cf
description: Obtenga información acerca de cómo mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo.
localization_priority: Priority
ms.openlocfilehash: 1618216cf69e08b2ae774264e0910856a59851af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455773"
---
# <a name="maintain-affinity-between-a-group-of-subscriptions-and-the-mailbox-server-in-exchange"></a><span data-ttu-id="0748b-103">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo de Exchange</span><span class="sxs-lookup"><span data-stu-id="0748b-103">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>

<span data-ttu-id="0748b-104">Obtenga información acerca de cómo mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0748b-104">Find out about maintaining the affinity between a group of subscriptions and the Mailbox server.</span></span>
  
<span data-ttu-id="0748b-105">Affinity es la Asociación de una secuencia de mensajes de solicitud y respuesta con un servidor de buzones de correo determinado.</span><span class="sxs-lookup"><span data-stu-id="0748b-105">Affinity is the association of a sequence of request and response messages with a particular Mailbox server.</span></span> <span data-ttu-id="0748b-106">Para la mayoría de las funciones de Exchange, la afinidad la administra el servidor.</span><span class="sxs-lookup"><span data-stu-id="0748b-106">For most functionality in Exchange, affinity is handled by the server.</span></span> <span data-ttu-id="0748b-107">Las notificaciones, sin embargo, son una excepción.</span><span class="sxs-lookup"><span data-stu-id="0748b-107">Notifications, however, are an exception.</span></span> <span data-ttu-id="0748b-108">El cliente es responsable de mantener la afinidad con el servidor de buzones de correo para las suscripciones de notificación.</span><span class="sxs-lookup"><span data-stu-id="0748b-108">The client is responsible for maintaining the affinity with the Mailbox server for notification subscriptions.</span></span> <span data-ttu-id="0748b-109">Esta afinidad permite que el equilibrador de carga y los servidores de acceso de cliente entre el cliente y el servidor enruten las suscripciones de notificación y las solicitudes relacionadas al servidor de buzones de correo que mantiene la suscripción.</span><span class="sxs-lookup"><span data-stu-id="0748b-109">This affinity enables the load balancer and Client Access servers between the client and the server to route notification subscriptions and related requests to the Mailbox server that maintains the subscription.</span></span> <span data-ttu-id="0748b-110">Sin afinidad, la solicitud se puede enrutar a un servidor de buzones de correo diferente que no incluye las suscripciones del cliente, lo que puede provocar que se devuelva un error [ErrorSubscriptionNotFound](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0748b-110">Without affinity, the request might get routed to a different Mailbox server that does not include the client's subscriptions, which can cause an [ErrorSubscriptionNotFound](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) error to be returned.</span></span> 
  
## <a name="how-is-affinity-maintained"></a><span data-ttu-id="0748b-111">¿Cómo se mantiene la afinidad?</span><span class="sxs-lookup"><span data-stu-id="0748b-111">How is affinity maintained?</span></span>
<span data-ttu-id="0748b-112"><a name="bk_howmaintained"> </a></span><span class="sxs-lookup"><span data-stu-id="0748b-112"><a name="bk_howmaintained"> </a></span></span>

<span data-ttu-id="0748b-113">La afinidad de Exchange se basa en cookies.</span><span class="sxs-lookup"><span data-stu-id="0748b-113">Affinity in Exchange is cookie based.</span></span> <span data-ttu-id="0748b-114">El cliente desencadena la creación de la cookie mediante la inclusión de encabezados específicos en la solicitud de suscripción y, a continuación, la respuesta de la suscripción contiene la cookie.</span><span class="sxs-lookup"><span data-stu-id="0748b-114">The client triggers the creation of the cookie by including specific headers in the subscription request, and then the subscription response contains the cookie.</span></span> <span data-ttu-id="0748b-115">A continuación, el cliente envía esa cookie en solicitudes posteriores para asegurarse de que la solicitud se enruta al servidor de buzones de correo correcto.</span><span class="sxs-lookup"><span data-stu-id="0748b-115">The client then sends that cookie in subsequent requests to ensure that the request is routed to the right Mailbox server.</span></span>
  
<span data-ttu-id="0748b-116">Más concretamente, la afinidad de Exchange se controla mediante lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0748b-116">More specifically, affinity in Exchange is handled by the following:</span></span> 
  
- <span data-ttu-id="0748b-117">X-AnchorMailbox: un encabezado HTTP que se incluye en la solicitud de suscripción inicial.</span><span class="sxs-lookup"><span data-stu-id="0748b-117">X-AnchorMailbox — An HTTP header that is included in the initial subscription request.</span></span> <span data-ttu-id="0748b-118">Identifica el primer buzón de un grupo de buzones que comparten la afinidad con el mismo servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0748b-118">It identifies the first mailbox in a group of mailboxes that share affinity with the same Mailbox server.</span></span>
    
- <span data-ttu-id="0748b-119">X-PreferServerAffinity: un encabezado HTTP que se incluye en la solicitud de suscripción inicial con el encabezado X-AnchorMailbox y se establece en true para indicar que el cliente está solicitando que se mantenga la afinidad con el servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0748b-119">X-PreferServerAffinity — An HTTP header that is included in the initial subscription request with the X-AnchorMailbox header and is set to true to indicate that the client is requesting that affinity be maintained with the Mailbox server.</span></span>
    
- <span data-ttu-id="0748b-120">X-BackEndOverrideCookie: una cookie que se incluye en la respuesta de suscripción inicial y contiene una cookie que el equilibrador de carga y el servidor de acceso de cliente usan para redirigir las solicitudes posteriores al mismo servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0748b-120">X-BackEndOverrideCookie — A cookie that is included in the initial subscription response and contains a cookie that the load balancer and Client Access server use to route subsequent requests to the same Mailbox server.</span></span>
    
## <a name="how-do-i-maintain-affinity-by-using-the-ews-managed-api-or-ews"></a><span data-ttu-id="0748b-121">¿Cómo puedo mantener la afinidad mediante la API administrada de EWS o EWS?</span><span class="sxs-lookup"><span data-stu-id="0748b-121">How do I maintain affinity by using the EWS Managed API or EWS?</span></span>
<span data-ttu-id="0748b-122"><a name="bk_howdoimaintain"> </a></span><span class="sxs-lookup"><span data-stu-id="0748b-122"><a name="bk_howdoimaintain"> </a></span></span>

<span data-ttu-id="0748b-123">Puede usar los mismos pasos para mantener la afinidad para varias suscripciones de buzones y sus servidores de buzones de correo, independientemente de si usa las notificaciones de streaming, pull o Push, y de si su objetivo es un servidor local de Exchange o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="0748b-123">You can use the same steps to maintain affinity for multiple mailbox subscriptions and their Mailbox servers, regardless of whether you are using streaming, pull, or push notifications, and regardless of whether you're targeting an Exchange on-premises server or Exchange Online.</span></span>
  
1. <span data-ttu-id="0748b-124">Para cada buzón, [llame a detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) y obtenga la configuración de usuario de GroupingInformation y ExternalEwsUrl.</span><span class="sxs-lookup"><span data-stu-id="0748b-124">For each mailbox, [call Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and get the GroupingInformation and ExternalEwsUrl user settings.</span></span> <span data-ttu-id="0748b-125">Para la detección automática de SOAP, use el elemento [Setting](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) y, para la detección automática de Pox, use el elemento [GroupingInformation](https://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0748b-125">For SOAP Autodiscover, you use the [Setting](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) element, and for POX Autodiscover, you use the [GroupingInformation](https://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) element.</span></span> 
    
2. <span data-ttu-id="0748b-126">Mediante la configuración GroupingInformation y ExternalEwsUrl de las respuestas de detección automática, ubique los buzones con el mismo valor concatenado de ExternalEwsUrl y GroupingInformation en el mismo grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-126">Using the GroupingInformation and ExternalEwsUrl settings from the Autodiscover responses, place mailboxes with the same ExternalEwsUrl and GroupingInformation concatenated value in the same group.</span></span> <span data-ttu-id="0748b-127">Si algún grupo tiene más de 200 buzones, separe los grupos más para que cada grupo no tenga más de 200 buzones.</span><span class="sxs-lookup"><span data-stu-id="0748b-127">If any groups have more than 200 mailboxes, break the groups down further so that each group has no more than 200 mailboxes.</span></span>
    
3. <span data-ttu-id="0748b-128">Cree y use un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) para el resto del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="0748b-128">Create and use one [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) object for the rest of the procedure.</span></span> <span data-ttu-id="0748b-129">Cuando se usa el mismo objeto **ExchangeService** , las cookies y los encabezados (cuando se establecen) se mantienen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0748b-129">When you use the same **ExchangeService** object, cookies and headers (when they are set) are automatically maintained.</span></span> <span data-ttu-id="0748b-130">Tenga en cuenta que si no desea agrupar las suscripciones de transmisión en una sola conexión, puede crear un objeto **ExchangeService** diferente para cada usuario suplantado.</span><span class="sxs-lookup"><span data-stu-id="0748b-130">Note that if you do not intend to group streaming subscriptions into a single connection, you are free to create a different **ExchangeService** object for each impersonated user.</span></span> 
    
4. <span data-ttu-id="0748b-131">[Envíe una](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) solicitud de suscripción para el usuario cuyo nombre de usuario aparezca primero cuando todos los usuarios del grupo estén ordenados alfabéticamente (nos referiremos a este usuario como el usuario de buzón de correo anclado).</span><span class="sxs-lookup"><span data-stu-id="0748b-131">[Send a subscription](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) request for the user whose user name appears first when all users in the group are sorted alphabetically (we'll refer to this user as the anchor mailbox user).</span></span> <span data-ttu-id="0748b-132">Haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0748b-132">Do the following:</span></span> 
    
  - <span data-ttu-id="0748b-133">Incluya el encabezado X-AnchorMailbox con un valor establecido en la dirección SMTP del usuario buzón de correo anclado.</span><span class="sxs-lookup"><span data-stu-id="0748b-133">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user.</span></span>
    
  - <span data-ttu-id="0748b-134">Incluya el encabezado X-PreferServerAffinity con un valor establecido en true.</span><span class="sxs-lookup"><span data-stu-id="0748b-134">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="0748b-135">Use el rol [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) (el tipo [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="0748b-135">Use the [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
5. <span data-ttu-id="0748b-136">En la respuesta de la suscripción, obtenga el valor X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="0748b-136">In the subscription response, get the X-BackEndOverrideCookie value.</span></span> <span data-ttu-id="0748b-137">Incluya este valor en cada una de las siguientes solicitudes de suscripción para los usuarios de este grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-137">Include this value in each of the subsequent subscription requests for users in this group.</span></span>
    
6. <span data-ttu-id="0748b-138">Para cada usuario adicional del grupo, envíe una solicitud de suscripción y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0748b-138">For each additional user in the group, send a subscription request and do the following:</span></span>
    
  - <span data-ttu-id="0748b-139">Incluya el encabezado X-AnchorMailbox con un valor establecido en la dirección SMTP del usuario buzón de correo de delimitador para el grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-139">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user for the group.</span></span>
    
  - <span data-ttu-id="0748b-140">Incluya el encabezado X-PreferServerAffinity con un valor establecido en true.</span><span class="sxs-lookup"><span data-stu-id="0748b-140">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="0748b-141">Incluya el X-BackEndOverrideCookie que se devolvió en la respuesta de la suscripción del usuario del buzón de correo anclado.</span><span class="sxs-lookup"><span data-stu-id="0748b-141">Include the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response.</span></span>
    
  - <span data-ttu-id="0748b-142">Use el rol [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) (el tipo [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="0748b-142">Use the [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
    <span data-ttu-id="0748b-143">Tenga en cuenta que el servidor usa los valores X-PreferServerAffinity y X-BackendOverrideCookie para realizar el enrutamiento al servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0748b-143">Note that the server uses the X-PreferServerAffinity and X-BackendOverrideCookie values together to perform the routing to the mailbox server.</span></span> <span data-ttu-id="0748b-144">El encabezado X-AnchorMailbox también es necesario, pero el servidor lo omite si los dos valores son válidos.</span><span class="sxs-lookup"><span data-stu-id="0748b-144">The X-AnchorMailbox header is also required, but is ignored by the server if the other two values are valid.</span></span> <span data-ttu-id="0748b-145">Si X-AnchorMailbox y X-PreferServerAffinity están en una solicitud y no se incluye X-BackendOverrideCookie, el valor X-AnchorMailbox se usa para enrutar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="0748b-145">If X-AnchorMailbox and X-PreferServerAffinity are in a request and X-BackendOverrideCookie is not included, the X-AnchorMailbox value is used to route the requests.</span></span>
    
    <span data-ttu-id="0748b-146">Debido a que los valores X-PreferServerAffinity y X-BackendOverrideCookie realizan el enrutamiento, si el buzón de correo del delimitador se mueve alguna vez a otro grupo o servidor, la lógica no cambia porque el BackendOverrideCookie X redirige la solicitud al servidor correcto para el grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-146">Because the X-PreferServerAffinity and X-BackendOverrideCookie values perform the routing, if the anchor mailbox ever moves to another group or server, the logic does not change because the X-BackendOverrideCookie will route the request to the correct server for the group.</span></span>
    
7. <span data-ttu-id="0748b-147">Envíe una sola solicitud [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) o [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) para el grupo y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0748b-147">Send a single [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) requests for the group, and do the following:</span></span> 
    
  - <span data-ttu-id="0748b-148">Incluya los valores de [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) devueltos en cada una de las respuestas de suscripción individuales para los buzones del grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-148">Include the [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values returned in each of the individual subscription responses for mailboxes in the group.</span></span> 
    
  - <span data-ttu-id="0748b-149">Si hay más de 200 suscripciones para el grupo, cree varias solicitudes.</span><span class="sxs-lookup"><span data-stu-id="0748b-149">If more than 200 subscriptions exist for the group, create multiple requests.</span></span> <span data-ttu-id="0748b-150">El número máximo de valores de [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) que se deben incluir en una solicitud es de 200.</span><span class="sxs-lookup"><span data-stu-id="0748b-150">The maximum number of [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values to include in a request is 200.</span></span> 
    
  - <span data-ttu-id="0748b-151">Si necesita más conexiones de las que hay disponibles para el buzón de correo de destino, use la cuenta de servicio para suplantar el buzón de correo de delimitador del grupo; de lo contrario, no use la suplantación.</span><span class="sxs-lookup"><span data-stu-id="0748b-151">If you need more connections than are available to the target mailbox, use the service account to impersonate the anchor mailbox for the group; otherwise, do not use impersonation.</span></span> <span data-ttu-id="0748b-152">Lo ideal es que desee suplantar un buzón de correo único por cada solicitud [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) o [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) , de modo que nunca se detecten límites de limitación.</span><span class="sxs-lookup"><span data-stu-id="0748b-152">Ideally, you want to impersonate a unique mailbox per [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) request so that you never encounter throttling limits.</span></span> 
    
  - <span data-ttu-id="0748b-153">Use ApplicationImpersonation si necesita [más conexiones de las que hay disponibles para el buzón de correo de destino](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); de lo contrario, no use ApplicationImpersonation.</span><span class="sxs-lookup"><span data-stu-id="0748b-153">Use ApplicationImpersonation if you need [more connections than are available to the target mailbox](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); otherwise, do not use ApplicationImpersonation.</span></span>
    
  - <span data-ttu-id="0748b-154">Incluya el encabezado X-PreferServerAffinity y establézcalo en true.</span><span class="sxs-lookup"><span data-stu-id="0748b-154">Include the X-PreferServerAffinity header and set it to true.</span></span> <span data-ttu-id="0748b-155">Este valor se incluye automáticamente si usa el objeto **ExchangeService** que creó en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="0748b-155">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
  - <span data-ttu-id="0748b-156">Incluya el X-BackEndOverrideCookie para el grupo (el BackEndOverrideCookie que se ha devuelto en la respuesta de suscripción del usuario del buzón de correo anclado).</span><span class="sxs-lookup"><span data-stu-id="0748b-156">Include the X-BackEndOverrideCookie for the group (the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response).</span></span> <span data-ttu-id="0748b-157">Este valor se incluye automáticamente si usa el objeto **ExchangeService** que creó en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="0748b-157">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
8. <span data-ttu-id="0748b-158">Pasar los eventos devueltos a un subproceso independiente para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="0748b-158">Pass the returned events to a separate thread for processing.</span></span>
    
## <a name="what-throttling-values-do-i-need-to-take-into-consideration"></a><span data-ttu-id="0748b-159">¿Qué valores de limitación se deben tener en cuenta?</span><span class="sxs-lookup"><span data-stu-id="0748b-159">What throttling values do I need to take into consideration?</span></span>
<span data-ttu-id="0748b-160"><a name="bk_throttling"> </a></span><span class="sxs-lookup"><span data-stu-id="0748b-160"><a name="bk_throttling"> </a></span></span>

<span data-ttu-id="0748b-161">Al planear la implementación de la notificación, querrá tener en cuenta dos valores: el número de conexiones y el número de suscripciones.</span><span class="sxs-lookup"><span data-stu-id="0748b-161">As you plan your notification implementation, you'll want to take two values into consideration: the number of connections, and the number of subscriptions.</span></span> <span data-ttu-id="0748b-162">En la siguiente tabla se enumeran los valores predeterminados para cada configuración de [limitación](ews-throttling-in-exchange.md) y cómo se usa la configuración.</span><span class="sxs-lookup"><span data-stu-id="0748b-162">The following table lists the default values for each [throttling](ews-throttling-in-exchange.md) setting and how the settings are used.</span></span> <span data-ttu-id="0748b-163">Para cada valor, el presupuesto se asigna al buzón de correo de destino.</span><span class="sxs-lookup"><span data-stu-id="0748b-163">For each value, the budget is allocated to the target mailbox.</span></span> <span data-ttu-id="0748b-164">Por este motivo, el uso de la suplantación para obtener conexiones adicionales es un paso necesario en muchos escenarios.</span><span class="sxs-lookup"><span data-stu-id="0748b-164">For this reason, using impersonation to gain additional connections is a required step in many scenarios.</span></span> 
  
<span data-ttu-id="0748b-165">**Tabla 1. Valores de limitación predeterminados**</span><span class="sxs-lookup"><span data-stu-id="0748b-165">**Table 1. Default throttling values**</span></span>

|<span data-ttu-id="0748b-166">**Área de consideración**</span><span class="sxs-lookup"><span data-stu-id="0748b-166">**Area of consideration**</span></span>|<span data-ttu-id="0748b-167">**Configuración de limitación**</span><span class="sxs-lookup"><span data-stu-id="0748b-167">**Throttling setting**</span></span>|<span data-ttu-id="0748b-168">**Valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="0748b-168">**Default value**</span></span>|<span data-ttu-id="0748b-169">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0748b-169">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0748b-170">Conexiones de transmisión</span><span class="sxs-lookup"><span data-stu-id="0748b-170">Streaming connections</span></span>  <br/> |<span data-ttu-id="0748b-171">Límite predeterminado de conexiones francesas</span><span class="sxs-lookup"><span data-stu-id="0748b-171">Default hanging connection limit</span></span>  <br/> |<span data-ttu-id="0748b-172">10 para Exchange Online</span><span class="sxs-lookup"><span data-stu-id="0748b-172">10 for Exchange Online</span></span>  <br/> <span data-ttu-id="0748b-173">3 para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0748b-173">3 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="0748b-174">Número máximo de conexiones simultáneas de transmisión por secuencias que una cuenta puede tener abiertas en el servidor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="0748b-174">The maximum number of concurrent streaming connections that an account can have open on the server at one time.</span></span> <span data-ttu-id="0748b-175">Para trabajar dentro de este límite, use una cuenta de servicio con el rol ApplicationImpersonation asignado para los buzones de correo de destino y suplante el primer usuario de cada grupo de identificador de suscripción al obtener eventos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="0748b-175">To work within this limit, use a service account with the ApplicationImpersonation role assigned for the target mailboxes, and impersonate the first user in each subscription ID group when getting streamed events.</span></span>  <br/> |
|<span data-ttu-id="0748b-176">Conexiones de inserción o extracción</span><span class="sxs-lookup"><span data-stu-id="0748b-176">Pull or push connections</span></span>  <br/> |<span data-ttu-id="0748b-177">EWSMaxConcurrency</span><span class="sxs-lookup"><span data-stu-id="0748b-177">EWSMaxConcurrency</span></span>  <br/> |<span data-ttu-id="0748b-178">,27</span><span class="sxs-lookup"><span data-stu-id="0748b-178">27</span></span>  <br/> |<span data-ttu-id="0748b-179">Número máximo de conexiones de extracción o inserción simultáneas (solicitudes que se han recibido pero que todavía no se han respondido) que una cuenta puede tener abierta en el servidor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="0748b-179">The maximum number of concurrent pull or push connections (requests that have been received but not yet responded to) that an account can have open on the server at one time.</span></span>  <br/> |
|<span data-ttu-id="0748b-180">Suscripciones</span><span class="sxs-lookup"><span data-stu-id="0748b-180">Subscriptions</span></span>  <br/> |<span data-ttu-id="0748b-181">EWSMaxSubscriptions</span><span class="sxs-lookup"><span data-stu-id="0748b-181">EWSMaxSubscriptions</span></span>  <br/> |<span data-ttu-id="0748b-182">20 para Exchange Online</span><span class="sxs-lookup"><span data-stu-id="0748b-182">20 for Exchange Online</span></span>  <br/> <span data-ttu-id="0748b-183">5000 para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0748b-183">5000 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="0748b-184">El número máximo de suscripciones no expiradas que puede tener una cuenta al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="0748b-184">The maximum number of nonexpired subscriptions that an account can have at one time.</span></span> <span data-ttu-id="0748b-185">Este valor se reduce cuando se crea la suscripción en el servidor.</span><span class="sxs-lookup"><span data-stu-id="0748b-185">This value is decremented when the subscription is created on the server.</span></span>  <br/> |
   
<span data-ttu-id="0748b-186">En el siguiente ejemplo se muestra cómo se administran los presupuestos entre cualquier buzón de correo de destino y la cuenta de servicio que tiene asignada la función [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) para los buzones de correo de destino.</span><span class="sxs-lookup"><span data-stu-id="0748b-186">The following example shows how budgets are handled between any target mailbox and the service account that has the [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) role assigned for the target mailboxes.</span></span> 
  
- <span data-ttu-id="0748b-187">ServiceAccount1 (SA1) suplanta a muchos usuarios (M1, m2, m3, etc.) y crea suscripciones para cada buzón.</span><span class="sxs-lookup"><span data-stu-id="0748b-187">ServiceAccount1 (sa1) impersonates many users (m1, m2, m3, and so on) and creates subscriptions for each mailbox.</span></span> <span data-ttu-id="0748b-188">Tenga en cuenta que, al crear las suscripciones, el propietario de la suscripción es SA1, por lo que cuando SA1 abre una conexión con las suscripciones, EWS exige que las suscripciones sean propiedad de SA1.</span><span class="sxs-lookup"><span data-stu-id="0748b-188">Note that when the subscriptions are created, the subscription owner is sa1, so when sa1 opens a connection with the subscriptions, EWS enforces that the subscriptions are owned by sa1.</span></span>
    
- <span data-ttu-id="0748b-189">SA1 puede abrir la conexión de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="0748b-189">Sa1 can open the connection in the following ways:</span></span>
    
1. <span data-ttu-id="0748b-190">Sin suplantación, de modo que la conexión se carga contra SA1.</span><span class="sxs-lookup"><span data-stu-id="0748b-190">Without impersonation, so the connection is charged against sa1.</span></span>
    
2. <span data-ttu-id="0748b-191">Mediante la suplantación de cualquiera de los usuarios (M1 por ejemplo) para que la conexión se cargue con una copia del presupuesto de m1's.</span><span class="sxs-lookup"><span data-stu-id="0748b-191">By impersonating any of the users — m1 for example — so that the connection is charged against a copy of m1's budget.</span></span> <span data-ttu-id="0748b-192">(M1 puede abrir diez conexiones mediante Exchange Online y todas las cuentas de servicio que suplantan a M1 pueden abrir diez conexiones mediante el presupuesto copiado).</span><span class="sxs-lookup"><span data-stu-id="0748b-192">(M1 itself can open ten connections by using Exchange Online, and all service accounts impersonating m1 can open ten connections by using the copied budget.)</span></span>
    
- <span data-ttu-id="0748b-193">Si se alcanza el límite de conexión, estarán disponibles las siguientes soluciones:</span><span class="sxs-lookup"><span data-stu-id="0748b-193">If the connection limit is hit, the following workarounds are available:</span></span>
    
  - <span data-ttu-id="0748b-194">Si se usa la opción 1, el administrador puede crear varias cuentas de servicio para suplantar a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="0748b-194">If option 1 is used, the administrator can create multiple service accounts to impersonate additional users.</span></span>
    
  - <span data-ttu-id="0748b-195">Si se usa la opción 2, el código puede suplantar a otro usuario, por ejemplo, m2.</span><span class="sxs-lookup"><span data-stu-id="0748b-195">If option 2 is used, the code can impersonate another user — m2 for example.</span></span>
    
## <a name="example-maintaining-affinity-between-a-group-of-subscriptions-and-the-mailbox-server"></a><span data-ttu-id="0748b-196">Ejemplo: mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo</span><span class="sxs-lookup"><span data-stu-id="0748b-196">Example: Maintaining affinity between a group of subscriptions and the Mailbox server</span></span>
<span data-ttu-id="0748b-197"><a name="bk_ce"> </a></span><span class="sxs-lookup"><span data-stu-id="0748b-197"><a name="bk_ce"> </a></span></span>

<span data-ttu-id="0748b-198">Bien, vamos a verlo en acción.</span><span class="sxs-lookup"><span data-stu-id="0748b-198">Okay, let's see it in action.</span></span> <span data-ttu-id="0748b-199">El siguiente ejemplo de código muestra cómo agrupar usuarios y usar los encabezados X-AnchorMailbox y X-PreferServerAffinity y la cookie X-BackendOverrideCookie para mantener la afinidad con el servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0748b-199">The following code example shows you how to group users and use the X-AnchorMailbox and X-PreferServerAffinity headers and the X-BackendOverrideCookie cookie to maintain affinity with the Mailbox server.</span></span> <span data-ttu-id="0748b-200">Como los encabezados y la cookie son de importancia primordial en el artículo de afinidad, este ejemplo se centra en las solicitudes y respuestas XML de EWS.</span><span class="sxs-lookup"><span data-stu-id="0748b-200">Because the headers and the cookie are of primary importance in the affinity story, this example focuses on the EWS XML requests and responses.</span></span> <span data-ttu-id="0748b-201">Para usar la API administrada de EWS para crear el cuerpo de las solicitudes y respuestas de suscripción, consulte [transmisiones por secuencias sobre eventos de buzón de correo con EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) y [extraer notificaciones sobre eventos de buzón de correo mediante EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="0748b-201">To use the EWS Managed API to create the body of the subscription requests and responses, see [Stream notifications about mailbox events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) and [Pull notifications about mailbox events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="0748b-202">En esta sección se incluyen pasos adicionales específicos para mantener la afinidad y agregar los encabezados a las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="0748b-202">This section includes additional steps particular to maintaining affinity and adding the headers to your requests.</span></span>
  
<span data-ttu-id="0748b-203">Este ejemplo tiene cuatro usuarios: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com y sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="0748b-203">This example has four users: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com, and sadie@contoso.com.</span></span> <span data-ttu-id="0748b-204">La siguiente figura muestra la [configuración de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) de GroupingInformation y ExternalEwsUrl para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="0748b-204">The following figure shows the GroupingInformation and ExternalEwsUrl [Autodiscover settings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) for the users.</span></span> 
  
<span data-ttu-id="0748b-205">**Figura 1. Configuración de detección automática usada para agrupar buzones**</span><span class="sxs-lookup"><span data-stu-id="0748b-205">**Figure 1. Autodiscover settings used to group mailboxes**</span></span>

![Tabla que muestra los valores de GroupingInformation y ExternalEwsUrl para cada uno de los usuarios.](media/Exchange2013_NotificationAffinityAutoDResults.png)
  
<span data-ttu-id="0748b-207">Mediante la configuración de las respuestas de detección automática, los buzones se agrupan por el valor concatenado de la configuración GroupingInformation y ExternalEwsUrl.</span><span class="sxs-lookup"><span data-stu-id="0748b-207">Using the settings from the Autodiscover responses, the mailboxes are grouped by the concatenated value of the GroupingInformation and ExternalEwsUrl settings.</span></span> <span data-ttu-id="0748b-208">En este ejemplo, Alfred y Sadie tienen los mismos valores, por lo que se encuentran en un grupo y alisa y Ronnie comparten los mismos valores, por lo que se encuentran en otro grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-208">In this example, Alfred and Sadie have the same values, so they are in one group, and Alisa and Ronnie share the same values, so they are in another group.</span></span>
  
<span data-ttu-id="0748b-209">**Figura 2. Creación de grupos de buzones**</span><span class="sxs-lookup"><span data-stu-id="0748b-209">**Figure 2. Creating mailbox groups**</span></span>

![Tabla que muestra cómo se crean los grupos de buzones usando la configuración de Detección automática.](media/Exchange2013_NotificationAffinityGrouping.png)
  
<span data-ttu-id="0748b-211">A efectos de este ejemplo, nos centraremos en el grupo A. Usaría los mismos pasos para el grupo B, pero usaré un valor X-AnchorMailbox diferente para ese grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-211">For the purpose of this example, we'll focus on Group A. We would use the same steps for group B, but use a different X-AnchorMailbox value for that group.</span></span>
  
<span data-ttu-id="0748b-212">Con [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx), cree la solicitud de suscripción para el buzón delimitado (Alfred@contoso.com), con el encabezado x-AnchorMailbox establecido en su dirección de correo electrónico y un valor de encabezado x-PreferServerAffinity de true.</span><span class="sxs-lookup"><span data-stu-id="0748b-212">Using [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx), create the subscription request for the anchor mailbox (alfred@contoso.com), with the X-AnchorMailbox header set to the their email address and an X-PreferServerAffinity header value of true.</span></span> <span data-ttu-id="0748b-213">Si se establecen estos dos valores de encabezado, se activará el servidor para crear un X-BackEndOverrideCookie para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0748b-213">Setting these two header values will trigger the server to create an X-BackEndOverrideCookie for the response.</span></span>
  
<span data-ttu-id="0748b-214">Si está usando la API administrada de EWS, use el método [HttpHeaders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)[para agregar los](https://msdn.microsoft.com/library/cy7xta5e) dos encabezados a la solicitud de suscripción, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="0748b-214">If you're using the EWS Managed API, use the [HttpHeaders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)[Add](https://msdn.microsoft.com/library/cy7xta5e) method to add the two headers to your subscription request, as shown.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", Mailbox.SMTPAddress);
service.HttpHeaders.Add("X-PreferServerAffinity", "true");
```

<span data-ttu-id="0748b-215">Por lo tanto, la solicitud de suscripción de Alfred tiene este aspecto.</span><span class="sxs-lookup"><span data-stu-id="0748b-215">So Alfred's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="0748b-216">El siguiente mensaje XML es la respuesta a la solicitud de suscripción de Alfred e incluye la X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="0748b-216">The following XML message is the response to Alfred's subscription request, and it includes the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="0748b-217">Vuelva a enviar esta cookie para todas las solicitudes posteriores para los usuarios de este grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-217">Resend this cookie for all subsequent requests for users in this group.</span></span> <span data-ttu-id="0748b-218">Observe que la respuesta también contiene cookies adicionales, como la cookie exchangecookie usada por Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="0748b-218">Notice that the response also contains additional cookies, such as the exchangecookie cookie used by Exchange 2010.</span></span> <span data-ttu-id="0748b-219">Exchange Online, Exchange online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013, ignore exchangecookie si se incluye en solicitudes de suscripción posteriores.</span><span class="sxs-lookup"><span data-stu-id="0748b-219">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013, ignore exchangecookie if it is included in subsequent subscription requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=ddb8c383aef34c7694132aa679744feb; expires=Thu, 25-Sep-2014 18:42:45 GMT; path=/;
    HttpOnly
Set-Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295; path=/; secure; HttpOnly
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
    expires=Wed, 25-Sep-2013 18:52:49 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="0748b-220">Si se usa el X-BackEndOverrideCookie de la respuesta de Alfred y el encabezado X-AnchorMailbox, se crea la solicitud de suscripción para Sadie, el otro miembro de la solicitud de suscripción del grupo A. Sadie tiene este aspecto.</span><span class="sxs-lookup"><span data-stu-id="0748b-220">Using the X-BackEndOverrideCookie from Alfred's response and the X-AnchorMailbox header, the subscription request is created for Sadie, the other member of Group A. Sadie's subscription request looks like this.</span></span>
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com </t:SmtpAddress>
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

<span data-ttu-id="0748b-221">La respuesta de la suscripción de Sadie tiene este aspecto.</span><span class="sxs-lookup"><span data-stu-id="0748b-221">Sadie's subscription response looks like this.</span></span> <span data-ttu-id="0748b-222">Tenga en cuenta que no incluye el X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="0748b-222">Note that it does not include the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="0748b-223">El cliente es responsable de almacenar en caché ese valor para las solicitudes futuras.</span><span class="sxs-lookup"><span data-stu-id="0748b-223">The client is responsible for caching that value for future requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=640ea858f69d47ff8cce8b44c337f6d9; path=/
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
   expires= Wed, 25-Sep-2013 18:53:06 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="0748b-224">Mediante el uso de los valores de [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) de las respuestas de suscripción, se ha creado una solicitud de operación [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) para todas las suscripciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="0748b-224">Using the [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values from the subscription responses, a [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) operation request was created for all the subscriptions in the group.</span></span> <span data-ttu-id="0748b-225">Como hay menos de 200 suscripciones en este grupo, todas se envían en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0748b-225">Because there are less than 200 subscriptions in this group, they are all sent in one request.</span></span> <span data-ttu-id="0748b-226">El encabezado X-PreferServerAffinity se establece en true y se incluye el X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="0748b-226">The X-PreferServerAffinity header is set to true and the X-BackEndOverrideCookie is included.</span></span> 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="0748b-227">A continuación, los eventos devueltos se pasan a un subproceso independiente para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="0748b-227">The returned events are then passed to a separate thread for processing.</span></span>
  
## <a name="how-has-affinity-changed"></a><span data-ttu-id="0748b-228">¿Cómo ha cambiado la afinidad?</span><span class="sxs-lookup"><span data-stu-id="0748b-228">How has affinity changed?</span></span>
<span data-ttu-id="0748b-229"><a name="bk_howchanged"> </a></span><span class="sxs-lookup"><span data-stu-id="0748b-229"><a name="bk_howchanged"> </a></span></span>

<span data-ttu-id="0748b-230">En Exchange 2010, las suscripciones se mantienen en el servidor de acceso de cliente, tal como se muestra en la figura 3.</span><span class="sxs-lookup"><span data-stu-id="0748b-230">In Exchange 2010, subscriptions are maintained on the Client Access server, as shown in Figure 3.</span></span> <span data-ttu-id="0748b-231">En versiones de Exchange posteriores a Exchange 2010, las suscripciones se mantienen en el servidor de buzones de correo, tal como se muestra en la figura 4.</span><span class="sxs-lookup"><span data-stu-id="0748b-231">In versions of Exchange later than Exchange 2010, subscriptions are maintained on the Mailbox server, as shown in Figure 4.</span></span>
  
<span data-ttu-id="0748b-232">**Figura 3. Proceso para mantener la afinidad en Exchange 2010**</span><span class="sxs-lookup"><span data-stu-id="0748b-232">**Figure 3. Process for maintaining affinity in Exchange 2010**</span></span>

![Ilustración que muestra cómo se mantiene la tabla de suscripciones activas en el servidor de acceso de cliente en Exchange 2010.](media/Exchange2013_NoficationAffinity2010.png)
  
<span data-ttu-id="0748b-234">**Figura 4. Proceso para mantener la afinidad en Exchange Online y Exchange 2013**</span><span class="sxs-lookup"><span data-stu-id="0748b-234">**Figure 4. Process for maintaining affinity in Exchange Online and Exchange 2013**</span></span>

![Ilustración que muestra cómo el equilibrador de carga y el servidor de acceso de cliente enrutan las solicitudes al servidor de buzones que mantiene la tabla de suscripciones activas en Exchange Server y Exchange Online.](media/Exchange2013_NoficationAffinity2013.png)
  
<span data-ttu-id="0748b-236">En Exchange 2010, el cliente solo conoce la dirección del equilibrador de carga y el exchangecookie devuelto por el servidor asegura que la solicitud se enruta al servidor de acceso de cliente correcto.</span><span class="sxs-lookup"><span data-stu-id="0748b-236">In Exchange 2010, the client only knows the address of the load balancer, and the exchangecookie that is returned by the server ensures that the request is routed to the right Client Access server.</span></span> <span data-ttu-id="0748b-237">Sin embargo, en versiones posteriores, el equilibrador de carga y los roles de servidor acceso de clientes tienen que enrutar las solicitudes adecuadamente antes de que lleguen al servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0748b-237">However, in later versions, the load balancer and the Client Access server roles both have to route the requests appropriately before they get to the Mailbox server.</span></span> <span data-ttu-id="0748b-238">Para ello, se necesita información adicional, que es la razón por la que se introdujeron los nuevos encabezados y la cookie.</span><span class="sxs-lookup"><span data-stu-id="0748b-238">To do that, additional information is required, which is why the new headers and cookie were introduced.</span></span> <span data-ttu-id="0748b-239">Las [suscripciones de notificación de artículo, los eventos de buzón y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explican cómo se mantienen las suscripciones en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0748b-239">The article [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explains how subscriptions are maintained in Exchange 2013.</span></span> 
  
<span data-ttu-id="0748b-240">Es posible que observe que el exchangecookie que usa Exchange 2010 sigue devuelto por versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0748b-240">You might notice that the exchangecookie that Exchange 2010 uses is still returned by later versions.</span></span> <span data-ttu-id="0748b-241">No hay ningún daño en incluir esta cookie en las solicitudes, pero las versiones más recientes de Exchange la omiten.</span><span class="sxs-lookup"><span data-stu-id="0748b-241">There's no harm in including this cookie in requests, but later versions of Exchange ignore it.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0748b-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="0748b-242">See also</span></span>

- [<span data-ttu-id="0748b-243">Suscripciones de notificación, eventos de buzón y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0748b-243">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [<span data-ttu-id="0748b-244">Notificaciones de secuencia sobre eventos de buzón de correo mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0748b-244">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="0748b-245">Extraer notificaciones sobre eventos de buzón de correo mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0748b-245">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="0748b-246">Control de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0748b-246">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
- [<span data-ttu-id="0748b-247">Cambios en la administración de la afinidad de las suscripciones de EWS...</span><span class="sxs-lookup"><span data-stu-id="0748b-247">Changes in Managing Affinity for EWS Subscriptions…</span></span>](https://blogs.msdn.com/b/mstehle/archive/2013/04/17/changes-in-managing-affinity-for-ews-subscriptions.aspx)
- [<span data-ttu-id="0748b-248">Limitación de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0748b-248">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    


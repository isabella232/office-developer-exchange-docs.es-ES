---
title: Operación GetEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: La operación GetEvents se usa en los clientes de suscripción de extracción a las notificaciones de solicitud desde el servidor de acceso de cliente. La respuesta de la operación GetEvents devuelve una matriz de elementos y eventos que se han producido en un buzón de correo desde la última vez la notificación.
ms.openlocfilehash: 1a23a9d570a4554e54becb7927f25dff89888c74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764821"
---
# <a name="getevents-operation"></a><span data-ttu-id="d8fda-104">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="d8fda-104">GetEvents operation</span></span>

<span data-ttu-id="d8fda-105">La operación **GetEvents** se usa en los clientes de suscripción de extracción a las notificaciones de solicitud desde el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d8fda-105">The **GetEvents** operation is used by pull subscription clients to request notifications from the Client Access server.</span></span> <span data-ttu-id="d8fda-106">La respuesta de la operación **GetEvents** devuelve una matriz de elementos y eventos que se han producido en un buzón de correo desde la última vez la notificación.</span><span class="sxs-lookup"><span data-stu-id="d8fda-106">The **GetEvents** operation response returns an array of items and events that have occurred in a mailbox since the last the notification.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d8fda-107">La operación de **DeleteUserConfiguration** activará un evento de mover para el sistema de notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="d8fda-107">The **DeleteUserConfiguration** operation will trigger a move event for the event notification system.</span></span> <span data-ttu-id="d8fda-108">El objeto de configuración de usuario se moverán al volcado de archivos.</span><span class="sxs-lookup"><span data-stu-id="d8fda-108">The user configuration object will be moved to the dumpster.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d8fda-109">Notas</span><span class="sxs-lookup"><span data-stu-id="d8fda-109">Remarks</span></span>

<span data-ttu-id="d8fda-110">En la generación de varios eventos pueden ocasionar que los cambios realizados en los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="d8fda-110">Changes to Calendar items may result in the generation of multiple events.</span></span> <span data-ttu-id="d8fda-111">Estos eventos son el resultado de elementos temporales que se crean en el buzón de correo, los elementos de almacenamiento de datos de disponibilidad que se está cambiando como parte de las operaciones de calendario normales, o ambos.</span><span class="sxs-lookup"><span data-stu-id="d8fda-111">These events are the result of temporary items being created in the mailbox, free/busy data storage items being changed as part of the normal Calendar operations, or both.</span></span> <span data-ttu-id="d8fda-112">Eventos de elemento de clase "IPM. SchedulePlus.FreeBusy.BinaryData"se debe omitir los clientes de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="d8fda-112">Events for item class "IPM.SchedulePlus.FreeBusy.BinaryData" should be ignored by Web service clients.</span></span> <span data-ttu-id="d8fda-113">Estos elementos temporales se eliminan después de que se crean; por lo tanto, si se realiza un intento para recuperar estos elementos, un error se devolverán que indica que no se encontró el elemento.</span><span class="sxs-lookup"><span data-stu-id="d8fda-113">These temporary items are deleted after they are created; therefore, if an attempt is made to retrieve these items, an error will be returned that states that the item was not found.</span></span>
  
## <a name="getevents-request-example"></a><span data-ttu-id="d8fda-114">Ejemplo de solicitud GetEvents</span><span class="sxs-lookup"><span data-stu-id="d8fda-114">GetEvents request example</span></span>

### <a name="description"></a><span data-ttu-id="d8fda-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8fda-115">Description</span></span>

<span data-ttu-id="d8fda-116">En el ejemplo siguiente se muestra cómo solicitar los eventos y los elementos que están asociados con una suscripción que se identifica con el identificador de suscripción y la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="d8fda-116">The following example shows how to request the events and items that are associated with a subscription that is identified by the subscription identifier and watermark.</span></span>
  
### <a name="code"></a><span data-ttu-id="d8fda-117">Código</span><span class="sxs-lookup"><span data-stu-id="d8fda-117">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a><span data-ttu-id="d8fda-118">Elementos de solicitudes GetEvents</span><span class="sxs-lookup"><span data-stu-id="d8fda-118">GetEvents Request Elements</span></span>

<span data-ttu-id="d8fda-119">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d8fda-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d8fda-120">GetEvents</span><span class="sxs-lookup"><span data-stu-id="d8fda-120">GetEvents</span></span>](getevents.md)
    
- [<span data-ttu-id="d8fda-121">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="d8fda-121">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="d8fda-122">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="d8fda-122">Watermark</span></span>](watermark.md)
    
## <a name="successful-getevents-response-example"></a><span data-ttu-id="d8fda-123">Ejemplo de respuesta correcta de GetEvents</span><span class="sxs-lookup"><span data-stu-id="d8fda-123">Successful GetEvents response example</span></span>

### <a name="description"></a><span data-ttu-id="d8fda-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8fda-124">Description</span></span>

<span data-ttu-id="d8fda-125">El siguiente ejemplo de una respuesta muestra una notificación de la existencia de dos nuevos mensajes de correo desde que se envió la última solicitud de notificación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d8fda-125">The following example of a response shows a notification of the existence of two new mail messages since the last notification request was sent to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="d8fda-126">Código</span><span class="sxs-lookup"><span data-stu-id="d8fda-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:PreviousWatermark>AAAAAMAGAAAAAAAAAQ==</t:PreviousWatermark>
            <t:MoreEvents>false</t:MoreEvents>
            <t:NewMailEvent>
              <t:Watermark>AAAAAM4GAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T00:36:29Z</t:TimeStamp>
              <t:ItemId Id="AQApAHR" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:NewMailEvent>
              <t:Watermark>AAAAAOQGAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T01:00:50Z</t:TimeStamp>
              <t:ItemId Id="AQApAHRw" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
          </m:Notification>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="d8fda-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8fda-127">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="d8fda-128">Los identificadores de elemento y carpeta se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d8fda-128">The item and folder identifiers have been shortened to preserve readability.</span></span> 
  
### <a name="getevents-response-elements"></a><span data-ttu-id="d8fda-129">Elementos de respuesta GetEvents</span><span class="sxs-lookup"><span data-stu-id="d8fda-129">GetEvents response elements</span></span>

<span data-ttu-id="d8fda-130">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d8fda-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d8fda-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d8fda-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d8fda-132">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="d8fda-132">GetEventsResponse</span></span>](geteventsresponse.md)
    
- [<span data-ttu-id="d8fda-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d8fda-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d8fda-134">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d8fda-134">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md)
    
- [<span data-ttu-id="d8fda-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d8fda-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d8fda-136">Notificación</span><span class="sxs-lookup"><span data-stu-id="d8fda-136">Notification</span></span>](notification-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d8fda-137">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="d8fda-137">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="d8fda-138">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="d8fda-138">PreviousWatermark</span></span>](previouswatermark.md)
    
- [<span data-ttu-id="d8fda-139">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="d8fda-139">MoreEvents</span></span>](moreevents.md)
    
- [<span data-ttu-id="d8fda-140">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="d8fda-140">NewMailEvent</span></span>](newmailevent.md)
    
- [<span data-ttu-id="d8fda-141">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="d8fda-141">Watermark</span></span>](watermark.md)
    
- [<span data-ttu-id="d8fda-142">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="d8fda-142">TimeStamp</span></span>](timestamp.md)
    
- [<span data-ttu-id="d8fda-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="d8fda-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="d8fda-144">Id</span><span class="sxs-lookup"><span data-stu-id="d8fda-144">ParentFolderId</span></span>](parentfolderid.md)
    
<span data-ttu-id="d8fda-145">Para buscar otras opciones para el mensaje de respuesta de la operación **GetEvents** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="d8fda-145">To find other options for the response message of the **GetEvents** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="d8fda-146">Comenzar en el elemento de [notificación](notification-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="d8fda-146">Start at the [Notification](notification-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="getevents-error-response-example"></a><span data-ttu-id="d8fda-147">Ejemplo de respuesta de GetEvents Error</span><span class="sxs-lookup"><span data-stu-id="d8fda-147">GetEvents Error response example</span></span>

### <a name="description"></a><span data-ttu-id="d8fda-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8fda-148">Description</span></span>

<span data-ttu-id="d8fda-149">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **GetEvents** .</span><span class="sxs-lookup"><span data-stu-id="d8fda-149">The following example shows an error response to a **GetEvents** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d8fda-150">Código</span><span class="sxs-lookup"><span data-stu-id="d8fda-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Error">
          <m:MessageText>Access is denied. Only the subscription owner may access the subscription.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionAccessDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a><span data-ttu-id="d8fda-151">Notas</span><span class="sxs-lookup"><span data-stu-id="d8fda-151">Remarks</span></span>

<span data-ttu-id="d8fda-152">Cuando se procesa una solicitud **GetEvents** , el servidor de acceso de cliente lleva a cabo los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="d8fda-152">When processing a **GetEvents** request, the Client Access server performs the following steps:</span></span> 
  
1. <span data-ttu-id="d8fda-153">El identificador de suscripción de la solicitud es confirmado como una suscripción válida que se hospeda en el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d8fda-153">The SubscriptionID of the request is confirmed to be a valid subscription that is hosted on the Client Access server.</span></span> <span data-ttu-id="d8fda-154">Si no es así, se produce un error en la llamada **GetEvents** .</span><span class="sxs-lookup"><span data-stu-id="d8fda-154">If it is not, the **GetEvents** call fails.</span></span> 
    
2. <span data-ttu-id="d8fda-155">La dirección SMTP del usuario autenticado para la solicitud se compara con la dirección SMTP del usuario que creó la suscripción.</span><span class="sxs-lookup"><span data-stu-id="d8fda-155">The SMTP address of the authenticated user for the request is compared to the SMTP address of the user who created the subscription.</span></span> <span data-ttu-id="d8fda-156">Si no coinciden, se produce un error en la solicitud de **GetEvents** .</span><span class="sxs-lookup"><span data-stu-id="d8fda-156">If they do not match, the **GetEvents** request fails.</span></span> 
    
3. <span data-ttu-id="d8fda-157">La cola de suscripción se consulta para los eventos que se esperan que se envíen al cliente.</span><span class="sxs-lookup"><span data-stu-id="d8fda-157">The subscription queue is queried for events that are waiting to be sent to the client.</span></span> <span data-ttu-id="d8fda-158">Si la cola no está vacía, los 50 primeros eventos de la cola se extrae de la cola y codificados en una notificación.</span><span class="sxs-lookup"><span data-stu-id="d8fda-158">If the queue is not empty, the first 50 events from the queue are pulled from the queue and encoded into a notification.</span></span>
    
4. <span data-ttu-id="d8fda-159">Si no se encontraron eventos en la cola, un objeto StatusEvent se genera y se codifican en una respuesta de notificación.</span><span class="sxs-lookup"><span data-stu-id="d8fda-159">If no events are found in the queue, a StatusEvent is generated and encoded into a notification response.</span></span>
    
5. <span data-ttu-id="d8fda-160">La respuesta de notificación se devuelve al cliente.</span><span class="sxs-lookup"><span data-stu-id="d8fda-160">The notification response is returned to the client.</span></span>
    
6. <span data-ttu-id="d8fda-161">Se quitan los eventos que se incluyen en la notificación de la cola de suscripción y se establece el acceso de cliente local última marca de agua server para la suscripción a la marca de agua del último evento que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="d8fda-161">The events that are included in the notification are removed from the subscription queue and the Client Access server local last watermark for the subscription is set to the watermark of the last event that is returned.</span></span>
    
7. <span data-ttu-id="d8fda-162">Se restablece el temporizador de tiempo de espera de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="d8fda-162">The timeout timer for the subscription is reset.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8fda-163">Ver también</span><span class="sxs-lookup"><span data-stu-id="d8fda-163">See also</span></span>



[<span data-ttu-id="d8fda-164">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="d8fda-164">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="d8fda-165">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="d8fda-165">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="d8fda-166">Uso de las suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="d8fda-166">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)


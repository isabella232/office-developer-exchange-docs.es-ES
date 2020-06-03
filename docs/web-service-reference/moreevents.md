---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: El elemento MoreEvents indica si hay más eventos en la cola que se entreguen al cliente.
ms.openlocfilehash: fd12dd2e2e64ce1711e553ba5eb29bd0eb64c892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462734"
---
# <a name="moreevents"></a><span data-ttu-id="90700-103">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="90700-103">MoreEvents</span></span>

<span data-ttu-id="90700-104">El elemento **MoreEvents** indica si hay más eventos en la cola que se entreguen al cliente.</span><span class="sxs-lookup"><span data-stu-id="90700-104">The **MoreEvents** element indicates whether there are more events in the queue to be delivered to the client.</span></span> 
  
```xml
<MoreEvents/>
```

 <span data-ttu-id="90700-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="90700-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90700-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="90700-106">Attributes and elements</span></span>

<span data-ttu-id="90700-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="90700-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90700-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="90700-108">Attributes</span></span>

<span data-ttu-id="90700-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="90700-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90700-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90700-110">Child elements</span></span>

<span data-ttu-id="90700-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="90700-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="90700-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="90700-112">Parent elements</span></span>

|<span data-ttu-id="90700-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="90700-113">**Element**</span></span>|<span data-ttu-id="90700-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90700-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90700-115">Notificación</span><span class="sxs-lookup"><span data-stu-id="90700-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="90700-116">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="90700-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="90700-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="90700-117">Text value</span></span>

<span data-ttu-id="90700-118">El valor de texto representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="90700-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="90700-119">Un valor de **true** indica que hay más eventos en la cola.</span><span class="sxs-lookup"><span data-stu-id="90700-119">A value of **true** indicates that more events are in the queue.</span></span> <span data-ttu-id="90700-120">Un valor de **false** indica que no hay más eventos en la cola.</span><span class="sxs-lookup"><span data-stu-id="90700-120">A value of **false** indicates that no more events are in the queue.</span></span> <span data-ttu-id="90700-121">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="90700-121">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90700-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90700-122">Remarks</span></span>

<span data-ttu-id="90700-123">En el caso de las notificaciones de extracción, un valor **true** en este elemento indica al cliente que se debe emitir otra solicitud GetEvents para obtener los eventos restantes.</span><span class="sxs-lookup"><span data-stu-id="90700-123">In the case of Pull notifications, a **true** value in this element indicates to the client that another GetEvents request should be issued to get the remaining events.</span></span> <span data-ttu-id="90700-124">Si se supone que las especificaciones de cliente requieren una latencia mínima para las notificaciones de eventos, las solicitudes GetEvents deben continuar en una sucesión continua hasta que se devuelva un valor **MoreEvents** **falso** .</span><span class="sxs-lookup"><span data-stu-id="90700-124">Assuming that the client specifications require minimum latency for event notifications, GetEvents requests should continue in a continuous succession until a **false** **MoreEvents** value is returned.</span></span> 
  
<span data-ttu-id="90700-125">En el caso de las notificaciones de inserción, un valor **true** para **MoreEvents** indica al cliente que se enviará al cliente otra solicitud de notificación para entregar los eventos restantes.</span><span class="sxs-lookup"><span data-stu-id="90700-125">In the case of Push notifications, a **true** value for **MoreEvents** indicates to the client that another notification request will be sent to the client to deliver the remaining events.</span></span> <span data-ttu-id="90700-126">De forma similar a las notificaciones de extracción, estas solicitudes de seguimiento continuarán en sucesión continuas hasta que la cola de eventos del servidor de acceso de cliente esté vacía.</span><span class="sxs-lookup"><span data-stu-id="90700-126">Similar to Pull notifications, these follow-up requests will continue in continuous succession until the event queue on the Client Access server is empty.</span></span> 
  
<span data-ttu-id="90700-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="90700-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90700-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="90700-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90700-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="90700-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="90700-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="90700-130">Schema Name</span></span>  <br/> |<span data-ttu-id="90700-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="90700-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="90700-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="90700-132">Validation File</span></span>  <br/> |<span data-ttu-id="90700-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="90700-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="90700-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="90700-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="90700-135">Falso</span><span class="sxs-lookup"><span data-stu-id="90700-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90700-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="90700-136">See also</span></span>



[<span data-ttu-id="90700-137">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="90700-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="90700-138">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="90700-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="90700-139">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="90700-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)


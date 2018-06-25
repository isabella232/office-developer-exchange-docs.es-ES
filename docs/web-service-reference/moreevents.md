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
description: El elemento MoreEvents indica si hay más eventos en la cola para entregar al cliente.
ms.openlocfilehash: cc3f7ed3b4b5f5ce27a9d45d508506bfa62e5086
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836489"
---
# <a name="moreevents"></a><span data-ttu-id="f4d17-103">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="f4d17-103">MoreEvents</span></span>

<span data-ttu-id="f4d17-104">El elemento **MoreEvents** indica si hay más eventos en la cola para entregar al cliente.</span><span class="sxs-lookup"><span data-stu-id="f4d17-104">The **MoreEvents** element indicates whether there are more events in the queue to be delivered to the client.</span></span> 
  
```xml
<MoreEvents/>
```

 <span data-ttu-id="f4d17-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f4d17-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4d17-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f4d17-106">Attributes and elements</span></span>

<span data-ttu-id="f4d17-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f4d17-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4d17-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4d17-108">Attributes</span></span>

<span data-ttu-id="f4d17-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4d17-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4d17-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4d17-110">Child elements</span></span>

<span data-ttu-id="f4d17-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4d17-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f4d17-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4d17-112">Parent elements</span></span>

|<span data-ttu-id="f4d17-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4d17-113">**Element**</span></span>|<span data-ttu-id="f4d17-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4d17-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4d17-115">Notificación</span><span class="sxs-lookup"><span data-stu-id="f4d17-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f4d17-116">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="f4d17-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f4d17-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f4d17-117">Text value</span></span>

<span data-ttu-id="f4d17-118">El valor de texto representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="f4d17-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="f4d17-119">Un valor de **true** indica que son más eventos en la cola.</span><span class="sxs-lookup"><span data-stu-id="f4d17-119">A value of **true** indicates that more events are in the queue.</span></span> <span data-ttu-id="f4d17-120">Un valor de **false** indica que no hay más eventos están en la cola.</span><span class="sxs-lookup"><span data-stu-id="f4d17-120">A value of **false** indicates that no more events are in the queue.</span></span> <span data-ttu-id="f4d17-121">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4d17-121">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4d17-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4d17-122">Remarks</span></span>

<span data-ttu-id="f4d17-123">En el caso de las notificaciones de extracción, un valor **true** en este elemento indica al cliente que se debe emitir otra solicitud GetEvents para obtener los eventos restantes.</span><span class="sxs-lookup"><span data-stu-id="f4d17-123">In the case of Pull notifications, a **true** value in this element indicates to the client that another GetEvents request should be issued to get the remaining events.</span></span> <span data-ttu-id="f4d17-124">Suponiendo que las especificaciones de cliente necesitan la latencia mínima para las notificaciones de eventos, Solicitudes GetEvents deberían seguir en una sucesión continua hasta que se devuelve **false** el valor de **MoreEvents** .</span><span class="sxs-lookup"><span data-stu-id="f4d17-124">Assuming that the client specifications require minimum latency for event notifications, GetEvents requests should continue in a continuous succession until a **false** **MoreEvents** value is returned.</span></span> 
  
<span data-ttu-id="f4d17-125">En el caso de las notificaciones de inserción, indica un valor **true** para **MoreEvents** al cliente que otra solicitud de notificación se enviarán al cliente para ofrecer los eventos restantes.</span><span class="sxs-lookup"><span data-stu-id="f4d17-125">In the case of Push notifications, a **true** value for **MoreEvents** indicates to the client that another notification request will be sent to the client to deliver the remaining events.</span></span> <span data-ttu-id="f4d17-126">Al igual que las notificaciones de extracción, estas solicitudes seguimiento continuará en sucesión continua hasta que la cola de eventos en el servidor de acceso de cliente está vacía.</span><span class="sxs-lookup"><span data-stu-id="f4d17-126">Similar to Pull notifications, these follow-up requests will continue in continuous succession until the event queue on the Client Access server is empty.</span></span> 
  
<span data-ttu-id="f4d17-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f4d17-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4d17-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4d17-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4d17-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4d17-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4d17-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f4d17-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f4d17-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f4d17-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4d17-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f4d17-132">Validation File</span></span>  <br/> |<span data-ttu-id="f4d17-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f4d17-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4d17-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f4d17-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4d17-135">False</span><span class="sxs-lookup"><span data-stu-id="f4d17-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4d17-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4d17-136">See also</span></span>



[<span data-ttu-id="f4d17-137">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="f4d17-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="f4d17-138">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="f4d17-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="f4d17-139">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="f4d17-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)


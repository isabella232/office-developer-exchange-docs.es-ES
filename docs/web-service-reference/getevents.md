---
title: GetEvents
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
ms.assetid: 22d4da6b-d8a8-484f-82c4-3e4b8f5431cd
description: El elemento GetEvents representa la operación usada por los clientes de extracción para las notificaciones de solicitud desde el servidor.
ms.openlocfilehash: e7b24207bff579a2f5230676d6520452f96fe0ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764820"
---
# <a name="getevents"></a><span data-ttu-id="6f30b-103">GetEvents</span><span class="sxs-lookup"><span data-stu-id="6f30b-103">GetEvents</span></span>

<span data-ttu-id="6f30b-104">El elemento **GetEvents** representa la operación usada por los clientes de extracción para las notificaciones de solicitud desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="6f30b-104">The **GetEvents** element represents the operation used by pull clients to request notifications from the server.</span></span> 
  
[<span data-ttu-id="6f30b-105">GetEvents</span><span class="sxs-lookup"><span data-stu-id="6f30b-105">GetEvents</span></span>](getevents.md)
  
```xml
<GetEvents>
   <SubscriptionId/>
   <Watermark/>
</GetEvents>
```

 <span data-ttu-id="6f30b-106">**GetEventsType**</span><span class="sxs-lookup"><span data-stu-id="6f30b-106">**GetEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f30b-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f30b-107">Attributes and elements</span></span>

<span data-ttu-id="6f30b-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f30b-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f30b-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f30b-109">Attributes</span></span>

<span data-ttu-id="6f30b-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f30b-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f30b-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f30b-111">Child elements</span></span>

|<span data-ttu-id="6f30b-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f30b-112">**Element**</span></span>|<span data-ttu-id="6f30b-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f30b-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f30b-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="6f30b-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="6f30b-115">Representa el identificador para una suscripción que se consulta para los eventos.</span><span class="sxs-lookup"><span data-stu-id="6f30b-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="6f30b-116">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="6f30b-116">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="6f30b-117">Representa la última marca de agua devuelta al cliente.</span><span class="sxs-lookup"><span data-stu-id="6f30b-117">Represents the last watermark returned to the client.</span></span> <span data-ttu-id="6f30b-118">Si no se ha llamado al GetEvents para esta suscripción, el cliente utiliza la marca de agua devuelto desde la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="6f30b-118">If GetEvents has not been called for this subscription, the client uses the watermark returned from the Subscribe request.</span></span> <span data-ttu-id="6f30b-119">De lo contrario, se utiliza la marca de agua desde el último evento de la última respuesta GetEvents.</span><span class="sxs-lookup"><span data-stu-id="6f30b-119">Otherwise, the watermark from the last event in the last GetEvents response is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f30b-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f30b-120">Parent elements</span></span>

<span data-ttu-id="6f30b-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f30b-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f30b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f30b-122">Remarks</span></span>

<span data-ttu-id="6f30b-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6f30b-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f30b-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6f30b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f30b-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f30b-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f30b-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6f30b-126">Schema name</span></span>  <br/> |<span data-ttu-id="6f30b-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6f30b-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f30b-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6f30b-128">Validation file</span></span>  <br/> |<span data-ttu-id="6f30b-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6f30b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f30b-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f30b-130">Can be empty</span></span>  <br/> |<span data-ttu-id="6f30b-131">falso</span><span class="sxs-lookup"><span data-stu-id="6f30b-131">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f30b-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="6f30b-132">See also</span></span>



[<span data-ttu-id="6f30b-133">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="6f30b-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="6f30b-134">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="6f30b-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="6f30b-135">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="6f30b-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)


---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: El elemento PreviousWatermark representa la marca de agua del evento más reciente que se ha comunicado correctamente al cliente para la suscripción.
ms.openlocfilehash: 93c6f90d0866ae13618391b8544ab593fe33922b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836886"
---
# <a name="previouswatermark"></a><span data-ttu-id="055d8-103">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="055d8-103">PreviousWatermark</span></span>

<span data-ttu-id="055d8-104">El elemento **PreviousWatermark** representa la marca de agua del evento más reciente que se ha comunicado correctamente al cliente para la suscripción.</span><span class="sxs-lookup"><span data-stu-id="055d8-104">The **PreviousWatermark** element represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span> 
  
```xml
<PreviousWatermark/>
```

 <span data-ttu-id="055d8-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="055d8-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="055d8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="055d8-106">Attributes and elements</span></span>

<span data-ttu-id="055d8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="055d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="055d8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="055d8-108">Attributes</span></span>

<span data-ttu-id="055d8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="055d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="055d8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="055d8-110">Child elements</span></span>

<span data-ttu-id="055d8-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="055d8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="055d8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="055d8-112">Parent elements</span></span>

|<span data-ttu-id="055d8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="055d8-113">**Element**</span></span>|<span data-ttu-id="055d8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="055d8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="055d8-115">Notificación</span><span class="sxs-lookup"><span data-stu-id="055d8-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="055d8-116">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="055d8-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="055d8-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="055d8-117">Text value</span></span>

<span data-ttu-id="055d8-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="055d8-118">A text value is required.</span></span> <span data-ttu-id="055d8-119">El valor de texto representa la última marca de agua.</span><span class="sxs-lookup"><span data-stu-id="055d8-119">The text value represents the latest watermark.</span></span> <span data-ttu-id="055d8-120">El valor de texto no puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="055d8-120">The text value cannot be an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="055d8-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="055d8-121">Remarks</span></span>

<span data-ttu-id="055d8-122">La propiedad **PreviousWatermark** es útil para el cliente en la determinación de la última notificación correcta.</span><span class="sxs-lookup"><span data-stu-id="055d8-122">The **PreviousWatermark** property is useful to the client in determining the last successful notification.</span></span> <span data-ttu-id="055d8-123">Por ejemplo, si una suscripción tiene tres eventos con marcas de agua de 1, 2 y 3, y se envía la notificación siguiente con un valor de **PreviousWatermark** de 3, el cliente puede comparar este valor en el valor de marca de agua de la última notificación recibida.</span><span class="sxs-lookup"><span data-stu-id="055d8-123">For example, if a subscription has three events with watermarks 1, 2, and 3, and the next notification is sent with a **PreviousWatermark** value of 3, the client can compare this value to the Watermark value of the last notification received.</span></span> <span data-ttu-id="055d8-124">Esto permite que el cliente garantizar la continuidad de eventos.</span><span class="sxs-lookup"><span data-stu-id="055d8-124">This enables the client to ensure the continuity of events.</span></span> 
  
<span data-ttu-id="055d8-125">Para los clientes de inserción, el **PreviousWatermark** se compara con la local, de cliente última conocido marca de agua.</span><span class="sxs-lookup"><span data-stu-id="055d8-125">For push clients, the **PreviousWatermark** is compared to the local, client-side last known watermark.</span></span> <span data-ttu-id="055d8-126">Si los valores son diferentes, el cliente no ha realizado una notificación de eventos y debe volver a establecer una suscripción mediante el uso de la marca de agua local más reciente.</span><span class="sxs-lookup"><span data-stu-id="055d8-126">If the values are different, the client has missed an event notification and should reestablish a subscription by using the latest local watermark.</span></span> <span data-ttu-id="055d8-127">Por ejemplo, si un cliente de inserción recibe tres eventos para una suscripción con marcas de agua de 1, 2 y 3, y la siguiente notificación viene con un valor de **PreviousWatermark** de 5, el cliente no ha realizado al menos una notificación y debe crear una nueva suscripción, pasando un 3 como la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="055d8-127">For example, if a push client receives three events for a subscription with watermarks 1, 2, and 3, and the next notification comes with a **PreviousWatermark** value of 5, the client has missed at least one notification and should create a new subscription, passing a 3 as the watermark.</span></span> 
  
<span data-ttu-id="055d8-128">En el caso de un cliente de extracción, el valor de **PreviousWatermark** será la misma que la [marca de agua](watermark.md) incluidas por el cliente en la llamada GetEvents.</span><span class="sxs-lookup"><span data-stu-id="055d8-128">In the case of a pull client, the value of **PreviousWatermark** will be the same as the [Watermark](watermark.md) included by the client in the GetEvents call.</span></span> 
  
<span data-ttu-id="055d8-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="055d8-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="055d8-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="055d8-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="055d8-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="055d8-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="055d8-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="055d8-132">Schema Name</span></span>  <br/> |<span data-ttu-id="055d8-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="055d8-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="055d8-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="055d8-134">Validation File</span></span>  <br/> |<span data-ttu-id="055d8-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="055d8-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="055d8-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="055d8-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="055d8-137">False</span><span class="sxs-lookup"><span data-stu-id="055d8-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="055d8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="055d8-138">See also</span></span>



[<span data-ttu-id="055d8-139">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="055d8-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="055d8-140">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="055d8-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="055d8-141">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="055d8-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


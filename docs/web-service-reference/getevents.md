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
description: El elemento GetEvents representa la operación usada por los clientes de extracción para solicitar notificaciones del servidor.
ms.openlocfilehash: 004f782ccd32b3c5e501080bfc59419a6e7d9ce4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462503"
---
# <a name="getevents"></a><span data-ttu-id="39c88-103">GetEvents</span><span class="sxs-lookup"><span data-stu-id="39c88-103">GetEvents</span></span>

<span data-ttu-id="39c88-104">El elemento **GetEvents** representa la operación usada por los clientes de extracción para solicitar notificaciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="39c88-104">The **GetEvents** element represents the operation used by pull clients to request notifications from the server.</span></span> 
  
[<span data-ttu-id="39c88-105">GetEvents</span><span class="sxs-lookup"><span data-stu-id="39c88-105">GetEvents</span></span>](getevents.md)
  
```xml
<GetEvents>
   <SubscriptionId/>
   <Watermark/>
</GetEvents>
```

 <span data-ttu-id="39c88-106">**GetEventsType**</span><span class="sxs-lookup"><span data-stu-id="39c88-106">**GetEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39c88-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="39c88-107">Attributes and elements</span></span>

<span data-ttu-id="39c88-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="39c88-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39c88-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="39c88-109">Attributes</span></span>

<span data-ttu-id="39c88-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="39c88-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39c88-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="39c88-111">Child elements</span></span>

|<span data-ttu-id="39c88-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="39c88-112">**Element**</span></span>|<span data-ttu-id="39c88-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39c88-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39c88-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="39c88-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="39c88-115">Representa el identificador de una suscripción que se consulta para eventos.</span><span class="sxs-lookup"><span data-stu-id="39c88-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="39c88-116">Watermark</span><span class="sxs-lookup"><span data-stu-id="39c88-116">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="39c88-117">Representa la última marca de agua devuelta al cliente.</span><span class="sxs-lookup"><span data-stu-id="39c88-117">Represents the last watermark returned to the client.</span></span> <span data-ttu-id="39c88-118">Si no se ha llamado GetEvents para esta suscripción, el cliente usa la marca de agua que devuelve la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="39c88-118">If GetEvents has not been called for this subscription, the client uses the watermark returned from the Subscribe request.</span></span> <span data-ttu-id="39c88-119">De lo contrario, se usa la marca de agua del último evento en la última respuesta GetEvents.</span><span class="sxs-lookup"><span data-stu-id="39c88-119">Otherwise, the watermark from the last event in the last GetEvents response is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39c88-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="39c88-120">Parent elements</span></span>

<span data-ttu-id="39c88-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="39c88-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39c88-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39c88-122">Remarks</span></span>

<span data-ttu-id="39c88-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="39c88-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39c88-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="39c88-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39c88-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="39c88-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="39c88-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="39c88-126">Schema name</span></span>  <br/> |<span data-ttu-id="39c88-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="39c88-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="39c88-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="39c88-128">Validation file</span></span>  <br/> |<span data-ttu-id="39c88-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="39c88-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39c88-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="39c88-130">Can be empty</span></span>  <br/> |<span data-ttu-id="39c88-131">false</span><span class="sxs-lookup"><span data-stu-id="39c88-131">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39c88-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="39c88-132">See also</span></span>



[<span data-ttu-id="39c88-133">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="39c88-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="39c88-134">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="39c88-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="39c88-135">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="39c88-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)


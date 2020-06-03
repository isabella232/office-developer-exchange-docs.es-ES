---
title: SubscriptionId (GetEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionId
api_type:
- schema
ms.assetid: 77c0abab-69e8-428e-8c20-22258e4ef71b
description: El elemento SubscriptionId representa el identificador de una suscripción.
ms.openlocfilehash: e103386f466d65717878b4a6c811f3c3ad6e7c7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465355"
---
# <a name="subscriptionid-getevents"></a><span data-ttu-id="8cce1-103">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="8cce1-103">SubscriptionId (GetEvents)</span></span>

<span data-ttu-id="8cce1-104">El elemento **SubscriptionId** representa el identificador de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="8cce1-104">The **SubscriptionId** element represents the identifier for a subscription.</span></span> 
  
```xml
<SubscriptionId/>
```

 <span data-ttu-id="8cce1-105">**SubscriptionIdType**</span><span class="sxs-lookup"><span data-stu-id="8cce1-105">**SubscriptionIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8cce1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8cce1-106">Attributes and elements</span></span>

<span data-ttu-id="8cce1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8cce1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8cce1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8cce1-108">Attributes</span></span>

<span data-ttu-id="8cce1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8cce1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8cce1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8cce1-110">Child elements</span></span>

<span data-ttu-id="8cce1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8cce1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8cce1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8cce1-112">Parent elements</span></span>

|<span data-ttu-id="8cce1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8cce1-113">**Element**</span></span>|<span data-ttu-id="8cce1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8cce1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cce1-115">GetEvents</span><span class="sxs-lookup"><span data-stu-id="8cce1-115">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="8cce1-116">Representa la operación usada por los clientes de extracción para solicitar notificaciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="8cce1-116">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="8cce1-117">Notificación</span><span class="sxs-lookup"><span data-stu-id="8cce1-117">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8cce1-118">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="8cce1-118">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="8cce1-119">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8cce1-119">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="8cce1-120">Contiene el estado y el resultado de una solicitud subscribe.</span><span class="sxs-lookup"><span data-stu-id="8cce1-120">Contains the status and result of a Subscribe request.</span></span>  <br/> |
|[<span data-ttu-id="8cce1-121">Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="8cce1-121">Unsubscribe</span></span>](unsubscribe.md) <br/> |<span data-ttu-id="8cce1-122">Contiene las propiedades usadas para cancelar la suscripción de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="8cce1-122">Contains the properties used to unsubscribe from a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8cce1-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8cce1-123">Text value</span></span>

<span data-ttu-id="8cce1-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="8cce1-124">A text value is required.</span></span> <span data-ttu-id="8cce1-125">El valor de texto es un GUID.</span><span class="sxs-lookup"><span data-stu-id="8cce1-125">The text value is a GUID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8cce1-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cce1-126">Remarks</span></span>

<span data-ttu-id="8cce1-127">El GUID que representa el identificador de suscripción lo genera el servidor de acceso de cliente cuando se crea la suscripción.</span><span class="sxs-lookup"><span data-stu-id="8cce1-127">The GUID that represents the subscription identifier is generated by the Client Access server when the subscription is created.</span></span>
  
<span data-ttu-id="8cce1-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8cce1-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8cce1-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8cce1-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cce1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cce1-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8cce1-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8cce1-131">Schema name</span></span>  <br/> |<span data-ttu-id="8cce1-132">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8cce1-132">messages schema</span></span>  <br/> |
|<span data-ttu-id="8cce1-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8cce1-133">Validation file</span></span>  <br/> |<span data-ttu-id="8cce1-134">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8cce1-134">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8cce1-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8cce1-135">Can be empty</span></span>  <br/> |<span data-ttu-id="8cce1-136">Falso</span><span class="sxs-lookup"><span data-stu-id="8cce1-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cce1-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cce1-137">See also</span></span>



[<span data-ttu-id="8cce1-138">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="8cce1-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="8cce1-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="8cce1-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="8cce1-140">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="8cce1-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


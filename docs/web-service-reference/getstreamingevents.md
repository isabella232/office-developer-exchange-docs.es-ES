---
title: GetStreamingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: dbe83857-c4f8-4d98-813f-e03c289697a1
description: El elemento GetStreamingEvents representa la operación que usan los clientes para solicitar notificaciones de transmisión por secuencias desde el servidor.
ms.openlocfilehash: ec133ecd69c05a2208e95f925133570af0233cf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457322"
---
# <a name="getstreamingevents"></a><span data-ttu-id="af698-103">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="af698-103">GetStreamingEvents</span></span>

<span data-ttu-id="af698-104">El elemento **GetStreamingEvents** representa la operación que usan los clientes para solicitar notificaciones de transmisión por secuencias desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="af698-104">The **GetStreamingEvents** element represents the operation that is used by clients to request streaming notifications from the server.</span></span> 
  
[<span data-ttu-id="af698-105">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="af698-105">GetStreamingEvents</span></span>](getstreamingevents.md)
  
```XML
<GetStreamingEvents>
   <SubscriptionId/>
   <ConnectionTimeout/>
</GetStreamingEvents>
```

 <span data-ttu-id="af698-106">**GetStreamingEventsType**</span><span class="sxs-lookup"><span data-stu-id="af698-106">**GetStreamingEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af698-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="af698-107">Attributes and elements</span></span>

<span data-ttu-id="af698-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="af698-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af698-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="af698-109">Attributes</span></span>

<span data-ttu-id="af698-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="af698-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af698-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="af698-111">Child elements</span></span>

|<span data-ttu-id="af698-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af698-112">**Element**</span></span>|<span data-ttu-id="af698-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af698-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af698-114">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="af698-114">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md) <br/> |<span data-ttu-id="af698-115">Representa el identificador de una suscripción que se consulta para eventos.</span><span class="sxs-lookup"><span data-stu-id="af698-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="af698-116">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="af698-116">ConnectionTimeout</span></span>](connectiontimeout.md) <br/> |<span data-ttu-id="af698-117">Representa el número de minutos que se debe mantener abierta una conexión.</span><span class="sxs-lookup"><span data-stu-id="af698-117">Represents the number of minutes to keep a connection open.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af698-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="af698-118">Parent elements</span></span>

<span data-ttu-id="af698-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="af698-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="af698-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="af698-120">Text value</span></span>

<span data-ttu-id="af698-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="af698-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af698-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af698-122">Remarks</span></span>

<span data-ttu-id="af698-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="af698-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af698-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="af698-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af698-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="af698-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="af698-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="af698-126">Schema name</span></span>  <br/> |<span data-ttu-id="af698-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="af698-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="af698-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="af698-128">Validation file</span></span>  <br/> |<span data-ttu-id="af698-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="af698-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="af698-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="af698-130">Can be empty</span></span>  <br/> |<span data-ttu-id="af698-131">Falso</span><span class="sxs-lookup"><span data-stu-id="af698-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af698-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="af698-132">See also</span></span>



[<span data-ttu-id="af698-133">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="af698-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="af698-134">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="af698-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="af698-135">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="af698-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="af698-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="af698-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


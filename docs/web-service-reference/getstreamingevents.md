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
description: El elemento GetStreamingEvents representa la operación que se usa en los clientes para solicitar las notificaciones de transmisión por secuencias desde el servidor.
ms.openlocfilehash: b07015541cf9c2fbbbc11ebc9f10421bdb9ee84f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835679"
---
# <a name="getstreamingevents"></a><span data-ttu-id="bf34b-103">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="bf34b-103">GetStreamingEvents</span></span>

<span data-ttu-id="bf34b-104">El elemento **GetStreamingEvents** representa la operación que se usa en los clientes para solicitar las notificaciones de transmisión por secuencias desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="bf34b-104">The **GetStreamingEvents** element represents the operation that is used by clients to request streaming notifications from the server.</span></span> 
  
[<span data-ttu-id="bf34b-105">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="bf34b-105">GetStreamingEvents</span></span>](getstreamingevents.md)
  
```XML
<GetStreamingEvents>
   <SubscriptionId/>
   <ConnectionTimeout/>
</GetStreamingEvents>
```

 <span data-ttu-id="bf34b-106">**GetStreamingEventsType**</span><span class="sxs-lookup"><span data-stu-id="bf34b-106">**GetStreamingEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf34b-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bf34b-107">Attributes and elements</span></span>

<span data-ttu-id="bf34b-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bf34b-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf34b-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf34b-109">Attributes</span></span>

<span data-ttu-id="bf34b-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bf34b-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf34b-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bf34b-111">Child elements</span></span>

|<span data-ttu-id="bf34b-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="bf34b-112">**Element**</span></span>|<span data-ttu-id="bf34b-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf34b-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf34b-114">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="bf34b-114">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md) <br/> |<span data-ttu-id="bf34b-115">Representa el identificador para una suscripción que se consulta para los eventos.</span><span class="sxs-lookup"><span data-stu-id="bf34b-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="bf34b-116">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="bf34b-116">ConnectionTimeout</span></span>](connectiontimeout.md) <br/> |<span data-ttu-id="bf34b-117">Representa el número de minutos que desea mantener una conexión abierta.</span><span class="sxs-lookup"><span data-stu-id="bf34b-117">Represents the number of minutes to keep a connection open.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bf34b-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bf34b-118">Parent elements</span></span>

<span data-ttu-id="bf34b-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bf34b-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="bf34b-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bf34b-120">Text value</span></span>

<span data-ttu-id="bf34b-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bf34b-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf34b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf34b-122">Remarks</span></span>

<span data-ttu-id="bf34b-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="bf34b-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf34b-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bf34b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf34b-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bf34b-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bf34b-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bf34b-126">Schema name</span></span>  <br/> |<span data-ttu-id="bf34b-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bf34b-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bf34b-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bf34b-128">Validation file</span></span>  <br/> |<span data-ttu-id="bf34b-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bf34b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bf34b-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bf34b-130">Can be empty</span></span>  <br/> |<span data-ttu-id="bf34b-131">False</span><span class="sxs-lookup"><span data-stu-id="bf34b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf34b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf34b-132">See also</span></span>



[<span data-ttu-id="bf34b-133">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="bf34b-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="bf34b-134">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="bf34b-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="bf34b-135">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="bf34b-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="bf34b-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="bf34b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


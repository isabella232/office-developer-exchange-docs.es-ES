---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: El elemento DeliveryStatus especifica el estado de un mensaje.
ms.openlocfilehash: 4e6f31e8ef4f98d8e838ba91167c7dd5d6ab2590
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764122"
---
# <a name="deliverystatus"></a><span data-ttu-id="d41d5-103">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="d41d5-103">DeliveryStatus</span></span>

<span data-ttu-id="d41d5-104">El elemento **DeliveryStatus** especifica el estado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d41d5-104">The **DeliveryStatus** element specifies the status for a message.</span></span> 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 <span data-ttu-id="d41d5-105">**MessageTrackingDeliveryStatusType**</span><span class="sxs-lookup"><span data-stu-id="d41d5-105">**MessageTrackingDeliveryStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d41d5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d41d5-106">Attributes and elements</span></span>

<span data-ttu-id="d41d5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d41d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d41d5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d41d5-108">Attributes</span></span>

<span data-ttu-id="d41d5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d41d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d41d5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d41d5-110">Child elements</span></span>

<span data-ttu-id="d41d5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d41d5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d41d5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d41d5-112">Parent elements</span></span>

|<span data-ttu-id="d41d5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d41d5-113">**Element**</span></span>|<span data-ttu-id="d41d5-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d41d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d41d5-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="d41d5-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="d41d5-116">Contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="d41d5-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d41d5-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d41d5-117">Text value</span></span>

<span data-ttu-id="d41d5-118">En la siguiente tabla se enumera los posibles valores de texto para el elemento **DeliveryStatus** .</span><span class="sxs-lookup"><span data-stu-id="d41d5-118">The following table lists the possible text values for the **DeliveryStatus** element.</span></span> 
  
<span data-ttu-id="d41d5-119">**Valores de elemento DeliveryStatus**</span><span class="sxs-lookup"><span data-stu-id="d41d5-119">**DeliveryStatus element values**</span></span>

|<span data-ttu-id="d41d5-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d41d5-120">**Value**</span></span>|<span data-ttu-id="d41d5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d41d5-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d41d5-122">Realizado correctamente</span><span class="sxs-lookup"><span data-stu-id="d41d5-122">Unsuccessful</span></span>  <br/> |<span data-ttu-id="d41d5-123">Especifica que un mensaje no se entregó.</span><span class="sxs-lookup"><span data-stu-id="d41d5-123">Specifies that a message was not delivered.</span></span>  <br/> |
|<span data-ttu-id="d41d5-124">Pendiente</span><span class="sxs-lookup"><span data-stu-id="d41d5-124">Pending</span></span>  <br/> |<span data-ttu-id="d41d5-125">Especifica que el mensaje está esperando la aprobación de un moderador.</span><span class="sxs-lookup"><span data-stu-id="d41d5-125">Specifies that the message is waiting for approval from a moderator.</span></span>  <br/> |
|<span data-ttu-id="d41d5-126">Entregado</span><span class="sxs-lookup"><span data-stu-id="d41d5-126">Delivered</span></span>  <br/> |<span data-ttu-id="d41d5-127">Especifica que el mensaje se entregó a todos los destinatarios especificados.</span><span class="sxs-lookup"><span data-stu-id="d41d5-127">Specifies that the message was delivered to all of the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="d41d5-128">Transfiere</span><span class="sxs-lookup"><span data-stu-id="d41d5-128">Transferred</span></span>  <br/> |<span data-ttu-id="d41d5-129">Especifica que el mensaje se ha transferido a un servidor fuera del ámbito de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d41d5-129">Specifies that the message was transferred to a server outside the search scope.</span></span>  <br/> |
|<span data-ttu-id="d41d5-130">Leído</span><span class="sxs-lookup"><span data-stu-id="d41d5-130">Read</span></span>  <br/> |<span data-ttu-id="d41d5-131">Especifica que el mensaje se entrega y leer los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d41d5-131">Specifies that the message was delivered and read by the recipients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d41d5-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d41d5-132">Remarks</span></span>

<span data-ttu-id="d41d5-133">El elemento **DeliveryStatus** era de tipo **MessageTrackingDeliveryStatusType** en Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d41d5-133">The **DeliveryStatus** element was of type **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span></span> 
  
<span data-ttu-id="d41d5-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d41d5-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d41d5-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d41d5-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d41d5-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d41d5-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d41d5-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d41d5-137">Schema Name</span></span>  <br/> |<span data-ttu-id="d41d5-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d41d5-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="d41d5-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d41d5-139">Validation File</span></span>  <br/> |<span data-ttu-id="d41d5-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d41d5-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d41d5-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d41d5-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="d41d5-142">False</span><span class="sxs-lookup"><span data-stu-id="d41d5-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d41d5-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d41d5-143">See also</span></span>

- [<span data-ttu-id="d41d5-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d41d5-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


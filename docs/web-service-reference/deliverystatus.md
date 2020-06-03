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
ms.openlocfilehash: ae32202284d3dd272f693fbb7b76070cb6019d28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461404"
---
# <a name="deliverystatus"></a><span data-ttu-id="d8a52-103">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="d8a52-103">DeliveryStatus</span></span>

<span data-ttu-id="d8a52-104">El elemento **DeliveryStatus** especifica el estado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d8a52-104">The **DeliveryStatus** element specifies the status for a message.</span></span> 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 <span data-ttu-id="d8a52-105">**MessageTrackingDeliveryStatusType**</span><span class="sxs-lookup"><span data-stu-id="d8a52-105">**MessageTrackingDeliveryStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8a52-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d8a52-106">Attributes and elements</span></span>

<span data-ttu-id="d8a52-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d8a52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8a52-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8a52-108">Attributes</span></span>

<span data-ttu-id="d8a52-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d8a52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8a52-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d8a52-110">Child elements</span></span>

<span data-ttu-id="d8a52-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d8a52-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d8a52-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d8a52-112">Parent elements</span></span>

|<span data-ttu-id="d8a52-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d8a52-113">**Element**</span></span>|<span data-ttu-id="d8a52-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8a52-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8a52-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="d8a52-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="d8a52-116">Contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="d8a52-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d8a52-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d8a52-117">Text value</span></span>

<span data-ttu-id="d8a52-118">En la siguiente tabla se enumeran los valores de texto posibles para el elemento **DeliveryStatus** .</span><span class="sxs-lookup"><span data-stu-id="d8a52-118">The following table lists the possible text values for the **DeliveryStatus** element.</span></span> 
  
<span data-ttu-id="d8a52-119">**Valores del elemento DeliveryStatus**</span><span class="sxs-lookup"><span data-stu-id="d8a52-119">**DeliveryStatus element values**</span></span>

|<span data-ttu-id="d8a52-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d8a52-120">**Value**</span></span>|<span data-ttu-id="d8a52-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8a52-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8a52-122">Correctamente</span><span class="sxs-lookup"><span data-stu-id="d8a52-122">Unsuccessful</span></span>  <br/> |<span data-ttu-id="d8a52-123">Especifica que no se entregó un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d8a52-123">Specifies that a message was not delivered.</span></span>  <br/> |
|<span data-ttu-id="d8a52-124">Pending</span><span class="sxs-lookup"><span data-stu-id="d8a52-124">Pending</span></span>  <br/> |<span data-ttu-id="d8a52-125">Especifica que el mensaje está esperando su aprobación de un moderador.</span><span class="sxs-lookup"><span data-stu-id="d8a52-125">Specifies that the message is waiting for approval from a moderator.</span></span>  <br/> |
|<span data-ttu-id="d8a52-126">Pronuncia</span><span class="sxs-lookup"><span data-stu-id="d8a52-126">Delivered</span></span>  <br/> |<span data-ttu-id="d8a52-127">Especifica que el mensaje se entregó a todos los destinatarios especificados.</span><span class="sxs-lookup"><span data-stu-id="d8a52-127">Specifies that the message was delivered to all of the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="d8a52-128">Transferido</span><span class="sxs-lookup"><span data-stu-id="d8a52-128">Transferred</span></span>  <br/> |<span data-ttu-id="d8a52-129">Especifica que el mensaje se transfirió a un servidor fuera del ámbito de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d8a52-129">Specifies that the message was transferred to a server outside the search scope.</span></span>  <br/> |
|<span data-ttu-id="d8a52-130">Read</span><span class="sxs-lookup"><span data-stu-id="d8a52-130">Read</span></span>  <br/> |<span data-ttu-id="d8a52-131">Especifica que el mensaje fue entregado y leído por los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d8a52-131">Specifies that the message was delivered and read by the recipients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8a52-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8a52-132">Remarks</span></span>

<span data-ttu-id="d8a52-133">El elemento **DeliveryStatus** era de tipo **MessageTrackingDeliveryStatusType** en Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d8a52-133">The **DeliveryStatus** element was of type **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span></span> 
  
<span data-ttu-id="d8a52-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8a52-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8a52-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d8a52-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8a52-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8a52-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8a52-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d8a52-137">Schema Name</span></span>  <br/> |<span data-ttu-id="d8a52-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d8a52-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="d8a52-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d8a52-139">Validation File</span></span>  <br/> |<span data-ttu-id="d8a52-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d8a52-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8a52-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d8a52-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8a52-142">Falso</span><span class="sxs-lookup"><span data-stu-id="d8a52-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8a52-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8a52-143">See also</span></span>

- [<span data-ttu-id="d8a52-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d8a52-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


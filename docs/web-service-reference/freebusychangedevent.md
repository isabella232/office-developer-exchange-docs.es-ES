---
title: FreeBusyChangedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyChangedEvent
api_type:
- schema
ms.assetid: 63abbfc5-c29f-4110-a922-6b1247187f28
description: El elemento FreeBusyChangedEvent representa un evento en el que ha cambiado la hora de disponibilidad de un elemento.
ms.openlocfilehash: d9ea8bc210ab503c4e9f606bcb66317cefe15de1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456482"
---
# <a name="freebusychangedevent"></a><span data-ttu-id="f677e-103">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="f677e-103">FreeBusyChangedEvent</span></span>

<span data-ttu-id="f677e-104">El elemento **FreeBusyChangedEvent** representa un evento en el que ha cambiado la hora de disponibilidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f677e-104">The **FreeBusyChangedEvent** element represents an event in which an item's free/busy time has changed.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 <span data-ttu-id="f677e-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="f677e-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f677e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f677e-106">Attributes and elements</span></span>

<span data-ttu-id="f677e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f677e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f677e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f677e-108">Attributes</span></span>

<span data-ttu-id="f677e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f677e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f677e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f677e-110">Child elements</span></span>

|<span data-ttu-id="f677e-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f677e-111">**Element**</span></span>|<span data-ttu-id="f677e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f677e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f677e-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="f677e-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="f677e-114">Representa un marcador de evento en la tabla de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="f677e-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="f677e-115">Marca</span><span class="sxs-lookup"><span data-stu-id="f677e-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="f677e-116">Representa la marca de hora de un evento de buzón de elemento de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="f677e-116">Represents the timestamp of a free/busy item mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="f677e-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="f677e-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f677e-118">Representa el identificador del elemento de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="f677e-118">Represents the identifier of the free/busy item.</span></span>  <br/> |
|[<span data-ttu-id="f677e-119">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="f677e-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f677e-120">Representa el identificador de la carpeta principal del elemento de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="f677e-120">Represents the identifier of the parent folder of the free/busy item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f677e-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f677e-121">Parent elements</span></span>

|<span data-ttu-id="f677e-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f677e-122">**Element**</span></span>|<span data-ttu-id="f677e-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f677e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f677e-124">Notificación</span><span class="sxs-lookup"><span data-stu-id="f677e-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f677e-125">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="f677e-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f677e-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f677e-126">Text value</span></span>

<span data-ttu-id="f677e-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f677e-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f677e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f677e-128">Remarks</span></span>

<span data-ttu-id="f677e-129">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f677e-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f677e-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f677e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f677e-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f677e-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f677e-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f677e-132">Schema name</span></span>  <br/> |<span data-ttu-id="f677e-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f677e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="f677e-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f677e-134">Validation file</span></span>  <br/> |<span data-ttu-id="f677e-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f677e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f677e-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f677e-136">Can be empty</span></span>  <br/> |<span data-ttu-id="f677e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f677e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f677e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f677e-138">See also</span></span>



[<span data-ttu-id="f677e-139">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="f677e-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="f677e-140">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="f677e-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="f677e-141">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="f677e-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="f677e-142">Uso de suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="f677e-142">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="f677e-143">Notificaciones de eventos en EWS</span><span class="sxs-lookup"><span data-stu-id="f677e-143">Event notifications in EWS</span></span>](https://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)


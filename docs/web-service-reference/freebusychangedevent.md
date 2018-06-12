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
description: El elemento FreeBusyChangedEvent representa un evento en el que se ha cambiado el tiempo de disponibilidad de un elemento.
ms.openlocfilehash: 7271d375526e7614d0150594c2b988666a59eb8d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764717"
---
# <a name="freebusychangedevent"></a><span data-ttu-id="965e3-103">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="965e3-103">FreeBusyChangedEvent</span></span>

<span data-ttu-id="965e3-104">El elemento **FreeBusyChangedEvent** representa un evento en el que se ha cambiado el tiempo de disponibilidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="965e3-104">The **FreeBusyChangedEvent** element represents an event in which an item's free/busy time has changed.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 <span data-ttu-id="965e3-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="965e3-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="965e3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="965e3-106">Attributes and elements</span></span>

<span data-ttu-id="965e3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="965e3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="965e3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="965e3-108">Attributes</span></span>

<span data-ttu-id="965e3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="965e3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="965e3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="965e3-110">Child elements</span></span>

|<span data-ttu-id="965e3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="965e3-111">**Element**</span></span>|<span data-ttu-id="965e3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="965e3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="965e3-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="965e3-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="965e3-114">Representa un marcador de evento en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="965e3-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="965e3-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="965e3-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="965e3-116">Representa la marca de hora de un evento de buzón de correo de elemento libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="965e3-116">Represents the timestamp of a free/busy item mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="965e3-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="965e3-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="965e3-118">Representa el identificador del elemento libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="965e3-118">Represents the identifier of the free/busy item.</span></span>  <br/> |
|[<span data-ttu-id="965e3-119">Id</span><span class="sxs-lookup"><span data-stu-id="965e3-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="965e3-120">Representa el identificador de la carpeta principal del elemento libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="965e3-120">Represents the identifier of the parent folder of the free/busy item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="965e3-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="965e3-121">Parent elements</span></span>

|<span data-ttu-id="965e3-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="965e3-122">**Element**</span></span>|<span data-ttu-id="965e3-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="965e3-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="965e3-124">Notificación</span><span class="sxs-lookup"><span data-stu-id="965e3-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="965e3-125">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="965e3-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="965e3-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="965e3-126">Text value</span></span>

<span data-ttu-id="965e3-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="965e3-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="965e3-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="965e3-128">Remarks</span></span>

<span data-ttu-id="965e3-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="965e3-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="965e3-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="965e3-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="965e3-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="965e3-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="965e3-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="965e3-132">Schema name</span></span>  <br/> |<span data-ttu-id="965e3-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="965e3-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="965e3-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="965e3-134">Validation file</span></span>  <br/> |<span data-ttu-id="965e3-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="965e3-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="965e3-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="965e3-136">Can be empty</span></span>  <br/> |<span data-ttu-id="965e3-137">False</span><span class="sxs-lookup"><span data-stu-id="965e3-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="965e3-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="965e3-138">See also</span></span>



[<span data-ttu-id="965e3-139">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="965e3-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="965e3-140">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="965e3-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="965e3-141">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="965e3-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="965e3-142">Uso de las suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="965e3-142">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="965e3-143">Notificaciones de eventos en EWS</span><span class="sxs-lookup"><span data-stu-id="965e3-143">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)


---
title: CreatedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreatedEvent
api_type:
- schema
ms.assetid: f0e53a53-c352-42a5-8280-cd808b0e961b
description: El elemento CreatedEvent representa un evento en el que se crea una carpeta o elemento.
ms.openlocfilehash: f52516090d0789b4dd9fc1ced824786ce000e885
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763922"
---
# <a name="createdevent"></a><span data-ttu-id="2a3d3-103">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="2a3d3-103">CreatedEvent</span></span>

<span data-ttu-id="2a3d3-104">El elemento **CreatedEvent** representa un evento en el que se crea una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-104">The **CreatedEvent** element represents an event in which an item or folder is created.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 <span data-ttu-id="2a3d3-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="2a3d3-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a3d3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2a3d3-106">Attributes and elements</span></span>

<span data-ttu-id="2a3d3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a3d3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a3d3-108">Attributes</span></span>

<span data-ttu-id="2a3d3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a3d3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a3d3-110">Child elements</span></span>

|<span data-ttu-id="2a3d3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a3d3-111">**Element**</span></span>|<span data-ttu-id="2a3d3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a3d3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a3d3-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="2a3d3-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="2a3d3-114">Representa un marcador de evento en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="2a3d3-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="2a3d3-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="2a3d3-116">Representa la marca de hora de un evento de buzón de carpeta o elemento creado.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-116">Represents the timestamp of a created item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="2a3d3-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="2a3d3-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="2a3d3-118">Representa el identificador de la carpeta creada.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-118">Represents the identifier of the created folder.</span></span>  <br/> |
|[<span data-ttu-id="2a3d3-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="2a3d3-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="2a3d3-120">Representa el identificador del elemento creado.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-120">Represents the identifier of the created item.</span></span>  <br/> |
|[<span data-ttu-id="2a3d3-121">Id</span><span class="sxs-lookup"><span data-stu-id="2a3d3-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="2a3d3-122">Representa el identificador de la carpeta principal de la carpeta o el elemento creado.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-122">Represents the identifier of the parent folder of the created item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a3d3-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2a3d3-123">Parent elements</span></span>

|<span data-ttu-id="2a3d3-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a3d3-124">**Element**</span></span>|<span data-ttu-id="2a3d3-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a3d3-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a3d3-126">Notificación</span><span class="sxs-lookup"><span data-stu-id="2a3d3-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2a3d3-127">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a3d3-128">Notas</span><span class="sxs-lookup"><span data-stu-id="2a3d3-128">Remarks</span></span>

<span data-ttu-id="2a3d3-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2a3d3-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a3d3-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2a3d3-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a3d3-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a3d3-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a3d3-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2a3d3-132">Schema name</span></span>  <br/> |<span data-ttu-id="2a3d3-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2a3d3-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a3d3-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2a3d3-134">Validation file</span></span>  <br/> |<span data-ttu-id="2a3d3-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a3d3-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a3d3-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2a3d3-136">Can be empty</span></span>  <br/> |<span data-ttu-id="2a3d3-137">False</span><span class="sxs-lookup"><span data-stu-id="2a3d3-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a3d3-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="2a3d3-138">See also</span></span>



[<span data-ttu-id="2a3d3-139">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="2a3d3-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="2a3d3-140">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="2a3d3-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="2a3d3-141">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="2a3d3-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="2a3d3-142">Uso de las suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="2a3d3-142">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="2a3d3-143">Notificaciones de eventos en EWS</span><span class="sxs-lookup"><span data-stu-id="2a3d3-143">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)


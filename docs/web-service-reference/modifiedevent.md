---
title: ModifiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: El elemento ModifiedEvent representa un evento en el que se modifica una carpeta o elemento.
ms.openlocfilehash: fb464fb0a270d8ca7d33d40e5425e260970b2f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836482"
---
# <a name="modifiedevent"></a><span data-ttu-id="82d8d-103">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="82d8d-103">ModifiedEvent</span></span>

<span data-ttu-id="82d8d-104">El elemento **ModifiedEvent** representa un evento en el que se modifica una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="82d8d-104">The **ModifiedEvent** element represents an event in which an item or folder is modified.</span></span> 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

 <span data-ttu-id="82d8d-105">**ModifiedEventType**</span><span class="sxs-lookup"><span data-stu-id="82d8d-105">**ModifiedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82d8d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="82d8d-106">Attributes and elements</span></span>

<span data-ttu-id="82d8d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="82d8d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82d8d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="82d8d-108">Attributes</span></span>

<span data-ttu-id="82d8d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82d8d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82d8d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="82d8d-110">Child elements</span></span>

|<span data-ttu-id="82d8d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="82d8d-111">**Element**</span></span>|<span data-ttu-id="82d8d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82d8d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82d8d-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="82d8d-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="82d8d-114">Representa un marcador de evento en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="82d8d-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="82d8d-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="82d8d-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="82d8d-116">Representa la marca de hora de un evento de buzón de carpeta o elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="82d8d-116">Represents the timestamp of a modified item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="82d8d-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="82d8d-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="82d8d-118">Representa el identificador de la carpeta modificada.</span><span class="sxs-lookup"><span data-stu-id="82d8d-118">Represents the identifier of the modified folder.</span></span>  <br/> |
|[<span data-ttu-id="82d8d-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="82d8d-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="82d8d-120">Representa el identificador del elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="82d8d-120">Represents the identifier of the modified item.</span></span>  <br/> |
|[<span data-ttu-id="82d8d-121">Id</span><span class="sxs-lookup"><span data-stu-id="82d8d-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="82d8d-122">Representa el identificador de la carpeta principal de la carpeta o el elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="82d8d-122">Represents the identifier of the parent folder of the modified item or folder.</span></span>  <br/> |
|[<span data-ttu-id="82d8d-123">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="82d8d-123">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="82d8d-124">Representa el recuento de elementos no leídos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="82d8d-124">Represents the count of unread items within a given folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="82d8d-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="82d8d-125">Parent elements</span></span>

|<span data-ttu-id="82d8d-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="82d8d-126">**Element**</span></span>|<span data-ttu-id="82d8d-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82d8d-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82d8d-128">Notificación</span><span class="sxs-lookup"><span data-stu-id="82d8d-128">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="82d8d-129">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="82d8d-129">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82d8d-130">Notas</span><span class="sxs-lookup"><span data-stu-id="82d8d-130">Remarks</span></span>

<span data-ttu-id="82d8d-131">Se generan dos eventos modificados para cada modificación de un elemento en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="82d8d-131">Two modified events are generated for each modification of an item in a folder.</span></span> <span data-ttu-id="82d8d-132">Un evento es relevante para el elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="82d8d-132">One event is relevant to the item that changed.</span></span> <span data-ttu-id="82d8d-133">El otro evento es relevante para la carpeta principal del elemento.</span><span class="sxs-lookup"><span data-stu-id="82d8d-133">The other event is relevant to the parent folder of the item.</span></span> <span data-ttu-id="82d8d-134">Esto es la misma carpeta que se creó la suscripción contra.</span><span class="sxs-lookup"><span data-stu-id="82d8d-134">This is the same folder that the subscription was created against.</span></span> <span data-ttu-id="82d8d-135">El evento que está asociado a la carpeta se usa para comunicarse un cambio posible para la propiedad [UnreadCount](unreadcount.md) en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="82d8d-135">The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder.</span></span> 
  
<span data-ttu-id="82d8d-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="82d8d-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82d8d-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="82d8d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82d8d-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="82d8d-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="82d8d-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="82d8d-139">Schema name</span></span>  <br/> |<span data-ttu-id="82d8d-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="82d8d-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="82d8d-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="82d8d-141">Validation file</span></span>  <br/> |<span data-ttu-id="82d8d-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="82d8d-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="82d8d-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="82d8d-143">Can be empty</span></span>  <br/> |<span data-ttu-id="82d8d-144">False</span><span class="sxs-lookup"><span data-stu-id="82d8d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82d8d-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="82d8d-145">See also</span></span>



[<span data-ttu-id="82d8d-146">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="82d8d-146">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="82d8d-147">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="82d8d-147">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="82d8d-148">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="82d8d-148">Unsubscribe operation</span></span>](unsubscribe-operation.md)


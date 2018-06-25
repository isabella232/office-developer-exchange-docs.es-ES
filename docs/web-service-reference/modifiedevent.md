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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836482"
---
# <a name="modifiedevent"></a><span data-ttu-id="bdb76-103">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="bdb76-103">ModifiedEvent</span></span>

<span data-ttu-id="bdb76-104">El elemento **ModifiedEvent** representa un evento en el que se modifica una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="bdb76-104">The **ModifiedEvent** element represents an event in which an item or folder is modified.</span></span> 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

 <span data-ttu-id="bdb76-105">**ModifiedEventType**</span><span class="sxs-lookup"><span data-stu-id="bdb76-105">**ModifiedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bdb76-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bdb76-106">Attributes and elements</span></span>

<span data-ttu-id="bdb76-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bdb76-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdb76-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bdb76-108">Attributes</span></span>

<span data-ttu-id="bdb76-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bdb76-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bdb76-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bdb76-110">Child elements</span></span>

|<span data-ttu-id="bdb76-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdb76-111">**Element**</span></span>|<span data-ttu-id="bdb76-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdb76-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdb76-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="bdb76-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="bdb76-114">Representa un marcador de evento en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="bdb76-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="bdb76-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="bdb76-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="bdb76-116">Representa la marca de hora de un evento de buzón de carpeta o elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="bdb76-116">Represents the timestamp of a modified item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="bdb76-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="bdb76-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="bdb76-118">Representa el identificador de la carpeta modificada.</span><span class="sxs-lookup"><span data-stu-id="bdb76-118">Represents the identifier of the modified folder.</span></span>  <br/> |
|[<span data-ttu-id="bdb76-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="bdb76-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="bdb76-120">Representa el identificador del elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="bdb76-120">Represents the identifier of the modified item.</span></span>  <br/> |
|[<span data-ttu-id="bdb76-121">Id</span><span class="sxs-lookup"><span data-stu-id="bdb76-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="bdb76-122">Representa el identificador de la carpeta principal de la carpeta o el elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="bdb76-122">Represents the identifier of the parent folder of the modified item or folder.</span></span>  <br/> |
|[<span data-ttu-id="bdb76-123">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="bdb76-123">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="bdb76-124">Representa el recuento de elementos no leídos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="bdb76-124">Represents the count of unread items within a given folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdb76-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bdb76-125">Parent elements</span></span>

|<span data-ttu-id="bdb76-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdb76-126">**Element**</span></span>|<span data-ttu-id="bdb76-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bdb76-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdb76-128">Notificación</span><span class="sxs-lookup"><span data-stu-id="bdb76-128">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bdb76-129">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="bdb76-129">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdb76-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bdb76-130">Remarks</span></span>

<span data-ttu-id="bdb76-131">Se generan dos eventos modificados para cada modificación de un elemento en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="bdb76-131">Two modified events are generated for each modification of an item in a folder.</span></span> <span data-ttu-id="bdb76-132">Un evento es relevante para el elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="bdb76-132">One event is relevant to the item that changed.</span></span> <span data-ttu-id="bdb76-133">El otro evento es relevante para la carpeta principal del elemento.</span><span class="sxs-lookup"><span data-stu-id="bdb76-133">The other event is relevant to the parent folder of the item.</span></span> <span data-ttu-id="bdb76-134">Esto es la misma carpeta que se creó la suscripción contra.</span><span class="sxs-lookup"><span data-stu-id="bdb76-134">This is the same folder that the subscription was created against.</span></span> <span data-ttu-id="bdb76-135">El evento que está asociado a la carpeta se usa para comunicarse un cambio posible para la propiedad [UnreadCount](unreadcount.md) en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="bdb76-135">The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder.</span></span> 
  
<span data-ttu-id="bdb76-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="bdb76-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdb76-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bdb76-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdb76-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bdb76-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bdb76-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bdb76-139">Schema name</span></span>  <br/> |<span data-ttu-id="bdb76-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bdb76-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="bdb76-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bdb76-141">Validation file</span></span>  <br/> |<span data-ttu-id="bdb76-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bdb76-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bdb76-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bdb76-143">Can be empty</span></span>  <br/> |<span data-ttu-id="bdb76-144">False</span><span class="sxs-lookup"><span data-stu-id="bdb76-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdb76-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdb76-145">See also</span></span>



[<span data-ttu-id="bdb76-146">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="bdb76-146">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="bdb76-147">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="bdb76-147">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="bdb76-148">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="bdb76-148">Unsubscribe operation</span></span>](unsubscribe-operation.md)


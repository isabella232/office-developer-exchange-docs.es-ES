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
description: El elemento ModifiedEvent representa un evento en el que se modifica un elemento o una carpeta.
ms.openlocfilehash: 1a798773601a0857b9064c7fa6a532a7a36517ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468554"
---
# <a name="modifiedevent"></a><span data-ttu-id="c449a-103">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="c449a-103">ModifiedEvent</span></span>

<span data-ttu-id="c449a-104">El elemento **ModifiedEvent** representa un evento en el que se modifica un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c449a-104">The **ModifiedEvent** element represents an event in which an item or folder is modified.</span></span> 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/> 
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

<span data-ttu-id="c449a-105">**ModifiedEventType**</span><span class="sxs-lookup"><span data-stu-id="c449a-105">**ModifiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c449a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c449a-106">Attributes and elements</span></span>

<span data-ttu-id="c449a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c449a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c449a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c449a-108">Attributes</span></span>

<span data-ttu-id="c449a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c449a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c449a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c449a-110">Child elements</span></span>

|<span data-ttu-id="c449a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c449a-111">**Element**</span></span>|<span data-ttu-id="c449a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c449a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c449a-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="c449a-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="c449a-114">Representa un marcador de evento en la tabla de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="c449a-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="c449a-115">Marca</span><span class="sxs-lookup"><span data-stu-id="c449a-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="c449a-116">Representa la marca de hora de un elemento modificado o un evento de buzón de carpeta.</span><span class="sxs-lookup"><span data-stu-id="c449a-116">Represents the timestamp of a modified item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="c449a-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="c449a-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c449a-118">Representa el identificador de la carpeta modificada.</span><span class="sxs-lookup"><span data-stu-id="c449a-118">Represents the identifier of the modified folder.</span></span>  <br/> |
|[<span data-ttu-id="c449a-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="c449a-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="c449a-120">Representa el identificador del elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="c449a-120">Represents the identifier of the modified item.</span></span>  <br/> |
|[<span data-ttu-id="c449a-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="c449a-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="c449a-122">Representa el identificador de la carpeta principal del elemento o carpeta que se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="c449a-122">Represents the identifier of the parent folder of the modified item or folder.</span></span>  <br/> |
|[<span data-ttu-id="c449a-123">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="c449a-123">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="c449a-124">Representa el número de elementos no leídos dentro de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="c449a-124">Represents the count of unread items within a given folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c449a-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c449a-125">Parent elements</span></span>

|<span data-ttu-id="c449a-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c449a-126">**Element**</span></span>|<span data-ttu-id="c449a-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c449a-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c449a-128">Notificación</span><span class="sxs-lookup"><span data-stu-id="c449a-128">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c449a-129">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="c449a-129">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c449a-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c449a-130">Remarks</span></span>

<span data-ttu-id="c449a-131">Se generan dos eventos modificados para cada modificación de un elemento en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c449a-131">Two modified events are generated for each modification of an item in a folder.</span></span> <span data-ttu-id="c449a-132">Un evento es relevante para el elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c449a-132">One event is relevant to the item that changed.</span></span> <span data-ttu-id="c449a-133">El otro evento es relevante para la carpeta principal del elemento.</span><span class="sxs-lookup"><span data-stu-id="c449a-133">The other event is relevant to the parent folder of the item.</span></span> <span data-ttu-id="c449a-134">Se trata de la misma carpeta en la que se creó la suscripción.</span><span class="sxs-lookup"><span data-stu-id="c449a-134">This is the same folder that the subscription was created against.</span></span> <span data-ttu-id="c449a-135">El evento asociado a la carpeta se usa para comunicar un cambio potencial a la propiedad [UnreadCount](unreadcount.md) de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c449a-135">The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder.</span></span> 
  
<span data-ttu-id="c449a-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c449a-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c449a-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c449a-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c449a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="c449a-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c449a-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c449a-139">Schema name</span></span>  <br/> |<span data-ttu-id="c449a-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c449a-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="c449a-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c449a-141">Validation file</span></span>  <br/> |<span data-ttu-id="c449a-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c449a-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c449a-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c449a-143">Can be empty</span></span>  <br/> |<span data-ttu-id="c449a-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c449a-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c449a-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c449a-145">See also</span></span>

- [<span data-ttu-id="c449a-146">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="c449a-146">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="c449a-147">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="c449a-147">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="c449a-148">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="c449a-148">Unsubscribe operation</span></span>](unsubscribe-operation.md)


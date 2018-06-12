---
title: MovedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: El elemento MovedEvent representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.
ms.openlocfilehash: a375f421ca9159103e47b515729316b21149c68a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836479"
---
# <a name="movedevent"></a><span data-ttu-id="37bf4-103">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="37bf4-103">MovedEvent</span></span>

<span data-ttu-id="37bf4-104">El elemento **MovedEvent** representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="37bf4-104">The **MovedEvent** element represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span> 
  
```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</MovedEvent>
```

 <span data-ttu-id="37bf4-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="37bf4-105">**MovedCopiedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37bf4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37bf4-106">Attributes and elements</span></span>

<span data-ttu-id="37bf4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37bf4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37bf4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="37bf4-108">Attributes</span></span>

<span data-ttu-id="37bf4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37bf4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37bf4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37bf4-110">Child elements</span></span>

|<span data-ttu-id="37bf4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="37bf4-111">**Element**</span></span>|<span data-ttu-id="37bf4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37bf4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37bf4-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="37bf4-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="37bf4-114">Representa un marcador de eventos en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="37bf4-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="37bf4-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="37bf4-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="37bf4-116">Representa la marca de hora de un evento de mover el buzón de correo elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="37bf4-116">Represents the timestamp of a move item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="37bf4-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="37bf4-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="37bf4-118">Representa el identificador de la carpeta que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="37bf4-118">Represents the identifier of the moved folder.</span></span>  <br/> |
|[<span data-ttu-id="37bf4-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="37bf4-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="37bf4-120">Representa el identificador del elemento que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="37bf4-120">Represents the identifier of the moved item.</span></span>  <br/> |
|[<span data-ttu-id="37bf4-121">Id</span><span class="sxs-lookup"><span data-stu-id="37bf4-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="37bf4-122">Representa el identificador de la carpeta que contiene el elemento que se ha movido o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="37bf4-122">Represents the identifier of the folder that contains the moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="37bf4-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="37bf4-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="37bf4-124">Contiene el identificador de la carpeta de la carpeta original antes de se ha movido o copiado.</span><span class="sxs-lookup"><span data-stu-id="37bf4-124">Contains the folder identifier of the original folder before it was moved or copied.</span></span>  <br/> |
|[<span data-ttu-id="37bf4-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="37bf4-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="37bf4-126">Contiene el identificador único del elemento original antes de que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="37bf4-126">Contains the unique identifier of the original item before it was moved.</span></span>  <br/> |
|[<span data-ttu-id="37bf4-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="37bf4-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="37bf4-128">Contiene el identificador de la carpeta principal original de un elemento o carpeta que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="37bf4-128">Contains the identifier of the original parent folder of an item or folder that was moved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37bf4-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37bf4-129">Parent elements</span></span>

|<span data-ttu-id="37bf4-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="37bf4-130">**Element**</span></span>|<span data-ttu-id="37bf4-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37bf4-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37bf4-132">Notificación</span><span class="sxs-lookup"><span data-stu-id="37bf4-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="37bf4-133">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="37bf4-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37bf4-134">Notas</span><span class="sxs-lookup"><span data-stu-id="37bf4-134">Remarks</span></span>

<span data-ttu-id="37bf4-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="37bf4-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37bf4-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37bf4-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37bf4-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37bf4-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="37bf4-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37bf4-138">Schema name</span></span>  <br/> |<span data-ttu-id="37bf4-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="37bf4-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="37bf4-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37bf4-140">Validation file</span></span>  <br/> |<span data-ttu-id="37bf4-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="37bf4-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="37bf4-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37bf4-142">Can be empty</span></span>  <br/> |<span data-ttu-id="37bf4-143">False</span><span class="sxs-lookup"><span data-stu-id="37bf4-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37bf4-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="37bf4-144">See also</span></span>



[<span data-ttu-id="37bf4-145">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="37bf4-145">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="37bf4-146">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="37bf4-146">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="37bf4-147">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="37bf4-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)


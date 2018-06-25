---
title: CopiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: El elemento CopiedEvent representa un evento en el que se copia un elemento o carpeta.
ms.openlocfilehash: 89ca9fb1fd2f4187efdec0e087d840bfee197a29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763890"
---
# <a name="copiedevent"></a><span data-ttu-id="83ff5-103">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="83ff5-103">CopiedEvent</span></span>

<span data-ttu-id="83ff5-104">El elemento **CopiedEvent** representa un evento en el que se copia un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="83ff5-104">The **CopiedEvent** element represents an event in which an item or folder is copied.</span></span> 
  
```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

 <span data-ttu-id="83ff5-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="83ff5-105">**MovedCopiedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83ff5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="83ff5-106">Attributes and elements</span></span>

<span data-ttu-id="83ff5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="83ff5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83ff5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="83ff5-108">Attributes</span></span>

<span data-ttu-id="83ff5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83ff5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83ff5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83ff5-110">Child elements</span></span>

|<span data-ttu-id="83ff5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="83ff5-111">**Element**</span></span>|<span data-ttu-id="83ff5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83ff5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83ff5-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="83ff5-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="83ff5-114">Representa un marcador de eventos en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="83ff5-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="83ff5-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="83ff5-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="83ff5-116">Representa la marca de hora de un evento de buzón de correo del elemento o la carpeta de copia.</span><span class="sxs-lookup"><span data-stu-id="83ff5-116">Represents the timestamp of a copy item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="83ff5-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="83ff5-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="83ff5-118">Representa el identificador de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="83ff5-118">Represents the identifier of the folder.</span></span>  <br/> |
|[<span data-ttu-id="83ff5-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="83ff5-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="83ff5-120">Representa el identificador del elemento.</span><span class="sxs-lookup"><span data-stu-id="83ff5-120">Represents the identifier of the item.</span></span>  <br/> |
|[<span data-ttu-id="83ff5-121">Id</span><span class="sxs-lookup"><span data-stu-id="83ff5-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="83ff5-122">Representa el identificador de la carpeta que contiene la copia.</span><span class="sxs-lookup"><span data-stu-id="83ff5-122">Represents the identifier of the folder that contains the copy.</span></span>  <br/> |
|[<span data-ttu-id="83ff5-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="83ff5-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="83ff5-124">Representa el identificador de la carpeta de la carpeta original antes de se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="83ff5-124">Represents the folder identifier of the original folder before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="83ff5-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="83ff5-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="83ff5-126">Contiene el identificador único del elemento original antes de se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="83ff5-126">Contains the unique identifier of the original item before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="83ff5-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="83ff5-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="83ff5-128">Contiene el identificador de la carpeta principal original de un elemento o carpeta que se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="83ff5-128">Contains the identifier of the original parent folder of an item or folder that was copied.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83ff5-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="83ff5-129">Parent elements</span></span>

|<span data-ttu-id="83ff5-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="83ff5-130">**Element**</span></span>|<span data-ttu-id="83ff5-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83ff5-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83ff5-132">Notificación</span><span class="sxs-lookup"><span data-stu-id="83ff5-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="83ff5-133">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="83ff5-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83ff5-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83ff5-134">Remarks</span></span>

<span data-ttu-id="83ff5-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="83ff5-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83ff5-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="83ff5-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83ff5-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83ff5-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83ff5-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="83ff5-138">Schema name</span></span>  <br/> |<span data-ttu-id="83ff5-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="83ff5-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="83ff5-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="83ff5-140">Validation file</span></span>  <br/> |<span data-ttu-id="83ff5-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83ff5-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83ff5-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="83ff5-142">Can be empty</span></span>  <br/> |<span data-ttu-id="83ff5-143">False</span><span class="sxs-lookup"><span data-stu-id="83ff5-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83ff5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="83ff5-144">See also</span></span>



[<span data-ttu-id="83ff5-145">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="83ff5-145">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="83ff5-146">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="83ff5-146">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="83ff5-147">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="83ff5-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="83ff5-148">Uso de las suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="83ff5-148">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="83ff5-149">Aplicación de ejemplo de notificación de inserción</span><span class="sxs-lookup"><span data-stu-id="83ff5-149">Push Notification Sample Application</span></span>](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)


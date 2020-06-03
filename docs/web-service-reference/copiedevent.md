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
description: El elemento CopiedEvent representa un evento en el que se copia un elemento o una carpeta.
ms.openlocfilehash: 928910ddbe0bf1e48549d1665ab373f7382366d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529248"
---
# <a name="copiedevent"></a><span data-ttu-id="caec0-103">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="caec0-103">CopiedEvent</span></span>

<span data-ttu-id="caec0-104">El elemento **CopiedEvent** representa un evento en el que se copia un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="caec0-104">The **CopiedEvent** element represents an event in which an item or folder is copied.</span></span> 
  
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

```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

<span data-ttu-id="caec0-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="caec0-105">**MovedCopiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="caec0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="caec0-106">Attributes and elements</span></span>

<span data-ttu-id="caec0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="caec0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="caec0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="caec0-108">Attributes</span></span>

<span data-ttu-id="caec0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="caec0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="caec0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="caec0-110">Child elements</span></span>

|<span data-ttu-id="caec0-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="caec0-111">**Element**</span></span>|<span data-ttu-id="caec0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="caec0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="caec0-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="caec0-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="caec0-114">Representa un marcador de eventos en la tabla de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="caec0-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="caec0-115">Marca</span><span class="sxs-lookup"><span data-stu-id="caec0-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="caec0-116">Representa la marca de hora de un evento de copia de elemento/buzón de carpeta.</span><span class="sxs-lookup"><span data-stu-id="caec0-116">Represents the timestamp of a copy item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="caec0-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="caec0-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="caec0-118">Representa el identificador de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="caec0-118">Represents the identifier of the folder.</span></span>  <br/> |
|[<span data-ttu-id="caec0-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="caec0-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="caec0-120">Representa el identificador del elemento.</span><span class="sxs-lookup"><span data-stu-id="caec0-120">Represents the identifier of the item.</span></span>  <br/> |
|[<span data-ttu-id="caec0-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="caec0-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="caec0-122">Representa el identificador de la carpeta que contiene la copia.</span><span class="sxs-lookup"><span data-stu-id="caec0-122">Represents the identifier of the folder that contains the copy.</span></span>  <br/> |
|[<span data-ttu-id="caec0-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="caec0-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="caec0-124">Representa el identificador de la carpeta original antes de que se copiara.</span><span class="sxs-lookup"><span data-stu-id="caec0-124">Represents the folder identifier of the original folder before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="caec0-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="caec0-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="caec0-126">Contiene el identificador único del elemento original antes de copiarlo.</span><span class="sxs-lookup"><span data-stu-id="caec0-126">Contains the unique identifier of the original item before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="caec0-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="caec0-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="caec0-128">Contiene el identificador de la carpeta principal original de un elemento o carpeta que se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="caec0-128">Contains the identifier of the original parent folder of an item or folder that was copied.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="caec0-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="caec0-129">Parent elements</span></span>

|<span data-ttu-id="caec0-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="caec0-130">**Element**</span></span>|<span data-ttu-id="caec0-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="caec0-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="caec0-132">Notificación</span><span class="sxs-lookup"><span data-stu-id="caec0-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="caec0-133">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="caec0-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="caec0-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="caec0-134">Remarks</span></span>

<span data-ttu-id="caec0-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="caec0-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="caec0-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="caec0-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="caec0-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="caec0-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="caec0-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="caec0-138">Schema name</span></span>  <br/> |<span data-ttu-id="caec0-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="caec0-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="caec0-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="caec0-140">Validation file</span></span>  <br/> |<span data-ttu-id="caec0-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="caec0-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="caec0-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="caec0-142">Can be empty</span></span>  <br/> |<span data-ttu-id="caec0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="caec0-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="caec0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="caec0-144">See also</span></span>

- [<span data-ttu-id="caec0-145">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="caec0-145">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="caec0-146">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="caec0-146">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="caec0-147">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="caec0-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="caec0-148">Uso de suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="caec0-148">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [<span data-ttu-id="caec0-149">Aplicación de ejemplo de notificación de inserción</span><span class="sxs-lookup"><span data-stu-id="caec0-149">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)


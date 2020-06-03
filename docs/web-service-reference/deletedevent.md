---
title: DeletedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedEvent
api_type:
- schema
ms.assetid: c4565eb4-b537-466c-b1ff-11602533812b
description: El elemento DeletedEvent representa un evento en el que se elimina un elemento o una carpeta.
ms.openlocfilehash: 5eb0c947aacc592f81c595da2cc00bf4874f300b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526945"
---
# <a name="deletedevent"></a><span data-ttu-id="6e125-103">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="6e125-103">DeletedEvent</span></span>

<span data-ttu-id="6e125-104">El elemento **DeletedEvent** representa un evento en el que se elimina un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="6e125-104">The **DeletedEvent** element represents an event in which an item or folder is deleted.</span></span> 
  
```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
</DeletedEvent>
```

<span data-ttu-id="6e125-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="6e125-105">**BaseObjectChangedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6e125-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6e125-106">Attributes and elements</span></span>

<span data-ttu-id="6e125-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6e125-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e125-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e125-108">Attributes</span></span>

<span data-ttu-id="6e125-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6e125-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e125-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6e125-110">Child elements</span></span>

|<span data-ttu-id="6e125-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e125-111">**Element**</span></span>|<span data-ttu-id="6e125-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e125-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e125-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="6e125-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="6e125-114">Representa un marcador de evento en la tabla de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="6e125-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="6e125-115">Marca</span><span class="sxs-lookup"><span data-stu-id="6e125-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="6e125-116">Representa la marca de hora de un evento de elemento o buzón de carpeta eliminado.</span><span class="sxs-lookup"><span data-stu-id="6e125-116">Represents the timestamp of a deleted item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="6e125-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="6e125-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="6e125-118">Representa el identificador de la carpeta eliminada.</span><span class="sxs-lookup"><span data-stu-id="6e125-118">Represents the identifier of the deleted folder.</span></span>  <br/> |
|[<span data-ttu-id="6e125-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="6e125-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="6e125-120">Representa el identificador del elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="6e125-120">Represents the identifier of the deleted item.</span></span>  <br/> |
|[<span data-ttu-id="6e125-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="6e125-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="6e125-122">Representa el identificador de la carpeta principal del elemento o carpeta eliminados antes de su eliminación.</span><span class="sxs-lookup"><span data-stu-id="6e125-122">Represents the identifier of the parent folder of the deleted item or folder before deletion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6e125-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6e125-123">Parent elements</span></span>

|<span data-ttu-id="6e125-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e125-124">**Element**</span></span>|<span data-ttu-id="6e125-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e125-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e125-126">Notificación</span><span class="sxs-lookup"><span data-stu-id="6e125-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6e125-127">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="6e125-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e125-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e125-128">Remarks</span></span>

<span data-ttu-id="6e125-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6e125-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e125-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6e125-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e125-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e125-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6e125-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6e125-132">Schema name</span></span>  <br/> |<span data-ttu-id="6e125-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6e125-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="6e125-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6e125-134">Validation file</span></span>  <br/> |<span data-ttu-id="6e125-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6e125-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6e125-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6e125-136">Can be empty</span></span>  <br/> |<span data-ttu-id="6e125-137">Falso</span><span class="sxs-lookup"><span data-stu-id="6e125-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e125-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e125-138">See also</span></span>

- [<span data-ttu-id="6e125-139">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="6e125-139">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="6e125-140">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="6e125-140">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="6e125-141">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="6e125-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


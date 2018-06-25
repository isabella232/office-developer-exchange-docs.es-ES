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
description: El elemento DeletedEvent representa un evento en el que se elimina un elemento o carpeta.
ms.openlocfilehash: f06ca0727916f415c648e876f88bf7eacef5a5ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764085"
---
# <a name="deletedevent"></a><span data-ttu-id="ee05e-103">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="ee05e-103">DeletedEvent</span></span>

<span data-ttu-id="ee05e-104">El elemento **DeletedEvent** representa un evento en el que se elimina un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="ee05e-104">The **DeletedEvent** element represents an event in which an item or folder is deleted.</span></span> 
  
```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

<span data-ttu-id="ee05e-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="ee05e-105">**BaseObjectChangedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ee05e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ee05e-106">Attributes and elements</span></span>

<span data-ttu-id="ee05e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ee05e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee05e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee05e-108">Attributes</span></span>

<span data-ttu-id="ee05e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ee05e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee05e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee05e-110">Child elements</span></span>

|<span data-ttu-id="ee05e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ee05e-111">**Element**</span></span>|<span data-ttu-id="ee05e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee05e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee05e-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="ee05e-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="ee05e-114">Representa un marcador de evento en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ee05e-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="ee05e-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="ee05e-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="ee05e-116">Representa la marca de hora de un evento de buzón de carpeta o elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="ee05e-116">Represents the timestamp of a deleted item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="ee05e-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="ee05e-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="ee05e-118">Representa el identificador de la carpeta eliminada.</span><span class="sxs-lookup"><span data-stu-id="ee05e-118">Represents the identifier of the deleted folder.</span></span>  <br/> |
|[<span data-ttu-id="ee05e-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="ee05e-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ee05e-120">Representa el identificador del elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="ee05e-120">Represents the identifier of the deleted item.</span></span>  <br/> |
|[<span data-ttu-id="ee05e-121">Id</span><span class="sxs-lookup"><span data-stu-id="ee05e-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="ee05e-122">Representa el identificador de la carpeta principal del elemento eliminado o la carpeta antes de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="ee05e-122">Represents the identifier of the parent folder of the deleted item or folder before deletion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ee05e-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ee05e-123">Parent elements</span></span>

|<span data-ttu-id="ee05e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ee05e-124">**Element**</span></span>|<span data-ttu-id="ee05e-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee05e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee05e-126">Notificación</span><span class="sxs-lookup"><span data-stu-id="ee05e-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ee05e-127">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="ee05e-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee05e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee05e-128">Remarks</span></span>

<span data-ttu-id="ee05e-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ee05e-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee05e-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ee05e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee05e-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ee05e-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ee05e-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ee05e-132">Schema name</span></span>  <br/> |<span data-ttu-id="ee05e-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ee05e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="ee05e-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ee05e-134">Validation file</span></span>  <br/> |<span data-ttu-id="ee05e-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ee05e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ee05e-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ee05e-136">Can be empty</span></span>  <br/> |<span data-ttu-id="ee05e-137">False</span><span class="sxs-lookup"><span data-stu-id="ee05e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee05e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee05e-138">See also</span></span>

- [<span data-ttu-id="ee05e-139">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="ee05e-139">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="ee05e-140">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="ee05e-140">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="ee05e-141">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="ee05e-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


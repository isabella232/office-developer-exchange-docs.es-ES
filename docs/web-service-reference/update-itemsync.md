---
title: Actualización (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: El elemento de actualización identifica un solo elemento que se debe actualizar en el almacén de cliente local.
ms.openlocfilehash: ef1bd46906152affbe54372472766afc2a6ae8c1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840803"
---
# <a name="update-itemsync"></a><span data-ttu-id="8a28d-103">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="8a28d-103">Update (ItemSync)</span></span>

<span data-ttu-id="8a28d-104">El elemento **Update** identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="8a28d-104">The **Update** element identifies a single item to update in the local client store.</span></span> 
  
[<span data-ttu-id="8a28d-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="8a28d-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="8a28d-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8a28d-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="8a28d-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8a28d-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="8a28d-108">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="8a28d-108">Changes (Items)</span></span>](changes-items.md)
  
[<span data-ttu-id="8a28d-109">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="8a28d-109">Update (ItemSync)</span></span>](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

 <span data-ttu-id="8a28d-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="8a28d-110">**SyncFolderItemsCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a28d-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8a28d-111">Attributes and elements</span></span>

<span data-ttu-id="8a28d-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8a28d-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a28d-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="8a28d-113">Attributes</span></span>

<span data-ttu-id="8a28d-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8a28d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a28d-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8a28d-115">Child elements</span></span>

|<span data-ttu-id="8a28d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a28d-116">**Element**</span></span>|<span data-ttu-id="8a28d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a28d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a28d-118">Item</span><span class="sxs-lookup"><span data-stu-id="8a28d-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="8a28d-119">Representa un elemento de Exchange genérico que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-119">Represents a generic Exchange item to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-120">Message</span><span class="sxs-lookup"><span data-stu-id="8a28d-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8a28d-121">Representa un mensaje de correo electrónico de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-121">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8a28d-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8a28d-123">Representa un elemento de calendario de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-123">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-124">Contact</span><span class="sxs-lookup"><span data-stu-id="8a28d-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="8a28d-125">Representa un elemento de contacto de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-125">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="8a28d-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="8a28d-127">Representa una lista de distribución que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-127">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="8a28d-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="8a28d-129">Representa un mensaje de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-129">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8a28d-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8a28d-131">Representa una convocatoria de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-131">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="8a28d-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="8a28d-133">Representa una respuesta a la reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-133">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="8a28d-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="8a28d-135">Representa una cancelación de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-135">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="8a28d-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="8a28d-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="8a28d-137">Representa una tarea que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8a28d-137">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8a28d-138">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8a28d-138">Parent elements</span></span>

|<span data-ttu-id="8a28d-139">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a28d-139">**Element**</span></span>|<span data-ttu-id="8a28d-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a28d-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a28d-141">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="8a28d-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="8a28d-142">Contiene una matriz de secuencia de tipos de cambio que representan el tipo de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8a28d-142">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a28d-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a28d-143">Remarks</span></span>

<span data-ttu-id="8a28d-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8a28d-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a28d-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8a28d-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a28d-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a28d-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8a28d-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8a28d-147">Schema name</span></span>  <br/> |<span data-ttu-id="8a28d-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8a28d-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="8a28d-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8a28d-149">Validation file</span></span>  <br/> |<span data-ttu-id="8a28d-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8a28d-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8a28d-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8a28d-151">Can be empty</span></span>  <br/> |<span data-ttu-id="8a28d-152">False</span><span class="sxs-lookup"><span data-stu-id="8a28d-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a28d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a28d-153">See also</span></span>



[<span data-ttu-id="8a28d-154">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="8a28d-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="8a28d-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8a28d-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


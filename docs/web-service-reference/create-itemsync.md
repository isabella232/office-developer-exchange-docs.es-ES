---
title: Crear (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: cb5e64a2-66a5-4447-921e-7c13efb8f6bf
description: El elemento Create identifica un solo elemento para crear en el almacén de cliente local.
ms.openlocfilehash: 39056bcaab3577b1b729421118a45571910922fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763911"
---
# <a name="create-itemsync"></a><span data-ttu-id="4afdb-103">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="4afdb-103">Create (ItemSync)</span></span>

<span data-ttu-id="4afdb-104">El elemento **Create** identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="4afdb-104">The **Create** element identifies a single item to create in the local client store.</span></span> 
  
[<span data-ttu-id="4afdb-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="4afdb-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="4afdb-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4afdb-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="4afdb-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4afdb-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="4afdb-108">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="4afdb-108">Changes (Items)</span></span>](changes-items.md)
  
[<span data-ttu-id="4afdb-109">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="4afdb-109">Create (ItemSync)</span></span>](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

 <span data-ttu-id="4afdb-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="4afdb-110">**SyncFolderItemsCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4afdb-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4afdb-111">Attributes and elements</span></span>

<span data-ttu-id="4afdb-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4afdb-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4afdb-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="4afdb-113">Attributes</span></span>

<span data-ttu-id="4afdb-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4afdb-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4afdb-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4afdb-115">Child elements</span></span>

|<span data-ttu-id="4afdb-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4afdb-116">**Element**</span></span>|<span data-ttu-id="4afdb-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4afdb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4afdb-118">Item</span><span class="sxs-lookup"><span data-stu-id="4afdb-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="4afdb-119">Representa un elemento genérico de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-119">Represents a generic Exchange item to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-120">Message</span><span class="sxs-lookup"><span data-stu-id="4afdb-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4afdb-121">Representa un mensaje de correo electrónico de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-121">Represents an Exchange e-mail message to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4afdb-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4afdb-123">Representa un elemento de calendario de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-123">Represents an Exchange calendar item to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-124">Contact</span><span class="sxs-lookup"><span data-stu-id="4afdb-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="4afdb-125">Representa un elemento de contacto de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-125">Represents an Exchange contact item to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="4afdb-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="4afdb-127">Representa una lista de distribución para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-127">Represents a distribution list to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="4afdb-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="4afdb-129">Representa un mensaje de reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-129">Represents a meeting message to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4afdb-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4afdb-131">Representa una convocatoria de reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-131">Represents a meeting request to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="4afdb-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="4afdb-133">Representa una respuesta a la reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-133">Represents a meeting response to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="4afdb-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="4afdb-135">Representa la cancelación de la reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-135">Represents a meeting cancellation to create.</span></span>  <br/> |
|[<span data-ttu-id="4afdb-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="4afdb-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="4afdb-137">Representa una tarea a crear.</span><span class="sxs-lookup"><span data-stu-id="4afdb-137">Represents a task to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4afdb-138">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4afdb-138">Parent elements</span></span>

|<span data-ttu-id="4afdb-139">**Element**</span><span class="sxs-lookup"><span data-stu-id="4afdb-139">**Element**</span></span>|<span data-ttu-id="4afdb-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4afdb-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4afdb-141">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="4afdb-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="4afdb-142">Contiene una matriz de secuencia de tipos de cambios que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4afdb-142">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4afdb-143">Notas</span><span class="sxs-lookup"><span data-stu-id="4afdb-143">Remarks</span></span>

<span data-ttu-id="4afdb-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4afdb-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4afdb-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4afdb-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4afdb-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4afdb-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4afdb-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4afdb-147">Schema name</span></span>  <br/> |<span data-ttu-id="4afdb-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4afdb-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="4afdb-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4afdb-149">Validation file</span></span>  <br/> |<span data-ttu-id="4afdb-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4afdb-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4afdb-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4afdb-151">Can be empty</span></span>  <br/> |<span data-ttu-id="4afdb-152">False</span><span class="sxs-lookup"><span data-stu-id="4afdb-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4afdb-153">Ver también</span><span class="sxs-lookup"><span data-stu-id="4afdb-153">See also</span></span>



[<span data-ttu-id="4afdb-154">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="4afdb-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="4afdb-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4afdb-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


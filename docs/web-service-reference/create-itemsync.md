---
title: Create (ItemSync)
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
ms.openlocfilehash: d49e54c64f7bd53dcb296d998a856c20570d81be
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353948"
---
# <a name="create-itemsync"></a><span data-ttu-id="8c943-103">Create (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="8c943-103">Create (ItemSync)</span></span>

<span data-ttu-id="8c943-104">El elemento **Create** identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="8c943-104">The **Create** element identifies a single item to create in the local client store.</span></span> 
  
- [<span data-ttu-id="8c943-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="8c943-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="8c943-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8c943-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="8c943-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8c943-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) 
- [<span data-ttu-id="8c943-108">Changes (Items)</span><span class="sxs-lookup"><span data-stu-id="8c943-108">Changes (Items)</span></span>](changes-items.md) 
- [<span data-ttu-id="8c943-109">Create (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="8c943-109">Create (ItemSync)</span></span>](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

```xml
<Create>
   <Task/> 
</Create>
```

```xml
<Create>
   <MeetingResponse/>
</Create>
```

```xml
<Create>
   <CalendarItem/>
</Create>
```

```xml
<Create>
   <MeetingMessage/>
</Create>
```

```xml
<Create>
   <DistributionList/>
</Create>
```

```xml
<Create>
   <MeetingCancellation/>
</Create>
```

```xml
<Create>
   <MeetingRequest/> 
</Create>
```

```xml
<Create>
   <Message/> 
</Create>
```

```xml
<Create>
   <Contact/> 
</Create>
```

<span data-ttu-id="8c943-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="8c943-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8c943-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8c943-111">Attributes and elements</span></span>

<span data-ttu-id="8c943-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8c943-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c943-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c943-113">Attributes</span></span>

<span data-ttu-id="8c943-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8c943-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8c943-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c943-115">Child elements</span></span>

|<span data-ttu-id="8c943-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c943-116">**Element**</span></span>|<span data-ttu-id="8c943-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c943-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c943-118">Item</span><span class="sxs-lookup"><span data-stu-id="8c943-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="8c943-119">Representa un elemento genérico de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-119">Represents a generic Exchange item to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-120">Message</span><span class="sxs-lookup"><span data-stu-id="8c943-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8c943-121">Representa un mensaje de correo electrónico de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-121">Represents an Exchange e-mail message to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8c943-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8c943-123">Representa un elemento de calendario de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-123">Represents an Exchange calendar item to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-124">Contact</span><span class="sxs-lookup"><span data-stu-id="8c943-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="8c943-125">Representa un elemento de contacto de Exchange para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-125">Represents an Exchange contact item to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="8c943-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="8c943-127">Representa una lista de distribución para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-127">Represents a distribution list to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="8c943-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="8c943-129">Representa un mensaje de reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-129">Represents a meeting message to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8c943-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8c943-131">Representa una convocatoria de reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-131">Represents a meeting request to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="8c943-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="8c943-133">Representa una respuesta a la reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-133">Represents a meeting response to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="8c943-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="8c943-135">Representa la cancelación de la reunión para crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-135">Represents a meeting cancellation to create.</span></span>  <br/> |
|[<span data-ttu-id="8c943-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="8c943-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="8c943-137">Representa una tarea a crear.</span><span class="sxs-lookup"><span data-stu-id="8c943-137">Represents a task to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8c943-138">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8c943-138">Parent elements</span></span>

|<span data-ttu-id="8c943-139">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c943-139">**Element**</span></span>|<span data-ttu-id="8c943-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c943-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c943-141">Changes (Items)</span><span class="sxs-lookup"><span data-stu-id="8c943-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="8c943-142">Contiene una matriz de secuencia de tipos de cambios que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c943-142">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c943-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c943-143">Remarks</span></span>

<span data-ttu-id="8c943-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8c943-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c943-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8c943-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c943-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c943-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8c943-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8c943-147">Schema name</span></span>  <br/> |<span data-ttu-id="8c943-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8c943-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="8c943-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8c943-149">Validation file</span></span>  <br/> |<span data-ttu-id="8c943-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8c943-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8c943-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8c943-151">Can be empty</span></span>  <br/> |<span data-ttu-id="8c943-152">False</span><span class="sxs-lookup"><span data-stu-id="8c943-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c943-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c943-153">See also</span></span>

- [<span data-ttu-id="8c943-154">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="8c943-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="8c943-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8c943-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


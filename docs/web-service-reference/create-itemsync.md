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
description: El elemento Create identifica un solo elemento que se va a crear en el almacén de cliente local.
ms.openlocfilehash: b9c0f28333594a6c17ee9581a227fc4773874fd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460802"
---
# <a name="create-itemsync"></a><span data-ttu-id="860fc-103">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="860fc-103">Create (ItemSync)</span></span>

<span data-ttu-id="860fc-104">El elemento **Create** identifica un solo elemento que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="860fc-104">The **Create** element identifies a single item to create in the local client store.</span></span> 
  
- [<span data-ttu-id="860fc-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="860fc-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="860fc-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="860fc-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="860fc-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="860fc-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) 
- [<span data-ttu-id="860fc-108">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="860fc-108">Changes (Items)</span></span>](changes-items.md) 
- [<span data-ttu-id="860fc-109">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="860fc-109">Create (ItemSync)</span></span>](create-itemsync.md)
  
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

<span data-ttu-id="860fc-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="860fc-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="860fc-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="860fc-111">Attributes and elements</span></span>

<span data-ttu-id="860fc-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="860fc-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="860fc-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="860fc-113">Attributes</span></span>

<span data-ttu-id="860fc-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="860fc-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="860fc-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="860fc-115">Child elements</span></span>

|<span data-ttu-id="860fc-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="860fc-116">**Element**</span></span>|<span data-ttu-id="860fc-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="860fc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="860fc-118">Item</span><span class="sxs-lookup"><span data-stu-id="860fc-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="860fc-119">Representa un elemento de Exchange genérico que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-119">Represents a generic Exchange item to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-120">Mensaje</span><span class="sxs-lookup"><span data-stu-id="860fc-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="860fc-121">Representa un mensaje de correo electrónico de Exchange que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-121">Represents an Exchange e-mail message to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="860fc-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="860fc-123">Representa un elemento de calendario de Exchange que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-123">Represents an Exchange calendar item to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-124">Contacto</span><span class="sxs-lookup"><span data-stu-id="860fc-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="860fc-125">Representa un elemento de contacto de Exchange que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-125">Represents an Exchange contact item to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="860fc-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="860fc-127">Representa una lista de distribución que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-127">Represents a distribution list to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="860fc-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="860fc-129">Representa un mensaje de reunión que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-129">Represents a meeting message to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="860fc-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="860fc-131">Representa una convocatoria de reunión que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-131">Represents a meeting request to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="860fc-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="860fc-133">Representa una respuesta de reunión que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-133">Represents a meeting response to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="860fc-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="860fc-135">Representa una cancelación de reunión que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-135">Represents a meeting cancellation to create.</span></span>  <br/> |
|[<span data-ttu-id="860fc-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="860fc-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="860fc-137">Representa una tarea que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="860fc-137">Represents a task to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="860fc-138">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="860fc-138">Parent elements</span></span>

|<span data-ttu-id="860fc-139">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="860fc-139">**Element**</span></span>|<span data-ttu-id="860fc-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="860fc-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="860fc-141">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="860fc-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="860fc-142">Contiene una matriz de secuencias de tipos de cambio que representan los tipos de diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="860fc-142">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="860fc-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="860fc-143">Remarks</span></span>

<span data-ttu-id="860fc-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="860fc-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="860fc-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="860fc-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="860fc-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="860fc-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="860fc-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="860fc-147">Schema name</span></span>  <br/> |<span data-ttu-id="860fc-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="860fc-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="860fc-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="860fc-149">Validation file</span></span>  <br/> |<span data-ttu-id="860fc-150">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="860fc-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="860fc-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="860fc-151">Can be empty</span></span>  <br/> |<span data-ttu-id="860fc-152">Falso</span><span class="sxs-lookup"><span data-stu-id="860fc-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="860fc-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="860fc-153">See also</span></span>

- [<span data-ttu-id="860fc-154">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="860fc-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="860fc-155">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="860fc-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


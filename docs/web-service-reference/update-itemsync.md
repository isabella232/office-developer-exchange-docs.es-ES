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
description: El elemento Update identifica un solo elemento que se debe actualizar en el almacén del cliente local.
ms.openlocfilehash: 12248cbbd5d47a19e36d49fcebe6d4753a2e162f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468890"
---
# <a name="update-itemsync"></a><span data-ttu-id="acb24-103">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="acb24-103">Update (ItemSync)</span></span>

<span data-ttu-id="acb24-104">El elemento **Update** identifica un solo elemento que se debe actualizar en el almacén del cliente local.</span><span class="sxs-lookup"><span data-stu-id="acb24-104">The **Update** element identifies a single item to update in the local client store.</span></span> 
  
- [<span data-ttu-id="acb24-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="acb24-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="acb24-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="acb24-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="acb24-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="acb24-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="acb24-108">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="acb24-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="acb24-109">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="acb24-109">Update (ItemSync)</span></span>](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

```xml
<Update>
   <MeetingRequest/>
</Update>
```

```xml
<Update>
   <MeetingCancellation/>
</Update>
```

```xml
<Update>
   <Task/>
</Update>
```

```xml
<Update>
   <CalendarItem/>
</Update>
```

```xml
<Update>
   <MeetingResponse/>
</Update>
```

```xml
<Update>
   <Message/>
</Update>
```

```xml
<Update>
   <DistributionList/>
</Update>
```

```xml
<Update>
   <MeetingMessage/>
</Update>
```

```xml
<Update>
   <Contact/> 
</Update>
```

<span data-ttu-id="acb24-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="acb24-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="acb24-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="acb24-111">Attributes and elements</span></span>

<span data-ttu-id="acb24-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="acb24-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acb24-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="acb24-113">Attributes</span></span>

<span data-ttu-id="acb24-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="acb24-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acb24-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="acb24-115">Child elements</span></span>

|<span data-ttu-id="acb24-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="acb24-116">**Element**</span></span>|<span data-ttu-id="acb24-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acb24-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acb24-118">Item</span><span class="sxs-lookup"><span data-stu-id="acb24-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="acb24-119">Representa un elemento de Exchange genérico que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-119">Represents a generic Exchange item to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-120">Message</span><span class="sxs-lookup"><span data-stu-id="acb24-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="acb24-121">Representa un mensaje de correo electrónico de Exchange que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-121">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="acb24-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="acb24-123">Representa un elemento de calendario de Exchange que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-123">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-124">Contacto</span><span class="sxs-lookup"><span data-stu-id="acb24-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="acb24-125">Representa un elemento de contacto de Exchange que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-125">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="acb24-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="acb24-127">Representa una lista de distribución que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-127">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="acb24-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="acb24-129">Representa un mensaje de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-129">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="acb24-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="acb24-131">Representa una convocatoria de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-131">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="acb24-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="acb24-133">Representa una respuesta de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-133">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="acb24-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="acb24-135">Representa una cancelación de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-135">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="acb24-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="acb24-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="acb24-137">Representa una tarea que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="acb24-137">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="acb24-138">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="acb24-138">Parent elements</span></span>

|<span data-ttu-id="acb24-139">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="acb24-139">**Element**</span></span>|<span data-ttu-id="acb24-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acb24-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acb24-141">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="acb24-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="acb24-142">Contiene una matriz de secuencias de tipos de cambios que representan el tipo de diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="acb24-142">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acb24-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="acb24-143">Remarks</span></span>

<span data-ttu-id="acb24-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="acb24-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acb24-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="acb24-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acb24-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="acb24-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="acb24-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="acb24-147">Schema name</span></span>  <br/> |<span data-ttu-id="acb24-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="acb24-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="acb24-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="acb24-149">Validation file</span></span>  <br/> |<span data-ttu-id="acb24-150">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="acb24-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="acb24-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="acb24-151">Can be empty</span></span>  <br/> |<span data-ttu-id="acb24-152">Falso</span><span class="sxs-lookup"><span data-stu-id="acb24-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="acb24-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="acb24-153">See also</span></span>

- [<span data-ttu-id="acb24-154">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="acb24-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="acb24-155">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="acb24-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


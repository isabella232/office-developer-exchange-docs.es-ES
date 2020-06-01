---
title: SetItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetItemField
api_type:
- schema
ms.assetid: 85284fcb-bd1e-4fda-9dab-cb4cd637cd5b
description: El elemento SetItemField representa una actualización de una propiedad única de un elemento en una operación de UpdateItem.
ms.openlocfilehash: b4606eb7d94b9d0c4c5bcd5a2b56d73a4d4270cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467427"
---
# <a name="setitemfield"></a><span data-ttu-id="23bfc-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="23bfc-103">SetItemField</span></span>

<span data-ttu-id="23bfc-104">El elemento **SetItemField** representa una actualización de una propiedad única de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="23bfc-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
```xml
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingRequest/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingResponse/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Contact/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <DistributionList/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingResponse/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingResponse/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingRequest/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Contact/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Message/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Task/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Message/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingCancellation/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Task/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingRequest/>  
</SetItemField>
```

```xml
<SetItemField>
    <FieldURI/> 
    <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
    <IndexedFieldURI/> 
    <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingCancellation/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <DistributionList/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingCancellation/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Task/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Message/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <DistributionList/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Contact/> 
</SetItemField>
```


<span data-ttu-id="23bfc-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="23bfc-105">**SetItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="23bfc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="23bfc-106">Attributes and elements</span></span>

<span data-ttu-id="23bfc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="23bfc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23bfc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="23bfc-108">Attributes</span></span>

<span data-ttu-id="23bfc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="23bfc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23bfc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="23bfc-110">Child elements</span></span>

|<span data-ttu-id="23bfc-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="23bfc-111">**Element**</span></span>|<span data-ttu-id="23bfc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23bfc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23bfc-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="23bfc-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="23bfc-114">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="23bfc-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="23bfc-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="23bfc-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="23bfc-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="23bfc-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="23bfc-118">Identifica las propiedades MAPI extendidas que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="23bfc-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="23bfc-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="23bfc-120">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="23bfc-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-121">Mensaje</span><span class="sxs-lookup"><span data-stu-id="23bfc-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="23bfc-122">Representa un mensaje de correo electrónico de Exchange que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="23bfc-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="23bfc-124">Representa un elemento de calendario de Exchange que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-125">Contacto</span><span class="sxs-lookup"><span data-stu-id="23bfc-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="23bfc-126">Representa un elemento de contacto de Exchange que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="23bfc-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="23bfc-128">Representa una lista de distribución que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="23bfc-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="23bfc-130">Representa un mensaje de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="23bfc-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="23bfc-132">Representa una convocatoria de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="23bfc-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="23bfc-134">Representa una respuesta de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="23bfc-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="23bfc-136">Representa una cancelación de reunión que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="23bfc-137">Tarea</span><span class="sxs-lookup"><span data-stu-id="23bfc-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="23bfc-138">Representa una tarea que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="23bfc-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23bfc-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="23bfc-139">Parent elements</span></span>

|<span data-ttu-id="23bfc-140">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="23bfc-140">**Element**</span></span>|<span data-ttu-id="23bfc-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23bfc-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23bfc-142">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="23bfc-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="23bfc-143">Contiene un conjunto de elementos que definen los cambios de anexar, establecer y eliminar en las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="23bfc-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23bfc-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23bfc-144">Remarks</span></span>

<span data-ttu-id="23bfc-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="23bfc-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23bfc-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="23bfc-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23bfc-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="23bfc-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23bfc-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="23bfc-148">Schema Name</span></span>  <br/> |<span data-ttu-id="23bfc-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="23bfc-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="23bfc-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="23bfc-150">Validation File</span></span>  <br/> |<span data-ttu-id="23bfc-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="23bfc-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="23bfc-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="23bfc-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="23bfc-153">Falso</span><span class="sxs-lookup"><span data-stu-id="23bfc-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23bfc-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="23bfc-154">See also</span></span>

- [<span data-ttu-id="23bfc-155">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="23bfc-155">UpdateItem operation</span></span>](updateitem-operation.md)


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
description: El elemento SetItemField representa una actualización para una única propiedad de un elemento en una operación UpdateItem.
ms.openlocfilehash: bd3e5bca3d61325ef3f218c5ada535346247f391
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353801"
---
# <a name="setitemfield"></a><span data-ttu-id="5fab4-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="5fab4-103">SetItemField</span></span>

<span data-ttu-id="5fab4-104">El elemento **SetItemField** representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5fab4-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
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


<span data-ttu-id="5fab4-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="5fab4-105">**SetItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5fab4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5fab4-106">Attributes and elements</span></span>

<span data-ttu-id="5fab4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5fab4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5fab4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5fab4-108">Attributes</span></span>

<span data-ttu-id="5fab4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5fab4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5fab4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5fab4-110">Child elements</span></span>

|<span data-ttu-id="5fab4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fab4-111">**Element**</span></span>|<span data-ttu-id="5fab4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5fab4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fab4-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="5fab4-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="5fab4-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="5fab4-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="5fab4-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="5fab4-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="5fab4-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="5fab4-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="5fab4-118">Identifica las propiedades extendidas de MAPI para establecer.</span><span class="sxs-lookup"><span data-stu-id="5fab4-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-119">Item</span><span class="sxs-lookup"><span data-stu-id="5fab4-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="5fab4-120">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5fab4-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-121">Message</span><span class="sxs-lookup"><span data-stu-id="5fab4-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5fab4-122">Representa un mensaje de correo electrónico de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5fab4-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5fab4-124">Representa un elemento de calendario de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-125">Contact</span><span class="sxs-lookup"><span data-stu-id="5fab4-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5fab4-126">Representa un elemento de contacto de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="5fab4-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="5fab4-128">Representa una lista de distribución que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5fab4-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="5fab4-130">Representa un mensaje de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5fab4-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5fab4-132">Representa una convocatoria de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="5fab4-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="5fab4-134">Representa una respuesta a la reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="5fab4-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="5fab4-136">Representa una cancelación de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="5fab4-137">Tarea</span><span class="sxs-lookup"><span data-stu-id="5fab4-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="5fab4-138">Representa una tarea que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="5fab4-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5fab4-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5fab4-139">Parent elements</span></span>

|<span data-ttu-id="5fab4-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fab4-140">**Element**</span></span>|<span data-ttu-id="5fab4-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5fab4-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fab4-142">Updates (Elemento)</span><span class="sxs-lookup"><span data-stu-id="5fab4-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="5fab4-143">Contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="5fab4-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fab4-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5fab4-144">Remarks</span></span>

<span data-ttu-id="5fab4-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5fab4-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5fab4-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5fab4-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fab4-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5fab4-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5fab4-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5fab4-148">Schema Name</span></span>  <br/> |<span data-ttu-id="5fab4-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5fab4-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="5fab4-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5fab4-150">Validation File</span></span>  <br/> |<span data-ttu-id="5fab4-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5fab4-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5fab4-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5fab4-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="5fab4-153">False</span><span class="sxs-lookup"><span data-stu-id="5fab4-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fab4-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fab4-154">See also</span></span>

- [<span data-ttu-id="5fab4-155">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="5fab4-155">UpdateItem operation</span></span>](updateitem-operation.md)


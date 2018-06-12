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
ms.openlocfilehash: 012e6ae21af653b4bf12588e5a97334a62884059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837439"
---
# <a name="setitemfield"></a><span data-ttu-id="4b8c0-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="4b8c0-103">SetItemField</span></span>

<span data-ttu-id="4b8c0-104">El elemento **SetItemField** representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="4b8c0-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
```xml
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

 <span data-ttu-id="4b8c0-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="4b8c0-105">**SetItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b8c0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4b8c0-106">Attributes and elements</span></span>

<span data-ttu-id="4b8c0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b8c0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4b8c0-108">Attributes</span></span>

<span data-ttu-id="4b8c0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b8c0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4b8c0-110">Child elements</span></span>

|<span data-ttu-id="4b8c0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b8c0-111">**Element**</span></span>|<span data-ttu-id="4b8c0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4b8c0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b8c0-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="4b8c0-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="4b8c0-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4b8c0-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="4b8c0-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4b8c0-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="4b8c0-118">Identifica las propiedades extendidas de MAPI para establecer.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-119">Item</span><span class="sxs-lookup"><span data-stu-id="4b8c0-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="4b8c0-120">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-121">Message</span><span class="sxs-lookup"><span data-stu-id="4b8c0-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4b8c0-122">Representa un mensaje de correo electrónico de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4b8c0-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4b8c0-124">Representa un elemento de calendario de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-125">Contact</span><span class="sxs-lookup"><span data-stu-id="4b8c0-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="4b8c0-126">Representa un elemento de contacto de Exchange para actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="4b8c0-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="4b8c0-128">Representa una lista de distribución que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="4b8c0-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="4b8c0-130">Representa un mensaje de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4b8c0-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4b8c0-132">Representa una convocatoria de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="4b8c0-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="4b8c0-134">Representa una respuesta a la reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="4b8c0-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="4b8c0-136">Representa una cancelación de reunión que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="4b8c0-137">Tarea</span><span class="sxs-lookup"><span data-stu-id="4b8c0-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="4b8c0-138">Representa una tarea que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4b8c0-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4b8c0-139">Parent elements</span></span>

|<span data-ttu-id="4b8c0-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b8c0-140">**Element**</span></span>|<span data-ttu-id="4b8c0-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4b8c0-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b8c0-142">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="4b8c0-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="4b8c0-143">Contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b8c0-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4b8c0-144">Remarks</span></span>

<span data-ttu-id="4b8c0-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4b8c0-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b8c0-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4b8c0-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b8c0-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b8c0-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4b8c0-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4b8c0-148">Schema Name</span></span>  <br/> |<span data-ttu-id="4b8c0-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4b8c0-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="4b8c0-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4b8c0-150">Validation File</span></span>  <br/> |<span data-ttu-id="4b8c0-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4b8c0-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4b8c0-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4b8c0-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b8c0-153">False</span><span class="sxs-lookup"><span data-stu-id="4b8c0-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b8c0-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="4b8c0-154">See also</span></span>



[<span data-ttu-id="4b8c0-155">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="4b8c0-155">UpdateItem operation</span></span>](updateitem-operation.md)


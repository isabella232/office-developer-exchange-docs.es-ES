---
title: AppendToItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppendToItemField
api_type:
- schema
ms.assetid: 66dbcb4a-ae6d-4648-8610-67187bdb105c
description: El elemento AppendToItemField identifica los datos que se van a anexar a una única propiedad de un elemento durante una operación de UpdateItem.
ms.openlocfilehash: 902239155bff45d6f81989de954c9459cf012288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466048"
---
# <a name="appendtoitemfield"></a><span data-ttu-id="c491d-103">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="c491d-103">AppendToItemField</span></span>

<span data-ttu-id="c491d-104">El elemento **AppendToItemField** identifica los datos que se van a anexar a una única propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c491d-104">The **AppendToItemField** element identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>
  
- [<span data-ttu-id="c491d-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c491d-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="c491d-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="c491d-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="c491d-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="c491d-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="c491d-108">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="c491d-108">Updates (Item)</span></span>](updates-item.md)
  
- [<span data-ttu-id="c491d-109">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="c491d-109">AppendToItemField</span></span>](appendtoitemfield.md)
  
```xml
<AppendToItemField>
   <FieldURI/>
   <Item/>
</AppendToItemField>
```

 <span data-ttu-id="c491d-110">**AppendToItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="c491d-110">**AppendToItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c491d-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c491d-111">Attributes and elements</span></span>

<span data-ttu-id="c491d-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c491d-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c491d-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="c491d-113">Attributes</span></span>

<span data-ttu-id="c491d-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c491d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c491d-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c491d-115">Child elements</span></span>

|<span data-ttu-id="c491d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c491d-116">**Element**</span></span>|<span data-ttu-id="c491d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c491d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c491d-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c491d-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="c491d-119">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="c491d-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="c491d-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c491d-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="c491d-121">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="c491d-121">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="c491d-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c491d-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="c491d-123">Identifica las propiedades MAPI extendidas que se van a anexar.</span><span class="sxs-lookup"><span data-stu-id="c491d-123">Identifies extended MAPI properties to append.</span></span>  <br/> |
|[<span data-ttu-id="c491d-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="c491d-124">Item</span></span>](item.md) <br/> |<span data-ttu-id="c491d-125">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-125">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c491d-126">Message</span><span class="sxs-lookup"><span data-stu-id="c491d-126">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c491d-127">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-127">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c491d-128">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c491d-128">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c491d-129">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-129">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c491d-130">Contacto</span><span class="sxs-lookup"><span data-stu-id="c491d-130">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c491d-131">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-131">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="c491d-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c491d-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c491d-133">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="c491d-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="c491d-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="c491d-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="c491d-135">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c491d-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="c491d-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="c491d-137">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c491d-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c491d-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c491d-139">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c491d-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="c491d-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="c491d-141">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c491d-142">Tarea</span><span class="sxs-lookup"><span data-stu-id="c491d-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="c491d-143">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c491d-143">Represents a task in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c491d-144">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c491d-144">Parent elements</span></span>

|<span data-ttu-id="c491d-145">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c491d-145">**Element**</span></span>|<span data-ttu-id="c491d-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c491d-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c491d-147">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="c491d-147">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="c491d-148">Contiene una matriz que define los cambios de anexión, establecimiento y eliminación en las propiedades de elemento.</span><span class="sxs-lookup"><span data-stu-id="c491d-148">Contains an array that defines append, set, and delete changes to item properties.</span></span>  <br/> <span data-ttu-id="c491d-149">La siguiente es la expresión XPath a este elemento:`/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="c491d-149">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c491d-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c491d-150">Remarks</span></span>

<span data-ttu-id="c491d-151">Solo algunas propiedades admiten operaciones de anexión.</span><span class="sxs-lookup"><span data-stu-id="c491d-151">Only certain properties support append operations.</span></span> <span data-ttu-id="c491d-152">Si se intenta anexar a una propiedad que no admite la anexión, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="c491d-152">An attempt to append to a property that does not support appending will result in an error.</span></span>
  
<span data-ttu-id="c491d-153">Para las operaciones de actualización, solo se puede modificar una propiedad en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="c491d-153">For update operations, only one property can be modified within a single request.</span></span> <span data-ttu-id="c491d-154">Se debe hacer referencia a esa propiedad única en el elemento [path](path.md) .</span><span class="sxs-lookup"><span data-stu-id="c491d-154">That single property must be referenced in the [Path](path.md) element.</span></span> <span data-ttu-id="c491d-155">El elemento **Item** de las clases derivadas solo puede contener una única propiedad que esté dentro del acuerdo con el elemento **path** único.</span><span class="sxs-lookup"><span data-stu-id="c491d-155">The **Item** element in the derived classes can then only hold a single property that is in agreement with the single **Path** element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c491d-156">El elemento [path](path.md) es abstracto.</span><span class="sxs-lookup"><span data-stu-id="c491d-156">The [Path](path.md) element is abstract.</span></span> <span data-ttu-id="c491d-157">Debe sustituirse por el elemento [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)o [ExtendedFieldURI](extendedfielduri.md) .</span><span class="sxs-lookup"><span data-stu-id="c491d-157">It must be substituted by the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="c491d-158">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c491d-158">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c491d-159">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c491d-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c491d-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="c491d-160">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c491d-161">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c491d-161">Schema Name</span></span>  <br/> |<span data-ttu-id="c491d-162">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c491d-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="c491d-163">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c491d-163">Validation File</span></span>  <br/> |<span data-ttu-id="c491d-164">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c491d-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c491d-165">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c491d-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="c491d-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c491d-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c491d-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="c491d-167">See also</span></span>

- [<span data-ttu-id="c491d-168">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c491d-168">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="c491d-169">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c491d-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


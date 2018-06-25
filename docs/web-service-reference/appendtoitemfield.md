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
description: El elemento AppendToItemField identifica los datos que se anexará a una sola propiedad de un elemento durante una operación UpdateItem.
ms.openlocfilehash: b432399e84ee4a3fd7edc5d3f803079435c79143
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763454"
---
# <a name="appendtoitemfield"></a><span data-ttu-id="26440-103">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="26440-103">AppendToItemField</span></span>

<span data-ttu-id="26440-104">El elemento **AppendToItemField** identifica los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="26440-104">The **AppendToItemField** element identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>
  
- [<span data-ttu-id="26440-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="26440-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="26440-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="26440-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="26440-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="26440-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="26440-108">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="26440-108">Updates (Item)</span></span>](updates-item.md)
  
- [<span data-ttu-id="26440-109">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="26440-109">AppendToItemField</span></span>](appendtoitemfield.md)
  
```xml
<AppendToItemField>
   <FieldURI/>
   <Item/>
</AppendToItemField>
```

 <span data-ttu-id="26440-110">**AppendToItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="26440-110">**AppendToItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26440-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26440-111">Attributes and elements</span></span>

<span data-ttu-id="26440-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26440-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26440-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="26440-113">Attributes</span></span>

<span data-ttu-id="26440-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26440-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26440-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26440-115">Child elements</span></span>

|<span data-ttu-id="26440-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="26440-116">**Element**</span></span>|<span data-ttu-id="26440-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26440-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26440-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="26440-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="26440-119">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="26440-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="26440-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="26440-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="26440-121">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="26440-121">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="26440-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="26440-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="26440-123">Identifica las propiedades extendidas de MAPI para anexar.</span><span class="sxs-lookup"><span data-stu-id="26440-123">Identifies extended MAPI properties to append.</span></span>  <br/> |
|[<span data-ttu-id="26440-124">Item</span><span class="sxs-lookup"><span data-stu-id="26440-124">Item</span></span>](item.md) <br/> |<span data-ttu-id="26440-125">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-125">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="26440-126">Message</span><span class="sxs-lookup"><span data-stu-id="26440-126">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="26440-127">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-127">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="26440-128">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="26440-128">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="26440-129">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-129">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="26440-130">Contact</span><span class="sxs-lookup"><span data-stu-id="26440-130">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="26440-131">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-131">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="26440-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="26440-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="26440-133">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="26440-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="26440-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="26440-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="26440-135">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="26440-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="26440-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="26440-137">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="26440-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="26440-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="26440-139">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="26440-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="26440-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="26440-141">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="26440-142">Tarea</span><span class="sxs-lookup"><span data-stu-id="26440-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="26440-143">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26440-143">Represents a task in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26440-144">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26440-144">Parent elements</span></span>

|<span data-ttu-id="26440-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="26440-145">**Element**</span></span>|<span data-ttu-id="26440-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26440-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26440-147">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="26440-147">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="26440-148">Contiene una matriz que define append, establecer y eliminar los cambios realizados en las propiedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="26440-148">Contains an array that defines append, set, and delete changes to item properties.</span></span>  <br/> <span data-ttu-id="26440-149">La siguiente es la expresión de XPath para este elemento:`/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="26440-149">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26440-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26440-150">Remarks</span></span>

<span data-ttu-id="26440-151">Sólo el soporte de ciertas propiedades anexe operaciones.</span><span class="sxs-lookup"><span data-stu-id="26440-151">Only certain properties support append operations.</span></span> <span data-ttu-id="26440-152">Anexar a una propiedad que no es compatible con la anexión de un intento, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="26440-152">An attempt to append to a property that does not support appending will result in an error.</span></span>
  
<span data-ttu-id="26440-153">Las operaciones de actualización, puede modificarse únicamente una propiedad dentro de una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="26440-153">For update operations, only one property can be modified within a single request.</span></span> <span data-ttu-id="26440-154">Debe hacer referencia a dicha propiedad único en el elemento de [ruta de acceso](path.md) .</span><span class="sxs-lookup"><span data-stu-id="26440-154">That single property must be referenced in the [Path](path.md) element.</span></span> <span data-ttu-id="26440-155">**El elemento en el que las clases derivadas** , a continuación, puede contener únicamente una sola propiedad que está de acuerdo con el único elemento de **ruta de acceso** .</span><span class="sxs-lookup"><span data-stu-id="26440-155">The **Item** element in the derived classes can then only hold a single property that is in agreement with the single **Path** element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="26440-156">El elemento de [ruta de acceso](path.md) es abstracto.</span><span class="sxs-lookup"><span data-stu-id="26440-156">The [Path](path.md) element is abstract.</span></span> <span data-ttu-id="26440-157">Se debe sustituir por el elemento [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)o [ExtendedFieldURI](extendedfielduri.md) .</span><span class="sxs-lookup"><span data-stu-id="26440-157">It must be substituted by the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="26440-158">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="26440-158">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26440-159">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26440-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26440-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26440-160">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26440-161">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26440-161">Schema Name</span></span>  <br/> |<span data-ttu-id="26440-162">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="26440-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="26440-163">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26440-163">Validation File</span></span>  <br/> |<span data-ttu-id="26440-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26440-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26440-165">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26440-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="26440-166">False</span><span class="sxs-lookup"><span data-stu-id="26440-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26440-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="26440-167">See also</span></span>

- [<span data-ttu-id="26440-168">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="26440-168">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="26440-169">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="26440-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: UpdateItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: La operación UpdateItem se usa para modificar las propiedades de un elemento existente en el almacén de Exchange.
ms.openlocfilehash: 009ba16315017c4418fbd71d49744015c4d6d1b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840841"
---
# <a name="updateitem-operation"></a><span data-ttu-id="00478-103">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="00478-103">UpdateItem operation</span></span>

<span data-ttu-id="00478-104">La operación **UpdateItem** se usa para modificar las propiedades de un elemento existente en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="00478-104">The **UpdateItem** operation is used to modify the properties of an existing item in the Exchange store.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="00478-105">Notas</span><span class="sxs-lookup"><span data-stu-id="00478-105">Remarks</span></span>

<span data-ttu-id="00478-106">Se pueden realizar tres acciones de actualización básica en un elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-106">You can perform three basic update actions on an item.</span></span> <span data-ttu-id="00478-107">En la siguiente tabla se enumera las acciones que puede realizar.</span><span class="sxs-lookup"><span data-stu-id="00478-107">The following table lists the actions that you can perform.</span></span>
  
|<span data-ttu-id="00478-108">**Acción**</span><span class="sxs-lookup"><span data-stu-id="00478-108">**Action**</span></span>|<span data-ttu-id="00478-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00478-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00478-110">Anexar</span><span class="sxs-lookup"><span data-stu-id="00478-110">Append</span></span>  <br/> |<span data-ttu-id="00478-111">Agrega datos a una propiedad existente.</span><span class="sxs-lookup"><span data-stu-id="00478-111">Adds data to an existing property.</span></span> <span data-ttu-id="00478-112">Esta acción conserva los datos actuales.</span><span class="sxs-lookup"><span data-stu-id="00478-112">This action preserves the current data.</span></span> <span data-ttu-id="00478-113">Append no se aplica a todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="00478-113">Append does not apply to all properties.</span></span>  <br/> |
|<span data-ttu-id="00478-114">Activado</span><span class="sxs-lookup"><span data-stu-id="00478-114">Set</span></span>  <br/> |<span data-ttu-id="00478-115">Reemplaza los datos de una propiedad si la propiedad contiene datos, o crea la propiedad y establece su valor si la propiedad no existe.</span><span class="sxs-lookup"><span data-stu-id="00478-115">Replaces data for a property if the property contains data, or creates the property and sets its value if the property does not exist.</span></span> <span data-ttu-id="00478-116">La acción de conjunto sólo es aplicable a propiedades modificables.</span><span class="sxs-lookup"><span data-stu-id="00478-116">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="00478-117">Eliminar</span><span class="sxs-lookup"><span data-stu-id="00478-117">Delete</span></span>  <br/> |<span data-ttu-id="00478-118">Quita una propiedad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-118">Removes a property from an item.</span></span> <span data-ttu-id="00478-119">Esto difiere de la configuración de una propiedad en un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="00478-119">This differs from setting a property to an empty value.</span></span> <span data-ttu-id="00478-120">Cuando finalice esta acción, la propiedad no existe para el elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-120">When this action is finished, the property does not exist for the item.</span></span> <span data-ttu-id="00478-121">Eliminar solo es aplicable a las propiedades de escritura.</span><span class="sxs-lookup"><span data-stu-id="00478-121">Delete is only applicable to writable properties.</span></span>  <br/> |
   
<span data-ttu-id="00478-122">Una llamada **UpdateItem** puede utilizarse para modificar uno o varios elementos y una o varias propiedades de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-122">An **UpdateItem** call can be used to modify one or more items, and one or more properties on each item.</span></span> <span data-ttu-id="00478-123">El elemento [ItemChanges](itemchanges.md) contiene todas las modificaciones que se van a realizar como parte de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="00478-123">The [ItemChanges](itemchanges.md) element contains all the modifications that are to be performed as part of this call.</span></span> <span data-ttu-id="00478-124">El elemento [ItemChange](itemchange.md) , un elemento secundario del elemento [ItemChanges](itemchanges.md) , representa las modificaciones que se debe realizar en un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-124">The [ItemChange](itemchange.md) element, a child of the [ItemChanges](itemchanges.md) element, represents the modifications to be performed on a single item.</span></span> <span data-ttu-id="00478-125">El elemento [ItemChange](itemchange.md) contiene un conjunto de acciones de actualización que se pueden realizar en un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-125">The [ItemChange](itemchange.md) element contains a set of update actions that can be performed on a single item.</span></span> <span data-ttu-id="00478-126">Estos cambios se encuentran en el elemento de [actualizaciones (elemento)](updates-item.md) .</span><span class="sxs-lookup"><span data-stu-id="00478-126">These changes are contained in the [Updates (Item)](updates-item.md) element.</span></span> <span data-ttu-id="00478-127">El elemento [ItemId](itemid.md) identifica el elemento que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="00478-127">The [ItemId](itemid.md) element identifies the item to update.</span></span> <span data-ttu-id="00478-128">Para actualizar más de una propiedad en un elemento, se debe proporcionar un [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md)o [DeleteItemField](deleteitemfield.md) para cada propiedad que requiere la actualización.</span><span class="sxs-lookup"><span data-stu-id="00478-128">To update more than one property on an item, a [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md), or [DeleteItemField](deleteitemfield.md) must be provided for each property that requires the update.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00478-129">Acciones de actualización se aplican en el orden en que se especifican.</span><span class="sxs-lookup"><span data-stu-id="00478-129">Update actions are applied in the order in which they are specified.</span></span> 
  
<span data-ttu-id="00478-130">Para cada cambio, es necesario especificar la ruta de acceso de la propiedad que se va a cambiar y una representación de ese elemento con su nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="00478-130">For each change, you have to specify the path of the property to change and a representation of that item with its new value.</span></span> <span data-ttu-id="00478-131">La acción de eliminar es ligeramente diferente en que se requiere sólo la ruta de acceso de la propiedad que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="00478-131">The delete action is slightly different in that only the path of the property that should be deleted is required.</span></span> <span data-ttu-id="00478-132">Para establecer y anexar acciones, la ruta de acceso especificada debe hacer referencia a la misma propiedad que se va a establecer en la representación del artículo.</span><span class="sxs-lookup"><span data-stu-id="00478-132">For set and append actions, the path that is specified must refer to the same property that is being set in the item representation.</span></span> <span data-ttu-id="00478-133">Si estos difieren, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="00478-133">If these differ, an error will be returned.</span></span>
  
<span data-ttu-id="00478-134">La operación **UpdateItem** puede establecer la hora de [Inicio](start.md) y [final](end-ex15websvcsotherref.md) de un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="00478-134">The **UpdateItem** operation can set the [Start](start.md) and [End ](end-ex15websvcsotherref.md) time of an Exchange store item.</span></span> <span data-ttu-id="00478-135">En una solicitud **UpdateItem** , se puede establecer la hora de [Inicio](start.md) sin establecer también la hora de [finalización](end-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="00478-135">In an **UpdateItem** request, the [Start](start.md) time can be set without also setting the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="00478-136">Esto puede producir un error si la hora de [Inicio](start.md) es posterior a la hora de [finalización](end-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="00478-136">This can cause an error if the [Start](start.md) time is later than the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="00478-137">Tenga en cuenta que las aplicaciones cliente deben ajustar la hora de [finalización](end-ex15websvcsotherref.md) cuando se cambia la hora de [Inicio](start.md) con el fin de conservar la duración.</span><span class="sxs-lookup"><span data-stu-id="00478-137">Be aware that client applications must adjust the [End ](end-ex15websvcsotherref.md) time when the [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
<span data-ttu-id="00478-138">Cuando se actualiza un elemento de calendario único se convierta en un elemento periódico del calendario principal, se debe establecer la propiedad [MeetingTimeZone](meetingtimezone.md) por la operación **UpdateItem** con el fin de conservar la zona horaria de original del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="00478-138">When a single calendar item is updated to become a recurring master calendar item, the [MeetingTimeZone](meetingtimezone.md) property must be set by the **UpdateItem** operation in order to preserve the calendar item's original time zone.</span></span> 
  
## <a name="setitemfield-request-example"></a><span data-ttu-id="00478-139">Ejemplo de solicitud de SetItemField</span><span class="sxs-lookup"><span data-stu-id="00478-139">SetItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="00478-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="00478-140">Description</span></span>

<span data-ttu-id="00478-141">El siguiente ejemplo de una solicitud de **UpdateItem** muestra cómo establecer la propiedad sensitivity de un elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-141">The following example of an **UpdateItem** request shows how to set the sensitivity property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="00478-142">Código</span><span class="sxs-lookup"><span data-stu-id="00478-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkb..." ChangeKey="CQAAABYAAAB..."/>
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Sensitivity"/>
              <t:Message>
                <t:Sensitivity>Normal</t:Sensitivity>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="00478-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00478-143">Comments</span></span>

<span data-ttu-id="00478-144">El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="00478-144">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="setitemfield-request-elements"></a><span data-ttu-id="00478-145">Elementos de solicitud de SetItemField</span><span class="sxs-lookup"><span data-stu-id="00478-145">SetItemField Request Elements</span></span>

<span data-ttu-id="00478-146">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="00478-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="00478-147">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="00478-147">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="00478-148">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="00478-148">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="00478-149">ItemChange</span><span class="sxs-lookup"><span data-stu-id="00478-149">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="00478-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="00478-150">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="00478-151">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="00478-151">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="00478-152">SetItemField</span><span class="sxs-lookup"><span data-stu-id="00478-152">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="00478-153">FieldURI</span><span class="sxs-lookup"><span data-stu-id="00478-153">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="00478-154">Message</span><span class="sxs-lookup"><span data-stu-id="00478-154">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="00478-155">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="00478-155">Sensitivity</span></span>](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a><span data-ttu-id="00478-156">Ejemplo de solicitud de AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="00478-156">AppendToItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="00478-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="00478-157">Description</span></span>

<span data-ttu-id="00478-158">El siguiente ejemplo de una solicitud de **UpdateItem** muestra cómo anexar texto a la propiedad body en un elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-158">The following example of an **UpdateItem** request shows how to append text to the body property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="00478-159">Código</span><span class="sxs-lookup"><span data-stu-id="00478-159">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYA..."/>
          <t:Updates>
            <t:AppendToItemField>
              <t:FieldURI FieldURI="item:Body"/>
              <t:Message>
                <t:Body BodyType="Text">Some additional text to append</t:Body>
              </t:Message>
            </t:AppendToItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="00478-160">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00478-160">Comments</span></span>

<span data-ttu-id="00478-161">Las siguientes propiedades admiten la acción de datos anexados:</span><span class="sxs-lookup"><span data-stu-id="00478-161">The following properties support the append action:</span></span>
  
- <span data-ttu-id="00478-162">**mensaje: ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="00478-162">**message:ReplyTo**</span></span>
    
- <span data-ttu-id="00478-163">**Cuerpo del elemento:**</span><span class="sxs-lookup"><span data-stu-id="00478-163">**item:Body**</span></span>
    
- <span data-ttu-id="00478-164">Todos los del destinatario y attendee propiedades de la colección</span><span class="sxs-lookup"><span data-stu-id="00478-164">All the recipient and attendee collection properties</span></span>
    
<span data-ttu-id="00478-165">El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="00478-165">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="appendtoitemfield-request-elements"></a><span data-ttu-id="00478-166">Elementos de solicitud de AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="00478-166">AppendToItemField Request Elements</span></span>

<span data-ttu-id="00478-167">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="00478-167">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="00478-168">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="00478-168">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="00478-169">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="00478-169">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="00478-170">ItemChange</span><span class="sxs-lookup"><span data-stu-id="00478-170">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="00478-171">ItemId</span><span class="sxs-lookup"><span data-stu-id="00478-171">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="00478-172">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="00478-172">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="00478-173">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="00478-173">AppendToItemField</span></span>](appendtoitemfield.md)
    
- [<span data-ttu-id="00478-174">FieldURI</span><span class="sxs-lookup"><span data-stu-id="00478-174">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="00478-175">Message</span><span class="sxs-lookup"><span data-stu-id="00478-175">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="00478-176">Body</span><span class="sxs-lookup"><span data-stu-id="00478-176">Body</span></span>](body.md)
    
## <a name="deleteitemfield-request-example"></a><span data-ttu-id="00478-177">Ejemplo de solicitud de DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="00478-177">DeleteItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="00478-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="00478-178">Description</span></span>

<span data-ttu-id="00478-179">El siguiente ejemplo de una solicitud de **UpdateItem** muestra cómo eliminar una propiedad en un elemento.</span><span class="sxs-lookup"><span data-stu-id="00478-179">The following example of an **UpdateItem** request shows how to delete a property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="00478-180">Código</span><span class="sxs-lookup"><span data-stu-id="00478-180">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbWluaXN0cm..." ChangeKey="CQAAABYAA..."/>
          <t:Updates>
            <t:DeleteItemField>
              <t:FieldURI FieldURI="item:Body"/>
            </t:DeleteItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="00478-181">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00478-181">Comments</span></span>

<span data-ttu-id="00478-182">El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="00478-182">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="deleteitemfield-request-elements"></a><span data-ttu-id="00478-183">Elementos de solicitud de DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="00478-183">DeleteItemField Request Elements</span></span>

<span data-ttu-id="00478-184">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="00478-184">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="00478-185">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="00478-185">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="00478-186">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="00478-186">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="00478-187">ItemChange</span><span class="sxs-lookup"><span data-stu-id="00478-187">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="00478-188">ItemId</span><span class="sxs-lookup"><span data-stu-id="00478-188">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="00478-189">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="00478-189">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="00478-190">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="00478-190">DeleteItemField</span></span>](deleteitemfield.md)
    
- [<span data-ttu-id="00478-191">FieldURI</span><span class="sxs-lookup"><span data-stu-id="00478-191">FieldURI</span></span>](fielduri.md)
    
## <a name="successful-response-example"></a><span data-ttu-id="00478-192">Ejemplo de la respuesta es correcta</span><span class="sxs-lookup"><span data-stu-id="00478-192">Successful response example</span></span>

### <a name="description"></a><span data-ttu-id="00478-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="00478-193">Description</span></span>

<span data-ttu-id="00478-194">En el ejemplo siguiente se muestra una respuesta a una solicitud de **UpdateItem** correcta.</span><span class="sxs-lookup"><span data-stu-id="00478-194">The following example shows a successful response to an **UpdateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="00478-195">Código</span><span class="sxs-lookup"><span data-stu-id="00478-195">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYAAA..."/>
            </t:Message>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="00478-196">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00478-196">Comments</span></span>

<span data-ttu-id="00478-197">El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="00478-197">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="00478-198">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="00478-198">Successful response elements</span></span>

<span data-ttu-id="00478-199">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="00478-199">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="00478-200">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="00478-200">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="00478-201">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="00478-201">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="00478-202">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="00478-202">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="00478-203">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="00478-203">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="00478-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="00478-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="00478-205">Items</span><span class="sxs-lookup"><span data-stu-id="00478-205">Items</span></span>](items.md)
    
- [<span data-ttu-id="00478-206">Message</span><span class="sxs-lookup"><span data-stu-id="00478-206">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="00478-207">ItemId</span><span class="sxs-lookup"><span data-stu-id="00478-207">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="00478-208">Ver también</span><span class="sxs-lookup"><span data-stu-id="00478-208">See also</span></span>



[<span data-ttu-id="00478-209">Operación UpdateItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="00478-209">UpdateItem operation (task)</span></span>](updateitem-operation-task.md)
  
[<span data-ttu-id="00478-210">Operación UpdateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="00478-210">UpdateItem operation (contact)</span></span>](updateitem-operation-contact.md)


- [<span data-ttu-id="00478-211">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="00478-211">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="00478-212">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="00478-212">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="00478-213">Actualización de tareas</span><span class="sxs-lookup"><span data-stu-id="00478-213">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)


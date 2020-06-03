---
title: Elementos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 0811a73e-bf1f-4889-9219-73902dd47639
description: El elemento items contiene una matriz de elementos.
ms.openlocfilehash: 489e34ad0e4bcc2520febb3c213db970fa496051
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458134"
---
# <a name="items"></a><span data-ttu-id="59656-103">Elementos</span><span class="sxs-lookup"><span data-stu-id="59656-103">Items</span></span>

<span data-ttu-id="59656-104">El elemento **Items** contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="59656-104">The **Items** element contains an array of items.</span></span> 
  
```xml
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <PostItem/>
</Items>
```

 <span data-ttu-id="59656-105">**ArrayOfRealItemsType**</span><span class="sxs-lookup"><span data-stu-id="59656-105">**ArrayOfRealItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59656-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="59656-106">Attributes and elements</span></span>

<span data-ttu-id="59656-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="59656-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59656-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="59656-108">Attributes</span></span>

<span data-ttu-id="59656-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="59656-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59656-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="59656-110">Child elements</span></span>

|<span data-ttu-id="59656-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59656-111">**Element**</span></span>|<span data-ttu-id="59656-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59656-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59656-113">Item</span><span class="sxs-lookup"><span data-stu-id="59656-113">Item</span></span>](item.md) <br/> |<span data-ttu-id="59656-114">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-114">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="59656-115">Message</span><span class="sxs-lookup"><span data-stu-id="59656-115">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="59656-116">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-116">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="59656-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="59656-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="59656-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="59656-119">Contacto</span><span class="sxs-lookup"><span data-stu-id="59656-119">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="59656-120">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-120">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="59656-121">DistributionList</span><span class="sxs-lookup"><span data-stu-id="59656-121">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="59656-122">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="59656-122">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="59656-123">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="59656-123">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="59656-124">Representa un mensaje de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-124">Represents a meeting message in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="59656-125">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="59656-125">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="59656-126">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-126">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="59656-127">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="59656-127">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="59656-128">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-128">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="59656-129">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="59656-129">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="59656-130">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-130">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="59656-131">Tarea</span><span class="sxs-lookup"><span data-stu-id="59656-131">Task</span></span>](task.md) <br/> |<span data-ttu-id="59656-132">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-132">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="59656-133">PostItem</span><span class="sxs-lookup"><span data-stu-id="59656-133">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="59656-134">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59656-134">Represents a post item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59656-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="59656-135">Parent elements</span></span>

|<span data-ttu-id="59656-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59656-136">**Element**</span></span>|<span data-ttu-id="59656-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59656-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59656-138">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59656-138">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md) <br/> |<span data-ttu-id="59656-139">Contiene el estado y el resultado de una solicitud de [operación CopyItem](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="59656-139">Contains the status and result of a [CopyItem operation](copyitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="59656-140">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59656-140">CreateItemResponseMessage</span></span>](createitemresponsemessage.md) <br/> |<span data-ttu-id="59656-141">Contiene el estado y el resultado de una única solicitud de [operación CreateItem](createitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="59656-141">Contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="59656-142">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59656-142">GetItemResponseMessage</span></span>](getitemresponsemessage.md) <br/> |<span data-ttu-id="59656-143">Contiene el estado y el resultado de una solicitud de [operación GetItem](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="59656-143">Contains the status and result of a [GetItem operation](getitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="59656-144">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="59656-144">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="59656-145">Representa una colección de elementos que son el resultado de una llamada de [operación FindItem](finditem-operation.md) agrupada.</span><span class="sxs-lookup"><span data-stu-id="59656-145">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="59656-146">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59656-146">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md) <br/> |<span data-ttu-id="59656-147">Contiene el estado y el resultado de una solicitud de [operación MoveItem](moveitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="59656-147">Contains the status and result of a [MoveItem operation](moveitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="59656-148">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="59656-148">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="59656-149">Contiene los resultados de una búsqueda de una carpeta raíz única durante una [operación FindItem](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="59656-149">Contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="59656-150">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59656-150">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="59656-151">Contiene el estado y el resultado de una solicitud de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="59656-151">Contains the status and result of an [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59656-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59656-152">Remarks</span></span>

<span data-ttu-id="59656-153">Para obtener información sobre el conjunto de elementos de una solicitud de [operación CreateItem](createitem-operation.md) , vea [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).</span><span class="sxs-lookup"><span data-stu-id="59656-153">For information about the set of items in a [CreateItem operation](createitem-operation.md) request, see [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).</span></span>
  
<span data-ttu-id="59656-154">Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no son fuertemente tipados por el esquema de servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="59656-154">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="59656-155">Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="59656-155">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="59656-156">Las versiones de Exchange que comienzan con Exchange Server 2010 no devuelven el elemento de [elemento](item.md) base en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="59656-156">Versions of Exchange starting with Exchange Server 2010 do not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="59656-157">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange y que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="59656-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59656-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="59656-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59656-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="59656-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="59656-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="59656-160">Schema Name</span></span>  <br/> |<span data-ttu-id="59656-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="59656-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="59656-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="59656-162">Validation File</span></span>  <br/> |<span data-ttu-id="59656-163">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="59656-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="59656-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="59656-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="59656-165">Falso</span><span class="sxs-lookup"><span data-stu-id="59656-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59656-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="59656-166">See also</span></span>



[<span data-ttu-id="59656-167">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="59656-167">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="59656-168">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="59656-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


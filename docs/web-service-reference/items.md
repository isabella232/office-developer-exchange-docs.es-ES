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
description: El elemento de elementos contiene una matriz de elementos.
ms.openlocfilehash: 241a56ee23e87d6a4320b93cc65b1f5aa1f60120
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836163"
---
# <a name="items"></a><span data-ttu-id="d5cf2-103">Elementos</span><span class="sxs-lookup"><span data-stu-id="d5cf2-103">Items</span></span>

<span data-ttu-id="d5cf2-104">El elemento de **elementos** contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-104">The **Items** element contains an array of items.</span></span> 
  
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

 <span data-ttu-id="d5cf2-105">**ArrayOfRealItemsType**</span><span class="sxs-lookup"><span data-stu-id="d5cf2-105">**ArrayOfRealItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5cf2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d5cf2-106">Attributes and elements</span></span>

<span data-ttu-id="d5cf2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5cf2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5cf2-108">Attributes</span></span>

<span data-ttu-id="d5cf2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5cf2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5cf2-110">Child elements</span></span>

|<span data-ttu-id="d5cf2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5cf2-111">**Element**</span></span>|<span data-ttu-id="d5cf2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5cf2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5cf2-113">Item</span><span class="sxs-lookup"><span data-stu-id="d5cf2-113">Item</span></span>](item.md) <br/> |<span data-ttu-id="d5cf2-114">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-114">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-115">Message</span><span class="sxs-lookup"><span data-stu-id="d5cf2-115">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d5cf2-116">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-116">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d5cf2-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d5cf2-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-119">Contact</span><span class="sxs-lookup"><span data-stu-id="d5cf2-119">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="d5cf2-120">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-120">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-121">DistributionList</span><span class="sxs-lookup"><span data-stu-id="d5cf2-121">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="d5cf2-122">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-122">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-123">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="d5cf2-123">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="d5cf2-124">Representa un mensaje de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-124">Represents a meeting message in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-125">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d5cf2-125">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d5cf2-126">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-126">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-127">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d5cf2-127">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="d5cf2-128">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-128">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-129">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="d5cf2-129">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="d5cf2-130">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-130">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-131">Tarea</span><span class="sxs-lookup"><span data-stu-id="d5cf2-131">Task</span></span>](task.md) <br/> |<span data-ttu-id="d5cf2-132">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-132">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-133">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="d5cf2-133">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="d5cf2-134">Representa un elemento para exponer en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-134">Represents a post item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5cf2-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d5cf2-135">Parent elements</span></span>

|<span data-ttu-id="d5cf2-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5cf2-136">**Element**</span></span>|<span data-ttu-id="d5cf2-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5cf2-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5cf2-138">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d5cf2-138">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md) <br/> |<span data-ttu-id="d5cf2-139">Contiene el estado y el resultado de una solicitud de [operación CopyItem](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d5cf2-139">Contains the status and result of a [CopyItem operation](copyitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-140">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d5cf2-140">CreateItemResponseMessage</span></span>](createitemresponsemessage.md) <br/> |<span data-ttu-id="d5cf2-141">Contiene el estado y el resultado de una única solicitud [CreateItem operation](createitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d5cf2-141">Contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-142">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d5cf2-142">GetItemResponseMessage</span></span>](getitemresponsemessage.md) <br/> |<span data-ttu-id="d5cf2-143">Contiene el estado y el resultado de una solicitud de [GetItem operation](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d5cf2-143">Contains the status and result of a [GetItem operation](getitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-144">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="d5cf2-144">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="d5cf2-145">Representa una colección de elementos que son el resultado de una [operación FindItem](finditem-operation.md) de agrupada de llamadas.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-145">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-146">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d5cf2-146">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md) <br/> |<span data-ttu-id="d5cf2-147">Contiene el estado y el resultado de una solicitud de [operación MoveItem](moveitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d5cf2-147">Contains the status and result of a [MoveItem operation](moveitem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-148">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="d5cf2-148">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="d5cf2-149">Contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación de FindItem](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d5cf2-149">Contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d5cf2-150">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d5cf2-150">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="d5cf2-151">Contiene el estado y el resultado de una solicitud de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d5cf2-151">Contains the status and result of an [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5cf2-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5cf2-152">Remarks</span></span>

<span data-ttu-id="d5cf2-153">Para obtener información sobre el conjunto de elementos en una solicitud de [operación CreateItem](createitem-operation.md) , vea [elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).</span><span class="sxs-lookup"><span data-stu-id="d5cf2-153">For information about the set of items in a [CreateItem operation](createitem-operation.md) request, see [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).</span></span>
  
<span data-ttu-id="d5cf2-154">Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de Exchange Web Services (EWS).</span><span class="sxs-lookup"><span data-stu-id="d5cf2-154">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="d5cf2-155">Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="d5cf2-155">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="d5cf2-156">Las versiones de Exchange a partir de Exchange Server 2010 no devuelven el elemento base del [elemento](item.md) en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-156">Versions of Exchange starting with Exchange Server 2010 do not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="d5cf2-157">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d5cf2-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5cf2-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d5cf2-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5cf2-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5cf2-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5cf2-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d5cf2-160">Schema Name</span></span>  <br/> |<span data-ttu-id="d5cf2-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d5cf2-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5cf2-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d5cf2-162">Validation File</span></span>  <br/> |<span data-ttu-id="d5cf2-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5cf2-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5cf2-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d5cf2-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5cf2-165">False</span><span class="sxs-lookup"><span data-stu-id="d5cf2-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5cf2-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5cf2-166">See also</span></span>



[<span data-ttu-id="d5cf2-167">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="d5cf2-167">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="d5cf2-168">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d5cf2-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


---
title: Categorías
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Categories
api_type:
- schema
ms.assetid: d84d4927-b524-4e62-bf3d-1f12fec8c21a
description: El elemento Categories contiene una colección de cadenas que identifican las categorías a las que pertenece un elemento del buzón.
ms.openlocfilehash: 0d9f7068aa81306a10436ed0ca0d45f6d3b2c3a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462216"
---
# <a name="categories"></a><span data-ttu-id="ec2ed-103">Categorías</span><span class="sxs-lookup"><span data-stu-id="ec2ed-103">Categories</span></span>

<span data-ttu-id="ec2ed-104">El elemento **Categories** contiene una colección de cadenas que identifican las categorías a las que pertenece un elemento del buzón.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-104">The **Categories** element contains a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span> 
  
```XML
<Categories>
   <String/>
</Categories>
```

 <span data-ttu-id="ec2ed-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="ec2ed-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec2ed-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ec2ed-106">Attributes and elements</span></span>

<span data-ttu-id="ec2ed-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec2ed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ec2ed-108">Attributes</span></span>

<span data-ttu-id="ec2ed-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec2ed-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ec2ed-110">Child elements</span></span>

|<span data-ttu-id="ec2ed-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ec2ed-111">**Element**</span></span>|<span data-ttu-id="ec2ed-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec2ed-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec2ed-113">String</span><span class="sxs-lookup"><span data-stu-id="ec2ed-113">String</span></span>](string.md) <br/> |<span data-ttu-id="ec2ed-114">Contiene una cadena que identifica una única categoría.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-114">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec2ed-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ec2ed-115">Parent elements</span></span>

|<span data-ttu-id="ec2ed-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ec2ed-116">**Element**</span></span>|<span data-ttu-id="ec2ed-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec2ed-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec2ed-118">Item</span><span class="sxs-lookup"><span data-stu-id="ec2ed-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="ec2ed-119">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-119">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="ec2ed-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="ec2ed-121">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-122">Message</span><span class="sxs-lookup"><span data-stu-id="ec2ed-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ec2ed-123">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-124">Tarea</span><span class="sxs-lookup"><span data-stu-id="ec2ed-124">Task</span></span>](task.md) <br/> |<span data-ttu-id="ec2ed-125">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-125">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ec2ed-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ec2ed-127">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-128">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-128">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ec2ed-129">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-129">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-130">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ec2ed-130">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ec2ed-131">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-131">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-132">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ec2ed-132">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ec2ed-133">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-133">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-134">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ec2ed-134">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ec2ed-135">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-135">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ec2ed-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ec2ed-137">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-138">Contacto</span><span class="sxs-lookup"><span data-stu-id="ec2ed-138">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="ec2ed-139">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-139">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-140">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ec2ed-140">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="ec2ed-141">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-141">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-142">Condiciones</span><span class="sxs-lookup"><span data-stu-id="ec2ed-142">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="ec2ed-143">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-143">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-144">Excepciones</span><span class="sxs-lookup"><span data-stu-id="ec2ed-144">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="ec2ed-145">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-145">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="ec2ed-146">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="ec2ed-146">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="ec2ed-147">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-147">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec2ed-148">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ec2ed-148">Text value</span></span>

<span data-ttu-id="ec2ed-149">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec2ed-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec2ed-150">Remarks</span></span>

<span data-ttu-id="ec2ed-151">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec2ed-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ec2ed-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec2ed-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec2ed-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec2ed-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ec2ed-154">Schema Name</span></span>  <br/> |<span data-ttu-id="ec2ed-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ec2ed-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec2ed-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ec2ed-156">Validation File</span></span>  <br/> |<span data-ttu-id="ec2ed-157">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ec2ed-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec2ed-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ec2ed-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec2ed-159">Falso</span><span class="sxs-lookup"><span data-stu-id="ec2ed-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec2ed-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec2ed-160">See also</span></span>



- [<span data-ttu-id="ec2ed-161">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ec2ed-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


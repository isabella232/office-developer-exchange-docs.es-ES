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
description: El elemento de categorías contiene una colección de cadenas que identifican las categorías a la que pertenece un elemento en el buzón de correo.
ms.openlocfilehash: 8f112a9a736ff4f242b9dfb084b3ad7541cc493d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763731"
---
# <a name="categories"></a><span data-ttu-id="5cb0a-103">Categorías</span><span class="sxs-lookup"><span data-stu-id="5cb0a-103">Categories</span></span>

<span data-ttu-id="5cb0a-104">El elemento de **categorías** contiene una colección de cadenas que identifican las categorías a la que pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-104">The **Categories** element contains a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span> 
  
```XML
<Categories>
   <String/>
</Categories>
```

 <span data-ttu-id="5cb0a-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="5cb0a-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5cb0a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5cb0a-106">Attributes and elements</span></span>

<span data-ttu-id="5cb0a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cb0a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5cb0a-108">Attributes</span></span>

<span data-ttu-id="5cb0a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5cb0a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5cb0a-110">Child elements</span></span>

|<span data-ttu-id="5cb0a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cb0a-111">**Element**</span></span>|<span data-ttu-id="5cb0a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5cb0a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cb0a-113">String</span><span class="sxs-lookup"><span data-stu-id="5cb0a-113">String</span></span>](string.md) <br/> |<span data-ttu-id="5cb0a-114">Contiene una cadena que identifica una única categoría.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-114">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5cb0a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5cb0a-115">Parent elements</span></span>

|<span data-ttu-id="5cb0a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cb0a-116">**Element**</span></span>|<span data-ttu-id="5cb0a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5cb0a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cb0a-118">Item</span><span class="sxs-lookup"><span data-stu-id="5cb0a-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="5cb0a-119">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-119">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="5cb0a-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="5cb0a-121">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-122">Message</span><span class="sxs-lookup"><span data-stu-id="5cb0a-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5cb0a-123">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-124">Tarea</span><span class="sxs-lookup"><span data-stu-id="5cb0a-124">Task</span></span>](task.md) <br/> |<span data-ttu-id="5cb0a-125">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-125">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5cb0a-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5cb0a-127">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-128">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="5cb0a-128">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="5cb0a-129">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-129">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-130">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5cb0a-130">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="5cb0a-131">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-131">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-132">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5cb0a-132">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5cb0a-133">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-133">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-134">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="5cb0a-134">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="5cb0a-135">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-135">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="5cb0a-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="5cb0a-137">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-138">Contact</span><span class="sxs-lookup"><span data-stu-id="5cb0a-138">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5cb0a-139">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-139">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-140">DistributionList</span><span class="sxs-lookup"><span data-stu-id="5cb0a-140">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="5cb0a-141">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-141">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-142">Condiciones</span><span class="sxs-lookup"><span data-stu-id="5cb0a-142">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="5cb0a-143">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-143">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-144">Excepciones</span><span class="sxs-lookup"><span data-stu-id="5cb0a-144">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="5cb0a-145">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-145">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="5cb0a-146">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="5cb0a-146">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="5cb0a-147">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-147">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5cb0a-148">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5cb0a-148">Text value</span></span>

<span data-ttu-id="5cb0a-149">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5cb0a-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cb0a-150">Remarks</span></span>

<span data-ttu-id="5cb0a-151">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cb0a-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5cb0a-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cb0a-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5cb0a-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5cb0a-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5cb0a-154">Schema Name</span></span>  <br/> |<span data-ttu-id="5cb0a-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5cb0a-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="5cb0a-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5cb0a-156">Validation File</span></span>  <br/> |<span data-ttu-id="5cb0a-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5cb0a-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5cb0a-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5cb0a-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="5cb0a-159">False</span><span class="sxs-lookup"><span data-stu-id="5cb0a-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5cb0a-160">Ver también</span><span class="sxs-lookup"><span data-stu-id="5cb0a-160">See also</span></span>



- [<span data-ttu-id="5cb0a-161">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5cb0a-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


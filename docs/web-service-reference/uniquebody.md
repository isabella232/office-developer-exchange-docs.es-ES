---
title: UniqueBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueBody
api_type:
- schema
ms.assetid: 06bc95d7-121c-433b-bd27-c2b0eb8c011f
description: El elemento UniqueBody representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.
ms.openlocfilehash: 49d3607926e0b985074d79cde76cad084f537f01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840765"
---
# <a name="uniquebody"></a><span data-ttu-id="c8967-103">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="c8967-103">UniqueBody</span></span>

<span data-ttu-id="c8967-104">El elemento **UniqueBody** representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="c8967-104">The **UniqueBody** element represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span> 
  
```XML
<UniqueBody BodyType=""/>
```

 <span data-ttu-id="c8967-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="c8967-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8967-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8967-106">Attributes and elements</span></span>

<span data-ttu-id="c8967-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8967-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8967-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8967-108">Attributes</span></span>

|<span data-ttu-id="c8967-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c8967-109">**Attribute**</span></span>|<span data-ttu-id="c8967-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8967-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8967-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="c8967-111">**BodyType**</span></span> <br/> |<span data-ttu-id="c8967-112">Describe cómo se almacena el cuerpo del elemento en el elemento.</span><span class="sxs-lookup"><span data-stu-id="c8967-112">Describes how the item body is stored in the item.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="c8967-113">Atributo BodyType</span><span class="sxs-lookup"><span data-stu-id="c8967-113">BodyType Attribute</span></span>

|<span data-ttu-id="c8967-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c8967-114">**Value**</span></span>|<span data-ttu-id="c8967-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8967-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8967-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="c8967-116">**HTML**</span></span> <br/> |<span data-ttu-id="c8967-117">Convierte todos los cuerpos en HTML.</span><span class="sxs-lookup"><span data-stu-id="c8967-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="c8967-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="c8967-118">**Text**</span></span> <br/> |<span data-ttu-id="c8967-119">Todos los cuerpos se convierte en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="c8967-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c8967-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8967-120">Child elements</span></span>

<span data-ttu-id="c8967-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8967-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8967-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8967-122">Parent elements</span></span>

|<span data-ttu-id="c8967-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8967-123">**Element**</span></span>|<span data-ttu-id="c8967-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8967-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8967-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c8967-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c8967-126">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c8967-127">Contact</span><span class="sxs-lookup"><span data-stu-id="c8967-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c8967-128">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-128">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="c8967-129">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c8967-129">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c8967-130">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="c8967-130">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="c8967-131">Item</span><span class="sxs-lookup"><span data-stu-id="c8967-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="c8967-132">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-132">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8967-133">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="c8967-133">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="c8967-134">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-134">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8967-135">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="c8967-135">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="c8967-136">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-136">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8967-137">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c8967-137">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c8967-138">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-138">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8967-139">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="c8967-139">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="c8967-140">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-140">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8967-141">Message</span><span class="sxs-lookup"><span data-stu-id="c8967-141">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c8967-142">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-142">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c8967-143">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="c8967-143">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="c8967-144">Representa un elemento para exponer en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-144">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8967-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="c8967-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="c8967-146">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-146">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c8967-147">Tarea</span><span class="sxs-lookup"><span data-stu-id="c8967-147">Task</span></span>](task.md) <br/> |<span data-ttu-id="c8967-148">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-148">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8967-149">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c8967-149">Text value</span></span>

<span data-ttu-id="c8967-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8967-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8967-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8967-151">Remarks</span></span>

<span data-ttu-id="c8967-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8967-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8967-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8967-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8967-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8967-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8967-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8967-155">Schema Name</span></span>  <br/> |<span data-ttu-id="c8967-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c8967-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8967-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8967-157">Validation File</span></span>  <br/> |<span data-ttu-id="c8967-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8967-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8967-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8967-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8967-160">False</span><span class="sxs-lookup"><span data-stu-id="c8967-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8967-161">Ver también</span><span class="sxs-lookup"><span data-stu-id="c8967-161">See also</span></span>



- [<span data-ttu-id="c8967-162">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c8967-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


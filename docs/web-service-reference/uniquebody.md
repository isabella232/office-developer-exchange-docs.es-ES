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
description: El elemento UniqueBody representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.
ms.openlocfilehash: 0a8d52c7d4eb8bda9fd41c4c25e448523185df93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461922"
---
# <a name="uniquebody"></a><span data-ttu-id="6adbd-103">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="6adbd-103">UniqueBody</span></span>

<span data-ttu-id="6adbd-104">El elemento **UniqueBody** representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="6adbd-104">The **UniqueBody** element represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span> 
  
```XML
<UniqueBody BodyType=""/>
```

 <span data-ttu-id="6adbd-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="6adbd-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6adbd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6adbd-106">Attributes and elements</span></span>

<span data-ttu-id="6adbd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6adbd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6adbd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6adbd-108">Attributes</span></span>

|<span data-ttu-id="6adbd-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6adbd-109">**Attribute**</span></span>|<span data-ttu-id="6adbd-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6adbd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6adbd-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="6adbd-111">**BodyType**</span></span> <br/> |<span data-ttu-id="6adbd-112">Describe cómo se almacena el cuerpo del elemento en el elemento.</span><span class="sxs-lookup"><span data-stu-id="6adbd-112">Describes how the item body is stored in the item.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="6adbd-113">Atributo BodyType</span><span class="sxs-lookup"><span data-stu-id="6adbd-113">BodyType Attribute</span></span>

|<span data-ttu-id="6adbd-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6adbd-114">**Value**</span></span>|<span data-ttu-id="6adbd-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6adbd-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6adbd-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="6adbd-116">**HTML**</span></span> <br/> |<span data-ttu-id="6adbd-117">Convierte todos los cuerpos en HTML.</span><span class="sxs-lookup"><span data-stu-id="6adbd-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="6adbd-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="6adbd-118">**Text**</span></span> <br/> |<span data-ttu-id="6adbd-119">Convierte todos los cuerpos en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="6adbd-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6adbd-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6adbd-120">Child elements</span></span>

<span data-ttu-id="6adbd-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6adbd-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6adbd-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6adbd-122">Parent elements</span></span>

|<span data-ttu-id="6adbd-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6adbd-123">**Element**</span></span>|<span data-ttu-id="6adbd-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6adbd-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6adbd-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="6adbd-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="6adbd-126">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-127">Contacto</span><span class="sxs-lookup"><span data-stu-id="6adbd-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6adbd-128">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-128">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-129">DistributionList</span><span class="sxs-lookup"><span data-stu-id="6adbd-129">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="6adbd-130">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="6adbd-130">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-131">Elemento</span><span class="sxs-lookup"><span data-stu-id="6adbd-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="6adbd-132">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-132">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-133">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="6adbd-133">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="6adbd-134">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-134">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-135">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="6adbd-135">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="6adbd-136">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-136">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-137">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="6adbd-137">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="6adbd-138">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-138">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-139">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="6adbd-139">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="6adbd-140">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-140">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-141">Mensaje</span><span class="sxs-lookup"><span data-stu-id="6adbd-141">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6adbd-142">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-142">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-143">PostItem</span><span class="sxs-lookup"><span data-stu-id="6adbd-143">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="6adbd-144">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-144">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="6adbd-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="6adbd-146">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-146">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6adbd-147">Tarea</span><span class="sxs-lookup"><span data-stu-id="6adbd-147">Task</span></span>](task.md) <br/> |<span data-ttu-id="6adbd-148">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-148">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6adbd-149">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6adbd-149">Text value</span></span>

<span data-ttu-id="6adbd-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6adbd-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6adbd-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6adbd-151">Remarks</span></span>

<span data-ttu-id="6adbd-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6adbd-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6adbd-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6adbd-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6adbd-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="6adbd-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6adbd-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6adbd-155">Schema Name</span></span>  <br/> |<span data-ttu-id="6adbd-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6adbd-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="6adbd-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6adbd-157">Validation File</span></span>  <br/> |<span data-ttu-id="6adbd-158">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6adbd-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6adbd-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6adbd-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="6adbd-160">Falso</span><span class="sxs-lookup"><span data-stu-id="6adbd-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6adbd-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="6adbd-161">See also</span></span>



- [<span data-ttu-id="6adbd-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6adbd-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


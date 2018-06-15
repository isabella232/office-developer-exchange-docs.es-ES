---
title: ConversationId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationId
api_type:
- schema
ms.assetid: d5f1ddb3-9af3-4677-a6ba-111b304a951e
description: El elemento ConversationId contiene el identificador de un elemento o conversación.
ms.openlocfilehash: 1f82e6ade60fb70db4a9f026fd72d9f11cc63821
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763872"
---
# <a name="conversationid"></a><span data-ttu-id="3a2f4-103">ConversationId</span><span class="sxs-lookup"><span data-stu-id="3a2f4-103">ConversationId</span></span>

<span data-ttu-id="3a2f4-104">El elemento **ConversationId** contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-104">The **ConversationId** element contains the identifier of an item or conversation.</span></span> 
  
```XML
<ConversationId Id="" ChangeKey="" />
```

 <span data-ttu-id="3a2f4-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="3a2f4-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a2f4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a2f4-106">Attributes and elements</span></span>

<span data-ttu-id="3a2f4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a2f4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a2f4-108">Attributes</span></span>

|<span data-ttu-id="3a2f4-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3a2f4-109">**Attribute**</span></span>|<span data-ttu-id="3a2f4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a2f4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a2f4-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="3a2f4-111">**Id**</span></span> <br/> |<span data-ttu-id="3a2f4-112">Identifica un elemento específico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="3a2f4-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="3a2f4-113">**ChangeKey**</span></span> <br/> | <span data-ttu-id="3a2f4-114">Identifica una versión específica de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-114">Identifies a specific version of an item.</span></span> <span data-ttu-id="3a2f4-115">Un **ChangeKey** es necesario para los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="3a2f4-115">A **ChangeKey** is required for the following scenarios:</span></span>  <br/><br/><span data-ttu-id="3a2f4-116">-El elemento [UpdateItem](updateitem.md) requiere un **ChangeKey** si se establece el atributo **ConflictResolution** para resolver automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-116">- The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve.</span></span> <span data-ttu-id="3a2f4-117">Resolución automática es un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-117">AutoResolve is a default value.</span></span> <span data-ttu-id="3a2f4-118">Si no se incluye el atributo **ChangeKey** , la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorChangeKeyRequired**.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-118">If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.</span></span><br/><br/><span data-ttu-id="3a2f4-119">- Elementos [SendItem](senditem.md), [DeleteItem](deleteitem.md)y [DeleteFolder](deletefolder.md) requieren un **ChangeKey** comprobar si la operación intentada actuará de la versión más reciente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-119">- [SendItem](senditem.md), [DeleteItem](deleteitem.md), and [DeleteFolder](deletefolder.md) elements require a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item.</span></span> <span data-ttu-id="3a2f4-120">Si el atributo **ChangeKey** no está incluido en la **ItemId** o si el **ChangeKey** está vacío, la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorStaleObject**.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-120">If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3a2f4-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a2f4-121">Child elements</span></span>

<span data-ttu-id="3a2f4-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3a2f4-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a2f4-123">Parent elements</span></span>

|<span data-ttu-id="3a2f4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a2f4-124">**Element**</span></span>|<span data-ttu-id="3a2f4-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a2f4-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a2f4-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3a2f4-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3a2f4-127">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-128">Contact</span><span class="sxs-lookup"><span data-stu-id="3a2f4-128">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="3a2f4-129">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-129">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-130">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="3a2f4-130">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="3a2f4-131">Representa una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-131">Represents a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="3a2f4-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="3a2f4-133">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-134">Item</span><span class="sxs-lookup"><span data-stu-id="3a2f4-134">Item</span></span>](item.md) <br/> |<span data-ttu-id="3a2f4-135">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-135">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="3a2f4-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="3a2f4-137">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-138">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="3a2f4-138">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="3a2f4-139">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-139">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-140">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3a2f4-140">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3a2f4-141">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-141">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-142">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="3a2f4-142">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="3a2f4-143">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-143">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-144">Message</span><span class="sxs-lookup"><span data-stu-id="3a2f4-144">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3a2f4-145">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-145">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-146">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="3a2f4-146">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="3a2f4-147">Representa un elemento para exponer en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-147">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-148">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="3a2f4-148">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="3a2f4-149">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-149">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-150">Tarea</span><span class="sxs-lookup"><span data-stu-id="3a2f4-150">Task</span></span>](task.md) <br/> |<span data-ttu-id="3a2f4-151">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-151">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a2f4-152">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="3a2f4-152">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="3a2f4-153">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-153">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a2f4-154">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3a2f4-154">Text value</span></span>

<span data-ttu-id="3a2f4-155">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a2f4-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a2f4-156">Remarks</span></span>

<span data-ttu-id="3a2f4-157">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2f4-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a2f4-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a2f4-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a2f4-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a2f4-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a2f4-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a2f4-160">Schema Name</span></span>  <br/> |<span data-ttu-id="3a2f4-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3a2f4-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a2f4-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a2f4-162">Validation File</span></span>  <br/> |<span data-ttu-id="3a2f4-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a2f4-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a2f4-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a2f4-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a2f4-165">False</span><span class="sxs-lookup"><span data-stu-id="3a2f4-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a2f4-166">Ver también</span><span class="sxs-lookup"><span data-stu-id="3a2f4-166">See also</span></span>

- [<span data-ttu-id="3a2f4-167">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="3a2f4-167">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="3a2f4-168">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3a2f4-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

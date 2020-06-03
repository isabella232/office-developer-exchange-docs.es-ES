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
description: El elemento ConversationId contiene el identificador de un elemento o una conversación.
ms.openlocfilehash: 4f12d70ae6b72773760a731f5778cf6743ce699f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461474"
---
# <a name="conversationid"></a><span data-ttu-id="c5fb1-103">ConversationId</span><span class="sxs-lookup"><span data-stu-id="c5fb1-103">ConversationId</span></span>

<span data-ttu-id="c5fb1-104">El elemento **ConversationId** contiene el identificador de un elemento o una conversación.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-104">The **ConversationId** element contains the identifier of an item or conversation.</span></span> 
  
```XML
<ConversationId Id="" ChangeKey="" />
```

 <span data-ttu-id="c5fb1-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="c5fb1-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5fb1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c5fb1-106">Attributes and elements</span></span>

<span data-ttu-id="c5fb1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5fb1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5fb1-108">Attributes</span></span>

|<span data-ttu-id="c5fb1-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c5fb1-109">**Attribute**</span></span>|<span data-ttu-id="c5fb1-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5fb1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5fb1-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="c5fb1-111">**Id**</span></span> <br/> |<span data-ttu-id="c5fb1-112">Identifica un elemento específico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="c5fb1-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="c5fb1-113">**ChangeKey**</span></span> <br/> | <span data-ttu-id="c5fb1-114">Identifica una versión específica de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-114">Identifies a specific version of an item.</span></span> <span data-ttu-id="c5fb1-115">Se necesita un **changekey** para los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="c5fb1-115">A **ChangeKey** is required for the following scenarios:</span></span>  <br/><br/><span data-ttu-id="c5fb1-116">-El elemento [UpdateItem](updateitem.md) requiere un **changekey** si el atributo **ConflictResolution** está establecido en autoresolve.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-116">- The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve.</span></span> <span data-ttu-id="c5fb1-117">Autoresolve es un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-117">AutoResolve is a default value.</span></span> <span data-ttu-id="c5fb1-118">Si no se incluye el atributo **changekey** , la respuesta devolverá un valor de [ResponseCode](responsecode.md) igual a **ErrorChangeKeyRequired**.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-118">If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.</span></span><br/><br/><span data-ttu-id="c5fb1-119">- Los elementos [SendItem](senditem.md), [DeleteItem](deleteitem.md)y [DeleteFolder](deletefolder.md) requieren un **changekey** para comprobar si la operación que se ha intentado actuar? a en la versión más reciente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-119">- [SendItem](senditem.md), [DeleteItem](deleteitem.md), and [DeleteFolder](deletefolder.md) elements require a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item.</span></span> <span data-ttu-id="c5fb1-120">Si el atributo **changekey** no se incluye en **Itemid** o si **changekey** está vacío, la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorStaleObject**.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-120">If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5fb1-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5fb1-121">Child elements</span></span>

<span data-ttu-id="c5fb1-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5fb1-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c5fb1-123">Parent elements</span></span>

|<span data-ttu-id="c5fb1-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c5fb1-124">**Element**</span></span>|<span data-ttu-id="c5fb1-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5fb1-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5fb1-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c5fb1-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c5fb1-127">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-128">Contacto</span><span class="sxs-lookup"><span data-stu-id="c5fb1-128">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c5fb1-129">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-129">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-130">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="c5fb1-130">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="c5fb1-131">Representa una única acción que se va a aplicar a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-131">Represents a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c5fb1-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c5fb1-133">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="c5fb1-134">Item</span></span>](item.md) <br/> |<span data-ttu-id="c5fb1-135">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-135">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="c5fb1-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="c5fb1-137">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-138">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="c5fb1-138">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="c5fb1-139">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-139">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-140">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c5fb1-140">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c5fb1-141">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-141">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-142">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="c5fb1-142">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="c5fb1-143">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-143">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-144">Message</span><span class="sxs-lookup"><span data-stu-id="c5fb1-144">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c5fb1-145">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-145">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-146">PostItem</span><span class="sxs-lookup"><span data-stu-id="c5fb1-146">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="c5fb1-147">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-147">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-148">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="c5fb1-148">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="c5fb1-149">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-149">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-150">Tarea</span><span class="sxs-lookup"><span data-stu-id="c5fb1-150">Task</span></span>](task.md) <br/> |<span data-ttu-id="c5fb1-151">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-151">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5fb1-152">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c5fb1-152">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c5fb1-153">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-153">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c5fb1-154">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c5fb1-154">Text value</span></span>

<span data-ttu-id="c5fb1-155">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5fb1-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5fb1-156">Remarks</span></span>

<span data-ttu-id="c5fb1-157">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5fb1-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5fb1-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c5fb1-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5fb1-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5fb1-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5fb1-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c5fb1-160">Schema Name</span></span>  <br/> |<span data-ttu-id="c5fb1-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c5fb1-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5fb1-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c5fb1-162">Validation File</span></span>  <br/> |<span data-ttu-id="c5fb1-163">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c5fb1-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5fb1-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c5fb1-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="c5fb1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c5fb1-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5fb1-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5fb1-166">See also</span></span>

- [<span data-ttu-id="c5fb1-167">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="c5fb1-167">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="c5fb1-168">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c5fb1-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


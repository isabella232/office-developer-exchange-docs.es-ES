---
title: InternetMessageHeaders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeaders
api_type:
- schema
ms.assetid: 4dcf8671-96df-4a2d-9836-7e8e3a67e0db
description: El elemento InternetMessageHeaders contiene una colección de algunos encabezados de mensajes de Internet incluidos en un elemento de un buzón. Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad PR_TRANSPORT_MESSAGE_HEADERS. Para obtener más información sobre los encabezados de mensajes de EWS e Internet, Consulteobtener Internet Message headersin EWS, MIME y los encabezados de mensajes de Internet que faltan.
ms.openlocfilehash: 4719050c02590e021b29173c234466de3fdc58a4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467329"
---
# <a name="internetmessageheaders"></a><span data-ttu-id="5dc38-105">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="5dc38-105">InternetMessageHeaders</span></span>

<span data-ttu-id="5dc38-106">El elemento **InternetMessageHeaders** contiene una colección de algunos encabezados de mensajes de Internet incluidos en un elemento de un buzón.</span><span class="sxs-lookup"><span data-stu-id="5dc38-106">The **InternetMessageHeaders** element contains a collection of some of the Internet message headers that are contained in an item in a mailbox.</span></span> <span data-ttu-id="5dc38-107">Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="5dc38-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="5dc38-108">Para obtener más información acerca de los encabezados de mensajes de Internet y EWS, vea "obtener encabezados de mensajes de Internet" en [EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5dc38-108">For more information about EWS and Internet message headers, see "Getting Internet message headers" in [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 <span data-ttu-id="5dc38-109">**NonEmptyArrayOfInternetHeadersType**</span><span class="sxs-lookup"><span data-stu-id="5dc38-109">**NonEmptyArrayOfInternetHeadersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5dc38-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5dc38-110">Attributes and elements</span></span>

<span data-ttu-id="5dc38-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5dc38-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5dc38-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5dc38-112">Attributes</span></span>

<span data-ttu-id="5dc38-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5dc38-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5dc38-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5dc38-114">Child elements</span></span>

|<span data-ttu-id="5dc38-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5dc38-115">**Element**</span></span>|<span data-ttu-id="5dc38-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5dc38-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5dc38-117">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="5dc38-117">InternetMessageHeader</span></span>](internetmessageheader.md) <br/> |<span data-ttu-id="5dc38-118">Representa el encabezado de un mensaje de Internet para un encabezado determinado dentro de la colección de encabezados.</span><span class="sxs-lookup"><span data-stu-id="5dc38-118">Represents the Internet message header for a given header within the headers collection.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5dc38-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5dc38-119">Parent elements</span></span>

|<span data-ttu-id="5dc38-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5dc38-120">**Element**</span></span>|<span data-ttu-id="5dc38-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5dc38-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5dc38-122">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="5dc38-122">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="5dc38-123">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="5dc38-123">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5dc38-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5dc38-125">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-126">Contacto</span><span class="sxs-lookup"><span data-stu-id="5dc38-126">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5dc38-127">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-127">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-128">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="5dc38-128">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="5dc38-129">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="5dc38-129">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-130">DistributionList</span><span class="sxs-lookup"><span data-stu-id="5dc38-130">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="5dc38-131">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="5dc38-131">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="5dc38-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="5dc38-133">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-133">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="5dc38-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="5dc38-135">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-135">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-136">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5dc38-136">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="5dc38-137">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-137">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5dc38-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5dc38-139">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-140">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="5dc38-140">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="5dc38-141">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-141">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-142">Message</span><span class="sxs-lookup"><span data-stu-id="5dc38-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5dc38-143">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-144">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="5dc38-144">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="5dc38-145">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-145">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-146">Tarea</span><span class="sxs-lookup"><span data-stu-id="5dc38-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="5dc38-147">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-147">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5dc38-148">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="5dc38-148">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="5dc38-149">Representa una respuesta aceptada provisionalmente a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="5dc38-149">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dc38-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5dc38-150">Remarks</span></span>

<span data-ttu-id="5dc38-151">La siguiente es la definición de propiedad extendida de la API administrada de EWS para la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="5dc38-151">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="5dc38-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5dc38-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5dc38-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5dc38-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dc38-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="5dc38-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5dc38-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5dc38-155">Schema Name</span></span>  <br/> |<span data-ttu-id="5dc38-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5dc38-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="5dc38-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5dc38-157">Validation File</span></span>  <br/> |<span data-ttu-id="5dc38-158">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5dc38-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5dc38-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5dc38-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="5dc38-160">Falso</span><span class="sxs-lookup"><span data-stu-id="5dc38-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5dc38-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dc38-161">See also</span></span>



- [<span data-ttu-id="5dc38-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5dc38-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5dc38-163">EWS, MIME y los encabezados de mensajes de Internet que faltan</span><span class="sxs-lookup"><span data-stu-id="5dc38-163">EWS, MIME, and the missing Internet message headers</span></span>](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)


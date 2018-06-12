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
description: El elemento InternetMessageHeaders contiene una colección de algunos de los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo. Para obtener la colección completa de los encabezados de mensaje de Internet, utilice la propiedad PR_TRANSPORT_MESSAGE_HEADERS. Para obtener más información acerca de EWS y encabezados de mensajes de Internet, headersin de mensaje de Internet seeGetting EWS, MIME y los encabezados de mensaje de Internet que faltan.
ms.openlocfilehash: 2da529a8a3532cebb2791b285b7673c962a2a656
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835954"
---
# <a name="internetmessageheaders"></a><span data-ttu-id="61907-105">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="61907-105">InternetMessageHeaders</span></span>

<span data-ttu-id="61907-106">El elemento **InternetMessageHeaders** contiene una colección de algunos de los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="61907-106">The **InternetMessageHeaders** element contains a collection of some of the Internet message headers that are contained in an item in a mailbox.</span></span> <span data-ttu-id="61907-107">Para obtener la colección completa de los encabezados de mensaje de Internet, utilice la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="61907-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="61907-108">Para obtener más información acerca de los encabezados de mensaje EWS y en Internet, vea "Encabezados de mensaje de Internet de introducción" en [EWS, MIME y los encabezados de mensaje de Internet que faltan](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="61907-108">For more information about EWS and Internet message headers, see "Getting Internet message headers" in [EWS, MIME, and the missing Internet message headers](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 <span data-ttu-id="61907-109">**NonEmptyArrayOfInternetHeadersType**</span><span class="sxs-lookup"><span data-stu-id="61907-109">**NonEmptyArrayOfInternetHeadersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61907-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="61907-110">Attributes and elements</span></span>

<span data-ttu-id="61907-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="61907-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61907-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="61907-112">Attributes</span></span>

<span data-ttu-id="61907-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="61907-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61907-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61907-114">Child elements</span></span>

|<span data-ttu-id="61907-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="61907-115">**Element**</span></span>|<span data-ttu-id="61907-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61907-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61907-117">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="61907-117">InternetMessageHeader</span></span>](internetmessageheader.md) <br/> |<span data-ttu-id="61907-118">Representa el encabezado del mensaje de Internet para un determinado encabezado dentro de la colección de encabezados.</span><span class="sxs-lookup"><span data-stu-id="61907-118">Represents the Internet message header for a given header within the headers collection.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61907-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="61907-119">Parent elements</span></span>

|<span data-ttu-id="61907-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="61907-120">**Element**</span></span>|<span data-ttu-id="61907-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61907-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61907-122">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="61907-122">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="61907-123">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="61907-123">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="61907-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="61907-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="61907-125">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="61907-126">Contact</span><span class="sxs-lookup"><span data-stu-id="61907-126">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="61907-127">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-127">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="61907-128">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="61907-128">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="61907-129">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="61907-129">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="61907-130">DistributionList</span><span class="sxs-lookup"><span data-stu-id="61907-130">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="61907-131">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="61907-131">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="61907-132">Item</span><span class="sxs-lookup"><span data-stu-id="61907-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="61907-133">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-133">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="61907-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="61907-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="61907-135">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-135">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="61907-136">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="61907-136">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="61907-137">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-137">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="61907-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="61907-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="61907-139">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="61907-140">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="61907-140">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="61907-141">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-141">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="61907-142">Message</span><span class="sxs-lookup"><span data-stu-id="61907-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="61907-143">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="61907-144">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="61907-144">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="61907-145">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-145">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="61907-146">Tarea</span><span class="sxs-lookup"><span data-stu-id="61907-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="61907-147">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-147">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="61907-148">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="61907-148">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="61907-149">Representa una respuesta a una convocatoria de reunión aceptada provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="61907-149">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61907-150">Notas</span><span class="sxs-lookup"><span data-stu-id="61907-150">Remarks</span></span>

<span data-ttu-id="61907-151">La siguiente es la API administrada de EWS extendido definición de propiedad para la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="61907-151">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="61907-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="61907-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61907-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="61907-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61907-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61907-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61907-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="61907-155">Schema Name</span></span>  <br/> |<span data-ttu-id="61907-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="61907-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="61907-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="61907-157">Validation File</span></span>  <br/> |<span data-ttu-id="61907-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61907-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="61907-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="61907-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="61907-160">False</span><span class="sxs-lookup"><span data-stu-id="61907-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61907-161">Ver también</span><span class="sxs-lookup"><span data-stu-id="61907-161">See also</span></span>



- [<span data-ttu-id="61907-162">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="61907-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="61907-163">EWS, MIME y los encabezados de mensaje de Internet que faltan</span><span class="sxs-lookup"><span data-stu-id="61907-163">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)


---
title: Proponer una nueva hora de reunión mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Descubra cómo proponer nuevas horas de reunión desde la aplicación de cliente de Exchange mediante el uso de EWS en Exchange.
ms.openlocfilehash: f9edd8511332474a728635a6aa369a772da24786
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763155"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a><span data-ttu-id="3b68f-103">Proponer una nueva hora de reunión mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b68f-103">Propose a new meeting time by using EWS in Exchange</span></span>

<span data-ttu-id="3b68f-104">Descubra cómo proponer nuevas horas de reunión desde la aplicación de cliente de Exchange mediante el uso de EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="3b68f-104">Find out how to propose new meeting times from your Exchange client application by using EWS in Exchange.</span></span>
  
<span data-ttu-id="3b68f-105">La nueva característica de tiempo proponer permite a los asistentes proponer nuevas horas de reunión al organizador de la reunión como parte del flujo de trabajo de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3b68f-105">The propose new time feature enables attendees to propose new meeting times to the meeting organizer as part of the Exchange calendar workflow.</span></span> <span data-ttu-id="3b68f-106">Cuando un asistente propone una nueva reunión, el organizador puede usar la nueva hora de reunión propuesta para actualizar la reunión y enviar actualizaciones a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="3b68f-106">When an attendee proposes a new meeting, the organizer can use the proposed new meeting time to update the meeting and send updates to all attendees.</span></span> <span data-ttu-id="3b68f-107">Antes de poder habilitar a los asistentes proponer nuevas horas de reunión, debe determinar si se permite el Organizador para nuevas propuestas de plazos.</span><span class="sxs-lookup"><span data-stu-id="3b68f-107">Before you can enable attendees to propose new meeting times, you need to determine whether the organizer allows for new time proposals.</span></span> <span data-ttu-id="3b68f-108">En este artículo se describe cómo determinar si puede proponer una nueva hora y cómo usar EWS para proponer una nueva hora.</span><span class="sxs-lookup"><span data-stu-id="3b68f-108">This article describes how to determine whether you can propose a new time and how to use EWS to propose a new time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3b68f-109">La API administrada de EWS no implementa esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3b68f-109">The EWS Managed API does not implement this functionality.</span></span> 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a><span data-ttu-id="3b68f-110">Determinar si puede proponer una nueva hora para una reunión mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="3b68f-110">Determine whether you can propose a new time for a meeting by using EWS</span></span>
<span data-ttu-id="3b68f-111"><a name="bk_Determine"> </a></span><span class="sxs-lookup"><span data-stu-id="3b68f-111"></span></span>

<span data-ttu-id="3b68f-112">Antes de proponer una nueva hora para una reunión, debe buscar una referencia a dicha reunión y determinar si el organizador de la reunión configurado la reunión para admitir nuevas propuestas de plazos.</span><span class="sxs-lookup"><span data-stu-id="3b68f-112">Before you can propose a new time for a meeting, you need to find a reference to that meeting and determine whether the meeting organizer configured the meeting to support new time proposals.</span></span> <span data-ttu-id="3b68f-113">Puede obtener una referencia a una reunión mediante una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="3b68f-113">You can get a reference to a meeting by doing either of the following:</span></span> 
  
- <span data-ttu-id="3b68f-114">Búsqueda de la convocatoria de reunión en la Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="3b68f-114">Finding the meeting request in the Inbox</span></span>
    
- <span data-ttu-id="3b68f-115">Búsqueda de la cita en el calendario</span><span class="sxs-lookup"><span data-stu-id="3b68f-115">Finding the appointment in the calendar</span></span>
    
<span data-ttu-id="3b68f-116">Use los pasos siguientes para buscar una referencia de la reunión:</span><span class="sxs-lookup"><span data-stu-id="3b68f-116">Use the following steps to find a meeting reference:</span></span>
  
1. <span data-ttu-id="3b68f-117">Use la operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) (o el método de la API administrada de EWS [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) ) para encontrar el destino solicitud o elemento de calendario de la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-117">Use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation (or the [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) EWS Managed API method) to find the target meeting request or calendar item.</span></span> <span data-ttu-id="3b68f-118">Como alternativa, puede usar la operación de EWS [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) para obtener el identificador del elemento de calendario o solicitud de reunión de destino.</span><span class="sxs-lookup"><span data-stu-id="3b68f-118">Alternatively, you can use the [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS operation to get the identifier of the target meeting request or calendar item.</span></span> 
    
2. <span data-ttu-id="3b68f-119">Analizar los resultados de la operación de **FindItem** (o el método **Folder.FindItems** ) para obtener el identificador de elemento del elemento de reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-119">Parse the results of the **FindItem** operation (or **Folder.FindItems** method) to get the item identifier of the meeting item.</span></span> 
    
3. <span data-ttu-id="3b68f-120">Use la operación de EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener los objetos de respuesta para la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-120">Use the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get the response objects for the meeting.</span></span> 
    
<span data-ttu-id="3b68f-121">El siguiente código XML muestra lo que se envía a los objetos de respuesta en un elemento de solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b68f-121">The following XML shows what is sent to request the response objects on an item.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ResponseObjects"/>
          <t:FieldURI FieldURI="item:Subject"/>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3b68f-122">La respuesta de la operación **GetItem** tendrá un aspecto similar al código XML siguiente si solicita el identificador del elemento, el inicio de la reunión y hora de finalización, la colección de objetos de respuesta, y si el organizador permite cambios propuestos para el tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-122">The **GetItem** operation response will look similar to the following XML if you request the item identifier, the meeting start and end time, the response object collection, and if the organizer allows for proposed changes to the meeting time.</span></span> <span data-ttu-id="3b68f-123">La colección de objetos de respuesta, que está representada por el elemento [ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) , contiene el conjunto de las respuestas que son válidos para el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="3b68f-123">The response object collection, which is represented by the [ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) element, contains the set of responses that are valid for the calendar item.</span></span> <span data-ttu-id="3b68f-124">El elemento **ProposeNewTime** es un objeto de respuesta que indica que el usuario puede proponer una nueva hora para la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-124">The **ProposeNewTime** element is a response object that indicates that the user can propose a new time for the meeting.</span></span> <span data-ttu-id="3b68f-125">Los elementos de [AcceptItem](http://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](http://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)y [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) representan los objetos de respuesta que puede usar para proponer una nueva hora de reunión al organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-125">The [AcceptItem](http://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](http://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx), and [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) elements represent the response objects that you can use to propose a new meeting time to the meeting organizer.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
              <t:Subject>Competitive analysis: kick off meeting</t:Subject>
              <t:ResponseObjects>
                <t:AcceptItem/>
                <t:TentativelyAcceptItem/>
                <t:DeclineItem/>
                <t:ProposeNewTime/>
                <t:ReplyToItem/>
                <t:ReplyAllToItem/>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2013-11-09T17:00:00Z</t:Start>
              <t:End>2013-11-09T17:30:00Z</t:End>
            </t:MeetingRequest>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="propose-a-new-meeting-time-by-using-ews"></a><span data-ttu-id="3b68f-126">Proponer una nueva hora de reunión mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="3b68f-126">Propose a new meeting time by using EWS</span></span>
<span data-ttu-id="3b68f-127"><a name="bk_Propose"> </a></span><span class="sxs-lookup"><span data-stu-id="3b68f-127"></span></span>

<span data-ttu-id="3b68f-128">Si ha recibido un objeto de respuesta **ProposeNewTime** cuando se usa la operación **GetItem** para obtener un elemento de calendario o convocatoria de reunión, puede responder con una nueva hora de reunión propuesta.</span><span class="sxs-lookup"><span data-stu-id="3b68f-128">If you received a **ProposeNewTime** response object when you used the **GetItem** operation to get a calendar item or meeting request, you can respond with a proposed new meeting time.</span></span> <span data-ttu-id="3b68f-129">Si no ha recibido un objeto de respuesta **ProposeNewTime** , no podrá proponer una nueva hora de reunión como parte del flujo de trabajo de calendario.</span><span class="sxs-lookup"><span data-stu-id="3b68f-129">If you didn't receive a **ProposeNewTime** response object, you won't be able to propose a new meeting time as part of the calendar workflow.</span></span> <span data-ttu-id="3b68f-130">Sin embargo, puede responder al organizador para solicitar una nueva hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-130">You can, however, reply to the organizer to request a new meeting time.</span></span> <span data-ttu-id="3b68f-131">Si recibe un objeto de respuesta **ProposeNewTime** , puede responder a la reunión mediante una referencia a su identificador y proponer una nueva hora de reunión del organizador.</span><span class="sxs-lookup"><span data-stu-id="3b68f-131">If you receive a **ProposeNewTime** response object, you can respond to the meeting by referencing its identifier, and propose a new meeting time to the organizer.</span></span> <span data-ttu-id="3b68f-132">Esto es donde el objeto de respuesta **ProposeNewTime** es diferente del modelo de objeto de respuesta típica en que no responde con un objeto de respuesta **ProposeNewTime** .</span><span class="sxs-lookup"><span data-stu-id="3b68f-132">This is where the **ProposeNewTime** response object is different than the typical response object pattern in that you don't respond with a **ProposeNewTime** response object.</span></span> <span data-ttu-id="3b68f-133">Use uno de los otros objetos de respuesta, como **AcceptItem**, **TentativelyAcceptItem**o **DeclineItem**, para proponer una nueva reunión de la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-133">You use one of the other meeting response objects, such as **AcceptItem**, **TentativelyAcceptItem**, or **DeclineItem**, to propose a new meeting.</span></span> <span data-ttu-id="3b68f-134">En este ejemplo se utiliza el objeto de respuesta de **AcceptItem** .</span><span class="sxs-lookup"><span data-stu-id="3b68f-134">This example uses the **AcceptItem** response object.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:CreateItem>
      <m:Items>
        <t:AcceptItem>
          <t:Body BodyType="Text">This time works better for the HiPPO.</t:Body>
          <t:ReferenceItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
          <t:ProposedStart>2013-11-28T04:00:00Z</t:ProposedStart>
          <t:ProposedEnd>2013-11-28T04:30:00Z</t:ProposedEnd>
        </t:AcceptItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3b68f-135">La respuesta a esta solicitud contiene el identificador del elemento de calendario que se ha agregado para el calendario del asistente y una copia de la convocatoria de reunión que se ha puesto en la carpeta de elementos eliminados del asistente.</span><span class="sxs-lookup"><span data-stu-id="3b68f-135">The response to this request contains the identifier of the calendar item that was added to the attendee's calendar and a copy of the meeting request that was placed in the attendee's Deleted Items folder.</span></span> <span data-ttu-id="3b68f-136">El mensaje de respuesta con la nueva propuesta de hora también se guardó en la carpeta de elementos enviados del asistente (necesita encontrar la reunión mensaje de respuesta para obtener un identificador en él).</span><span class="sxs-lookup"><span data-stu-id="3b68f-136">The response message with the new time proposal was also saved in the attendee's Sent Items folder (you will need to find the meeting response message to get a handle on it).</span></span>
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAGRmOWE2OWAAA=" ChangeKey="DwAAJsmU"/>
            </t:CalendarItem>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkAGRmOWE2AAABB=" ChangeKey="AAAGJu1A"/>
            </t:MeetingRequest>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="3b68f-137">El organizador recibirá un mensaje de [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) cuando el Asistente responde con una nueva hora de reunión propuesta.</span><span class="sxs-lookup"><span data-stu-id="3b68f-137">The organizer will receive a [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) message when the attendee responds with a proposed new meeting time.</span></span> <span data-ttu-id="3b68f-138">El mensaje de **MeetingResponse** contiene la reunión propuesta de nueva hora de inicio y hora de finalización y el identificador del elemento de calendario asociado en el calendario del organizer.</span><span class="sxs-lookup"><span data-stu-id="3b68f-138">The **MeetingResponse** message contains the proposed new meeting start time and end time, and the identifier of the associated calendar item in the organizer's calendar.</span></span> <span data-ttu-id="3b68f-139">El organizador puede utilizar esa información para actualizar su elemento de calendario existente para la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-139">The organizer can use that information to update their existing calendar item for the meeting.</span></span> <span data-ttu-id="3b68f-140">El siguiente es el flujo de trabajo para el organizador responder a un mensaje de **MeetingResponse** que propone una nueva hora de reunión:</span><span class="sxs-lookup"><span data-stu-id="3b68f-140">The following is the workflow for the organizer to respond to a **MeetingResponse** message that proposes a new meeting time:</span></span> 
  
1. <span data-ttu-id="3b68f-141">Determinar si se han establecido los elementos **ProposedStart** o **///ProposedEnd** en el **MeetingResponse**.</span><span class="sxs-lookup"><span data-stu-id="3b68f-141">Determine whether the **ProposedStart** or **ProposedEnd** elements have been set in the **MeetingResponse**.</span></span> <span data-ttu-id="3b68f-142">Si es así, vaya al paso 2.</span><span class="sxs-lookup"><span data-stu-id="3b68f-142">If so, go to step 2.</span></span> <span data-ttu-id="3b68f-143">Si no es así, el mensaje de **MeetingResponse** sólo indica si el asistente ha aceptado, aceptado provisionalmente o rechazado la reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-143">If not, the **MeetingResponse** message only indicates whether the attendee has accepted, tentatively accepted, or declined the meeting.</span></span> 
    
2. <span data-ttu-id="3b68f-144">Obtener elemento de calendario existente del organizador de la reunión utilizando el identificador EWS devuelto en el elemento **AssociatedCalendarItemId** .</span><span class="sxs-lookup"><span data-stu-id="3b68f-144">Get the organizer's existing calendar item for the meeting by using the EWS identifier returned in the **AssociatedCalendarItemId** element.</span></span> 
    
3. <span data-ttu-id="3b68f-145">Compare el inicio original y la hora de finalización con la nueva hora de reunión propuesta.</span><span class="sxs-lookup"><span data-stu-id="3b68f-145">Compare the original start and end time with the proposed new meeting time.</span></span> <span data-ttu-id="3b68f-146">Si la nueva hora de reunión propuesta es aceptable para el organizador, vaya al paso 4.</span><span class="sxs-lookup"><span data-stu-id="3b68f-146">If the proposed new meeting time is acceptable to the organizer, go to step 4.</span></span> <span data-ttu-id="3b68f-147">De lo contrario, el organizador de la reunión puede omitir la hora de reunión propuesta o enviar una respuesta de correo electrónico a los asistentes que proponen la nueva hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="3b68f-147">Otherwise, the meeting organizer can either ignore the proposed meeting time, or send an email response to the attendee that proposed the new meeting time.</span></span>
    
4. <span data-ttu-id="3b68f-148">(Opcional) Realizar una llamada de operación de EWS [GetUserAvailability](http://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) para averiguar si la hora propuesta funcionará para todos los asistentes, incluidos los buzones de sala y recursos.</span><span class="sxs-lookup"><span data-stu-id="3b68f-148">(Optional) Perform a [GetUserAvailability](http://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS operation call to find out whether the proposed time will work for all attendees, including room and resource mailboxes.</span></span> <span data-ttu-id="3b68f-149">(Se puede utilizar el método de la API administrada de EWS [ExchangeService.GetUserAvailability](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) hacerlo.)</span><span class="sxs-lookup"><span data-stu-id="3b68f-149">(You can also use the [ExchangeService.GetUserAvailability](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS Managed API method to do this.)</span></span> 
    
5. <span data-ttu-id="3b68f-150">El organizador, a continuación, puede actualizar sus reuniones con los nuevos tiempos de reunión propuesta y enviar las actualizaciones a todos los asistentes mediante el uso de la operación de EWS [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) (o el método de la API administrada de EWS [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="3b68f-150">The organizer can then update their meeting with the new proposed meeting times and send the updates to all attendees by using the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS operation (or the [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) EWS Managed API method).</span></span> 
    
<span data-ttu-id="3b68f-151">La siguiente ilustración muestra el proceso que se produce entre el organizador de la reunión, el asistente y el servidor de Exchange que administra las llamadas EWS.</span><span class="sxs-lookup"><span data-stu-id="3b68f-151">The following figure shows the process that occurs between the meeting organizer, the attendee, and the Exchange server that handled the EWS calls.</span></span>
  
<span data-ttu-id="3b68f-152">**En la figura 1. Proceso para proponer una nueva hora de reunión**</span><span class="sxs-lookup"><span data-stu-id="3b68f-152">**Figure 1. Process for proposing a new meeting time**</span></span>

![La figura muestra el flujo de trabajo entre el organizador, Exchange y un asistente cuando se propone una nueva hora de reunión. Si el organizador permite nuevas propuestas para la reunión, un asistente puede proponer una nueva hora de reunión con un objeto Response.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a><span data-ttu-id="3b68f-155">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="3b68f-155">Version differences</span></span>
<span data-ttu-id="3b68f-156"><a name="bk_Behavior"> </a></span><span class="sxs-lookup"><span data-stu-id="3b68f-156"></span></span>

<span data-ttu-id="3b68f-157">La nueva característica de tiempo proponer se introdujo en la versión de compilación de Exchange 15.00.0800.007.</span><span class="sxs-lookup"><span data-stu-id="3b68f-157">The propose new time feature was introduced in Exchange build version 15.00.0800.007.</span></span> <span data-ttu-id="3b68f-158">En versiones anteriores de Exchange, usuarios de la aplicación de EWS tienen que enviar un correo electrónico independiente al organizador de la reunión para solicitar una hora de reunión diferente.</span><span class="sxs-lookup"><span data-stu-id="3b68f-158">In earlier versions of Exchange, EWS application users have to send a separate email to the meeting organizer to request a different meeting time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b68f-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b68f-159">See also</span></span>


- [<span data-ttu-id="3b68f-160">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b68f-160">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="3b68f-161">Crear citas y reuniones mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3b68f-161">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="3b68f-162">Obtener las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b68f-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="3b68f-163">Actualizar las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b68f-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="3b68f-164">Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b68f-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    


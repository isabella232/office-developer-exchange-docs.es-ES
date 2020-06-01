---
title: Proponer una nueva hora de reunión mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Descubra cómo proponer nuevas horas de reunión desde la aplicación cliente de Exchange mediante EWS en Exchange.
ms.openlocfilehash: 4f001bb82d2325624b567412620283619b51f25b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456815"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a><span data-ttu-id="a1535-103">Proponer una nueva hora de reunión mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a1535-103">Propose a new meeting time by using EWS in Exchange</span></span>

<span data-ttu-id="a1535-104">Descubra cómo proponer nuevas horas de reunión desde la aplicación cliente de Exchange mediante EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="a1535-104">Find out how to propose new meeting times from your Exchange client application by using EWS in Exchange.</span></span>
  
<span data-ttu-id="a1535-105">La característica proponer nueva hora permite a los asistentes proponer nuevas horas de reunión al organizador de la reunión como parte del flujo de trabajo del calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a1535-105">The propose new time feature enables attendees to propose new meeting times to the meeting organizer as part of the Exchange calendar workflow.</span></span> <span data-ttu-id="a1535-106">Cuando un asistente propone una nueva reunión, el organizador puede usar la nueva hora de reunión propuesta para actualizar la reunión y enviar actualizaciones a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="a1535-106">When an attendee proposes a new meeting, the organizer can use the proposed new meeting time to update the meeting and send updates to all attendees.</span></span> <span data-ttu-id="a1535-107">Antes de permitir que los asistentes propongan nuevas horas de reunión, debe determinar si el organizador permite nuevas propuestas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a1535-107">Before you can enable attendees to propose new meeting times, you need to determine whether the organizer allows for new time proposals.</span></span> <span data-ttu-id="a1535-108">En este artículo se describe cómo determinar si se puede proponer una nueva hora y cómo usar EWS para proponer una nueva hora.</span><span class="sxs-lookup"><span data-stu-id="a1535-108">This article describes how to determine whether you can propose a new time and how to use EWS to propose a new time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a1535-109">La API administrada de EWS no implementa esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="a1535-109">The EWS Managed API does not implement this functionality.</span></span> 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a><span data-ttu-id="a1535-110">Determinar si se puede proponer una nueva hora para una reunión con EWS</span><span class="sxs-lookup"><span data-stu-id="a1535-110">Determine whether you can propose a new time for a meeting by using EWS</span></span>
<span data-ttu-id="a1535-111"><a name="bk_Determine"> </a></span><span class="sxs-lookup"><span data-stu-id="a1535-111"><a name="bk_Determine"> </a></span></span>

<span data-ttu-id="a1535-112">Antes de proponer una nueva hora para una reunión, debe encontrar una referencia a esa reunión y determinar si el organizador de la reunión la configuró para admitir nuevas propuestas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a1535-112">Before you can propose a new time for a meeting, you need to find a reference to that meeting and determine whether the meeting organizer configured the meeting to support new time proposals.</span></span> <span data-ttu-id="a1535-113">Puede obtener una referencia a una reunión realizando uno de los procedimientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1535-113">You can get a reference to a meeting by doing either of the following:</span></span> 
  
- <span data-ttu-id="a1535-114">Buscar la convocatoria de reunión en la bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="a1535-114">Finding the meeting request in the Inbox</span></span>
    
- <span data-ttu-id="a1535-115">Buscar la cita en el calendario</span><span class="sxs-lookup"><span data-stu-id="a1535-115">Finding the appointment in the calendar</span></span>
    
<span data-ttu-id="a1535-116">Siga estos pasos para buscar una referencia de reunión:</span><span class="sxs-lookup"><span data-stu-id="a1535-116">Use the following steps to find a meeting reference:</span></span>
  
1. <span data-ttu-id="a1535-117">Use la operación EWS de [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) (o el método [Folder. FINDITEMS](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) de la API administrada de EWS) para buscar la convocatoria de reunión o el elemento de calendario de destino.</span><span class="sxs-lookup"><span data-stu-id="a1535-117">Use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation (or the [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) EWS Managed API method) to find the target meeting request or calendar item.</span></span> <span data-ttu-id="a1535-118">Como alternativa, puede usar la operación de EWS [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) para obtener el identificador de la convocatoria de reunión o del elemento de calendario de destino.</span><span class="sxs-lookup"><span data-stu-id="a1535-118">Alternatively, you can use the [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS operation to get the identifier of the target meeting request or calendar item.</span></span> 
    
2. <span data-ttu-id="a1535-119">Analizar los resultados de la operación **FindItem** (o el método **Folder. FindItems** ) para obtener el identificador de elemento del elemento de reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-119">Parse the results of the **FindItem** operation (or **Folder.FindItems** method) to get the item identifier of the meeting item.</span></span> 
    
3. <span data-ttu-id="a1535-120">Use la operación de EWS de [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener los objetos de respuesta de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-120">Use the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get the response objects for the meeting.</span></span> 
    
<span data-ttu-id="a1535-121">El siguiente XML muestra lo que se envía para solicitar los objetos de respuesta de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a1535-121">The following XML shows what is sent to request the response objects on an item.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="a1535-122">La respuesta de la operación **GetItem** será similar al siguiente código XML si solicita el identificador del elemento, la hora de inicio y finalización de la reunión, la colección de objetos de respuesta y si el organizador permite los cambios propuestos en la hora de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-122">The **GetItem** operation response will look similar to the following XML if you request the item identifier, the meeting start and end time, the response object collection, and if the organizer allows for proposed changes to the meeting time.</span></span> <span data-ttu-id="a1535-123">La colección de objetos de respuesta, que se representa mediante el elemento [ResponseObjects](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) , contiene el conjunto de respuestas que son válidas para el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="a1535-123">The response object collection, which is represented by the [ResponseObjects](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) element, contains the set of responses that are valid for the calendar item.</span></span> <span data-ttu-id="a1535-124">El elemento **ProposeNewTime** es un objeto Response que indica que el usuario puede proponer una nueva hora para la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-124">The **ProposeNewTime** element is a response object that indicates that the user can propose a new time for the meeting.</span></span> <span data-ttu-id="a1535-125">Los elementos [AcceptItem](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)y [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) representan los objetos de respuesta que puede usar para proponer una nueva hora de reunión al organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-125">The [AcceptItem](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx), and [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) elements represent the response objects that you can use to propose a new meeting time to the meeting organizer.</span></span> 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="propose-a-new-meeting-time-by-using-ews"></a><span data-ttu-id="a1535-126">Proponer una nueva hora de reunión mediante EWS</span><span class="sxs-lookup"><span data-stu-id="a1535-126">Propose a new meeting time by using EWS</span></span>
<span data-ttu-id="a1535-127"><a name="bk_Propose"> </a></span><span class="sxs-lookup"><span data-stu-id="a1535-127"><a name="bk_Propose"> </a></span></span>

<span data-ttu-id="a1535-128">Si recibió un objeto de respuesta **ProposeNewTime** cuando usó la operación **GetItem** para obtener un elemento de calendario o una convocatoria de reunión, puede responder con una nueva hora de reunión propuesta.</span><span class="sxs-lookup"><span data-stu-id="a1535-128">If you received a **ProposeNewTime** response object when you used the **GetItem** operation to get a calendar item or meeting request, you can respond with a proposed new meeting time.</span></span> <span data-ttu-id="a1535-129">Si no ha recibido un objeto de respuesta **ProposeNewTime** , no podrá proponer una nueva hora de reunión como parte del flujo de trabajo del calendario.</span><span class="sxs-lookup"><span data-stu-id="a1535-129">If you didn't receive a **ProposeNewTime** response object, you won't be able to propose a new meeting time as part of the calendar workflow.</span></span> <span data-ttu-id="a1535-130">Sin embargo, puede responder al organizador para solicitar una nueva hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-130">You can, however, reply to the organizer to request a new meeting time.</span></span> <span data-ttu-id="a1535-131">Si recibe un objeto de respuesta **ProposeNewTime** , puede responder a la reunión haciendo referencia a su identificador y proponer una nueva hora de reunión al organizador.</span><span class="sxs-lookup"><span data-stu-id="a1535-131">If you receive a **ProposeNewTime** response object, you can respond to the meeting by referencing its identifier, and propose a new meeting time to the organizer.</span></span> <span data-ttu-id="a1535-132">Aquí es donde el objeto de respuesta **ProposeNewTime** es diferente al modelo de objeto de respuesta típico en el que no responde con un objeto de respuesta **ProposeNewTime** .</span><span class="sxs-lookup"><span data-stu-id="a1535-132">This is where the **ProposeNewTime** response object is different than the typical response object pattern in that you don't respond with a **ProposeNewTime** response object.</span></span> <span data-ttu-id="a1535-133">Puede usar uno de los demás objetos de respuesta a reuniones, como **AcceptItem**, **TentativelyAcceptItem**o **DeclineItem**, para proponer una nueva reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-133">You use one of the other meeting response objects, such as **AcceptItem**, **TentativelyAcceptItem**, or **DeclineItem**, to propose a new meeting.</span></span> <span data-ttu-id="a1535-134">En este ejemplo se usa el objeto de respuesta **AcceptItem** .</span><span class="sxs-lookup"><span data-stu-id="a1535-134">This example uses the **AcceptItem** response object.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="a1535-135">La respuesta a esta solicitud contiene el identificador del elemento de calendario que se agregó al calendario del asistente y una copia de la convocatoria de reunión que se colocó en la carpeta elementos eliminados del asistente.</span><span class="sxs-lookup"><span data-stu-id="a1535-135">The response to this request contains the identifier of the calendar item that was added to the attendee's calendar and a copy of the meeting request that was placed in the attendee's Deleted Items folder.</span></span> <span data-ttu-id="a1535-136">El mensaje de respuesta con la nueva propuesta de tiempo también se guardó en la carpeta elementos enviados del asistente (tendrá que buscar el mensaje de respuesta de la reunión para obtener un controlador).</span><span class="sxs-lookup"><span data-stu-id="a1535-136">The response message with the new time proposal was also saved in the attendee's Sent Items folder (you will need to find the meeting response message to get a handle on it).</span></span>
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="a1535-137">El organizador recibirá un mensaje [MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) cuando el asistente responda con una nueva hora de reunión propuesta.</span><span class="sxs-lookup"><span data-stu-id="a1535-137">The organizer will receive a [MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) message when the attendee responds with a proposed new meeting time.</span></span> <span data-ttu-id="a1535-138">El mensaje **MeetingResponse** contiene la hora de inicio y la hora de finalización de la nueva reunión propuestas y el identificador del elemento de calendario asociado en el calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="a1535-138">The **MeetingResponse** message contains the proposed new meeting start time and end time, and the identifier of the associated calendar item in the organizer's calendar.</span></span> <span data-ttu-id="a1535-139">El organizador puede usar esa información para actualizar su elemento de calendario existente para la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-139">The organizer can use that information to update their existing calendar item for the meeting.</span></span> <span data-ttu-id="a1535-140">El siguiente es el flujo de trabajo para que el organizador responda a un mensaje de **MeetingResponse** que propone una nueva hora de la reunión:</span><span class="sxs-lookup"><span data-stu-id="a1535-140">The following is the workflow for the organizer to respond to a **MeetingResponse** message that proposes a new meeting time:</span></span> 
  
1. <span data-ttu-id="a1535-141">Determine si los elementos **ProposedStart** o **ProposedEnd** se han establecido en la **MeetingResponse**.</span><span class="sxs-lookup"><span data-stu-id="a1535-141">Determine whether the **ProposedStart** or **ProposedEnd** elements have been set in the **MeetingResponse**.</span></span> <span data-ttu-id="a1535-142">Si es así, vaya al paso 2.</span><span class="sxs-lookup"><span data-stu-id="a1535-142">If so, go to step 2.</span></span> <span data-ttu-id="a1535-143">De lo contrario, el mensaje **MeetingResponse** sólo indica si el asistente ha aceptado, aceptado provisionalmente o rechazado la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-143">If not, the **MeetingResponse** message only indicates whether the attendee has accepted, tentatively accepted, or declined the meeting.</span></span> 
    
2. <span data-ttu-id="a1535-144">Obtener el elemento de calendario existente del organizador para la reunión mediante el identificador de EWS devuelto en el elemento **AssociatedCalendarItemId** .</span><span class="sxs-lookup"><span data-stu-id="a1535-144">Get the organizer's existing calendar item for the meeting by using the EWS identifier returned in the **AssociatedCalendarItemId** element.</span></span> 
    
3. <span data-ttu-id="a1535-145">Compare la hora de inicio y finalización originales con la nueva hora propuesta de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-145">Compare the original start and end time with the proposed new meeting time.</span></span> <span data-ttu-id="a1535-146">Si la nueva hora propuesta para la reunión es aceptable para el organizador, vaya al paso 4.</span><span class="sxs-lookup"><span data-stu-id="a1535-146">If the proposed new meeting time is acceptable to the organizer, go to step 4.</span></span> <span data-ttu-id="a1535-147">De lo contrario, el organizador de la reunión puede omitir la hora de la reunión propuesta o enviar una respuesta por correo electrónico al asistente que propuso la nueva hora de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a1535-147">Otherwise, the meeting organizer can either ignore the proposed meeting time, or send an email response to the attendee that proposed the new meeting time.</span></span>
    
4. <span data-ttu-id="a1535-148">Opcional Realice una llamada de operación de EWS de [GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) para averiguar si la hora propuesta funcionará para todos los asistentes, incluidos los buzones de sala y de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1535-148">(Optional) Perform a [GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS operation call to find out whether the proposed time will work for all attendees, including room and resource mailboxes.</span></span> <span data-ttu-id="a1535-149">(También puede usar el método de la API administrada de EWS [ExchangeService. GetUserAvailability](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) para hacerlo).</span><span class="sxs-lookup"><span data-stu-id="a1535-149">(You can also use the [ExchangeService.GetUserAvailability](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS Managed API method to do this.)</span></span> 
    
5. <span data-ttu-id="a1535-150">A continuación, el organizador puede actualizar su reunión con las nuevas horas de reunión propuestas y enviar las actualizaciones a todos los asistentes mediante la operación de EWS de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) (o la [cita. actualice](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) el método de la API administrada de EWS).</span><span class="sxs-lookup"><span data-stu-id="a1535-150">The organizer can then update their meeting with the new proposed meeting times and send the updates to all attendees by using the [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS operation (or the [Appointment.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) EWS Managed API method).</span></span> 
    
<span data-ttu-id="a1535-151">La siguiente ilustración muestra el proceso que se produce entre el organizador de la reunión, el asistente y el servidor de Exchange que administra las llamadas de EWS.</span><span class="sxs-lookup"><span data-stu-id="a1535-151">The following figure shows the process that occurs between the meeting organizer, the attendee, and the Exchange server that handled the EWS calls.</span></span>
  
<span data-ttu-id="a1535-152">**Figura 1. Proceso para proponer una nueva hora de reunión**</span><span class="sxs-lookup"><span data-stu-id="a1535-152">**Figure 1. Process for proposing a new meeting time**</span></span>

![La figura muestra el flujo de trabajo entre el organizador, Exchange y un asistente cuando se propone una nueva hora de reunión. Si el organizador permite nuevas propuestas para la reunión, un asistente puede proponer una nueva hora de reunión con un objeto Response.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a><span data-ttu-id="a1535-155">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="a1535-155">Version differences</span></span>
<span data-ttu-id="a1535-156"><a name="bk_Behavior"> </a></span><span class="sxs-lookup"><span data-stu-id="a1535-156"><a name="bk_Behavior"> </a></span></span>

<span data-ttu-id="a1535-157">La característica proponer nueva hora se introdujo en la versión de compilación de Exchange 15.00.0800.007.</span><span class="sxs-lookup"><span data-stu-id="a1535-157">The propose new time feature was introduced in Exchange build version 15.00.0800.007.</span></span> <span data-ttu-id="a1535-158">En versiones anteriores de Exchange, los usuarios de la aplicación de EWS deben enviar un correo electrónico independiente al organizador de la reunión para solicitar una hora de reunión diferente.</span><span class="sxs-lookup"><span data-stu-id="a1535-158">In earlier versions of Exchange, EWS application users have to send a separate email to the meeting organizer to request a different meeting time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1535-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1535-159">See also</span></span>


- [<span data-ttu-id="a1535-160">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a1535-160">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="a1535-161">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a1535-161">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="a1535-162">Obtener citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a1535-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="a1535-163">Actualizar citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a1535-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="a1535-164">Eliminar citas y cancelar reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a1535-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    


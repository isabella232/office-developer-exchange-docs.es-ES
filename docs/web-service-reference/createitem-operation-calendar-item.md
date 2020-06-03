---
title: Operación CreateItem (elemento de calendario)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: aa4a7c94-f668-4bd2-8079-c855f6ab17e1
description: La operación CreateItem crea elementos de calendario en el almacén de Exchange.
ms.openlocfilehash: 535edf9fe567bc3063a5b853f01d604ea4c7eb95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457504"
---
# <a name="createitem-operation-calendar-item"></a><span data-ttu-id="0b026-103">Operación CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="0b026-103">CreateItem operation (calendar item)</span></span>

<span data-ttu-id="0b026-104">La operación CreateItem crea elementos de calendario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0b026-104">The CreateItem operation creates calendar items in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b026-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b026-105">Remarks</span></span>

<span data-ttu-id="0b026-106">La operación CreateItem crea citas, reuniones y convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="0b026-106">The CreateItem operation creates appointments, meetings, and meeting requests.</span></span> <span data-ttu-id="0b026-107">Si se crea un elemento de calendario sin asistentes, se considera una cita.</span><span class="sxs-lookup"><span data-stu-id="0b026-107">If a calendar item is created without attendees, it is considered an appointment.</span></span> <span data-ttu-id="0b026-108">Si se especifican asistentes, el elemento de calendario es una reunión.</span><span class="sxs-lookup"><span data-stu-id="0b026-108">If attendees are specified, the calendar item is a meeting.</span></span> <span data-ttu-id="0b026-109">Cuando se crea una reunión mediante la operación CreateItem, las convocatorias de reunión se envían automáticamente a los asistentes identificados si el atributo SendMeetingInvitations está configurado para enviar las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="0b026-109">When a meeting is created by using the CreateItem operation, meeting requests are automatically sent to the identified attendees if the SendMeetingInvitations attribute is set to send the meeting requests.</span></span>
  
## <a name="createitem-calendar-item-request-example"></a><span data-ttu-id="0b026-110">Ejemplo de solicitud CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="0b026-110">CreateItem (Calendar Item) request example</span></span>

### <a name="description"></a><span data-ttu-id="0b026-111">Description</span><span class="sxs-lookup"><span data-stu-id="0b026-111">Description</span></span>

<span data-ttu-id="0b026-112">El siguiente ejemplo de una solicitud CreateItem muestra cómo crear una reunión con dos asistentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="0b026-112">The following example of a CreateItem request shows how to create a meeting with two required attendees.</span></span> <span data-ttu-id="0b026-113">Esta solicitud enviará las convocatorias de reunión a los dos asistentes.</span><span class="sxs-lookup"><span data-stu-id="0b026-113">This request will send the meeting requests to the two attendees.</span></span>
  
### <a name="code"></a><span data-ttu-id="0b026-114">Código</span><span class="sxs-lookup"><span data-stu-id="0b026-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                SendMeetingInvitations="SendToAllAndSaveCopy" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar"/>
      </SavedItemFolderId>
      <Items>
        <t:CalendarItem xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Planning Meeting</Subject>
          <Body BodyType="Text">Plan the agenda for next week's meeting.</Body>
          <ReminderIsSet>true</ReminderIsSet>
          <ReminderMinutesBeforeStart>60</ReminderMinutesBeforeStart>
          <Start>2006-11-02T14:00:00</Start>
          <End>2006-11-02T15:00:00</End>
          <IsAllDayEvent>false</IsAllDayEvent>
          <LegacyFreeBusyStatus>Busy</LegacyFreeBusyStatus>
          <Location>Conference Room 721</Location>
          <RequiredAttendees>
            <Attendee>
              <Mailbox>
                <EmailAddress>User1@example.com</EmailAddress>
              </Mailbox>
            </Attendee>
            <Attendee>
              <Mailbox>
                <EmailAddress>User2@example.com</EmailAddress>
              </Mailbox>
            </Attendee>
          </RequiredAttendees>
        </t:CalendarItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0b026-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b026-115">Comments</span></span>

<span data-ttu-id="0b026-116">Para obtener un ejemplo de cómo responder a una convocatoria de reunión, vea el tema [Operation CreateItem (solicitud de reunión)](createitem-operation-meeting-request.md) .</span><span class="sxs-lookup"><span data-stu-id="0b026-116">For an example of how to respond to a meeting request, see the [CreateItem operation (meeting request)](createitem-operation-meeting-request.md) topic.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="0b026-117">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b026-117">Request elements</span></span>

<span data-ttu-id="0b026-118">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="0b026-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0b026-119">CreateItem</span><span class="sxs-lookup"><span data-stu-id="0b026-119">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="0b026-120">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="0b026-120">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="0b026-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0b026-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="0b026-122">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="0b026-122">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="0b026-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0b026-123">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="0b026-124">Asunto</span><span class="sxs-lookup"><span data-stu-id="0b026-124">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="0b026-125">Body</span><span class="sxs-lookup"><span data-stu-id="0b026-125">Body</span></span>](body.md)
    
- [<span data-ttu-id="0b026-126">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="0b026-126">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="0b026-127">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="0b026-127">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="0b026-128">Start</span><span class="sxs-lookup"><span data-stu-id="0b026-128">Start</span></span>](start.md)
    
- [<span data-ttu-id="0b026-129">Centraliza</span><span class="sxs-lookup"><span data-stu-id="0b026-129">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0b026-130">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="0b026-130">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="0b026-131">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0b026-131">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="0b026-132">Ubicación</span><span class="sxs-lookup"><span data-stu-id="0b026-132">Location</span></span>](location.md)
    
- [<span data-ttu-id="0b026-133">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="0b026-133">RequiredAttendees</span></span>](requiredattendees.md)
    
- [<span data-ttu-id="0b026-134">Asistente</span><span class="sxs-lookup"><span data-stu-id="0b026-134">Attendee</span></span>](attendee.md)
    
- [<span data-ttu-id="0b026-135">Buzón</span><span class="sxs-lookup"><span data-stu-id="0b026-135">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="0b026-136">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0b026-136">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-createitem-calendar-item-response"></a><span data-ttu-id="0b026-137">Se ha realizado correctamente CreateItem (elemento de calendario) Response</span><span class="sxs-lookup"><span data-stu-id="0b026-137">Successful CreateItem (Calendar Item) Response</span></span>

### <a name="description"></a><span data-ttu-id="0b026-138">Description</span><span class="sxs-lookup"><span data-stu-id="0b026-138">Description</span></span>

<span data-ttu-id="0b026-139">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateItem.</span><span class="sxs-lookup"><span data-stu-id="0b026-139">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="0b026-140">Código</span><span class="sxs-lookup"><span data-stu-id="0b026-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAAlAFV" ChangeKey="DwAAABYA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0b026-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b026-141">Comments</span></span>

<span data-ttu-id="0b026-142">El **identificador** del elemento [Itemid](itemid.md) y los atributos **changekey** se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0b026-142">The [ItemId](itemid.md) element **Id** and **ChangeKey** attributes have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="0b026-143">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="0b026-143">Successful response elements</span></span>

<span data-ttu-id="0b026-144">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b026-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0b026-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b026-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0b026-146">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="0b026-146">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="0b026-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b026-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0b026-148">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b026-148">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="0b026-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b026-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0b026-150">Items</span><span class="sxs-lookup"><span data-stu-id="0b026-150">Items</span></span>](items.md)
    
- [<span data-ttu-id="0b026-151">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0b026-151">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="0b026-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b026-152">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="0b026-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b026-153">See also</span></span>



[<span data-ttu-id="0b026-154">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="0b026-154">CreateItem operation</span></span>](createitem-operation.md)


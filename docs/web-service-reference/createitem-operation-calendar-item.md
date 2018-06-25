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
description: La operación CreateItem crea los elementos de calendario en el almacén de Exchange.
ms.openlocfilehash: c2174dd806b922e640ef7afcab32b98c67c65b41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763949"
---
# <a name="createitem-operation-calendar-item"></a><span data-ttu-id="3f738-103">Operación CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="3f738-103">CreateItem operation (calendar item)</span></span>

<span data-ttu-id="3f738-104">La operación CreateItem crea los elementos de calendario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f738-104">The CreateItem operation creates calendar items in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f738-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f738-105">Remarks</span></span>

<span data-ttu-id="3f738-106">La operación CreateItem crea citas, reuniones y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="3f738-106">The CreateItem operation creates appointments, meetings, and meeting requests.</span></span> <span data-ttu-id="3f738-107">Si se crea un elemento de calendario sin asistentes, se considera una cita.</span><span class="sxs-lookup"><span data-stu-id="3f738-107">If a calendar item is created without attendees, it is considered an appointment.</span></span> <span data-ttu-id="3f738-108">Si se especifican los asistentes, el elemento de calendario es una reunión.</span><span class="sxs-lookup"><span data-stu-id="3f738-108">If attendees are specified, the calendar item is a meeting.</span></span> <span data-ttu-id="3f738-109">Cuando se crea una reunión mediante el uso de la operación CreateItem, las convocatorias de reunión se envían automáticamente a los asistentes identificados si se establece el atributo SendMeetingInvitations para enviar las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="3f738-109">When a meeting is created by using the CreateItem operation, meeting requests are automatically sent to the identified attendees if the SendMeetingInvitations attribute is set to send the meeting requests.</span></span>
  
## <a name="createitem-calendar-item-request-example"></a><span data-ttu-id="3f738-110">Ejemplo de solicitud CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="3f738-110">CreateItem (Calendar Item) request example</span></span>

### <a name="description"></a><span data-ttu-id="3f738-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f738-111">Description</span></span>

<span data-ttu-id="3f738-112">El siguiente ejemplo de una solicitud CreateItem muestra cómo crear una reunión con dos asistentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="3f738-112">The following example of a CreateItem request shows how to create a meeting with two required attendees.</span></span> <span data-ttu-id="3f738-113">Esta solicitud enviará las convocatorias de reunión a los asistentes de dos.</span><span class="sxs-lookup"><span data-stu-id="3f738-113">This request will send the meeting requests to the two attendees.</span></span>
  
### <a name="code"></a><span data-ttu-id="3f738-114">Código</span><span class="sxs-lookup"><span data-stu-id="3f738-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                SendMeetingInvitations="SendToAllAndSaveCopy" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar"/>
      </SavedItemFolderId>
      <Items>
        <t:CalendarItem xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="3f738-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f738-115">Comments</span></span>

<span data-ttu-id="3f738-116">Para obtener un ejemplo de cómo responder a una convocatoria de reunión, vea el tema [operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md) .</span><span class="sxs-lookup"><span data-stu-id="3f738-116">For an example of how to respond to a meeting request, see the [CreateItem operation (meeting request)](createitem-operation-meeting-request.md) topic.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="3f738-117">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f738-117">Request elements</span></span>

<span data-ttu-id="3f738-118">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="3f738-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="3f738-119">CreateItem</span><span class="sxs-lookup"><span data-stu-id="3f738-119">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="3f738-120">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="3f738-120">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="3f738-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="3f738-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="3f738-122">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="3f738-122">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="3f738-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3f738-123">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="3f738-124">Subject</span><span class="sxs-lookup"><span data-stu-id="3f738-124">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="3f738-125">Body</span><span class="sxs-lookup"><span data-stu-id="3f738-125">Body</span></span>](body.md)
    
- [<span data-ttu-id="3f738-126">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="3f738-126">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="3f738-127">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="3f738-127">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="3f738-128">Start</span><span class="sxs-lookup"><span data-stu-id="3f738-128">Start</span></span>](start.md)
    
- [<span data-ttu-id="3f738-129">End</span><span class="sxs-lookup"><span data-stu-id="3f738-129">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3f738-130">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="3f738-130">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="3f738-131">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="3f738-131">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="3f738-132">Location</span><span class="sxs-lookup"><span data-stu-id="3f738-132">Location</span></span>](location.md)
    
- [<span data-ttu-id="3f738-133">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="3f738-133">RequiredAttendees</span></span>](requiredattendees.md)
    
- [<span data-ttu-id="3f738-134">Attendee</span><span class="sxs-lookup"><span data-stu-id="3f738-134">Attendee</span></span>](attendee.md)
    
- [<span data-ttu-id="3f738-135">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="3f738-135">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="3f738-136">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="3f738-136">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-createitem-calendar-item-response"></a><span data-ttu-id="3f738-137">Respuesta correcta CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="3f738-137">Successful CreateItem (Calendar Item) Response</span></span>

### <a name="description"></a><span data-ttu-id="3f738-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f738-138">Description</span></span>

<span data-ttu-id="3f738-139">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateItem.</span><span class="sxs-lookup"><span data-stu-id="3f738-139">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="3f738-140">Código</span><span class="sxs-lookup"><span data-stu-id="3f738-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="3f738-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f738-141">Comments</span></span>

<span data-ttu-id="3f738-142">Los atributos del elemento [ItemId](itemid.md) **identificador** y **ChangeKey** se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="3f738-142">The [ItemId](itemid.md) element **Id** and **ChangeKey** attributes have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="3f738-143">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="3f738-143">Successful response elements</span></span>

<span data-ttu-id="3f738-144">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="3f738-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3f738-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3f738-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3f738-146">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="3f738-146">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="3f738-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3f738-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3f738-148">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3f738-148">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="3f738-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3f738-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3f738-150">Items</span><span class="sxs-lookup"><span data-stu-id="3f738-150">Items</span></span>](items.md)
    
- [<span data-ttu-id="3f738-151">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3f738-151">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="3f738-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="3f738-152">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="3f738-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f738-153">See also</span></span>



[<span data-ttu-id="3f738-154">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="3f738-154">CreateItem operation</span></span>](createitem-operation.md)


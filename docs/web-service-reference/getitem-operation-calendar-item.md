---
title: Operación GetItem (elemento de calendario)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8
description: La operación GetItem obtiene los elementos de calendario del almacén de Exchange.
ms.openlocfilehash: 09fe92af12f03ce4cebd1e98f4e01c087ace64f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460620"
---
# <a name="getitem-operation-calendar-item"></a><span data-ttu-id="d36eb-103">Operación GetItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="d36eb-103">GetItem operation (calendar item)</span></span>

<span data-ttu-id="d36eb-104">La operación GetItem obtiene los elementos de calendario del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d36eb-104">The GetItem operation gets calendar items from the Exchange store.</span></span>
  
## <a name="getitem-request-example"></a><span data-ttu-id="d36eb-105">Ejemplo de solicitud GetItem</span><span class="sxs-lookup"><span data-stu-id="d36eb-105">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="d36eb-106">Description</span><span class="sxs-lookup"><span data-stu-id="d36eb-106">Description</span></span>

<span data-ttu-id="d36eb-107">El siguiente ejemplo de una solicitud GetItem muestra cómo crear una solicitud para obtener la identidad y el asunto de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d36eb-107">The following example of a GetItem request shows how to form a request to get the identity and subject of an item.</span></span>
  
### <a name="code"></a><span data-ttu-id="d36eb-108">Código</span><span class="sxs-lookup"><span data-stu-id="d36eb-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AsdD89=" ChangeKey="Jajs3=="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="d36eb-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="d36eb-109">Request elements</span></span>

<span data-ttu-id="d36eb-110">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="d36eb-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d36eb-111">GetItem</span><span class="sxs-lookup"><span data-stu-id="d36eb-111">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="d36eb-112">ItemShape</span><span class="sxs-lookup"><span data-stu-id="d36eb-112">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="d36eb-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="d36eb-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="d36eb-114">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="d36eb-114">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="d36eb-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="d36eb-115">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="d36eb-116">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d36eb-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="d36eb-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="d36eb-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="d36eb-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d36eb-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="d36eb-119">Para buscar otras opciones para el mensaje de solicitud de la operación GetItem, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="d36eb-119">To find other options for the request message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="d36eb-120">Comienza en el elemento [GetItem](getitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d36eb-120">Start at the [GetItem](getitem.md) element.</span></span> 
  
## <a name="successful-getitem-response"></a><span data-ttu-id="d36eb-121">Respuesta GetItem correcta</span><span class="sxs-lookup"><span data-stu-id="d36eb-121">Successful GetItem Response</span></span>

### <a name="description"></a><span data-ttu-id="d36eb-122">Description</span><span class="sxs-lookup"><span data-stu-id="d36eb-122">Description</span></span>

<span data-ttu-id="d36eb-123">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud GetItem.</span><span class="sxs-lookup"><span data-stu-id="d36eb-123">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="d36eb-124">La solicitud que creó esta respuesta usó la IdOnly baseshape.</span><span class="sxs-lookup"><span data-stu-id="d36eb-124">The request that created this response used the IdOnly baseshape.</span></span> <span data-ttu-id="d36eb-125">En este ejemplo, la respuesta devuelve solo el identificador del elemento.</span><span class="sxs-lookup"><span data-stu-id="d36eb-125">In this example, the response returns only the ID of the item.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d36eb-126">El identificador de elemento y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d36eb-126">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d36eb-127">Código</span><span class="sxs-lookup"><span data-stu-id="d36eb-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAd" ChangeKey="otlIqB=="/>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="description"></a><span data-ttu-id="d36eb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d36eb-128">Description</span></span>

<span data-ttu-id="d36eb-129">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud GetItem.</span><span class="sxs-lookup"><span data-stu-id="d36eb-129">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="d36eb-130">La solicitud que creó esta respuesta usó el valor predeterminado de baseshape.</span><span class="sxs-lookup"><span data-stu-id="d36eb-130">The request that created this response used the Default baseshape.</span></span> <span data-ttu-id="d36eb-131">En este ejemplo, la respuesta devuelve la forma predeterminada para un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="d36eb-131">In this example, the response returns the Default shape for a calendar item.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d36eb-132">El identificador de elemento y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d36eb-132">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d36eb-133">Código</span><span class="sxs-lookup"><span data-stu-id="d36eb-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAdTB" ChangeKey="otlIqBwrt=="/>
              <t:ResponseObjects>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2006-06-16T00:30:00Z</t:Start>
              <t:End>2006-06-16T01:00:00Z</t:End>
              <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
              <t:CalendarItemType>Single</t:CalendarItemType>
              <t:Organizer>
                <t:Mailbox>
                  <t:Name>Bob</t:Name>
                  <t:EmailAddress>someone@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:Organizer>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="description"></a><span data-ttu-id="d36eb-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="d36eb-134">Description</span></span>

<span data-ttu-id="d36eb-135">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud GetItem.</span><span class="sxs-lookup"><span data-stu-id="d36eb-135">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="d36eb-136">La solicitud que creó esta respuesta usó la AllProperties baseshape.</span><span class="sxs-lookup"><span data-stu-id="d36eb-136">The request that created this response used the AllProperties baseshape.</span></span> <span data-ttu-id="d36eb-137">En este ejemplo, la respuesta devuelve la forma AllProperties para un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="d36eb-137">In this example, the response returns the AllProperties shape for a calendar item.</span></span>
  
### <a name="code"></a><span data-ttu-id="d36eb-138">Código</span><span class="sxs-lookup"><span data-stu-id="d36eb-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAdT" ChangeKey="otlIqB=="/>
              <t:ParentFolderId Id="ASUAdT=="/>
              <t:ItemClass>IPM.Appointment</t:ItemClass>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text"/>
              <t:DateTimeReceived>2006-06-16T00:12:41Z</t:DateTimeReceived>
              <t:Size>374</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>false</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-06-16T00:12:41Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-06-16T00:12:41Z</t:DateTimeCreated>
              <t:ResponseObjects>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:ReminderDueBy>2006-06-16T00:30:00Z</t:ReminderDueBy>
              <t:ReminderIsSet>true</t:ReminderIsSet>
              <t:ReminderMinutesBeforeStart>15</t:ReminderMinutesBeforeStart>
              <t:DisplayCc/>
              <t:DisplayTo/>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en-US</t:Culture>
              <t:Start>2006-06-16T00:30:00Z</t:Start>
              <t:End>2006-06-16T01:00:00Z</t:End>
              <t:IsAllDayEvent>false</t:IsAllDayEvent>
              <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
              <t:IsMeeting>false</t:IsMeeting>
              <t:IsCancelled>false</t:IsCancelled>
              <t:IsRecurring>false</t:IsRecurring>
              <t:MeetingRequestWasSent>false</t:MeetingRequestWasSent>
              <t:CalendarItemType>Single</t:CalendarItemType>
              <t:MyResponseType>Organizer</t:MyResponseType>
              <t:Organizer>
                <t:Mailbox>
                  <t:Name>Bob</t:Name>
                  <t:EmailAddress>someone@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:Organizer>
              <t:ConflictingMeetingCount>2</t:ConflictingMeetingCount>
              <t:AdjacentMeetingCount>0</t:AdjacentMeetingCount>
              <t:ConflictingMeetings>
                <t:CalendarItem>
                  <t:ItemId Id="ASUAdTB" ChangeKey="otlIqBwr=="/>
                  <t:Subject/>
                  <t:Start>2006-06-16T00:30:00Z</t:Start>
                  <t:End>2006-06-16T01:00:00Z</t:End>
                  <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
                  <t:Location/>
                </t:CalendarItem>
                <t:CalendarItem>
                  <t:ItemId Id="ASUAd" ChangeKey="otlIqBw=="/>
                  <t:Subject/>
                  <t:Start>2006-06-16T00:30:00Z</t:Start>
                  <t:End>2006-06-16T01:00:00Z</t:End>
                  <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
                  <t:Location/>
                </t:CalendarItem>
              </t:ConflictingMeetings>
              <t:Duration>PT30M</t:Duration>
              <t:TimeZone>Pacific Standard Time</t:TimeZone>
              <t:AppointmentSequenceNumber>0</t:AppointmentSequenceNumber>
              <t:AppointmentState>0</t:AppointmentState>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="d36eb-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d36eb-139">Comments</span></span>

<span data-ttu-id="d36eb-140">Para buscar otras opciones para el mensaje de respuesta de la operación GetItem, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="d36eb-140">To find other options for the response message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="d36eb-141">Empiece en el elemento [GetItemResponse](getitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="d36eb-141">Start at the [GetItemResponse](getitemresponse.md) element.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="d36eb-142">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="d36eb-142">Successful response elements</span></span>

<span data-ttu-id="d36eb-143">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d36eb-143">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d36eb-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d36eb-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d36eb-145">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="d36eb-145">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="d36eb-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d36eb-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d36eb-147">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d36eb-147">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="d36eb-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d36eb-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d36eb-149">Items</span><span class="sxs-lookup"><span data-stu-id="d36eb-149">Items</span></span>](items.md)
    
- [<span data-ttu-id="d36eb-150">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d36eb-150">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="d36eb-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="d36eb-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="d36eb-152">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="d36eb-152">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="d36eb-153">ItemClass</span><span class="sxs-lookup"><span data-stu-id="d36eb-153">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="d36eb-154">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="d36eb-154">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="d36eb-155">Body</span><span class="sxs-lookup"><span data-stu-id="d36eb-155">Body</span></span>](body.md)
    
- [<span data-ttu-id="d36eb-156">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="d36eb-156">DateTimeReceived</span></span>](datetimereceived.md)
    
- [<span data-ttu-id="d36eb-157">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d36eb-157">Size</span></span>](size.md)
    
- [<span data-ttu-id="d36eb-158">Importance</span><span class="sxs-lookup"><span data-stu-id="d36eb-158">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="d36eb-159">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="d36eb-159">IsSubmitted</span></span>](issubmitted.md)
    
- [<span data-ttu-id="d36eb-160">IsDraft</span><span class="sxs-lookup"><span data-stu-id="d36eb-160">IsDraft</span></span>](isdraft.md)
    
- [<span data-ttu-id="d36eb-161">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="d36eb-161">IsFromMe</span></span>](isfromme.md)
    
- [<span data-ttu-id="d36eb-162">IsResend</span><span class="sxs-lookup"><span data-stu-id="d36eb-162">IsResend</span></span>](isresend.md)
    
- [<span data-ttu-id="d36eb-163">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="d36eb-163">IsUnmodified</span></span>](isunmodified.md)
    
- [<span data-ttu-id="d36eb-164">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="d36eb-164">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="d36eb-165">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="d36eb-165">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="d36eb-166">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d36eb-166">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="d36eb-167">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="d36eb-167">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="d36eb-168">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="d36eb-168">ReminderDueBy</span></span>](reminderdueby.md)
    
- [<span data-ttu-id="d36eb-169">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="d36eb-169">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="d36eb-170">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="d36eb-170">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="d36eb-171">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="d36eb-171">DisplayCc</span></span>](displaycc.md)
    
- [<span data-ttu-id="d36eb-172">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="d36eb-172">DisplayTo</span></span>](displayto.md)
    
- [<span data-ttu-id="d36eb-173">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d36eb-173">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="d36eb-174">Culture</span><span class="sxs-lookup"><span data-stu-id="d36eb-174">Culture</span></span>](culture.md)
    
- [<span data-ttu-id="d36eb-175">Start</span><span class="sxs-lookup"><span data-stu-id="d36eb-175">Start</span></span>](start.md)
    
- [<span data-ttu-id="d36eb-176">Centraliza</span><span class="sxs-lookup"><span data-stu-id="d36eb-176">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d36eb-177">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="d36eb-177">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="d36eb-178">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="d36eb-178">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="d36eb-179">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="d36eb-179">IsMeeting</span></span>](ismeeting.md)
    
- [<span data-ttu-id="d36eb-180">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="d36eb-180">IsCancelled</span></span>](iscancelled.md)
    
- [<span data-ttu-id="d36eb-181">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="d36eb-181">IsRecurring</span></span>](isrecurring.md)
    
- [<span data-ttu-id="d36eb-182">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="d36eb-182">MeetingRequestWasSent</span></span>](meetingrequestwassent.md)
    
- [<span data-ttu-id="d36eb-183">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="d36eb-183">CalendarItemType</span></span>](calendaritemtype.md)
    
- [<span data-ttu-id="d36eb-184">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="d36eb-184">MyResponseType</span></span>](myresponsetype.md)
    
- [<span data-ttu-id="d36eb-185">Organizador</span><span class="sxs-lookup"><span data-stu-id="d36eb-185">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="d36eb-186">Buzón</span><span class="sxs-lookup"><span data-stu-id="d36eb-186">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="d36eb-187">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d36eb-187">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="d36eb-188">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d36eb-188">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="d36eb-189">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d36eb-189">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="d36eb-190">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="d36eb-190">ConflictingMeetingCount</span></span>](conflictingmeetingcount.md)
    
- [<span data-ttu-id="d36eb-191">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="d36eb-191">AdjacentMeetingCount</span></span>](adjacentmeetingcount.md)
    
- [<span data-ttu-id="d36eb-192">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d36eb-192">ConflictingMeetings</span></span>](conflictingmeetings.md)
    
- [<span data-ttu-id="d36eb-193">Ubicación</span><span class="sxs-lookup"><span data-stu-id="d36eb-193">Location</span></span>](location.md)
    
- [<span data-ttu-id="d36eb-194">Duración (elementos)</span><span class="sxs-lookup"><span data-stu-id="d36eb-194">Duration (Items)</span></span>](duration-items.md)
    
- [<span data-ttu-id="d36eb-195">TimeZone (elemento)</span><span class="sxs-lookup"><span data-stu-id="d36eb-195">TimeZone (Item)</span></span>](timezone-item.md)
    
- [<span data-ttu-id="d36eb-196">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="d36eb-196">AppointmentSequenceNumber</span></span>](appointmentsequencenumber.md)
    
- [<span data-ttu-id="d36eb-197">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="d36eb-197">AppointmentState</span></span>](appointmentstate.md)
    
## <a name="see-also"></a><span data-ttu-id="d36eb-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="d36eb-198">See also</span></span>



[<span data-ttu-id="d36eb-199">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="d36eb-199">GetItem operation</span></span>](getitem-operation.md)


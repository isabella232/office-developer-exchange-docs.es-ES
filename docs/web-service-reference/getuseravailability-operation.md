---
title: Operación GetUserAvailability
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailability
api_type:
- schema
ms.assetid: 8da17226-5d3a-4525-9ffa-d83730f47bb1
description: Buscar información sobre la operación de EWS de GetUserAvailability.
ms.openlocfilehash: b6d03c7da65e3f30f093b7e41448abcca2330a84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458225"
---
# <a name="getuseravailability-operation"></a><span data-ttu-id="c0f96-103">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c0f96-103">GetUserAvailability operation</span></span>

<span data-ttu-id="c0f96-104">Buscar información sobre la operación de EWS de **GetUserAvailability** .</span><span class="sxs-lookup"><span data-stu-id="c0f96-104">Find information about the **GetUserAvailability** EWS operation.</span></span> 
  
<span data-ttu-id="c0f96-105">La operación **GetUserAvailability** proporciona información detallada sobre la disponibilidad de un conjunto de usuarios, salones y recursos en un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="c0f96-105">The **GetUserAvailability** operation provides detailed information about the availability of a set of users, rooms, and resources within a specified time period.</span></span> 
  
## <a name="using-the-getuseravailability-operation"></a><span data-ttu-id="c0f96-106">Uso de la operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c0f96-106">Using the GetUserAvailability operation</span></span>

<span data-ttu-id="c0f96-107">La operación **GetUserAvailability** proporciona información actual sobre la disponibilidad del usuario en un nivel de detalle especificado.</span><span class="sxs-lookup"><span data-stu-id="c0f96-107">The **GetUserAvailability** operation provides current user availability information at a specified level of detail.</span></span> <span data-ttu-id="c0f96-108">Las aplicaciones cliente como Outlook, Outlook Web Access, Outlook Mobile Access y otras usan direcciones SMTP para identificar la información de usuario solicitada.</span><span class="sxs-lookup"><span data-stu-id="c0f96-108">Client applications such as Outlook, Outlook Web Access, Outlook Mobile Access, and others use SMTP addresses to identify the requested user information.</span></span> 
  
<span data-ttu-id="c0f96-109">El servicio de disponibilidad expande las listas de distribución para recuperar el estado de disponibilidad de cada miembro de la lista, siempre que el número de buzones de la lista de distribución sea inferior a 100, que es el número máximo de identidades que la operación **GetUserAvailability** puede solicitar.</span><span class="sxs-lookup"><span data-stu-id="c0f96-109">The Availability service expands distribution lists to retrieve the free/busy status for each member of the list, as long as the number of mailboxes in the distribution list is less than 100, which is the maximum number of identities that the **GetUserAvailability** operation can request.</span></span> <span data-ttu-id="c0f96-110">Los Estados de disponibilidad de los miembros de la lista de distribución se combinan en un solo Estado de disponibilidad para toda la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="c0f96-110">The free/busy statuses of the members of the distribution list are merged into a single free/busy status for the whole distribution list.</span></span> 
  
<span data-ttu-id="c0f96-111">Las solicitudes de aplicación de cliente especifican el período de tiempo de la consulta de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="c0f96-111">Client application requests specify the time period of the availability query.</span></span> <span data-ttu-id="c0f96-112">El período de tiempo predeterminado para la información solicitada es de 42 días.</span><span class="sxs-lookup"><span data-stu-id="c0f96-112">The default time period for the requested information is 42 days.</span></span> <span data-ttu-id="c0f96-113">Si el calendario del usuario contiene citas o reuniones que están dentro y fuera del período de tiempo definido para la consulta, se devuelve la cita.</span><span class="sxs-lookup"><span data-stu-id="c0f96-113">If the user's calendar contains appointments or meetings that are both within and outside the defined time period for the query, the appointment is returned.</span></span> 
  
<span data-ttu-id="c0f96-114">Las horas de citas y reuniones que se devuelven se encuentran en la misma zona horaria que la aplicación cliente que solicita la reunión.</span><span class="sxs-lookup"><span data-stu-id="c0f96-114">The appointment and meeting times that are returned are in the same time zone as the client application that is requesting the meeting.</span></span>
  
<span data-ttu-id="c0f96-115">El servicio de disponibilidad procesa la solicitud para cada cliente.</span><span class="sxs-lookup"><span data-stu-id="c0f96-115">The Availability service processes the request for each client.</span></span> <span data-ttu-id="c0f96-116">El servicio expande todas las citas periódicas y devuelve el número máximo de detalles del calendario que el cliente solicitante tiene permiso para recibir.</span><span class="sxs-lookup"><span data-stu-id="c0f96-116">The service expands all the recurring appointments and returns the maximum number of calendar details that the requesting client has permission to receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c0f96-117">Si el buzón de destino no está disponible o no se encuentra, se produce una excepción **MailRecipientNotFoundException** .</span><span class="sxs-lookup"><span data-stu-id="c0f96-117">If the target mailbox is unavailable or cannot be found, a **MailRecipientNotFoundException** exception is thrown.</span></span> <span data-ttu-id="c0f96-118">El cliente recibe un mensaje de error que indica que el destinatario de correo no se encuentra en el servicio de directorio Active Directory o en los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="c0f96-118">The client receives an error message that states that the mail recipient is not found in the Active Directory directory service or Active Directory Domain Services (AD DS).</span></span> 
  
### <a name="getuseravailability-operation-soap-headers"></a><span data-ttu-id="c0f96-119">Encabezados SOAP de operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c0f96-119">GetUserAvailability operation SOAP headers</span></span>

<span data-ttu-id="c0f96-120">La operación **GetUserAvailability** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0f96-120">The **GetUserAvailability** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c0f96-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="c0f96-121">**Header**</span></span>|<span data-ttu-id="c0f96-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c0f96-122">**Element**</span></span>|<span data-ttu-id="c0f96-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0f96-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0f96-124">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="c0f96-124">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c0f96-125">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c0f96-125">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c0f96-126">Identifica al usuario que el cliente está suplantando.</span><span class="sxs-lookup"><span data-stu-id="c0f96-126">Identifies the user whom the client is impersonating.</span></span> <span data-ttu-id="c0f96-127">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0f96-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c0f96-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c0f96-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c0f96-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c0f96-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c0f96-130">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="c0f96-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c0f96-131">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0f96-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c0f96-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c0f96-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c0f96-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c0f96-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c0f96-134">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0f96-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c0f96-135">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0f96-135">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="c0f96-136">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="c0f96-136">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="c0f96-137">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c0f96-137">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="c0f96-138">Especifica un encabezado SOAP que identifica la zona horaria que se va a usar para todas las respuestas del servidor.</span><span class="sxs-lookup"><span data-stu-id="c0f96-138">Specifies a SOAP header that identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="c0f96-139">Todas las horas que se devuelven del servidor se convertirán en la zona horaria especificada.</span><span class="sxs-lookup"><span data-stu-id="c0f96-139">All times that are returned from the server will be converted to the specified time zone.</span></span> <span data-ttu-id="c0f96-140">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0f96-140">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a><span data-ttu-id="c0f96-141">Ejemplo de solicitud GetUserAvailability: obtener información de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="c0f96-141">GetUserAvailability request example: Get availability information</span></span>

<span data-ttu-id="c0f96-142">El siguiente ejemplo de una solicitud de operación de **GetUserAvailability** muestra cómo obtener información detallada de disponibilidad para dos usuarios en la zona horaria del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="c0f96-142">The following example of a **GetUserAvailability** operation request shows how to get detailed availability information for two users in the Pacific Time time zone.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <t:TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Bias>480</Bias>
        <StandardTime>
          <Bias>0</Bias>
          <Time>02:00:00</Time>
          <DayOrder>5</DayOrder>
          <Month>10</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </StandardTime>
        <DaylightTime>
          <Bias>-60</Bias>
          <Time>02:00:00</Time>
          <DayOrder>1</DayOrder>
          <Month>4</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </DaylightTime>
      </t:TimeZone>
      <MailboxDataArray>
        <t:MailboxData>
          <t:Email>
            <t:Address>user1@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
        <t:MailboxData>
          <t:Email>
            <t:Address>user2@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
      </MailboxDataArray>
      <t:FreeBusyViewOptions>
        <t:TimeWindow>
          <t:StartTime>2006-10-16T00:00:00</t:StartTime>
          <t:EndTime>2006-10-16T23:59:59</t:EndTime>
        </t:TimeWindow>
        <t:MergedFreeBusyIntervalInMinutes>60</t:MergedFreeBusyIntervalInMinutes>
        <t:RequestedView>DetailedMerged</t:RequestedView>
      </t:FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c0f96-143">Para obtener más información sobre cómo recuperar reuniones sugeridas mediante el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) , vea el esquema en el directorio virtual EWS.</span><span class="sxs-lookup"><span data-stu-id="c0f96-143">For more information about retrieving suggested meetings by using the [SuggestionsViewOptions](suggestionsviewoptions.md) element, see the schema in the EWS virtual directory.</span></span> 
  
<span data-ttu-id="c0f96-144">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c0f96-144">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c0f96-145">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="c0f96-145">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
    
- [<span data-ttu-id="c0f96-146">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="c0f96-146">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="c0f96-147">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="c0f96-147">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="c0f96-148">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="c0f96-148">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="c0f96-149">Sesgo</span><span class="sxs-lookup"><span data-stu-id="c0f96-149">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="c0f96-150">Time</span><span class="sxs-lookup"><span data-stu-id="c0f96-150">Time</span></span>](time.md)
    
- [<span data-ttu-id="c0f96-151">DayOrder</span><span class="sxs-lookup"><span data-stu-id="c0f96-151">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="c0f96-152">Month</span><span class="sxs-lookup"><span data-stu-id="c0f96-152">Month</span></span>](month.md)
    
- [<span data-ttu-id="c0f96-153">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="c0f96-153">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="c0f96-154">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="c0f96-154">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="c0f96-155">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="c0f96-155">MailboxDataArray</span></span>](mailboxdataarray.md)
    
- [<span data-ttu-id="c0f96-156">MailboxData</span><span class="sxs-lookup"><span data-stu-id="c0f96-156">MailboxData</span></span>](mailboxdata.md)
    
- [<span data-ttu-id="c0f96-157">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c0f96-157">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
    
- [<span data-ttu-id="c0f96-158">Address (cadena)</span><span class="sxs-lookup"><span data-stu-id="c0f96-158">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="c0f96-159">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="c0f96-159">AttendeeType</span></span>](attendeetype.md)
    
- [<span data-ttu-id="c0f96-160">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="c0f96-160">ExcludeConflicts</span></span>](excludeconflicts.md)
    
- [<span data-ttu-id="c0f96-161">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="c0f96-161">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
    
- [<span data-ttu-id="c0f96-162">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="c0f96-162">TimeWindow</span></span>](timewindow.md)
    
- [<span data-ttu-id="c0f96-163">StartTime</span><span class="sxs-lookup"><span data-stu-id="c0f96-163">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="c0f96-164">EndTime</span><span class="sxs-lookup"><span data-stu-id="c0f96-164">EndTime</span></span>](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a><span data-ttu-id="c0f96-165">Respuesta de operación GetUserAvailability correcta</span><span class="sxs-lookup"><span data-stu-id="c0f96-165">Successful GetUserAvailability operation response</span></span>

<span data-ttu-id="c0f96-166">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de operación **GetUserAvailability** .</span><span class="sxs-lookup"><span data-stu-id="c0f96-166">The following example shows a successful response to the **GetUserAvailability** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c0f96-167">Los identificadores de eventos de calendario se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c0f96-167">The calendar event identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="665" MinorBuildNumber="7" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserAvailabilityResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FreeBusyResponseArray>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">DetailedMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000002220220000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T06:00:00-07:00</StartTime>
                <EndTime>2006-10-16T06:30:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0</ID>
                  <Subject>Meet with Contoso Account Executives</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T07:00:00-07:00</StartTime>
                <EndTime>2006-10-16T08:00:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>E14B6414B0B</ID>
                  <Subject>Pick up my groceries</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T09:40:00-07:00</StartTime>
                <EndTime>2006-10-16T10:10:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0B1</ID>
                  <Subject>Meet with doctor</Subject>
                  <Location>Kirkland</Location>
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
                <Bias>480</Bias>
                <StandardTime>
                  <Bias>0</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>5</DayOrder>
                  <Month>10</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </StandardTime>
                <DaylightTime>
                  <Bias>-60</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>1</DayOrder>
                  <Month>4</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </DaylightTime>
              </TimeZone>
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">FreeBusyMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000000001100000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T09:00:00-07:00</StartTime>
                <EndTime>2006-10-16T10:00:00-07:00</EndTime>
                <BusyType>Tentative</BusyType>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
                <Bias>480</Bias>
                <StandardTime>
                  <Bias>0</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>5</DayOrder>
                  <Month>10</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </StandardTime>
                <DaylightTime>
                  <Bias>-60</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>1</DayOrder>
                  <Month>4</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </DaylightTime>
              </TimeZone>
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
      </FreeBusyResponseArray>
    </GetUserAvailabilityResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c0f96-168">La información de disponibilidad de cada usuario aparece en un elemento [FreeBusyResponse](freebusyresponse.md) único.</span><span class="sxs-lookup"><span data-stu-id="c0f96-168">The availability information for each user appears in a unique [FreeBusyResponse](freebusyresponse.md) element.</span></span> <span data-ttu-id="c0f96-169">El orden de los usuarios en la solicitud de operación **GetUserAvailability** determina el orden de los datos de disponibilidad para cada usuario en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0f96-169">The order of users in the **GetUserAvailability** operation request determines the order of availability data for each user in the response.</span></span> 
  
<span data-ttu-id="c0f96-170">Se devolverá un error al cliente si el número de citas en el período de tiempo definido en la consulta es mayor que el número máximo especificado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="c0f96-170">An error will be returned to the client if the number of appointments in the time period that is defined in the query is greater than the administrator-specified maximum number.</span></span> <span data-ttu-id="c0f96-171">El número máximo predeterminado de citas es 10.000 instancias únicas y elementos de periodicidad ampliada.</span><span class="sxs-lookup"><span data-stu-id="c0f96-171">The default maximum number of appointments is 10,000 single instances and expanded recurrence items.</span></span> <span data-ttu-id="c0f96-172">Solo un administrador puede configurar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c0f96-172">This property can be configured only by an administrator.</span></span>
  
<span data-ttu-id="c0f96-173">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c0f96-173">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c0f96-174">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c0f96-174">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c0f96-175">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c0f96-175">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
    
- [<span data-ttu-id="c0f96-176">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="c0f96-176">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
    
- [<span data-ttu-id="c0f96-177">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="c0f96-177">FreeBusyResponse</span></span>](freebusyresponse.md)
    
- [<span data-ttu-id="c0f96-178">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c0f96-178">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="c0f96-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c0f96-179">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c0f96-180">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="c0f96-180">FreeBusyView</span></span>](freebusyview.md)
    
- [<span data-ttu-id="c0f96-181">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="c0f96-181">FreeBusyViewType</span></span>](freebusyviewtype.md)
    
- [<span data-ttu-id="c0f96-182">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="c0f96-182">MergedFreeBusy</span></span>](mergedfreebusy.md)
    
- [<span data-ttu-id="c0f96-183">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="c0f96-183">CalendarEventArray</span></span>](calendareventarray.md)
    
- [<span data-ttu-id="c0f96-184">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="c0f96-184">CalendarEvent</span></span>](calendarevent.md)
    
- [<span data-ttu-id="c0f96-185">StartTime</span><span class="sxs-lookup"><span data-stu-id="c0f96-185">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="c0f96-186">EndTime</span><span class="sxs-lookup"><span data-stu-id="c0f96-186">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="c0f96-187">BusyType</span><span class="sxs-lookup"><span data-stu-id="c0f96-187">BusyType</span></span>](busytype.md)
    
- [<span data-ttu-id="c0f96-188">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="c0f96-188">CalendarEventDetails</span></span>](calendareventdetails.md)
    
- [<span data-ttu-id="c0f96-189">Id.</span><span class="sxs-lookup"><span data-stu-id="c0f96-189">ID</span></span>](id.md)
    
- [<span data-ttu-id="c0f96-190">Asunto (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c0f96-190">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md)
    
- [<span data-ttu-id="c0f96-191">Ubicación (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c0f96-191">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
    
- [<span data-ttu-id="c0f96-192">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c0f96-192">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
    
- [<span data-ttu-id="c0f96-193">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c0f96-193">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
    
- [<span data-ttu-id="c0f96-194">IsException</span><span class="sxs-lookup"><span data-stu-id="c0f96-194">IsException</span></span>](isexception.md)
    
- [<span data-ttu-id="c0f96-195">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="c0f96-195">IsReminderSet</span></span>](isreminderset.md)
    
- [<span data-ttu-id="c0f96-196">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="c0f96-196">IsPrivate</span></span>](isprivate.md)
    
- [<span data-ttu-id="c0f96-197">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="c0f96-197">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c0f96-198">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="c0f96-198">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="c0f96-199">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="c0f96-199">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="c0f96-200">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="c0f96-200">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="c0f96-201">Sesgo</span><span class="sxs-lookup"><span data-stu-id="c0f96-201">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="c0f96-202">Time</span><span class="sxs-lookup"><span data-stu-id="c0f96-202">Time</span></span>](time.md)
    
- [<span data-ttu-id="c0f96-203">DayOrder</span><span class="sxs-lookup"><span data-stu-id="c0f96-203">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="c0f96-204">Month</span><span class="sxs-lookup"><span data-stu-id="c0f96-204">Month</span></span>](month.md)
    
- [<span data-ttu-id="c0f96-205">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="c0f96-205">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="c0f96-206">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="c0f96-206">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="c0f96-207">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="c0f96-207">WorkingPeriodArray</span></span>](workingperiodarray.md)
    
- [<span data-ttu-id="c0f96-208">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="c0f96-208">WorkingPeriod</span></span>](workingperiod.md)
    
- [<span data-ttu-id="c0f96-209">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="c0f96-209">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
    
- [<span data-ttu-id="c0f96-210">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="c0f96-210">StartTimeInMinutes</span></span>](starttimeinminutes.md)
    
- [<span data-ttu-id="c0f96-211">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="c0f96-211">EndTimeInMinutes</span></span>](endtimeinminutes.md)
    
## <a name="see-also"></a><span data-ttu-id="c0f96-212">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0f96-212">See also</span></span>

- [<span data-ttu-id="c0f96-213">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c0f96-213">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="c0f96-214">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="c0f96-214">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    


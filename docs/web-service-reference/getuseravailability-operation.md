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
description: Busque información sobre la EWS GetUserAvailability operación.
ms.openlocfilehash: 41246fe22bfb7444cd4aa7b1d4651d475dd9231c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835686"
---
# <a name="getuseravailability-operation"></a><span data-ttu-id="f2141-103">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f2141-103">GetUserAvailability operation</span></span>

<span data-ttu-id="f2141-104">Obtenga información acerca de la operación de EWS **GetUserAvailability** .</span><span class="sxs-lookup"><span data-stu-id="f2141-104">Find information about the **GetUserAvailability** EWS operation.</span></span> 
  
<span data-ttu-id="f2141-105">La operación **GetUserAvailability** proporciona información detallada acerca de la disponibilidad de un conjunto de usuarios, salones y recursos dentro de un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="f2141-105">The **GetUserAvailability** operation provides detailed information about the availability of a set of users, rooms, and resources within a specified time period.</span></span> 
  
## <a name="using-the-getuseravailability-operation"></a><span data-ttu-id="f2141-106">Mediante la operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f2141-106">Using the GetUserAvailability operation</span></span>

<span data-ttu-id="f2141-107">La operación **GetUserAvailability** proporciona información de disponibilidad del usuario actual en un nivel de detalle especificado.</span><span class="sxs-lookup"><span data-stu-id="f2141-107">The **GetUserAvailability** operation provides current user availability information at a specified level of detail.</span></span> <span data-ttu-id="f2141-108">Las aplicaciones de cliente, como Outlook, Outlook Web Access, Outlook Mobile Access y otras usan direcciones SMTP para identificar la información del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="f2141-108">Client applications such as Outlook, Outlook Web Access, Outlook Mobile Access, and others use SMTP addresses to identify the requested user information.</span></span> 
  
<span data-ttu-id="f2141-109">El servicio de disponibilidad expande listas de distribución para recuperar el estado de disponibilidad para cada miembro de la lista, como el número de buzones de correo en la lista de distribución es menor que 100, que es el número máximo de identidades que la **GetUserAvailability **operación puede solicitar.</span><span class="sxs-lookup"><span data-stu-id="f2141-109">The Availability service expands distribution lists to retrieve the free/busy status for each member of the list, as long as the number of mailboxes in the distribution list is less than 100, which is the maximum number of identities that the **GetUserAvailability** operation can request.</span></span> <span data-ttu-id="f2141-110">Los Estados de libre/ocupado de los miembros de la lista de distribución se combinan en un único estado libre/ocupado para la lista de distribución completa.</span><span class="sxs-lookup"><span data-stu-id="f2141-110">The free/busy statuses of the members of the distribution list are merged into a single free/busy status for the whole distribution list.</span></span> 
  
<span data-ttu-id="f2141-111">Las solicitudes de aplicación de cliente especifican el período de tiempo de la consulta de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="f2141-111">Client application requests specify the time period of the availability query.</span></span> <span data-ttu-id="f2141-112">El valor predeterminado de período de tiempo para la información solicitada es 42 días.</span><span class="sxs-lookup"><span data-stu-id="f2141-112">The default time period for the requested information is 42 days.</span></span> <span data-ttu-id="f2141-113">Si el calendario del usuario contiene las citas o reuniones que están dentro y fuera del período de tiempo definido para la consulta, se devuelve la cita.</span><span class="sxs-lookup"><span data-stu-id="f2141-113">If the user's calendar contains appointments or meetings that are both within and outside the defined time period for the query, the appointment is returned.</span></span> 
  
<span data-ttu-id="f2141-114">Las horas de citas y reuniones que se devuelven están en la misma zona horaria como la aplicación cliente que está solicitando la reunión.</span><span class="sxs-lookup"><span data-stu-id="f2141-114">The appointment and meeting times that are returned are in the same time zone as the client application that is requesting the meeting.</span></span>
  
<span data-ttu-id="f2141-115">El servicio de disponibilidad procesa la solicitud para cada cliente.</span><span class="sxs-lookup"><span data-stu-id="f2141-115">The Availability service processes the request for each client.</span></span> <span data-ttu-id="f2141-116">El servicio expande todas las citas periódicas y devuelve el número máximo de detalles del calendario que el cliente solicitante tiene permiso para recibir.</span><span class="sxs-lookup"><span data-stu-id="f2141-116">The service expands all the recurring appointments and returns the maximum number of calendar details that the requesting client has permission to receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f2141-117">Si el buzón de destino no está disponible o no se encuentra, se produce una excepción **MailRecipientNotFoundException** .</span><span class="sxs-lookup"><span data-stu-id="f2141-117">If the target mailbox is unavailable or cannot be found, a **MailRecipientNotFoundException** exception is thrown.</span></span> <span data-ttu-id="f2141-118">El cliente recibe un mensaje de error que indica que el destinatario de correo no se encuentra en el servicio de directorio de Active Directory o los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f2141-118">The client receives an error message that states that the mail recipient is not found in the Active Directory directory service or Active Directory Domain Services (AD DS).</span></span> 
  
### <a name="getuseravailability-operation-soap-headers"></a><span data-ttu-id="f2141-119">Encabezados SOAP de operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f2141-119">GetUserAvailability operation SOAP headers</span></span>

<span data-ttu-id="f2141-120">La operación **GetUserAvailability** puede usar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f2141-120">The **GetUserAvailability** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f2141-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="f2141-121">**Header**</span></span>|<span data-ttu-id="f2141-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2141-122">**Element**</span></span>|<span data-ttu-id="f2141-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2141-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2141-124">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="f2141-124">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f2141-125">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f2141-125">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f2141-126">Identifica el usuario que está realizando la suplantación del cliente.</span><span class="sxs-lookup"><span data-stu-id="f2141-126">Identifies the user whom the client is impersonating.</span></span> <span data-ttu-id="f2141-127">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2141-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f2141-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f2141-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f2141-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f2141-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f2141-130">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="f2141-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f2141-131">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2141-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f2141-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f2141-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f2141-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f2141-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f2141-134">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2141-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f2141-135">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2141-135">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="f2141-136">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="f2141-136">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="f2141-137">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="f2141-137">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="f2141-138">Especifica un encabezado SOAP que identifica la zona horaria que se usará para todas las respuestas desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="f2141-138">Specifies a SOAP header that identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="f2141-139">Todas las veces que se devuelven desde el servidor se convertirán en la zona horaria especificada.</span><span class="sxs-lookup"><span data-stu-id="f2141-139">All times that are returned from the server will be converted to the specified time zone.</span></span> <span data-ttu-id="f2141-140">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2141-140">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a><span data-ttu-id="f2141-141">Ejemplo de solicitud de GetUserAvailability: obtener la información de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="f2141-141">GetUserAvailability request example: Get availability information</span></span>

<span data-ttu-id="f2141-142">El siguiente ejemplo de una solicitud de operación **GetUserAvailability** muestra cómo obtener información detallada de disponibilidad para los usuarios de dos en la zona horaria de hora del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="f2141-142">The following example of a **GetUserAvailability** operation request shows how to get detailed availability information for two users in the Pacific Time time zone.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <t:TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="f2141-143">Para obtener más información acerca de cómo recuperar las reuniones sugeridas mediante el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) , vea el esquema en el directorio virtual de EWS.</span><span class="sxs-lookup"><span data-stu-id="f2141-143">For more information about retrieving suggested meetings by using the [SuggestionsViewOptions](suggestionsviewoptions.md) element, see the schema in the EWS virtual directory.</span></span> 
  
<span data-ttu-id="f2141-144">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f2141-144">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f2141-145">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="f2141-145">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
    
- [<span data-ttu-id="f2141-146">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="f2141-146">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="f2141-147">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="f2141-147">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="f2141-148">StandardTime</span><span class="sxs-lookup"><span data-stu-id="f2141-148">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="f2141-149">Bias</span><span class="sxs-lookup"><span data-stu-id="f2141-149">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="f2141-150">Time</span><span class="sxs-lookup"><span data-stu-id="f2141-150">Time</span></span>](time.md)
    
- [<span data-ttu-id="f2141-151">DayOrder</span><span class="sxs-lookup"><span data-stu-id="f2141-151">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="f2141-152">Month</span><span class="sxs-lookup"><span data-stu-id="f2141-152">Month</span></span>](month.md)
    
- [<span data-ttu-id="f2141-153">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="f2141-153">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="f2141-154">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="f2141-154">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="f2141-155">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="f2141-155">MailboxDataArray</span></span>](mailboxdataarray.md)
    
- [<span data-ttu-id="f2141-156">MailboxData</span><span class="sxs-lookup"><span data-stu-id="f2141-156">MailboxData</span></span>](mailboxdata.md)
    
- [<span data-ttu-id="f2141-157">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f2141-157">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
    
- [<span data-ttu-id="f2141-158">Dirección (cadena)</span><span class="sxs-lookup"><span data-stu-id="f2141-158">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="f2141-159">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="f2141-159">AttendeeType</span></span>](attendeetype.md)
    
- [<span data-ttu-id="f2141-160">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="f2141-160">ExcludeConflicts</span></span>](excludeconflicts.md)
    
- [<span data-ttu-id="f2141-161">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="f2141-161">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
    
- [<span data-ttu-id="f2141-162">Ventana de tiempo</span><span class="sxs-lookup"><span data-stu-id="f2141-162">TimeWindow</span></span>](timewindow.md)
    
- [<span data-ttu-id="f2141-163">StartTime</span><span class="sxs-lookup"><span data-stu-id="f2141-163">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="f2141-164">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="f2141-164">EndTime</span></span>](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a><span data-ttu-id="f2141-165">Respuesta es correcta de operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f2141-165">Successful GetUserAvailability operation response</span></span>

<span data-ttu-id="f2141-166">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de la operación **GetUserAvailability** .</span><span class="sxs-lookup"><span data-stu-id="f2141-166">The following example shows a successful response to the **GetUserAvailability** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f2141-167">Los identificadores de eventos de calendario se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f2141-167">The calendar event identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="665" MinorBuildNumber="7" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserAvailabilityResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FreeBusyResponseArray>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">DetailedMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="http://schemas.microsoft.com/exchange/services/2006/types">000002220220000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <WorkingHours xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <FreeBusyViewType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">FreeBusyMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="http://schemas.microsoft.com/exchange/services/2006/types">000000001100000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T09:00:00-07:00</StartTime>
                <EndTime>2006-10-16T10:00:00-07:00</EndTime>
                <BusyType>Tentative</BusyType>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="f2141-168">Aparece la información de disponibilidad para cada usuario en un único elemento de [FreeBusyResponse](freebusyresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="f2141-168">The availability information for each user appears in a unique [FreeBusyResponse](freebusyresponse.md) element.</span></span> <span data-ttu-id="f2141-169">El orden de los usuarios en la solicitud de operación **GetUserAvailability** determina el orden de los datos de disponibilidad para cada usuario en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2141-169">The order of users in the **GetUserAvailability** operation request determines the order of availability data for each user in the response.</span></span> 
  
<span data-ttu-id="f2141-170">Si el número de citas en el período de tiempo que se define en la consulta es mayor que el número máximo de especificados por el administrador, se devolverá un error al cliente.</span><span class="sxs-lookup"><span data-stu-id="f2141-170">An error will be returned to the client if the number of appointments in the time period that is defined in the query is greater than the administrator-specified maximum number.</span></span> <span data-ttu-id="f2141-171">El número máximo predeterminado de citas es 10.000 instancias únicas y expande elementos de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="f2141-171">The default maximum number of appointments is 10,000 single instances and expanded recurrence items.</span></span> <span data-ttu-id="f2141-172">Esta propiedad puede configurarse únicamente por un administrador.</span><span class="sxs-lookup"><span data-stu-id="f2141-172">This property can be configured only by an administrator.</span></span>
  
<span data-ttu-id="f2141-173">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f2141-173">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="f2141-174">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f2141-174">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="f2141-175">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f2141-175">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
    
- [<span data-ttu-id="f2141-176">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="f2141-176">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
    
- [<span data-ttu-id="f2141-177">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="f2141-177">FreeBusyResponse</span></span>](freebusyresponse.md)
    
- [<span data-ttu-id="f2141-178">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f2141-178">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="f2141-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f2141-179">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f2141-180">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="f2141-180">FreeBusyView</span></span>](freebusyview.md)
    
- [<span data-ttu-id="f2141-181">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="f2141-181">FreeBusyViewType</span></span>](freebusyviewtype.md)
    
- [<span data-ttu-id="f2141-182">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="f2141-182">MergedFreeBusy</span></span>](mergedfreebusy.md)
    
- [<span data-ttu-id="f2141-183">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="f2141-183">CalendarEventArray</span></span>](calendareventarray.md)
    
- [<span data-ttu-id="f2141-184">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="f2141-184">CalendarEvent</span></span>](calendarevent.md)
    
- [<span data-ttu-id="f2141-185">StartTime</span><span class="sxs-lookup"><span data-stu-id="f2141-185">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="f2141-186">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="f2141-186">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="f2141-187">BusyType</span><span class="sxs-lookup"><span data-stu-id="f2141-187">BusyType</span></span>](busytype.md)
    
- [<span data-ttu-id="f2141-188">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="f2141-188">CalendarEventDetails</span></span>](calendareventdetails.md)
    
- [<span data-ttu-id="f2141-189">ID</span><span class="sxs-lookup"><span data-stu-id="f2141-189">ID</span></span>](id.md)
    
- [<span data-ttu-id="f2141-190">Asunto (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f2141-190">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md)
    
- [<span data-ttu-id="f2141-191">Ubicación (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f2141-191">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
    
- [<span data-ttu-id="f2141-192">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f2141-192">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
    
- [<span data-ttu-id="f2141-193">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f2141-193">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
    
- [<span data-ttu-id="f2141-194">IsException</span><span class="sxs-lookup"><span data-stu-id="f2141-194">IsException</span></span>](isexception.md)
    
- [<span data-ttu-id="f2141-195">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="f2141-195">IsReminderSet</span></span>](isreminderset.md)
    
- [<span data-ttu-id="f2141-196">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="f2141-196">IsPrivate</span></span>](isprivate.md)
    
- [<span data-ttu-id="f2141-197">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="f2141-197">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
    
- [<span data-ttu-id="f2141-198">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="f2141-198">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="f2141-199">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="f2141-199">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="f2141-200">StandardTime</span><span class="sxs-lookup"><span data-stu-id="f2141-200">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="f2141-201">Bias</span><span class="sxs-lookup"><span data-stu-id="f2141-201">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="f2141-202">Time</span><span class="sxs-lookup"><span data-stu-id="f2141-202">Time</span></span>](time.md)
    
- [<span data-ttu-id="f2141-203">DayOrder</span><span class="sxs-lookup"><span data-stu-id="f2141-203">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="f2141-204">Month</span><span class="sxs-lookup"><span data-stu-id="f2141-204">Month</span></span>](month.md)
    
- [<span data-ttu-id="f2141-205">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="f2141-205">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="f2141-206">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="f2141-206">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="f2141-207">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="f2141-207">WorkingPeriodArray</span></span>](workingperiodarray.md)
    
- [<span data-ttu-id="f2141-208">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="f2141-208">WorkingPeriod</span></span>](workingperiod.md)
    
- [<span data-ttu-id="f2141-209">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="f2141-209">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
    
- [<span data-ttu-id="f2141-210">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f2141-210">StartTimeInMinutes</span></span>](starttimeinminutes.md)
    
- [<span data-ttu-id="f2141-211">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f2141-211">EndTimeInMinutes</span></span>](endtimeinminutes.md)
    
## <a name="see-also"></a><span data-ttu-id="f2141-212">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2141-212">See also</span></span>

- [<span data-ttu-id="f2141-213">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f2141-213">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f2141-214">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="f2141-214">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    


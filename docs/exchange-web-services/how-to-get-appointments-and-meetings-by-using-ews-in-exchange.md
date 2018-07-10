---
title: Obtener las citas y reuniones con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bae582a-8cb3-4e77-be2a-7e107fad26fe
description: Obtenga información sobre cómo obtener las citas y reuniones con la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 0f5eb135142e807f30f48f01d7948fbdbf147ac2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763066"
---
# <a name="get-appointments-and-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="84b38-103">Obtener las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84b38-103">Get appointments and meetings by using EWS in Exchange</span></span>

<span data-ttu-id="84b38-104">Obtenga información sobre cómo obtener las citas y reuniones con la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="84b38-104">Learn how to get appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="84b38-105">Puede recuperar las citas y reuniones desde una carpeta Calendario mediante el método de la API administrada de EWS [CalendarFolder.FindAppointments](http://msdn.microsoft.com/es-es/library/dd636179%28v=exchg.80%29.aspx) o la operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="84b38-105">You can retrieve appointments and meetings from a calendar folder by using the [CalendarFolder.FindAppointments](http://msdn.microsoft.com/es-es/library/dd636179%28v=exchg.80%29.aspx) EWS Managed API method or the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation.</span></span> 
  
## <a name="get-appointments-by-using-the-ews-managed-api"></a><span data-ttu-id="84b38-106">Obtener las citas mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="84b38-106">Get appointments by using the EWS Managed API</span></span>
<span data-ttu-id="84b38-107"><a name="bk_retrieveappsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="84b38-107"></span></span>

<span data-ttu-id="84b38-108">En el ejemplo de código siguiente se muestra cómo usar la API administrada de EWS para recuperar las citas de un usuario que se dividen entre un inicio especificada y la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="84b38-108">The following code example shows how to use the EWS Managed API to retrieve a user's appointments that fall between a specified start and end time.</span></span>
  
```cs
       // Initialize values for the start and end times, and the number of appointments to retrieve.
            DateTime startDate = DateTime.Now;
            DateTime endDate = startDate.AddDays(30);
            const int NUM_APPTS = 5;
            // Initialize the calendar folder object with only the folder ID. 
            CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
            // Set the start and end time and number of appointments to retrieve.
            CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
            // Limit the properties returned to the appointment's subject, start time, and end time.
            cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
            // Retrieve a collection of appointments by using the calendar view.
            FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
            Console.WriteLine("\nThe first " + NUM_APPTS + " appointments on your calendar from " + startDate.Date.ToShortDateString() + 
                              " to " + endDate.Date.ToShortDateString() + " are: \n");
            
            foreach (Appointment a in appointments)
            {
                Console.Write("Subject: " + a.Subject.ToString() + " ");
                Console.Write("Start: " + a.Start.ToString() + " ");
                Console.Write("End: " + a.End.ToString());
                Console.WriteLine();
            }

```

<span data-ttu-id="84b38-109">El siguiente es el resultado del ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="84b38-109">The following is the output from the code example.</span></span>
  
<span data-ttu-id="84b38-110">Las cinco primeras citas en su calendario de 21/8/2013 a 20/9/2013 son:</span><span class="sxs-lookup"><span data-stu-id="84b38-110">The first five appointments on your calendar from 8/21/2013 to 9/20/2013 are:</span></span> 
  
<span data-ttu-id="84b38-111">Asunto: Reuniones inicio de equipo de desarrolladores de Contoso: 21/8/2013 12:30:00 P.M. final: 21/8/2013 1:00:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="84b38-111">Subject: Contoso devs team meeting Start: 8/21/2013 12:30:00 PM End: 8/21/2013 1:00:00 PM</span></span>
  
<span data-ttu-id="84b38-112">Asunto: Reunión diaria de estado Inicio: 21/8/2013 1:00:00 P.M. final: 21/8/2013 2:00:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="84b38-112">Subject: Daily status meeting Start: 8/21/2013 1:00:00 PM End: 8/21/2013 2:00:00 PM</span></span>
  
<span data-ttu-id="84b38-113">Asunto: Almuerzo con el equipo de ventas inicio: 21/8/2013 2:30:00 P.M. final: 21/8/2013 3:30:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="84b38-113">Subject: Lunch with sales team Start: 8/21/2013 2:30:00 PM End: 8/21/2013 3:30:00 PM</span></span>
  
<span data-ttu-id="84b38-114">Asunto: Tenis en el inicio de club: 22/8/2013 11:00:00 AM final: 22/8/2013 12:00:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="84b38-114">Subject: Tennis at the club Start: 8/22/2013 11:00:00 AM End: 8/22/2013 12:00:00 PM</span></span>
  
<span data-ttu-id="84b38-115">Asunto: Formación en línea difusión por Web: 22/8/2013 2:00:00 P.M. final: 22/8/2013 3:00:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="84b38-115">Subject: Online training webcast: 8/22/2013 2:00:00 PM End: 8/22/2013 3:00:00 PM</span></span>
## <a name="get-appointments-by-using-ews"></a><span data-ttu-id="84b38-116">Obtener las citas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="84b38-116">Get appointments by using EWS</span></span>
<span data-ttu-id="84b38-117"><a name="bk_xml"> </a></span><span class="sxs-lookup"><span data-stu-id="84b38-117"></span></span>

<span data-ttu-id="84b38-118">El siguiente código XML muestra una solicitud de operación [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para devolver un identificador de la carpeta para la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="84b38-118">The following XML shows a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request to return a folder ID for the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="84b38-119">El siguiente código XML muestra la respuesta **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="84b38-119">The following XML shows the **GetFolder** response.</span></span> <span data-ttu-id="84b38-120">Tenga en cuenta que los atributos **FolderID** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="84b38-120">Note that the **FolderID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:CalendarFolder>
              <t:FolderId Id="AAMk" ChangeKey="AgAA" />
            </t:CalendarFolder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="84b38-121">El siguiente código XML muestra la solicitud **FindItem** que se usa para devolver las citas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="84b38-121">The following XML shows the **FindItem** request used to return the requested appointments.</span></span> <span data-ttu-id="84b38-122">Tenga en cuenta que los atributos **FolderID** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="84b38-122">Note that the **FolderID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-08-21T17:30:24.127Z" EndDate="2013-09-20T17:30:24.127Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAMk" ChangeKey="AgAA" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="84b38-123">El siguiente código XML muestra la respuesta **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="84b38-123">The following XML shows the **FindItem** response.</span></span> <span data-ttu-id="84b38-124">Tenga en cuenta que los atributos **ItemID** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="84b38-124">Note that the **ItemID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="33" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Contoso devs team meeting</t:Subject>
                <t:Start>2013-08-21T19:30:00Z</t:Start>
                <t:End>2013-08-21T20:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Daily status meeting</t:Subject>
                <t:Start>2013-08-21T20:00:00Z</t:Start>
                <t:End>2013-08-21T21:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Lunch with sales team</t:Subject>
                <t:Start>2013-08-21T21:30:00Z</t:Start>
                <t:End>2013-08-21T22:30:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Tennis at the club</t:Subject>
                <t:Start>2013-08-22T18:00:00Z</t:Start>
                <t:End>2013-08-22T19:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA" ChangeKey="DwAA" />
                <t:Subject>Online training webcast</t:Subject>
                <t:Start>2013-08-22T21:00:00Z</t:Start>
                <t:End>2013-08-22T22:00:00Z</t:End>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="recurring-meetings-and-the-calendar-view"></a><span data-ttu-id="84b38-125">Reuniones periódicas y la vista de calendario</span><span class="sxs-lookup"><span data-stu-id="84b38-125">Recurring meetings and the calendar view</span></span>
<span data-ttu-id="84b38-126"><a name="bk_recurring"> </a></span><span class="sxs-lookup"><span data-stu-id="84b38-126"></span></span>

<span data-ttu-id="84b38-127">La carpeta de calendario es un poco diferente de otras carpetas en un buzón debido a que no son elementos real en el buzón de repeticiones en una serie periódica y las excepciones de una serie periódica, pero en su lugar se almacenan internamente como datos adjuntos a un maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="84b38-127">The calendar folder is a little different from other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="84b38-128">Esto significa, si bien puede crear una solicitud de EWS devuelve valores entre un conjunto de **start** y **end** valores mediante el uso de uno de la API administrada de EWS **FindItems** sobrecargan métodos, como [ExchangeService.FindItems](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o la [EWS FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operación, EWS no tendría un aspecto a través de la tabla de datos adjuntos de todos los elementos de calendario para buscar excepciones y repeticiones.</span><span class="sxs-lookup"><span data-stu-id="84b38-128">This means that although you can create an EWS request that returns values between a set of **start** and **end** values by using one of the EWS Managed API **FindItems** overload methods, such as [ExchangeService.FindItems](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or the EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, EWS would not look through the attachment table of every calendar item to find exceptions and occurrences.</span></span> 
  
<span data-ttu-id="84b38-129">En su lugar, ¿qué desea hacer en realidad es algo parecido a la aplicación de una *Dataview* en una unión de dos tablas SQL, con un objeto [CalendarView](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="84b38-129">Instead, what you really want to do is something akin to applying a  *Dataview*  onto a union of two SQL tables, using a [CalendarView](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="84b38-130">Tenga en cuenta que por motivos de rendimiento, se recomienda que utilice la propiedad [PropertySet](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para limitar el tamaño de la respuesta de forma que indica el número de citas o reuniones que desea devolver, así como las propiedades específicas que desee.</span><span class="sxs-lookup"><span data-stu-id="84b38-130">Note that for performance reasons, we recommend that you use the [PropertySet](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) property to limit the size of the response by indicating the number of appointments or meetings you want returned, as well as the specific properties you want.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84b38-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="84b38-131">See also</span></span>
<span data-ttu-id="84b38-132"><a name="bk_additional"> </a></span><span class="sxs-lookup"><span data-stu-id="84b38-132"></span></span>

- [<span data-ttu-id="84b38-133">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84b38-133">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="84b38-134">Crear citas y reuniones mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="84b38-134">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="84b38-135">Actualizar las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84b38-135">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="84b38-136">Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84b38-136">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="84b38-137">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="84b38-137">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    


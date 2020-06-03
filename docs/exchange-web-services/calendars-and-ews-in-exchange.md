---
title: Calendarios y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: Obtenga información sobre calendarios, carpetas y elementos de calendario, citas y reuniones en Exchange.
localization_priority: Priority
ms.openlocfilehash: 3312ebb4deeb6645ccd7048564d61c3db5ea4b94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456202"
---
# <a name="calendars-and-ews-in-exchange"></a><span data-ttu-id="74163-103">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-103">Calendars and EWS in Exchange</span></span>

<span data-ttu-id="74163-104">Obtenga información sobre calendarios, carpetas y elementos de calendario, citas y reuniones en Exchange.</span><span class="sxs-lookup"><span data-stu-id="74163-104">Learn about calendars, calendar folders and items, appointments, and meetings in Exchange.</span></span>
  
<span data-ttu-id="74163-105">Probablemente esté familiarizado con muchas de las características de calendario de los clientes de correo electrónico como Outlook, lo que le permite realizar un seguimiento de las citas, programar reuniones, comprobar la disponibilidad de los usuarios, invitar a los asistentes y cambiar o cancelar reuniones.</span><span class="sxs-lookup"><span data-stu-id="74163-105">You're probably familiar with many of the calendar features in email clients like Outlook, which enable you to track appointments, schedule meetings, check people's availability, invite attendees, and change or cancel meetings.</span></span>
  
<span data-ttu-id="74163-106">Las características relacionadas con el calendario de Exchange son un poco diferentes de las que se ven en un cliente como Outlook.</span><span class="sxs-lookup"><span data-stu-id="74163-106">Calendar-related features in Exchange are a little different than what you see in a client like Outlook.</span></span> <span data-ttu-id="74163-107">En lugar de Mostrar información, EWS en Exchange le permite hacer cosas como crear, almacenar, enviar o cambiar la información.</span><span class="sxs-lookup"><span data-stu-id="74163-107">Instead of displaying information, EWS in Exchange enables you to do things like create, store, send, or change information.</span></span> <span data-ttu-id="74163-108">Para usar EWS para trabajar con calendarios, debe estar familiarizado con los conceptos, como el almacenamiento de la información, el tiempo, la periodicidad y el flujo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="74163-108">To use EWS to work with calendars, you'll need to be familiar with concepts such as information storage, time, recurrence, and message flow.</span></span> <span data-ttu-id="74163-109">Más concretamente, debe estar familiarizado con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="74163-109">More specifically, you'll need to be familiar with the following:</span></span>
  
- <span data-ttu-id="74163-110">Carpetas de calendario, elementos de calendario y vistas de calendario</span><span class="sxs-lookup"><span data-stu-id="74163-110">Calendar folders, calendar items, and calendar views</span></span>
    
- <span data-ttu-id="74163-111">Convocatorias de reunión, respuestas, programación, asistentes, recursos, salas y disponibilidad</span><span class="sxs-lookup"><span data-stu-id="74163-111">Meeting requests, responses, scheduling, attendees, resources, rooms, and availability</span></span>
    
- <span data-ttu-id="74163-112">Duraciones de tiempo, zonas horarias y horas de inicio y finalización de reuniones y citas</span><span class="sxs-lookup"><span data-stu-id="74163-112">Time durations, time zones, and start and end times of meetings and appointments</span></span>
    
- <span data-ttu-id="74163-113">Series periódicas, patrones de periodicidad, excepciones y citas y reuniones de instancia única</span><span class="sxs-lookup"><span data-stu-id="74163-113">Recurring series, recurrence patterns, exceptions, and single instance appointments and meetings</span></span>
    
<span data-ttu-id="74163-114">Afortunadamente, EWS y la API administrada de EWS proporcionan un amplio conjunto de operaciones y métodos que permiten realizar una amplia variedad de tareas relacionadas con el calendario.</span><span class="sxs-lookup"><span data-stu-id="74163-114">Fortunately, EWS and the EWS Managed API provide a rich set of operations and methods that enable you to perform a wide range of calendar-related tasks.</span></span> <span data-ttu-id="74163-115">Por ejemplo, mediante la API administrada de EWS, puede crear una reunión y enviar invitaciones a los asistentes con unas pocas líneas de código, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="74163-115">For example, using the EWS Managed API, you can create a meeting and send invitations to attendees with just a few lines of code, as shown in the following example.</span></span>
  
```cs
            Appointment meeting = new Appointment(service);
            // Set the properties on the meeting object to create the meeting.
            meeting.Subject = "Team building exercise";
            meeting.Body = "Let's learn to really work as a team and then have lunch!";
            meeting.Start = DateTime.Now.AddDays(2);
            meeting.End = meeting.Start.AddHours(2);
            meeting.Location = "Conference Room 12";
            meeting.RequiredAttendees.Add("Mack.Chaves@contoso.com");
            meeting.RequiredAttendees.Add("Sadie.Daniels@contoso.com");
            meeting.OptionalAttendees.Add("Magdalena.Kemp@contoso.com");
            meeting.ReminderMinutesBeforeStart = 60;
            // Send the meeting request
            meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);

```

## <a name="calendar-folders-and-calendar-items"></a><span data-ttu-id="74163-116">Carpetas de calendario y elementos de calendario</span><span class="sxs-lookup"><span data-stu-id="74163-116">Calendar folders and calendar items</span></span>
<span data-ttu-id="74163-117"><a name="bk_CalendarFolder"> </a></span><span class="sxs-lookup"><span data-stu-id="74163-117"><a name="bk_CalendarFolder"> </a></span></span>

<span data-ttu-id="74163-118">Las carpetas de calendario contienen elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="74163-118">Calendar folders contain calendar items.</span></span> <span data-ttu-id="74163-119">Las carpetas de calendarios tienen una [clase de carpeta](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) de **ipf. Cita**y puede incluir solo los elementos definidos por la propiedad de la API administrada de EWS de [ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) , que está asociada con un objeto de [clase de cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="74163-119">Calendar folders have a [folder class](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) of **IPF.Appointment**, and can include only the items defined by the [ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS Managed API property, which is associated with an [Appointment Class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, or the EWS [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="74163-120">Los elementos de una carpeta calendario son ligeramente diferentes de los elementos de otras carpetas de un buzón, ya que las repeticiones de una serie periódica y las excepciones a una serie periódica no son elementos reales en el buzón de correo, sino que se almacenan internamente como datos adjuntos en un maestro recurrente.</span><span class="sxs-lookup"><span data-stu-id="74163-120">Items in a Calendar folder are a little different from items in other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="74163-121">Por lo tanto, para poder recuperar todas las citas de un intervalo de fechas determinado, debe usar una vista de calendario.</span><span class="sxs-lookup"><span data-stu-id="74163-121">Therefore, in order to retrieve all appointments in a given date range, you need to use a calendar view.</span></span> <span data-ttu-id="74163-122">Para obtener más información sobre cómo recuperar las citas y las vistas de calendario, vea [obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="74163-122">To learn more about retrieving appointments and calendar views, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="meetings-and-appointments"></a><span data-ttu-id="74163-123">Reuniones y citas</span><span class="sxs-lookup"><span data-stu-id="74163-123">Meetings and appointments</span></span>
<span data-ttu-id="74163-124"><a name="bk_meetings"> </a></span><span class="sxs-lookup"><span data-stu-id="74163-124"><a name="bk_meetings"> </a></span></span>

<span data-ttu-id="74163-125">La diferencia fundamental entre las reuniones y las citas es que las reuniones tienen asistentes y las citas no.</span><span class="sxs-lookup"><span data-stu-id="74163-125">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="74163-126">Internamente, Exchange usa el mismo objeto para las reuniones y las citas.</span><span class="sxs-lookup"><span data-stu-id="74163-126">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="74163-127">Use la [clase de cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) de API administrada EWS o el elemento [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) de EWS para trabajar con reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="74163-127">You use the EWS Managed API [Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="74163-128">Las citas y las reuniones pueden ser únicas o formar parte de una [serie periódica](recurrence-patterns-and-ews.md), pero debido a que las citas no incluyen asistentes, salones o recursos, no necesitan que se envíe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="74163-128">Both appointments and meetings can be single instances or part of a [recurring series](recurrence-patterns-and-ews.md), but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span>
  
<span data-ttu-id="74163-129">Debido a que las reuniones incluyen el envío y la respuesta a solicitudes y actualizaciones, implican algo más que obtener acceso a los elementos de una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="74163-129">Because meetings include sending and responding to requests and updates, they involve more than just accessing items in a Calendar folder.</span></span> <span data-ttu-id="74163-130">También tienen un flujo de trabajo asociado.</span><span class="sxs-lookup"><span data-stu-id="74163-130">They also have an associated workflow.</span></span> <span data-ttu-id="74163-131">Las reuniones deben programarse cuando los asistentes están disponibles, y también pueden implicar la reserva de una sala de reuniones o recursos como un proyector u otro equipo.</span><span class="sxs-lookup"><span data-stu-id="74163-131">Meetings must be scheduled when attendees are available, and can also involve reserving a meeting room, or resources such as a projector or other equipment.</span></span>
  
<span data-ttu-id="74163-132">El flujo de trabajo de reuniones suele implicar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="74163-132">The meeting workflow typically involves the following steps:</span></span>
  
1. <span data-ttu-id="74163-133">Una reunión se crea y se rellena con información como la hora de inicio y finalización, la ubicación y el cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="74163-133">A meeting is created and populated with information such as start and end time, location, and a message body.</span></span>
    
2. <span data-ttu-id="74163-134">Se crea una lista de los asistentes, los recursos y las salas potenciales.</span><span class="sxs-lookup"><span data-stu-id="74163-134">A list of prospective attendees, resources, and rooms is created.</span></span>
    
3. <span data-ttu-id="74163-135">Se comprueba el estado de disponibilidad de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="74163-135">The availability status of attendees is checked.</span></span> 
    
4. <span data-ttu-id="74163-136">Se envía una convocatoria de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="74163-136">A meeting request is sent to attendees.</span></span>
    
5. <span data-ttu-id="74163-137">Los asistentes responden a la reunión con su intención de asistir o no.</span><span class="sxs-lookup"><span data-stu-id="74163-137">Attendees reply to the meeting with their intention to attend or not.</span></span> <span data-ttu-id="74163-138">Los asistentes también pueden proponer una nueva hora para la reunión.</span><span class="sxs-lookup"><span data-stu-id="74163-138">Attendees may also propose a new time for the meeting.</span></span>
    
6. <span data-ttu-id="74163-139">Las reuniones se pueden cancelar o actualizar, lo que normalmente desencadena que se envíen nuevos mensajes a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="74163-139">Meetings can be canceled or updated, which typically trigger new messages to be sent to attendees.</span></span>
    
## <a name="calendars-and-time"></a><span data-ttu-id="74163-140">Calendarios y hora</span><span class="sxs-lookup"><span data-stu-id="74163-140">Calendars and time</span></span>
<span data-ttu-id="74163-141"><a name="bk_Time"> </a></span><span class="sxs-lookup"><span data-stu-id="74163-141"><a name="bk_Time"> </a></span></span>

<span data-ttu-id="74163-142">La funcionalidad relacionada con el tiempo es fundamental para el calendario.</span><span class="sxs-lookup"><span data-stu-id="74163-142">Time-related functionality is integral to calendaring.</span></span> <span data-ttu-id="74163-143">Las citas y las reuniones tienen horas de inicio y finalización, duraciones y otras propiedades relacionadas con el tiempo, como la hora en la que se crea, envía y recibe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="74163-143">Appointments and meetings have start and end times, durations, and other time-related properties, such as the time at which a message is created, sent, and received.</span></span> <span data-ttu-id="74163-144">Las citas y reuniones existentes se pueden recuperar de una carpeta de calendario a partir de una hora de inicio y de finalización.</span><span class="sxs-lookup"><span data-stu-id="74163-144">Existing appointments and meetings can be retrieved from a Calendar folder based on a start and end time.</span></span> <span data-ttu-id="74163-145">Las series periódicas tienen principio y fin.</span><span class="sxs-lookup"><span data-stu-id="74163-145">Recurring series have beginnings and ends.</span></span> <span data-ttu-id="74163-146">Las reuniones se producen dentro de una zona horaria determinada, que es cada vez más importante en una economía global.</span><span class="sxs-lookup"><span data-stu-id="74163-146">And meetings occur within a given time zone, which is increasingly important in a global economy.</span></span>
  
<span data-ttu-id="74163-147">Las horas se almacenan internamente en un servidor de Exchange en la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="74163-147">Times are stored internally on an Exchange server in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="74163-148">Exchange los convierte en la zona horaria local según la configuración del cliente.</span><span class="sxs-lookup"><span data-stu-id="74163-148">Exchange converts them to local time zone based on client settings.</span></span> <span data-ttu-id="74163-149">Las propiedades [DateTime](https://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) tienen un ámbito de la zona horaria local del equipo.</span><span class="sxs-lookup"><span data-stu-id="74163-149">[DateTime](https://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) properties are scoped to the computer's local time zone.</span></span> 
  
## <a name="recurring-series"></a><span data-ttu-id="74163-150">Serie periódica</span><span class="sxs-lookup"><span data-stu-id="74163-150">Recurring series</span></span>
<span data-ttu-id="74163-151"><a name="bk_recurrence"> </a></span><span class="sxs-lookup"><span data-stu-id="74163-151"><a name="bk_recurrence"> </a></span></span>

<span data-ttu-id="74163-152">Una serie de citas o reuniones periódicas consta de un maestro recurrente, un conjunto de elementos de repeticiones y, opcionalmente, un conjunto de elementos de excepción.</span><span class="sxs-lookup"><span data-stu-id="74163-152">A recurring series of appointments or meetings is comprised of a recurring master, a set of occurrence items, and optionally, a set of exception items.</span></span> <span data-ttu-id="74163-153">La información de periodicidad se almacena en el elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="74163-153">Recurrence information is stored on the recurring master item.</span></span> <span data-ttu-id="74163-154">El elemento EWS [RecurringMasterItemId](https://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) está asociado a ocurrencias y excepciones en una serie, o bien puede usar el método de API administrada de EWS [appointment. BindToRecurringMaster](https://msdn.microsoft.com/library/dd635978%28v=EXCHG.80%29.aspx) para obtener el patrón recurrente.</span><span class="sxs-lookup"><span data-stu-id="74163-154">The [RecurringMasterItemId](https://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS element is associated with occurrences and exceptions in a series, or you can use the [Appointment.BindToRecurringMaster](https://msdn.microsoft.com/library/dd635978%28v=EXCHG.80%29.aspx) EWS Managed API method to get the recurring master.</span></span> <span data-ttu-id="74163-155">Mediante el uso de una instancia de una serie, puede encontrar todos los elementos e información asociados a la serie.</span><span class="sxs-lookup"><span data-stu-id="74163-155">Using an instance of a series, you can find all the elements and information associated with the series.</span></span> 
  
<span data-ttu-id="74163-156">Tenga en cuenta que las propiedades de periodicidad existen en todos los elementos de calendario, pero solo se rellenan en elementos maestros periódicos.</span><span class="sxs-lookup"><span data-stu-id="74163-156">Note that recurrence properties exist on all calendar items, but they are populated only on recurring master items.</span></span> <span data-ttu-id="74163-157">Además de un índice de todas las apariciones de una serie, el patrón recurrente tiene una referencia a repeticiones modificadas y eliminadas, así como el patrón de periodicidad de una serie (por ejemplo, diaria, semanal, mensual o anual).</span><span class="sxs-lookup"><span data-stu-id="74163-157">In addition to an index of all occurrences in a series, the recurring master has a reference to modified and deleted occurrences and the recurrence pattern of a series (for example, daily, weekly, monthly, or yearly).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="74163-158">En esta sección</span><span class="sxs-lookup"><span data-stu-id="74163-158">In this section</span></span>
<span data-ttu-id="74163-159"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="74163-159"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="74163-160">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="74163-160">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="74163-161">Crear eventos de día completo mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-161">Create all-day events by using EWS in Exchange</span></span>](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="74163-162">Obtener citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="74163-163">Actualizar citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="74163-164">Eliminar citas y cancelar reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="74163-165">Obtener listas de salas con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-165">Get room lists by using EWS in Exchange</span></span>](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="74163-166">Obtener información de disponibilidad mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-166">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="74163-167">Proponer una nueva hora de reunión mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-167">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="74163-168">Procesar elementos de calendario en lotes en Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-168">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [<span data-ttu-id="74163-169">Patrones de periodicidad y EWS</span><span class="sxs-lookup"><span data-stu-id="74163-169">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a><span data-ttu-id="74163-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="74163-170">See also</span></span>


- [<span data-ttu-id="74163-171">Desarrollar clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="74163-172">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-172">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="74163-173">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="74163-173">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    


---
title: Calendarios y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: Obtenga información sobre los calendarios, las carpetas de calendario y los elementos, las citas y reuniones en Exchange.
ms.openlocfilehash: bb9702118ff1db66862a5788c2d8f58dd55c4d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762992"
---
# <a name="calendars-and-ews-in-exchange"></a><span data-ttu-id="8b2de-103">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-103">Calendars and EWS in Exchange</span></span>

<span data-ttu-id="8b2de-104">Obtenga información sobre los calendarios, las carpetas de calendario y los elementos, las citas y reuniones en Exchange.</span><span class="sxs-lookup"><span data-stu-id="8b2de-104">Learn about calendars, calendar folders and items, appointments, and meetings in Exchange.</span></span>
  
<span data-ttu-id="8b2de-105">Es probablemente familiarizado con muchas de las características de calendario en los clientes de correo electrónico como Outlook, lo que permite realizar un seguimiento de las citas, programar reuniones, comprobar la disponibilidad de las personas, invitar a los asistentes y cambiar o cancelar las reuniones.</span><span class="sxs-lookup"><span data-stu-id="8b2de-105">You're probably familiar with many of the calendar features in email clients like Outlook, which enable you to track appointments, schedule meetings, check people's availability, invite attendees, and change or cancel meetings.</span></span>
  
<span data-ttu-id="8b2de-106">Características relacionadas con el calendario de Exchange son un poco diferentes de lo que se ve en un cliente como Outlook.</span><span class="sxs-lookup"><span data-stu-id="8b2de-106">Calendar-related features in Exchange are a little different than what you see in a client like Outlook.</span></span> <span data-ttu-id="8b2de-107">En lugar de mostrar información, EWS en Exchange le permite realizar tareas como crear, almacenar, enviar o cambiar la información.</span><span class="sxs-lookup"><span data-stu-id="8b2de-107">Instead of displaying information, EWS in Exchange enables you to do things like create, store, send, or change information.</span></span> <span data-ttu-id="8b2de-108">Para usar EWS para trabajar con los calendarios, debe estar familiarizado con los conceptos de almacenamiento de información, la hora, periodicidad y flujo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8b2de-108">To use EWS to work with calendars, you'll need to be familiar with concepts such as information storage, time, recurrence, and message flow.</span></span> <span data-ttu-id="8b2de-109">Más concretamente, deberá estar familiarizado con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8b2de-109">More specifically, you'll need to be familiar with the following:</span></span>
  
- <span data-ttu-id="8b2de-110">Las carpetas de calendario, elementos de calendario y vistas de calendario</span><span class="sxs-lookup"><span data-stu-id="8b2de-110">Calendar folders, calendar items, and calendar views</span></span>
    
- <span data-ttu-id="8b2de-111">Las convocatorias de reunión, respuestas, programación, los asistentes, recursos, salones y disponibilidad</span><span class="sxs-lookup"><span data-stu-id="8b2de-111">Meeting requests, responses, scheduling, attendees, resources, rooms, and availability</span></span>
    
- <span data-ttu-id="8b2de-112">Duraciones de tiempo, zonas horarias y horas de comienzo y finalización de las reuniones y citas</span><span class="sxs-lookup"><span data-stu-id="8b2de-112">Time durations, time zones, and start and end times of meetings and appointments</span></span>
    
- <span data-ttu-id="8b2de-113">Serie periódica, patrones de periodicidad, excepciones y las citas de instancia única y las reuniones</span><span class="sxs-lookup"><span data-stu-id="8b2de-113">Recurring series, recurrence patterns, exceptions, and single instance appointments and meetings</span></span>
    
<span data-ttu-id="8b2de-114">Afortunadamente, EWS y la API administrada de EWS proporcionan un amplio conjunto de operaciones y métodos que permiten realizar una amplia variedad de tareas relacionadas con el calendario.</span><span class="sxs-lookup"><span data-stu-id="8b2de-114">Fortunately, EWS and the EWS Managed API provide a rich set of operations and methods that enable you to perform a wide range of calendar-related tasks.</span></span> <span data-ttu-id="8b2de-115">Por ejemplo, mediante la API administrada de EWS, puede crear una reunión y enviar invitaciones a los asistentes con unas pocas líneas de código, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8b2de-115">For example, using the EWS Managed API, you can create a meeting and send invitations to attendees with just a few lines of code, as shown in the following example.</span></span>
  
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

## <a name="calendar-folders-and-calendar-items"></a><span data-ttu-id="8b2de-116">Las carpetas de calendario y elementos de calendario</span><span class="sxs-lookup"><span data-stu-id="8b2de-116">Calendar folders and calendar items</span></span>
<span data-ttu-id="8b2de-117"><a name="bk_CalendarFolder"> </a></span><span class="sxs-lookup"><span data-stu-id="8b2de-117"></span></span>

<span data-ttu-id="8b2de-118">Las carpetas de calendario contienen elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="8b2de-118">Calendar folders contain calendar items.</span></span> <span data-ttu-id="8b2de-119">Las carpetas de calendario tienen una [clase de carpeta](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) de **IPF. Cita**y puede incluir sólo los elementos definidos por la propiedad de API administrada de EWS [ItemClass](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) , que está asociada a un objeto de [Clase de la cita](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento EWS [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8b2de-119">Calendar folders have a [folder class](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) of **IPF.Appointment**, and can include only the items defined by the [ItemClass](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS Managed API property, which is associated with an [Appointment Class](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, or the EWS [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="8b2de-120">Los elementos de una carpeta Calendario son un poco diferentes de elementos en otras carpetas de un buzón de correo porque repeticiones en una serie periódica y las excepciones de una serie periódica no son elementos real en el buzón de correo, pero en su lugar se almacenan internamente como datos adjuntos a una periódica patrón.</span><span class="sxs-lookup"><span data-stu-id="8b2de-120">Items in a Calendar folder are a little different from items in other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="8b2de-121">Por lo tanto, con el fin de recuperar todas las citas de un intervalo de fechas determinado, debe utilizar una vista de calendario.</span><span class="sxs-lookup"><span data-stu-id="8b2de-121">Therefore, in order to retrieve all appointments in a given date range, you need to use a calendar view.</span></span> <span data-ttu-id="8b2de-122">Para obtener más información acerca de cómo recuperar las citas y vistas del calendario, vea [obtener las citas y reuniones mediante el uso de EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="8b2de-122">To learn more about retrieving appointments and calendar views, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="meetings-and-appointments"></a><span data-ttu-id="8b2de-123">Reuniones y citas</span><span class="sxs-lookup"><span data-stu-id="8b2de-123">Meetings and appointments</span></span>
<span data-ttu-id="8b2de-124"><a name="bk_meetings"> </a></span><span class="sxs-lookup"><span data-stu-id="8b2de-124"></span></span>

<span data-ttu-id="8b2de-125">La diferencia entre las reuniones y citas esencial es que las reuniones tienen asistentes, y no las citas.</span><span class="sxs-lookup"><span data-stu-id="8b2de-125">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="8b2de-126">Internamente, Exchange utiliza el mismo objeto para las reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="8b2de-126">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="8b2de-127">Usar la API administrada de EWS [clase de cita](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para trabajar con las reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="8b2de-127">You use the EWS Managed API [Appointment class](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="8b2de-128">Las citas y reuniones pueden ser instancias únicas o parte de una [serie periódica](recurrence-patterns-and-ews.md)pero, debido a que las citas no incluyen los asistentes, salas o recursos, no requieren que se envíe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8b2de-128">Both appointments and meetings can be single instances or part of a [recurring series](recurrence-patterns-and-ews.md), but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span>
  
<span data-ttu-id="8b2de-129">Debido a que las reuniones incluyen enviar y responder a las solicitudes y las actualizaciones, que implican algo más que obtener acceso a los elementos de una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="8b2de-129">Because meetings include sending and responding to requests and updates, they involve more than just accessing items in a Calendar folder.</span></span> <span data-ttu-id="8b2de-130">También tienen un flujo de trabajo asociado.</span><span class="sxs-lookup"><span data-stu-id="8b2de-130">They also have an associated workflow.</span></span> <span data-ttu-id="8b2de-131">Se deben programar reuniones cuando los asistentes están disponibles y también pueden implicar la reserva una sala de reuniones, o los recursos, como un proyector u otros equipos.</span><span class="sxs-lookup"><span data-stu-id="8b2de-131">Meetings must be scheduled when attendees are available, and can also involve reserving a meeting room, or resources such as a projector or other equipment.</span></span>
  
<span data-ttu-id="8b2de-132">Normalmente, el flujo de trabajo de reunión implica los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="8b2de-132">The meeting workflow typically involves the following steps:</span></span>
  
1. <span data-ttu-id="8b2de-133">Se crea una reunión y se rellena con información como el inicio y la hora de finalización, la ubicación y un cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8b2de-133">A meeting is created and populated with information such as start and end time, location, and a message body.</span></span>
    
2. <span data-ttu-id="8b2de-134">Se crea una lista de posibles asistentes, recursos y salas.</span><span class="sxs-lookup"><span data-stu-id="8b2de-134">A list of prospective attendees, resources, and rooms is created.</span></span>
    
3. <span data-ttu-id="8b2de-135">Se comprueba el estado de disponibilidad de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="8b2de-135">The availability status of attendees is checked.</span></span> 
    
4. <span data-ttu-id="8b2de-136">Se envía una convocatoria de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="8b2de-136">A meeting request is sent to attendees.</span></span>
    
5. <span data-ttu-id="8b2de-137">Respondan a los asistentes a la reunión con su intención de asistir o no.</span><span class="sxs-lookup"><span data-stu-id="8b2de-137">Attendees reply to the meeting with their intention to attend or not.</span></span> <span data-ttu-id="8b2de-138">Los asistentes también pueden proponer una nueva hora para la reunión.</span><span class="sxs-lookup"><span data-stu-id="8b2de-138">Attendees may also propose a new time for the meeting.</span></span>
    
6. <span data-ttu-id="8b2de-139">Las reuniones se pueden cancelar o actualizar, que normalmente desencadenar nuevos mensajes que se envíen a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="8b2de-139">Meetings can be canceled or updated, which typically trigger new messages to be sent to attendees.</span></span>
    
## <a name="calendars-and-time"></a><span data-ttu-id="8b2de-140">Calendarios y la hora</span><span class="sxs-lookup"><span data-stu-id="8b2de-140">Calendars and time</span></span>
<span data-ttu-id="8b2de-141"><a name="bk_Time"> </a></span><span class="sxs-lookup"><span data-stu-id="8b2de-141"></span></span>

<span data-ttu-id="8b2de-142">Funcionalidad relacionada con el tiempo es parte integral de calendario.</span><span class="sxs-lookup"><span data-stu-id="8b2de-142">Time-related functionality is integral to calendaring.</span></span> <span data-ttu-id="8b2de-143">Las citas y reuniones tienen inicio y finalización, duraciones y otras propiedades relacionadas con el tiempo, como la hora a la que un mensaje creado, enviado y recibido.</span><span class="sxs-lookup"><span data-stu-id="8b2de-143">Appointments and meetings have start and end times, durations, and other time-related properties, such as the time at which a message is created, sent, and received.</span></span> <span data-ttu-id="8b2de-144">Las reuniones y las citas existentes se pueden recuperar desde una carpeta de calendario en función de una hora de inicio y final.</span><span class="sxs-lookup"><span data-stu-id="8b2de-144">Existing appointments and meetings can be retrieved from a Calendar folder based on a start and end time.</span></span> <span data-ttu-id="8b2de-145">Serie periódica tiene comienzo y al final.</span><span class="sxs-lookup"><span data-stu-id="8b2de-145">Recurring series have beginnings and ends.</span></span> <span data-ttu-id="8b2de-146">Y las reuniones se producen dentro de una zona horaria determinada, que es cada vez más importante en una economía global.</span><span class="sxs-lookup"><span data-stu-id="8b2de-146">And meetings occur within a given time zone, which is increasingly important in a global economy.</span></span>
  
<span data-ttu-id="8b2de-147">Horas se almacenan internamente en un servidor de Exchange en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="8b2de-147">Times are stored internally on an Exchange server in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8b2de-148">Exchange convierte a la zona horaria local en función de la configuración del cliente.</span><span class="sxs-lookup"><span data-stu-id="8b2de-148">Exchange converts them to local time zone based on client settings.</span></span> <span data-ttu-id="8b2de-149">Propiedades de [fecha y hora](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) se aplican a la zona de hora local del equipo.</span><span class="sxs-lookup"><span data-stu-id="8b2de-149">[DateTime](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) properties are scoped to the computer's local time zone.</span></span> 
  
## <a name="recurring-series"></a><span data-ttu-id="8b2de-150">Serie periódica</span><span class="sxs-lookup"><span data-stu-id="8b2de-150">Recurring series</span></span>
<span data-ttu-id="8b2de-151"><a name="bk_recurrence"> </a></span><span class="sxs-lookup"><span data-stu-id="8b2de-151"></span></span>

<span data-ttu-id="8b2de-152">Una serie de citas o reuniones periódicas se compone de un patrón periódico, un conjunto de elementos de repetición y, opcionalmente, un conjunto de elementos de la excepción.</span><span class="sxs-lookup"><span data-stu-id="8b2de-152">A recurring series of appointments or meetings is comprised of a recurring master, a set of occurrence items, and optionally, a set of exception items.</span></span> <span data-ttu-id="8b2de-153">Información sobre la periodicidad se almacena en el elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="8b2de-153">Recurrence information is stored on the recurring master item.</span></span> <span data-ttu-id="8b2de-154">El elemento EWS [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) está asociado con las repeticiones y excepciones en una serie, o puede usar el método de la API administrada de EWS [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/es-es/library/dd635978%28v=EXCHG.80%29.aspx) para obtener la periódica maestra.</span><span class="sxs-lookup"><span data-stu-id="8b2de-154">The [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS element is associated with occurrences and exceptions in a series, or you can use the [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/es-es/library/dd635978%28v=EXCHG.80%29.aspx) EWS Managed API method to get the recurring master.</span></span> <span data-ttu-id="8b2de-155">Uso de una instancia de una serie, puede encontrar todos los elementos y la información asociada con la serie.</span><span class="sxs-lookup"><span data-stu-id="8b2de-155">Using an instance of a series, you can find all the elements and information associated with the series.</span></span> 
  
<span data-ttu-id="8b2de-156">Tenga en cuenta que las propiedades de periodicidad existen en todos los elementos de calendario, pero se rellenan sólo en los elementos maestros periódicos.</span><span class="sxs-lookup"><span data-stu-id="8b2de-156">Note that recurrence properties exist on all calendar items, but they are populated only on recurring master items.</span></span> <span data-ttu-id="8b2de-157">Además de un índice de todas las apariciones de una serie, el patrón periódico tiene una referencia a las apariciones modificadas y eliminadas y el patrón de periodicidad de una serie (por ejemplo, diariamente, semanalmente, mensualmente o anualmente).</span><span class="sxs-lookup"><span data-stu-id="8b2de-157">In addition to an index of all occurrences in a series, the recurring master has a reference to modified and deleted occurrences and the recurrence pattern of a series (for example, daily, weekly, monthly, or yearly).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="8b2de-158">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8b2de-158">In this section</span></span>
<span data-ttu-id="8b2de-159"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="8b2de-159"></span></span>

- [<span data-ttu-id="8b2de-160">Crear citas y reuniones mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8b2de-160">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="8b2de-161">Crear eventos de día completo mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-161">Create all-day events by using EWS in Exchange</span></span>](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8b2de-162">Obtener las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8b2de-163">Actualizar las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8b2de-164">Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8b2de-165">Obtener listas de las salas mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-165">Get room lists by using EWS in Exchange</span></span>](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8b2de-166">Obtener información de disponibilidad con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-166">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8b2de-167">Proponer una nueva hora de reunión mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-167">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8b2de-168">Procesar por lotes los elementos del calendario en Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-168">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [<span data-ttu-id="8b2de-169">Patrones de periodicidad y EWS</span><span class="sxs-lookup"><span data-stu-id="8b2de-169">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a><span data-ttu-id="8b2de-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b2de-170">See also</span></span>


- [<span data-ttu-id="8b2de-171">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="8b2de-172">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-172">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="8b2de-173">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="8b2de-173">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    


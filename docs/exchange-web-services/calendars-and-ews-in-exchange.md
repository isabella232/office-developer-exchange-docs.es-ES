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
# <a name="calendars-and-ews-in-exchange"></a>Calendarios y EWS en Exchange

Obtenga información sobre los calendarios, las carpetas de calendario y los elementos, las citas y reuniones en Exchange.
  
Es probablemente familiarizado con muchas de las características de calendario en los clientes de correo electrónico como Outlook, lo que permite realizar un seguimiento de las citas, programar reuniones, comprobar la disponibilidad de las personas, invitar a los asistentes y cambiar o cancelar las reuniones.
  
Características relacionadas con el calendario de Exchange son un poco diferentes de lo que se ve en un cliente como Outlook. En lugar de mostrar información, EWS en Exchange le permite realizar tareas como crear, almacenar, enviar o cambiar la información. Para usar EWS para trabajar con los calendarios, debe estar familiarizado con los conceptos de almacenamiento de información, la hora, periodicidad y flujo de mensajes. Más concretamente, deberá estar familiarizado con lo siguiente:
  
- Las carpetas de calendario, elementos de calendario y vistas de calendario
    
- Las convocatorias de reunión, respuestas, programación, los asistentes, recursos, salones y disponibilidad
    
- Duraciones de tiempo, zonas horarias y horas de comienzo y finalización de las reuniones y citas
    
- Serie periódica, patrones de periodicidad, excepciones y las citas de instancia única y las reuniones
    
Afortunadamente, EWS y la API administrada de EWS proporcionan un amplio conjunto de operaciones y métodos que permiten realizar una amplia variedad de tareas relacionadas con el calendario. Por ejemplo, mediante la API administrada de EWS, puede crear una reunión y enviar invitaciones a los asistentes con unas pocas líneas de código, tal como se muestra en el siguiente ejemplo.
  
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

## <a name="calendar-folders-and-calendar-items"></a>Las carpetas de calendario y elementos de calendario
<a name="bk_CalendarFolder"> </a>

Las carpetas de calendario contienen elementos de calendario. Las carpetas de calendario tienen una [clase de carpeta](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) de **IPF. Cita**y puede incluir sólo los elementos definidos por la propiedad de API administrada de EWS [ItemClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) , que está asociada a un objeto de [Clase de la cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento EWS [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) . 
  
Los elementos de una carpeta Calendario son un poco diferentes de elementos en otras carpetas de un buzón de correo porque repeticiones en una serie periódica y las excepciones de una serie periódica no son elementos real en el buzón de correo, pero en su lugar se almacenan internamente como datos adjuntos a una periódica patrón. Por lo tanto, con el fin de recuperar todas las citas de un intervalo de fechas determinado, debe utilizar una vista de calendario. Para obtener más información acerca de cómo recuperar las citas y vistas del calendario, vea [obtener las citas y reuniones mediante el uso de EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="meetings-and-appointments"></a>Reuniones y citas
<a name="bk_meetings"> </a>

La diferencia entre las reuniones y citas esencial es que las reuniones tienen asistentes, y no las citas. Internamente, Exchange utiliza el mismo objeto para las reuniones y citas. Usar la API administrada de EWS [clase de cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para trabajar con las reuniones y citas. 
  
Las citas y reuniones pueden ser instancias únicas o parte de una [serie periódica](recurrence-patterns-and-ews.md)pero, debido a que las citas no incluyen los asistentes, salas o recursos, no requieren que se envíe un mensaje.
  
Debido a que las reuniones incluyen enviar y responder a las solicitudes y las actualizaciones, que implican algo más que obtener acceso a los elementos de una carpeta de calendario. También tienen un flujo de trabajo asociado. Se deben programar reuniones cuando los asistentes están disponibles y también pueden implicar la reserva una sala de reuniones, o los recursos, como un proyector u otros equipos.
  
Normalmente, el flujo de trabajo de reunión implica los siguientes pasos:
  
1. Se crea una reunión y se rellena con información como el inicio y la hora de finalización, la ubicación y un cuerpo del mensaje.
    
2. Se crea una lista de posibles asistentes, recursos y salas.
    
3. Se comprueba el estado de disponibilidad de los asistentes. 
    
4. Se envía una convocatoria de reunión a los asistentes.
    
5. Respondan a los asistentes a la reunión con su intención de asistir o no. Los asistentes también pueden proponer una nueva hora para la reunión.
    
6. Las reuniones se pueden cancelar o actualizar, que normalmente desencadenar nuevos mensajes que se envíen a los asistentes.
    
## <a name="calendars-and-time"></a>Calendarios y la hora
<a name="bk_Time"> </a>

Funcionalidad relacionada con el tiempo es parte integral de calendario. Las citas y reuniones tienen inicio y finalización, duraciones y otras propiedades relacionadas con el tiempo, como la hora a la que un mensaje creado, enviado y recibido. Las reuniones y las citas existentes se pueden recuperar desde una carpeta de calendario en función de una hora de inicio y final. Serie periódica tiene comienzo y al final. Y las reuniones se producen dentro de una zona horaria determinada, que es cada vez más importante en una economía global.
  
Horas se almacenan internamente en un servidor de Exchange en hora Universal coordinada (UTC). Exchange convierte a la zona horaria local en función de la configuración del cliente. Propiedades de [fecha y hora](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) se aplican a la zona de hora local del equipo. 
  
## <a name="recurring-series"></a>Serie periódica
<a name="bk_recurrence"> </a>

Una serie de citas o reuniones periódicas se compone de un patrón periódico, un conjunto de elementos de repetición y, opcionalmente, un conjunto de elementos de la excepción. Información sobre la periodicidad se almacena en el elemento maestro periódico. El elemento EWS [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) está asociado con las repeticiones y excepciones en una serie, o puede usar el método de la API administrada de EWS [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/dd635978%28v=EXCHG.80%29.aspx) para obtener la periódica maestra. Uso de una instancia de una serie, puede encontrar todos los elementos y la información asociada con la serie. 
  
Tenga en cuenta que las propiedades de periodicidad existen en todos los elementos de calendario, pero se rellenan sólo en los elementos maestros periódicos. Además de un índice de todas las apariciones de una serie, el patrón periódico tiene una referencia a las apariciones modificadas y eliminadas y el patrón de periodicidad de una serie (por ejemplo, diariamente, semanalmente, mensualmente o anualmente).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Crear eventos de día completo mediante el uso de EWS en Exchange](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [Obtener las citas y reuniones con EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Actualizar las citas y reuniones con EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [Obtener listas de las salas mediante el uso de EWS en Exchange](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [Obtener información de disponibilidad con EWS en Exchange](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [Proponer una nueva hora de reunión mediante el uso de EWS en Exchange](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [Procesar por lotes los elementos del calendario en Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [Patrones de periodicidad y EWS](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


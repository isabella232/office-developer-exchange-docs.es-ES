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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456202"
---
# <a name="calendars-and-ews-in-exchange"></a>Calendarios y EWS en Exchange

Obtenga información sobre calendarios, carpetas y elementos de calendario, citas y reuniones en Exchange.
  
Probablemente esté familiarizado con muchas de las características de calendario de los clientes de correo electrónico como Outlook, lo que le permite realizar un seguimiento de las citas, programar reuniones, comprobar la disponibilidad de los usuarios, invitar a los asistentes y cambiar o cancelar reuniones.
  
Las características relacionadas con el calendario de Exchange son un poco diferentes de las que se ven en un cliente como Outlook. En lugar de Mostrar información, EWS en Exchange le permite hacer cosas como crear, almacenar, enviar o cambiar la información. Para usar EWS para trabajar con calendarios, debe estar familiarizado con los conceptos, como el almacenamiento de la información, el tiempo, la periodicidad y el flujo de mensajes. Más concretamente, debe estar familiarizado con lo siguiente:
  
- Carpetas de calendario, elementos de calendario y vistas de calendario
    
- Convocatorias de reunión, respuestas, programación, asistentes, recursos, salas y disponibilidad
    
- Duraciones de tiempo, zonas horarias y horas de inicio y finalización de reuniones y citas
    
- Series periódicas, patrones de periodicidad, excepciones y citas y reuniones de instancia única
    
Afortunadamente, EWS y la API administrada de EWS proporcionan un amplio conjunto de operaciones y métodos que permiten realizar una amplia variedad de tareas relacionadas con el calendario. Por ejemplo, mediante la API administrada de EWS, puede crear una reunión y enviar invitaciones a los asistentes con unas pocas líneas de código, como se muestra en el ejemplo siguiente.
  
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

## <a name="calendar-folders-and-calendar-items"></a>Carpetas de calendario y elementos de calendario
<a name="bk_CalendarFolder"> </a>

Las carpetas de calendario contienen elementos de calendario. Las carpetas de calendarios tienen una [clase de carpeta](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) de **ipf. Cita**y puede incluir solo los elementos definidos por la propiedad de la API administrada de EWS de [ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) , que está asociada con un objeto de [clase de cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) de EWS. 
  
Los elementos de una carpeta calendario son ligeramente diferentes de los elementos de otras carpetas de un buzón, ya que las repeticiones de una serie periódica y las excepciones a una serie periódica no son elementos reales en el buzón de correo, sino que se almacenan internamente como datos adjuntos en un maestro recurrente. Por lo tanto, para poder recuperar todas las citas de un intervalo de fechas determinado, debe usar una vista de calendario. Para obtener más información sobre cómo recuperar las citas y las vistas de calendario, vea [obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="meetings-and-appointments"></a>Reuniones y citas
<a name="bk_meetings"> </a>

La diferencia fundamental entre las reuniones y las citas es que las reuniones tienen asistentes y las citas no. Internamente, Exchange usa el mismo objeto para las reuniones y las citas. Use la [clase de cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) de API administrada EWS o el elemento [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) de EWS para trabajar con reuniones y citas. 
  
Las citas y las reuniones pueden ser únicas o formar parte de una [serie periódica](recurrence-patterns-and-ews.md), pero debido a que las citas no incluyen asistentes, salones o recursos, no necesitan que se envíe un mensaje.
  
Debido a que las reuniones incluyen el envío y la respuesta a solicitudes y actualizaciones, implican algo más que obtener acceso a los elementos de una carpeta de calendario. También tienen un flujo de trabajo asociado. Las reuniones deben programarse cuando los asistentes están disponibles, y también pueden implicar la reserva de una sala de reuniones o recursos como un proyector u otro equipo.
  
El flujo de trabajo de reuniones suele implicar los siguientes pasos:
  
1. Una reunión se crea y se rellena con información como la hora de inicio y finalización, la ubicación y el cuerpo de un mensaje.
    
2. Se crea una lista de los asistentes, los recursos y las salas potenciales.
    
3. Se comprueba el estado de disponibilidad de los asistentes. 
    
4. Se envía una convocatoria de reunión a los asistentes.
    
5. Los asistentes responden a la reunión con su intención de asistir o no. Los asistentes también pueden proponer una nueva hora para la reunión.
    
6. Las reuniones se pueden cancelar o actualizar, lo que normalmente desencadena que se envíen nuevos mensajes a los asistentes.
    
## <a name="calendars-and-time"></a>Calendarios y hora
<a name="bk_Time"> </a>

La funcionalidad relacionada con el tiempo es fundamental para el calendario. Las citas y las reuniones tienen horas de inicio y finalización, duraciones y otras propiedades relacionadas con el tiempo, como la hora en la que se crea, envía y recibe un mensaje. Las citas y reuniones existentes se pueden recuperar de una carpeta de calendario a partir de una hora de inicio y de finalización. Las series periódicas tienen principio y fin. Las reuniones se producen dentro de una zona horaria determinada, que es cada vez más importante en una economía global.
  
Las horas se almacenan internamente en un servidor de Exchange en la hora universal coordinada (UTC). Exchange los convierte en la zona horaria local según la configuración del cliente. Las propiedades [DateTime](https://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) tienen un ámbito de la zona horaria local del equipo. 
  
## <a name="recurring-series"></a>Serie periódica
<a name="bk_recurrence"> </a>

Una serie de citas o reuniones periódicas consta de un maestro recurrente, un conjunto de elementos de repeticiones y, opcionalmente, un conjunto de elementos de excepción. La información de periodicidad se almacena en el elemento maestro periódico. El elemento EWS [RecurringMasterItemId](https://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) está asociado a ocurrencias y excepciones en una serie, o bien puede usar el método de API administrada de EWS [appointment. BindToRecurringMaster](https://msdn.microsoft.com/library/dd635978%28v=EXCHG.80%29.aspx) para obtener el patrón recurrente. Mediante el uso de una instancia de una serie, puede encontrar todos los elementos e información asociados a la serie. 
  
Tenga en cuenta que las propiedades de periodicidad existen en todos los elementos de calendario, pero solo se rellenan en elementos maestros periódicos. Además de un índice de todas las apariciones de una serie, el patrón recurrente tiene una referencia a repeticiones modificadas y eliminadas, así como el patrón de periodicidad de una serie (por ejemplo, diaria, semanal, mensual o anual).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Crear eventos de día completo mediante EWS en Exchange](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [Obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [Obtener listas de salas con EWS en Exchange](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [Obtener información de disponibilidad mediante EWS en Exchange](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [Proponer una nueva hora de reunión mediante EWS en Exchange](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [Procesar elementos de calendario en lotes en Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [Patrones de periodicidad y EWS](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


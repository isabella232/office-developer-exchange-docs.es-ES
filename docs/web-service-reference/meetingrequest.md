---
title: MeetingRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingRequest
api_type:
- schema
ms.assetid: c44f8804-a355-473d-a837-48cc91617251
description: El elemento MeetingRequest representa una solicitud de reunión en Exchange almacén.
ms.openlocfilehash: 76bad3d920aa38bd2b7f42a9d0b30b8f01c8d1bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542186"
---
# <a name="meetingrequest"></a>MeetingRequest

El **elemento MeetingRequest** representa una solicitud de reunión en Exchange almacén. 
  
```xml
<MeetingRequest>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <Importance/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <AssociatedCalendarItemId/>
   <IsDelegated/>
   <IsOutOfDate/>
   <HasBeenProcessed/>
   <ResponseType/>
   <MeetingRequestType/>
   <IntendedFreeBusyStatus/>
   <Start/>
   <End/>
   <OriginalStart/>
   <IsAllDayEvent/>
   <LegacyFreeBusyStatus/>
   <Location/>
   <When/>
   <IsMeeting/>
   <IsCancelled/>
   <IsRecurring/>
   <MeetingRequestWasSent/>
   <CalendarItemType/>
   <MyResponseType/>
   <Organizer/>
   <RequiredAttendees/>
   <OptionalAttendees/>
   <Resources/>
   <ConflictingMeetingCount/>
   <AdjacentMeetingCount/>
   <ConflictingMeetings/>
   <AdjacentMeetings/>
   <Duration/>
   <TimeZone/>
   <AppointmentReplyTime/>
   <AppointmentSequenceNumber/>
   <AppointmentState/>
   <Recurrence/>
   <FirstOccurrence/>
   <LastOccurrence/>
   <ModifiedOccurrences/>
   <DeletedOccurrences/>
   <MeetingTimeZone/>
   <StartTimeZone/>
   <EndTimeZone/>
   <ConferenceType/>
   <AllowNewTimeProposal/>
   <IsOnlineMeeting/>
   <MeetingWorkspaceUrl/>
   <NetShowUrl/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</MeetingRequest>
```

 **MeetingRequestMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia nativa Multipurpose Internet Mail Extensions (MIME) de un objeto representado en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el Exchange almacén. Esta propiedad es de sólo lectura.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Asunto](subject.md) <br/> |Representa el asunto de los Exchange almacenar y los objetos de respuesta. El asunto está limitado a 255 caracteres.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indica el nivel de confidencialidad de un elemento.  <br/> |
|[Cuerpo](body.md) <br/> |Representa el contenido real del cuerpo de un mensaje.  <br/> |
|[Adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos adjuntos a un elemento del Exchange almacén.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Representa los datos y la hora en que se recibió un elemento de un buzón.  <br/> |
|[Tamaño](size.md) <br/> |Representa el tamaño en bytes de un elemento. Esta propiedad es de sólo lectura.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.  <br/> |
|[Importance](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Representa el identificador del elemento al que este elemento es una respuesta.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si se ha enviado un elemento a la carpeta predeterminada bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Indica si aún no se ha enviado un elemento.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario envió un elemento a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se envió anteriormente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si el elemento se ha modificado.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensajes de Internet contenidos en un elemento de un buzón.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y hora en que se envió un elemento de un buzón.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y hora en que se creó un elemento determinado en el buzón.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta asociados con un elemento del Exchange almacén.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y hora en que se produce el evento. El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el Exchange almacén.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea CC. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios CC.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena de presentación que se usa para el contenido de la línea Para. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios To.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible. Esta propiedad es de solo lectura.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica propiedades extendidas en carpetas y elementos.  <br/> |
|[Culture](culture.md) <br/> |Representa la referencia cultural de un elemento determinado en un buzón.  <br/> |
|[Sender](sender.md) <br/> |Identifica al remitente de un elemento.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Contiene un conjunto de destinatarios de un mensaje.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Representa una colección de destinatarios que recibirán una copia del mensaje.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Representa una colección de destinatarios para recibir una copia a ciegas (CCO) de un correo electrónico.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita un recibo de lectura.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita un recibo de entrega.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Representa el identificador de conversación.  <br/> |
|[From](from.md) <br/> |Representa el destinatario desde el que se envió el mensaje.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Representa el identificador de mensaje de Internet de un elemento.  <br/> |
|[IsRead](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Indica si se solicita una respuesta a un mensaje de correo electrónico.  <br/> |
|[Referencias](references.md) <br/> |Representa el encabezado Usenet que se usa para correlacionar las respuestas con sus mensajes originales.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifica un conjunto de direcciones a las que se deben enviar respuestas.  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |Representa el elemento de calendario asociado a [un objeto MeetingMessage](meetingmessage.md).  <br/> |
|[IsDelegated](isdelegated.md) <br/> |Indica si una reunión fue manejada por una cuenta con acceso delegado.  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |Indica si un mensaje de reunión está actualizado.  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |Indica si se ha procesado un elemento de mensaje de reunión.  <br/> |
|[ResponseType](responsetype.md) <br/> |Representa el tipo de respuesta de destinatario que se recibe para una reunión.  <br/> |
|[MeetingRequestType](meetingrequesttype.md) <br/> |Describe el tipo de la solicitud de reunión.  <br/> |
|[IntendedFreeBusyStatus](intendedfreebusystatus.md) <br/> |Representa el estado previsto para el elemento de calendario asociado a la solicitud de reunión.  <br/> |
|[Start](start.md) <br/> |Representa el inicio de un elemento de calendario. Este elemento solo se aplica a una única aparición de un elemento de calendario.  <br/> |
|[Fin ](end-ex15websvcsotherref.md) <br/> |Representa el final de una duración. Este elemento solo se aplica a una única aparición de un elemento de calendario.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Representa la hora de inicio original de un elemento de calendario.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Indica si un elemento de calendario o una solicitud de reunión representa un evento de todo el día.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Representa el estado de disponibilidad del elemento de calendario.  <br/> |
|[Location](location.md) <br/> |Representa la ubicación de una reunión o cita.  <br/> |
|[When](when.md) <br/> |Proporciona una descripción de cuándo se produce una reunión.  <br/> |
|[IsMeeting](ismeeting.md) <br/> |Indica si el elemento del calendario es una reunión o una cita.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Indica si se ha cancelado una cita o reunión.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Indica si un elemento de calendario forma parte de un elemento periódico. Este elemento es de solo lectura.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Indica si se ha enviado una solicitud de reunión a los asistentes solicitados.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Representa el tipo de repetición de un elemento de calendario.  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |Contiene el estado o la respuesta a un elemento de calendario.  <br/> |
|[Organizador](organizer.md) <br/> |Representa el organizador de una reunión.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Representa los asistentes necesarios para asistir a una reunión.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Representa los asistentes que no son necesarios para asistir a una reunión.  <br/> |
|[Recursos](resources.md) <br/> |Representa un recurso programado para una reunión.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Representa el número de reuniones que entra en conflicto con la solicitud de reunión.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Representa el número total de elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entren en conflicto con una hora de reunión.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[Duration (Items)](duration-items.md) <br/> |Representa la duración de un elemento de calendario.  <br/> |
|[TimeZone (Item)](timezone-item.md) <br/> |Proporciona una descripción de texto de una zona horaria.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Representa la fecha y hora en que un asistente respondió a una solicitud de reunión.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Especifica el número de secuencia de una versión de una cita.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Especifica el estado de la cita.  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad de los elementos de calendario y las solicitudes de reunión.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento de calendario periódico.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última aparición de un elemento de calendario periódico.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contiene una matriz de repeticiones periódicas de elementos de calendario que se han modificado para que sean diferentes del elemento maestro de periodicidad.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Contiene una matriz de repeticiones eliminadas de un elemento de calendario periódico.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Representa la zona horaria de la ubicación donde se hospeda la reunión.  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |Representa la zona horaria de inicio del elemento de calendario.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Representa la zona horaria final del elemento de calendario.  <br/> |
|[ConferenceType](conferencetype.md) <br/> |Describe el tipo de conferencia que se realiza con un elemento de calendario.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Representa si se puede proponer una nueva hora de reunión para una reunión.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Indica si la reunión está en línea.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Contiene la dirección URL del área de trabajo de reunión a la que está vinculado el elemento de calendario.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Especifica la dirección URL de una reunión en línea de Microsoft Netshow.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos del elemento o carpeta. Este elemento es de solo lectura.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contiene el nombre para mostrar del último usuario que modifica un elemento.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indica cuándo se modificó por última vez un elemento.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indica si el elemento está asociado a una carpeta.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Representa una dirección URL para concatenar al punto de conexión Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Representa una dirección URL para concatenar al punto Outlook Web App para editar un elemento en Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de un elemento o conversación.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.  <br/> |
|[UID](uid.md) <br/> |Identifica un elemento de calendario.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Se usa para identificar una instancia específica de un elemento de calendario periódico.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Indica la fecha y hora en que se creó una instancia de un objeto iCalendar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Identifica todos los elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se anexarán a una sola propiedad de un elemento durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entren en conflicto con una hora de reunión.  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento para crear en el almacén de cliente local.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos para crear.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un Exchange que se adjunta a otro Exchange elemento.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización de una sola propiedad de un elemento en una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifica un solo elemento para actualizar en el almacén de cliente local.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


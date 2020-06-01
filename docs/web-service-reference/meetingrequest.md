---
title: MeetingRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequest
api_type:
- schema
ms.assetid: c44f8804-a355-473d-a837-48cc91617251
description: El elemento MeetingRequest representa una convocatoria de reunión en el almacén de Exchange.
ms.openlocfilehash: 7b39ec52d2b4fe8b3cdd2b6fd5e7ba97cfa69c7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465831"
---
# <a name="meetingrequest"></a>MeetingRequest

El elemento **MeetingRequest** representa una convocatoria de reunión en el almacén de Exchange. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia nativa de extensiones multipropósito de correo Internet (MIME) de un objeto representado en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange. Esta propiedad es de sólo lectura.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal que contiene el elemento o carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Asunto](subject.md) <br/> |Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta. El asunto está limitado a 255 caracteres.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indica el nivel de confidencialidad de un elemento.  <br/> |
|[Body](body.md) <br/> |Representa el contenido del cuerpo real de un mensaje.  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Representa los datos y la hora en que se recibió un elemento en un buzón.  <br/> |
|[Tamaño](size.md) <br/> |Representa el tamaño en bytes de un elemento. Esta propiedad es de sólo lectura.  <br/> |
|[Categorías](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.  <br/> |
|[Importance](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[Inreplyto](inreplyto.md) <br/> |Representa el identificador del elemento al que se reenviará este elemento.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Indica si todavía no se ha enviado un elemento.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario envió un elemento a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se ha enviado previamente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si se ha modificado el elemento.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensajes de Internet contenidos en un elemento de un buzón.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y la hora en que se envió un elemento en un buzón.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y la hora en que se creó un elemento determinado en el buzón.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y la hora en que se produce el evento. El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea CC. Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea para. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible. Esta propiedad es de sólo lectura.  <br/> |
|[Las extendedproperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas de las carpetas y los elementos.  <br/> |
|[Culture](culture.md) <br/> |Representa la referencia cultural de un elemento determinado en un buzón.  <br/> |
|[Sender](sender.md) <br/> |Identifica al remitente de un elemento.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Contiene un conjunto de destinatarios de un mensaje.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Representa una colección de destinatarios que recibirán una copia del mensaje.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita una confirmación de lectura.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita una confirmación de entrega.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Contiene un identificador binario que representa el subproceso al que pertenece el mensaje.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Representa el identificador de la conversación.  <br/> |
|[From](from.md) <br/> |Representa el destinatario del remitente del mensaje.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Representa el identificador de mensaje de Internet de un elemento.  <br/> |
|[IsRead](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Indica si se solicita una respuesta a un mensaje de correo electrónico.  <br/> |
|[References](references.md) <br/> |Representa el encabezado Usenet que se usa para correlacionar las respuestas con sus mensajes originales.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifica un conjunto de direcciones a las que se deben enviar las respuestas.  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |Representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md).  <br/> |
|[IsDelegated](isdelegated.md) <br/> |Indica si una reunión se controló mediante una cuenta con acceso de delegado.  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |Indica si un mensaje de reunión está obsoleto.  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |Indica si se ha procesado un elemento de mensaje de reunión.  <br/> |
|[ResponseType](responsetype.md) <br/> |Representa el tipo de respuesta de destinatario que se recibe para una reunión.  <br/> |
|[MeetingRequestType](meetingrequesttype.md) <br/> |Describe el tipo de convocatoria de reunión.  <br/> |
|[IntendedFreeBusyStatus](intendedfreebusystatus.md) <br/> |Representa el estado previsto para el elemento de calendario que está asociado a la convocatoria de reunión.  <br/> |
|[Start](start.md) <br/> |Representa el inicio de un elemento de calendario. Este elemento solo se aplica a una única ocurrencia de un elemento de calendario.  <br/> |
|[Centraliza](end-ex15websvcsotherref.md) <br/> |Representa el final de una duración. Este elemento solo se aplica a una única ocurrencia de un elemento de calendario.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Representa la hora de inicio original de un elemento de calendario.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Indica si un elemento de calendario o una convocatoria de reunión representa un evento de todo el día.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Representa el estado de disponibilidad del elemento de calendario.  <br/> |
|[Ubicación](location.md) <br/> |Representa la ubicación de una reunión o cita.  <br/> |
|[When](when.md) <br/> |Proporciona una descripción de Cuándo tiene lugar una reunión.  <br/> |
|[IsMeeting](ismeeting.md) <br/> |Indica si el elemento de calendario es una reunión o una cita.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Indica si se ha cancelado una cita o una reunión.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Indica si un elemento de calendario es parte de un elemento periódico. Este elemento es de sólo lectura.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Indica si se ha enviado una convocatoria de reunión a los asistentes solicitados.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Representa el tipo de ocurrencia de un elemento de calendario.  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |Contiene el estado o la respuesta a un elemento de calendario.  <br/> |
|[Organizador](organizer.md) <br/> |Representa al organizador de una reunión.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Representa a los asistentes necesarios para asistir a una reunión.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Representa a los asistentes que no necesitan asistir a una reunión.  <br/> |
|[Recursos](resources.md) <br/> |Representa un recurso programado para una reunión.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Representa el número de reuniones que entran en conflicto con la convocatoria de reunión.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Representa el número total de elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con una hora de reunión.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[Duración (elementos)](duration-items.md) <br/> |Representa la duración de un elemento de calendario.  <br/> |
|[TimeZone (elemento)](timezone-item.md) <br/> |Proporciona una descripción de texto de una zona horaria.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Representa la fecha y la hora en que un asistente respondió a una convocatoria de reunión.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Especifica el número de secuencia de una versión de una cita.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Especifica el estado de la cita.  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento de calendario periódico.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última repetición de un elemento de calendario periódico.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contiene una matriz de repeticiones de elementos de calendario periódicas que se han modificado para que sean diferentes que el elemento del patrón de periodicidad.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Contiene una matriz de ocurrencias eliminadas de un elemento de calendario periódico.  <br/> Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Representa la zona horaria de la ubicación donde se hospeda la reunión.  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |Representa la zona horaria de inicio del elemento de calendario.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Representa la zona horaria de finalización del elemento de calendario.  <br/> |
|[ConferenceType](conferencetype.md) <br/> |Describe el tipo de conferencia que se realiza con un elemento de calendario.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Representa si se puede proponer una nueva hora de reunión para una reunión.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Indica si la reunión está en línea.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Contiene la dirección URL del área de reuniones que está vinculada al elemento de calendario.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Especifica la dirección URL de una reunión en línea de Microsoft NetShow.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta. Este elemento es de sólo lectura.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contiene el nombre para mostrar del último usuario que modificó un elemento.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indica cuándo se modificó por última vez un elemento.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indica si el elemento está asociado a una carpeta.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de un elemento o una conversación.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.  <br/> |
|[EXCLUSIVO](uid.md) <br/> |Identifica un elemento de calendario.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Se usa para identificar una instancia específica de un elemento de calendario periódico.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Indica la fecha y la hora en que se creó una instancia de un objeto iCalendar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Identifica todos los elementos del calendario adyacentes a una hora de reunión.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se van a anexar a una sola propiedad de un elemento durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con una hora de reunión.  <br/> |
|[Crear (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento que se va a crear en el almacén de cliente local.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que se van a crear.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[Actualización (ItemSync)](update-itemsync.md) <br/> |Identifica un elemento único para actualizar en el almacén de cliente local.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


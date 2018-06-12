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
ms.openlocfilehash: 3e290613293cb6ad1563912e5015742ffc503d08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836450"
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto representado en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange. Esta propiedad es de sólo lectura.  <br/> |
|[Id](parentfolderid.md) <br/> |Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Subject](subject.md) <br/> |Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta. El asunto está limitado a 255 caracteres.  <br/> |
|[Sensibilidad](sensitivity.md) <br/> |Indica el nivel de confidencialidad de un elemento.  <br/> |
|[Body](body.md) <br/> |Representa el contenido real del cuerpo de un mensaje.  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Representa los datos y la hora en que se recibió un elemento en un buzón de correo.  <br/> |
|[Size](size.md) <br/> |Representa el tamaño en bytes de un elemento. Esta propiedad es de sólo lectura.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.  <br/> |
|[Importancia](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Representa el identificador del elemento al que este elemento es una respuesta.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Indica si un elemento no se ha enviado todavía.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario envía un elemento a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se había enviado anteriormente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si el elemento se ha modificado.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensaje de Internet dentro de un elemento en un buzón de correo.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y hora en que se envió un elemento en un buzón de correo.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y hora cuando se produce el evento. Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea CC. Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de CC.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea para. Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible. Esta propiedad es de sólo lectura.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas en carpetas y elementos.  <br/> |
|[Referencia cultural](culture.md) <br/> |Representa la referencia cultural para un elemento determinado en un buzón de correo.  <br/> |
|[Sender](sender.md) <br/> |Identifica el remitente de un elemento.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Contiene un conjunto de destinatarios de un mensaje.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Representa una colección de los destinatarios que recibirán una copia del mensaje.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita una confirmación de lectura.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita una confirmación de entrega.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Representa el identificador de conversación.  <br/> |
|[From](from.md) <br/> |Representa al destinatario de la que se envió el mensaje.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Representa el identificador de mensaje de Internet de un elemento.  <br/> |
|[Estáleído](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Indica si se ha solicitado una respuesta a un mensaje de correo electrónico.  <br/> |
|[Referencias](references.md) <br/> |Representa el encabezado de Usenet que se usa para correlacionar las respuestas con sus mensajes originales.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifica un conjunto de direcciones a la que se deben enviar las respuestas.  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |Representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md).  <br/> |
|[IsDelegated](isdelegated.md) <br/> |Indica si una reunión se ha controlado por una cuenta con acceso de delegado.  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |Indica si un mensaje de reunión no está actualizado.  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |Indica si un mensaje de reunión item se han procesado.  <br/> |
|[ResponseType](responsetype.md) <br/> |Representa el tipo de destinatario respuesta que se recibió para una reunión.  <br/> |
|[MeetingRequestType](meetingrequesttype.md) <br/> |Describe el tipo de la convocatoria de reunión.  <br/> |
|[IntendedFreeBusyStatus](intendedfreebusystatus.md) <br/> |Representa el estado deseado para el elemento de calendario que está asociado con la convocatoria de reunión.  <br/> |
|[Start](start.md) <br/> |Representa el inicio de un elemento de calendario. Este elemento solo se aplica a una sola aparición de un elemento de calendario.  <br/> |
|[End](end-ex15websvcsotherref.md) <br/> |Representa el final de una duración. Este elemento solo se aplica a una sola aparición de un elemento de calendario.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Representa la hora de inicio original de un elemento de calendario.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Indica si una convocatoria de reunión o elemento de calendario representa un evento de día completo.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Representa el estado de disponibilidad del elemento de calendario.  <br/> |
|[Location](location.md) <br/> |Representa la ubicación de una reunión o una cita.  <br/> |
|[When](when.md) <br/> |Proporciona una descripción de cuándo se produce una reunión.  <br/> |
|[IsMeeting](ismeeting.md) <br/> |Indica si el elemento de calendario es una reunión o una cita.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Indica si se ha cancelado una reunión o cita.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Indica si un elemento de calendario es parte de un elemento periódico. Este elemento es de sólo lectura.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Indica si se ha enviado una convocatoria de reunión a los asistentes solicitados.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Representa el tipo de aparición de un elemento de calendario.  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |Contiene el estado de o la respuesta a un elemento de calendario.  <br/> |
|[Organizer](organizer.md) <br/> |Representa el organizador de una reunión.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Representa a los asistentes necesarios para asistir a una reunión.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Representa a los asistentes que no sean necesarios para asistir a una reunión.  <br/> |
|[Recursos](resources.md) <br/> |Representa un recurso para una reunión programado.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Representa el número de las reuniones que entre en conflicto con la convocatoria de reunión.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Representa el número total de elementos de calendario que están junto a una hora de reunión.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario que están junto a una hora de reunión.  <br/> |
|[Duración (elementos)](duration-items.md) <br/> |Representa la duración de un elemento de calendario.  <br/> |
|[TimeZone (elemento)](timezone-item.md) <br/> |Proporciona una descripción de texto de una zona horaria.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Representa la fecha y hora cuando se responde un asistente a una convocatoria de reunión.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Especifica el número de secuencia de una versión de una cita.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Especifica el estado de la cita.  <br/> |
|[Periodicidad (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento periódico del calendario.  <br/> Este elemento es válida si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última aparición de un elemento periódico del calendario.  <br/> Este elemento es válida si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contiene una matriz de periódica repeticiones del elemento de calendario que se han modificado para que sean diferentes que el elemento de patrón de periodicidad.  <br/> Este elemento es válida si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Contiene una matriz de eliminado apariciones de un elemento periódico del calendario.  <br/> Este elemento es válida si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Representa la zona horaria de la ubicación donde se hospeda la reunión.  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |Representa la zona de hora de inicio del elemento de calendario.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Representa la zona horaria de final del elemento de calendario.  <br/> |
|[ConferenceType](conferencetype.md) <br/> |Describe el tipo de conferencia que se lleva a cabo con un elemento de calendario.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Representa si se puede proponer una nueva hora de reunión para una reunión.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Indica si la reunión está en línea.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Contiene la dirección URL para el área de reuniones que está vinculado el elemento de calendario.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Especifica la dirección URL de una reunión en línea de Microsoft Netshow.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta. Este elemento es de sólo lectura.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contiene el nombre para mostrar del último usuario para modificar un elemento.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indica cuándo se modificó por última vez un elemento.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indica si el elemento está asociado a una carpeta.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de un elemento o conversación.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.  <br/> |
|[UID](uid.md) <br/> |Identifica un elemento de calendario.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Se usa para identificar una instancia específica de un elemento periódico del calendario.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Indica la fecha y hora en que se ha creado una instancia de un objeto de iCalendar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Identifica todos los elementos de calendario que están junto a una hora de reunión.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.  <br/> |
|[Crear (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento para crear en el almacén de cliente local.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que desea crear.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[Actualización (ItemSync)](update-itemsync.md) <br/> |Identifica un solo elemento que se debe actualizar en el almacén de cliente local.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


---
title: ResponseCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 4b84d670-74c9-4d6d-84e7-f0a9f76f0d93
description: El elemento ResponseCode proporciona información de estado sobre la solicitud.
ms.openlocfilehash: 6481272c61aab3dc9aeb2fd988e3544169306f06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457469"
---
# <a name="responsecode"></a>ResponseCode

El elemento **ResponseCode** proporciona información de estado sobre la solicitud. 
  
- [ResponseMessage](responsemessage.md) 
- [ResponseCode](responsecode.md)
  
```XML
<ResponseCode/>
```

**ResponseCodeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|Elemento|Descripción|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Proporciona información descriptiva sobre el estado de la respuesta.<br/><br/>  Las siguientes son las posibles expresiones de XPath a este elemento:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación DeleteItem](deleteitem-operation.md) .  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación SendItem](senditem-operation.md) .  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación DeleteFolder](deletefolder-operation.md) .  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación DeleteAttachment](deleteattachment-operation.md) .  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación de cancelación de suscripción](unsubscribe-operation.md) .  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetFolder](getfolder-operation.md) .  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación UpdateFolder](updatefolder-operation.md) .  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación MoveFolder](movefolder-operation.md) .  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación CopyFolder](copyfolder-operation.md).  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación CreateManagedFolder](createmanagedfolder-operation.md) .  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación FindFolder](findfolder-operation.md) .  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateItem](createitem-operation.md) .  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetItem](getitem-operation.md) .  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación UpdateItem](updateitem-operation.md) .  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación MoveItem](moveitem-operation.md) .  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CopyItem](copyitem-operation.md) .  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación CreateAttachment](createattachment-operation.md) .  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetAttachment](getattachment-operation.md) .  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación FindItem](finditem-operation.md) .  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación ResolveNames](resolvenames-operation.md) .  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación ExpandDL](expanddl-operation.md) .  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación subscribe](subscribe-operation.md) .  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetEvents](getevents-operation.md) .  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de operación SendNotification.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación SyncFolderHierarchy](syncfolderhierarchy-operation.md) .  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación SyncFolderItems](syncfolderitems-operation.md) .  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación AddDelegate](adddelegate-operation.md) .  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación RemoveDelegate](removedelegate-operation.md) .  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación UpdateDelegate](updatedelegate-operation.md) .  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetServerTimeZones](getservertimezones-operation.md) .  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud de [operación de GetSharingFolder](getsharingfolder-operation.md) .  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Define una respuesta a una solicitud de [operación de GetSharingMetadata](getsharingmetadata-operation.md) .  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación RefreshSharingFolder](refreshsharingfolder-operation.md) .  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud de [operación de RefreshSharingFolder](refreshsharingfolder-operation.md) .  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Contiene el estado y los resultados de una respuesta de [operación FindConversation](findconversation-operation.md) .  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud de [operación ApplyConversationAction](applyconversationaction-operation.md) .  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación EmptyFolder](emptyfolder-operation.md) .  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación UpdateInboxRules](updateinboxrules-operation.md) .  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación UploadItems](uploaditems-operation.md) .  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Contiene una respuesta a una [GetInboxRules Operation](getinboxrules-operation.md) * * * * request.  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Contiene una respuesta a una solicitud de [operación GetServiceConfiguration](getserviceconfiguration-operation.md) .  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene las opciones de configuración del servicio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Es necesario un valor de texto si se usa este elemento. En la tabla siguiente se describen los valores que se devuelven con este elemento.
  
|Valor|Description|
|:-----|:-----|
|NoError  <br/> |No se ha producido ningún error en la solicitud.  <br/> |
|ErrorAccessDenied  <br/> |Este error se produce cuando la cuenta que realiza la llamada no tiene los derechos necesarios para realizar la acción solicitada.  <br/> |
|ErrorAccessModeSpecified  <br/> |Este error es solo para uso interno. Este error no se devuelve.  <br/> |
|ErrorAccountDisabled  <br/> |Este error se produce cuando se ha deshabilitado la cuenta en cuestión.  <br/> |
|ErrorAddDelegatesFailed  <br/> |Este error se produce cuando no se puede guardar una lista con delegados agregados.  <br/> |
|ErrorAddressSpaceNotFound  <br/> |Este error se produce cuando no se encuentra el registro del espacio de direcciones o el nombre de dominio del sistema de nombres de dominio (DNS) para la disponibilidad entre bosques en la base de datos de Active Directory.  <br/> |
|ErrorADOperation  <br/> |Este error se produce cuando se produjo un error en la operación debido a problemas de comunicación con los servicios de dominio de Active Directory (AD DS).  <br/> |
|ErrorADSessionFilter  <br/> |Este error se devuelve cuando una solicitud de operación de **ResolveNames** especifica un nombre que no es válido.  <br/> |
|ErrorADUnavailable  <br/> |Este error se produce cuando AD DS no está disponible. Vuelva a intentar la solicitud más adelante.  <br/> |
|ErrorAffectedTaskOccurrencesRequired  <br/> |Este error indica que no se ha especificado el atributo **AffectedTaskOccurrences** . Cuando se usa el elemento [DeleteItem](deleteitem.md) para eliminar al menos un elemento que es una tarea, y independientemente de si la tarea es periódica o no, se debe especificar el atributo **AffectedTaskOccurrences** para que **DeleteItem** pueda determinar si se elimina la ocurrencia actual o toda la serie.  <br/> |
|ErrorArchiveFolderPathCreation  <br/> |Indica un error en la creación de la ruta de acceso a la carpeta de archivo.  <br/> |
|ErrorArchiveMailboxNotEnabled  <br/> |Indica que el buzón de archivo no está habilitado.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |Indica que no se pudo detectar el servicio de buzón de archivo.  <br/> |
|ErrorAttachmentNestLevelLimitExceeded  <br/> |Especifica que se ha intentado crear un elemento con más de 10 datos adjuntos anidados. Este valor se introdujo en Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|ErrorAttachmentSizeLimitExceeded  <br/> |El elemento [CreateAttachment](createattachment.md) devuelve este error si se intenta crear un dato adjunto con un tamaño superior a Int32. MaxValue, en bytes.  <br/> El elemento [GetAttachment](getattachment.md) devuelve este error si se intenta recuperar datos adjuntos existentes con un tamaño superior a Int32. MaxValue, en bytes.  <br/> |
|ErrorAutoDiscoverFailed  <br/> |Este error indica que los servicios Web de Exchange intentaron determinar la ubicación de un equipo entre bosques que ejecuta Exchange 2010 y que tiene el rol de servidor acceso de clientes instalado mediante el servicio Detección automática, pero se produjo un error en la llamada al servicio Detección automática.  <br/> |
|ErrorAvailabilityConfigNotFound  <br/> |Este error indica que falta la información de configuración de disponibilidad del bosque local en AD DS.  <br/> |
|ErrorBatchProcessingStopped  <br/> | Este error indica que se produjo una excepción al procesar un elemento y que es probable que se produzca una excepción para los elementos que siguen. Las solicitudes pueden incluir varios elementos; por ejemplo, una solicitud de la operación GetItem puede incluir varios identificadores. En general, los elementos se procesan de uno en uno. Si se produce una excepción al procesar un elemento y es probable que se produzca una excepción para los elementos que siguen, los siguientes no se procesarán.  <br/><br/>  Los siguientes son ejemplos de errores que detendrán el procesamiento de los elementos siguientes:<br/>  <br/>- ErrorAccessDenied  <br/>- ErrorAccountDisabled  <br/>- ErrorADUnavailable  <br/>- ErrorADOperation  <br/>- ErrorConnectionFailed  <br/>- ErrorMailboxStoreUnavailable  <br/>- ErrorMailboxMoveInProgress  <br/>- ErrorPasswordChangeRequired  <br/>- ErrorPasswordExpired  <br/>- ErrorQuotaExceeded  <br/>- ErrorInsufficientResources  <br/> |
|ErrorCalendarCannotMoveOrCopyOccurrence  <br/> |Este error se produce cuando se realiza un intento de mover o copiar una ocurrencia de un elemento de calendario periódico.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> | Este error se produce cuando se intenta actualizar un elemento de calendario que se encuentra en la carpeta elementos eliminados y cuando las actualizaciones o cancelaciones de reunión se envían de acuerdo con el valor del atributo **SendMeetingInvitationsOrCancellations** . <br/><br/>A continuación se muestran los valores posibles para este atributo:  <br/><br/>- SendToAllAndSaveCopy  <br/>- SendToChangedAndSaveCopy  <br/>- SendOnlyToAll  <br/>- SendOnlyToChanged  <br/>  <br/>Sin embargo, esta actualización solo se permite cuando el valor de este atributo está establecido en SendToNone.  <br/> |
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |Este error se produce cuando se llama a la operación UpdateItem, GetItem, DeleteItem, MoveItem, CopyItem o SendItem y el identificador especificado no es un identificador de ocurrencia de ningún elemento de calendario periódico.  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |Este error se produce cuando se llama a la operación **UpdateItem**, **GetItem**, **DeleteItem**, **MOVEITEM**, **CopyItem**o **SendItem** y el identificador especificado no es un identificador de ningún elemento maestro periódico.  <br/> |
|ErrorCalendarDurationIsTooLong  <br/> |Este error se produce durante una operación **CreateItem** o **UpdateItem** cuando la duración de un elemento de calendario es superior a la cantidad máxima permitida, que actualmente es de 5 años.  <br/> |
|ErrorCalendarEndDateIsEarlierThanStartDate  <br/> |Este error se produce cuando una hora de finalización del calendario se establece en la misma hora o después de la hora de inicio.  <br/> |
|ErrorCalendarFolderIsInvalidForCalendarView  <br/> |Este error se produce cuando la carpeta especificada para una operación **FindItem** con un elemento [CalendarView](calendarview.md) no es del tipo de carpeta de calendario.  <br/> |
|ErrorCalendarInvalidAttributeValue  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorCalendarInvalidDayForTimeChangePattern  <br/> |Este error se produce durante una operación **CreateItem** o **UpdateItem** cuando se usan valores no válidos de Day, WeekendDay y Weekday para definir el patrón de cambio de hora.  <br/> |
|ErrorCalendarInvalidDayForWeeklyRecurrence  <br/> |Este error se produce durante una operación **CreateItem** o **UpdateItem** cuando se usan valores no válidos de día, día de la semana y WeekendDay para especificar la periodicidad semanal.  <br/> |
|ErrorCalendarInvalidPropertyState  <br/> |Este error se produce cuando el estado de un objeto binario grande (BLOB) en periodicidad de un elemento de calendario del almacén de Exchange no es válido.  <br/> |
|ErrorCalendarInvalidPropertyValue  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorCalendarInvalidRecurrence  <br/> |Este error se produce cuando no se puede crear la periodicidad especificada.  <br/> |
|ErrorCalendarInvalidTimeZone  <br/> |Este error se produce cuando se encuentra una zona horaria no válida.  <br/> |
|ErrorCalendarIsCancelledForAccept  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForDecline  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForRemove  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForTentative  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsDelegatedForAccept  <br/> |Este error indica que el elemento [AcceptItem](acceptitem.md) no es válido para un elemento de calendario o una convocatoria de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsDelegatedForDecline  <br/> |Este error indica que el elemento [DeclineItem](declineitem.md) no es válido para un elemento de calendario o una convocatoria de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsDelegatedForRemove  <br/> |Este error indica que el elemento [RemoveItem](removeitem.md) no es válido para una cancelación de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsDelegatedForTentative  <br/> |Este error indica que el elemento [TentativelyAcceptItem](tentativelyacceptitem.md) no es válido para un elemento de calendario o una convocatoria de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsNotOrganizer  <br/> |Este error indica que la operación (actualmente, CancelItem) en el elemento de calendario no es válida para un asistente. Solo el organizador de la reunión puede cancelar la reunión.  <br/> |
|ErrorCalendarIsOrganizerForAccept  <br/> |Este error indica que [AcceptItem](acceptitem.md) no es válido para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarIsOrganizerForDecline  <br/> |Este error indica que [DeclineItem](declineitem.md) no es válido para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarIsOrganizerForRemove  <br/> |Este error indica que [RemoveItem](removeitem.md) no es válido para el elemento de calendario del organizador. Para quitar una reunión del calendario, el organizador debe usar CancelCalendarItem.  <br/> |
|ErrorCalendarIsOrganizerForTentative  <br/> |Este error indica que [TentativelyAcceptItem](tentativelyacceptitem.md) no es válido para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarMeetingRequestIsOutOfDate  <br/> |Este error indica que una convocatoria de reunión está obsoleta y no se puede actualizar.  <br/> |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange  <br/> |Este error indica que el índice de ocurrencia no apunta a una ocurrencia dentro de la periodicidad actual. Por ejemplo, si el patrón de periodicidad define un conjunto de tres repeticiones de reunión y se intenta obtener acceso a la quinta ocurrencia, se producirá este código de respuesta.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Este error indica que cualquier operación que se produzca en una ocurrencia eliminada (a través del identificador maestro periódico y del índice de ocurrencia) no es válida.  <br/> |
|ErrorCalendarOutOfRange  <br/> |Este error se notifica en las operaciones CreateItem y UpdateItem para los elementos de calendario o las propiedades de periodicidad de la tarea cuando el valor de la propiedad está fuera del intervalo. Por ejemplo, si especificas la decimoquinta semana del mes, se obtendrá este código de respuesta.  <br/> |
|ErrorCalendarViewRangeTooBig  <br/> |Este error se produce cuando el intervalo de inicio al final del elemento [CalendarView](calendarview.md) es mayor que el máximo permitido actualmente en 2 años.  <br/> |
|ErrorCallerIsInvalidADAccount  <br/> |Este error indica que la cuenta que se está solicitando no es una cuenta válida en la base de datos del directorio.  <br/> |
|ErrorCannotArchiveCalendarContactTaskFolderException  <br/> |Indica que se ha intentado archivar una carpeta de tareas de contacto de calendario.  <br/> |
|ErrorCannotArchiveItemsInPublicFolders  <br/> |Indica que se ha realizado un intento de archivar elementos en carpetas públicas.  <br/> |
|ErrorCannotArchiveItemsInArchiveMailbox  <br/> |Indica que se ha intentado archivar elementos en el buzón de archivo.  <br/> |
|ErrorCannotCreateCalendarItemInNonCalendarFolder  <br/> |Este error se produce cuando se crea un elemento de calendario y el atributo **SavedItemFolderId** hace referencia a una carpeta que no está en el calendario.  <br/> |
|ErrorCannotCreateContactInNonContactFolder  <br/> |Este error se produce cuando se crea un contacto y el atributo **SavedItemFolderId** hace referencia a una carpeta que no es de contacto.  <br/> |
|ErrorCannotCreatePostItemInNonMailFolder  <br/> |Este error indica que no se puede crear un elemento post en una carpeta que no sea una carpeta de correo, como calendario, contacto, tareas, notas, etc.  <br/> |
|ErrorCannotCreateTaskInNonTaskFolder  <br/> |Este error se produce cuando se crea una tarea y el atributo **SavedItemFolderId** hace referencia a una carpeta que no pertenece a la tarea.  <br/> |
|ErrorCannotDeleteObject  <br/> |Este error se produce cuando no se puede eliminar el elemento o la carpeta que se va a eliminar.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |La [operación DeleteItem](deleteitem-operation.md) devuelve este error cuando no puede eliminar la ocurrencia actual de una tarea repetitiva. Esto solo puede ocurrir si el atributo **AffectedTaskOccurrences** se ha establecido en SpecifiedOccurrenceOnly.  <br/> |
|ErrorCannotDisableMandatoryExtension  <br/> |Indica que se ha intentado deshabilitar una extensión mandatorty.  <br/> |
|ErrorCannotEmptyFolder  <br/> |Este error debe devolverse cuando el servidor no puede vaciar una carpeta.  <br/> |
|ErrorCannotGetSourceFolderPath  <br/> |Indica que no se pudo recuperar la ruta de acceso de la carpeta de origen.  <br/> |
|ErrorCannotGetExternalEcpUrl  <br/> |Especifica que el servidor no pudo recuperar la dirección URL externa para las opciones de Outlook Web App.  <br/> |
|ErrorCannotOpenFileAttachment  <br/> |La operación **GetAttachment** devuelve este error si no puede recuperar el cuerpo de un archivo de datos adjuntos.  <br/> |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder  <br/> |Este error indica que el autor de la llamada intentó establecer permisos de calendario en una carpeta que no es de calendario.  <br/> |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder  <br/> |Este error indica que el autor de la llamada intentó establecer permisos que no son del calendario en una carpeta de calendario.  <br/> |
|ErrorCannotSetPermissionUnknownEntries  <br/> |Este error indica que no se pueden establecer permisos desconocidos en un conjunto de permisos.  <br/> |
|ErrorCannotSpecifySearchFolderAsSourceFolder  <br/> |Indica que se ha intentado especificar la carpeta de búsqueda como carpeta de origen.  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |Este error se produce cuando una solicitud que requiere un identificador de elemento recibe un identificador de carpeta.  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |Este error se produce cuando una solicitud que requiere un identificador de carpeta recibe un identificador de elemento.  <br/> |
|ErrorChangeKeyRequired  <br/> |Este código de respuesta ha sido reemplazado por **ErrorChangeKeyRequiredForWriteOperations** <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |Este error se devuelve cuando la clave de cambio de un elemento falta o está obsoleta. <br/><br/>Para las operaciones SendItem, UpdateItem y UpdateFolder, el autor de la llamada debe pasar una clave de cambio correcta y actual para el elemento. Tenga en cuenta que este es el caso con UpdateItem incluso cuando la resolución de conflictos está configurada para sobrescribirse siempre.  <br/> |
|ErrorClientDisconnected  <br/> |Especifica que el cliente se desconectó.  <br/> |
|ErrorClientIntentInvalidStateDefinition  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorClientIntentNotFound  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorConnectionFailed  <br/> |Este error se produce cuando los servicios Web de Exchange no se pueden conectar con el buzón.  <br/> |
|ErrorContainsFilterWrongType  <br/> |Este error indica que la propiedad que se ha inspeccionado para un filtro Contains no es un tipo de cadena.  <br/> |
|ErrorContentConversionFailed  <br/> |La operación **GetItem** devuelve este error cuando servicios web Exchange no puede recuperar el contenido MIME para el elemento solicitado. <br/><br/>La operación **CreateItem** devuelve este error cuando servicios web Exchange no puede crear el elemento a partir del contenido MIME proporcionado. Normalmente, esto indica que la propiedad del elemento está dañada o truncada.  <br/> |
|ErrorContentIndexingNotEnabled  <br/> |Este error se produce cuando se realiza una solicitud de búsqueda con la opción QueryString y la indización de contenido no está habilitada para el buzón de correo de destino.  <br/> |
|ErrorCorruptData  <br/> |Este error se produce cuando los datos están dañados y no se pueden procesar.  <br/> |
|ErrorCreateItemAccessDenied  <br/> |Este error se produce cuando el autor de la llamada no tiene permiso para crear el elemento.  <br/> |
|ErrorCreateManagedFolderPartialCompletion  <br/> |Este error se produce cuando no se pudo crear una o varias de las carpetas administradas que se especificaron en la solicitud de operación CreateManagedFolder. Busque cada carpeta para determinar las carpetas que se han creado y las carpetas que no existen.  <br/> |
|ErrorCreateSubfolderAccessDenied  <br/> |Este error se produce cuando la cuenta que realiza la llamada no tiene los permisos necesarios para crear la subcarpeta.  <br/> |
|ErrorCrossMailboxMoveCopy  <br/> |Este error se produce cuando se realiza un intento de mover un elemento o una carpeta de un buzón a otro. Si el buzón de origen y el buzón de destino son diferentes, recibirá este error.  <br/> |
|ErrorCrossSiteRequest  <br/> |Este error indica que la solicitud no está permitida porque el servidor de acceso de cliente que debería atender la solicitud se encuentra en un sitio diferente.  <br/> |
|ErrorDataSizeLimitExceeded  <br/> |Este error puede producirse en las siguientes situaciones:<br/>  <br/>-Se realiza un intento de acceso o escritura de una propiedad en un elemento y el valor de la propiedad es demasiado grande.<br/>-La longitud del contenido MIME codificado en Base64 en el XML de la solicitud supera el límite.<br/>-El tamaño del cuerpo de un cuerpo de elemento existente supera el límite.<br/>-El consumidor intenta establecer un cuerpo de texto o HTML cuya longitud (o la longitud combinada en el caso de append) supera el límite. |
|ErrorDataSourceOperation  <br/> |Este error se produce cuando el proveedor de datos subyacente no puede completar la operación.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Este error se produce en una operación **AddDelegate** si el usuario especificado ya existe en la lista de delegados.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Este error se produce en una operación **AddDelegate** cuando el usuario especificado que se va a agregar es el propietario del buzón.  <br/> |
|ErrorDelegateMissingConfiguration  <br/> |Este error se produce en una operación **GetDelegate** cuando no hay información de delegado en el mensaje de FreeBusy local o no hay ningún delegado público de Active Directory (ningún "delegado público" o ninguna entrada "enviar en nombre de" en AD DS).  <br/> |
|ErrorDelegateNoUser  <br/> |Este error se produce cuando no se puede asignar un usuario especificado a un usuario de AD DS.  <br/> |
|ErrorDelegateValidationFailed  <br/> |Este error se produce en la operación **AddDelegate** cuando un usuario delegado agregado no es válido.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Este error se produce cuando se realiza un intento para eliminar una carpeta distintiva.  <br/> |
|ErrorDeleteItemsFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorDeleteUnifiedMessagingPromptFailed  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorDistinguishedUserNotSupported  <br/> |Este error indica que un identificador de usuario distinguido no es válido para la operación. **DistinguishedUserType** no debe estar presente en la solicitud.  <br/> |
|ErrorDistributionListMemberNotExist  <br/> |Este error indica que no existe un miembro de la lista de distribución de solicitudes en la lista de distribución.  <br/> |
|ErrorDuplicateInputFolderNames  <br/> |Este error se produce cuando se especifican nombres de carpeta duplicados en el elemento [FolderNames](foldernames.md) de la solicitud de operación **CreateManagedFolder** .  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |Este error indica que hay encabezados SOAP duplicados.  <br/> |
|ErrorDuplicateUserIdsSpecified  <br/> |Este error indica que se ha encontrado un identificador de usuario duplicado en un conjunto de permisos, ya sea default o Anonymous más de una vez, o hay SID o destinatarios duplicados.  <br/> |
|ErrorEmailAddressMismatch  <br/> |Este error se produce cuando una solicitud intenta crear o actualizar los parámetros de búsqueda de una carpeta de búsqueda. Por ejemplo, esto puede ocurrir cuando se crea una carpeta de búsqueda en el buzón, pero la carpeta de búsqueda se dirige para buscar en otro buzón de correo.  <br/> |
|ErrorEventNotFound  <br/> |Este error se produce cuando el evento que está asociado a una marca de agua se elimina antes de que se devuelva el evento. Cuando se devuelve este error, la suscripción también se elimina.  <br/> |
|ErrorExceededConnectionCount  <br/> |Este error-indica que hay más solicitudes simultáneas en el servidor de las permitidas por la Directiva de un usuario.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |Este error indica que se ha superado el número máximo de suscripciones de la Directiva de limitación de un usuario.  <br/> |
|ErrorExceededFindCountLimit  <br/> |Este error indica que la llamada a una operación de búsqueda ha superado el número total de elementos que se pueden devolver.  <br/> |
|ErrorExpiredSubscription  <br/> |Este error se produce si se llama a la [operación GetEvents](getevents-operation.md) porque se está eliminando una suscripción porque ha expirado.  <br/> |
|ErrorExtensionNotFound  <br/> |Indica que no se ha encontrado la extensión.  <br/> |
|ErrorFolderCorrupt  <br/> |Este error se produce cuando la carpeta está dañada y no se puede guardar.  <br/> |
|ErrorFolderExists  <br/> |Este error se produce cuando se intenta crear una carpeta que tiene el mismo nombre que otra carpeta en el mismo elemento primario. No se permiten los nombres de carpeta duplicados.  <br/> |
|ErrorFolderNotFound  <br/> |Este error indica que el identificador de carpeta que se especificó no corresponde a una carpeta válida o que el delegado no tiene permiso para obtener acceso a la carpeta.  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |Este error indica que no se pudo recuperar la propiedad solicitada. Esto no indica que la propiedad no existe, pero que la propiedad estaba dañada de alguna manera para que se produjeron errores en la recuperación.  <br/> |
|ErrorFolderSave  <br/> |Este error indica que no se pudo crear o actualizar la carpeta debido a un estado no válido.  <br/> |
|ErrorFolderSaveFailed  <br/> |Este error indica que no se pudo crear o actualizar la carpeta debido a un estado no válido.  <br/> |
|ErrorFolderSavePropertyError  <br/> |Este error indica que no se pudo crear o actualizar la carpeta debido a valores de propiedad no válidos. El código de respuesta enumera las propiedades que han causado el problema.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |Este error indica que se ha alcanzado el número máximo de miembros del grupo para obtener información de disponibilidad para una lista de distribución.  <br/> |
|ErrorFreeBusyGenerationFailed  <br/> |Este error se devuelve cuando no se puede recuperar la información de disponibilidad debido a un error intermedio.  <br/> |
|ErrorGetServerSecurityDescriptorFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorImContactLimitReached  <br/> |Este error se devuelve cuando no se pueden agregar nuevos contactos de mensajería instantánea (mi) porque se ha alcanzado el número máximo de contactos. Este error se introdujo en Exchange Server 2013.  <br/> |
|ErrorImGroupDisplayNameAlreadyExists  <br/> |Este error se devuelve cuando se intenta agregar un nombre para mostrar de grupo cuando ya hay un grupo existente con el mismo nombre para mostrar. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorImGroupLimitReached  <br/> |Este error se devuelve cuando no se pueden agregar nuevos grupos de mensajería instantánea porque se ha alcanzado el número máximo de grupos. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorImpersonateUserDenied  <br/> |El error se devuelve en el caso de la autorización de servidor a servidor para la suplantación de Exchange cuando el autor de la llamada no tiene los derechos necesarios para suplantar al usuario específico en cuestión. Este error se asigna al derecho de Active Directory extendido MS-Exch-EPI-May-Impersonate.  <br/> |
|ErrorImpersonationDenied  <br/> |Este error se devuelve en la autorización de servidor a servidor para la suplantación de Exchange cuando el autor de la llamada no tiene los derechos necesarios para la suplantación a través del servidor de acceso de cliente con el que realizan la solicitud. Se asigna al derecho MS-Exch-EPI-suplantación extendida de Active Directory.  <br/> |
|ErrorImpersonationFailed  <br/> |Este error indica que se produjo un error inesperado cuando se intentó realizar la autenticación de servidor a servidor. Este código de respuesta suele indicar que la cuenta de servicio que ejecuta el grupo de aplicaciones de servicios web Exchange no está configurada correctamente, que los servicios Web de Exchange no pueden comunicarse con el directorio o que no se ha configurado correctamente una confianza entre bosques.  <br/> |
|ErrorIncorrectSchemaVersion  <br/> |Este error indica que la solicitud era válida para la versión actual de Exchange Server, pero no era válida para la versión del servidor de solicitud que se especificó.  <br/> |
|ErrorIncorrectUpdatePropertyCount  <br/> |Este error indica que cada descripción de cambio en los elementos [UpdateItem](updateitem.md) o [UpdateFolder](updatefolder.md) debe mostrar solo una propiedad para actualizar.  <br/> |
|ErrorIndividualMailboxLimitReached  <br/> |Este error se produce cuando la solicitud contiene demasiados asistentes para resolver. De forma predeterminada, el número máximo de asistentes que se deben resolver es de 100.  <br/> |
|ErrorInsufficientResources  <br/> |Este error se produce cuando el servidor de buzones de correo está sobrecargado. Vuelva a intentar la solicitud más adelante.  <br/> |
|ErrorInternalServerError  <br/> |Este error indica que servicios Web de Exchange detectó un error del que no se pudo realizar la recuperación, y que no existe un código de respuesta más específico asociado con el error que se produjo.  <br/> |
|ErrorInternalServerTransientError  <br/> |Este error indica que se ha producido un error interno del servidor y que debe volver a intentar la solicitud más adelante.  <br/> |
|ErrorInvalidAccessLevel  <br/> |Este error indica que el nivel de acceso que el autor de la llamada tiene en los datos de disponibilidad no es válido.  <br/> |
|ErrorInvalidArgument  <br/> |Este error indica un error causado por todos los argumentos no válidos pasados a la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).<br/><br/> Este error se devuelve en las siguientes situaciones: <br/><br/>-El usuario especificado en el parámetro _send-as_ no existe en el directorio. <br/>-El usuario especificado en el parámetro _send-as_ no es único en el directorio. <br/>-La dirección de _envío_ está vacía.<br/>-La dirección de _envío como_ no es una dirección de correo electrónico válida.  <br/> |
|ErrorInvalidAttachmentId  <br/> |Este error lo devuelve la [operación GetAttachment](getattachment-operation.md) o la [operación DeleteAttachment](deleteattachment-operation.md) cuando no se encuentran los datos adjuntos que corresponden al identificador especificado.  <br/> |
|ErrorInvalidAttachmentSubfilter  <br/> |Este error se produce cuando se intenta enlazar a una carpeta de búsqueda existente usando una restricción compleja de la tabla de datos adjuntos. Los servicios web Exchange solo admiten filtros de Contains simples en la tabla de datos adjuntos. Si intenta enlazar a una carpeta de búsqueda existente que tiene una restricción de tabla de datos adjuntos más compleja (un subfiltro), los servicios Web de Exchange no pueden representar el XML para ese filtro y devuelve este código de respuesta. <br/><br/>Tenga en cuenta que todavía puede llamar a la operación GetFolder en la carpeta, pero no solicitar el elemento [SearchParameters](searchparameters.md) .  <br/> |
|ErrorInvalidAttachmentSubfilterTextFilter  <br/> |Este error se produce cuando se intenta enlazar a una carpeta de búsqueda existente usando una restricción compleja de la tabla de datos adjuntos. Los servicios web Exchange solo admiten filtros de Contains simples en la tabla de datos adjuntos. <br/><br/>Si intenta enlazar a una carpeta de búsqueda existente que tiene una restricción de tabla de datos adjuntos más compleja, servicios web Exchange no puede representar el XML para ese filtro. En este caso, el subfiltro de datos adjuntos contiene un filtro de texto, pero no mira el nombre para mostrar de los datos adjuntos.<br/><br/> Tenga en cuenta que todavía puede llamar a la operación GetFolder en la carpeta, pero no solicitar el elemento [SearchParameters](searchparameters.md) .  <br/> |
|ErrorInvalidAuthorizationContext  <br/> | Este error indica que se ha producido un error en el procedimiento de autorización para el solicitante.  <br/> |
|ErrorInvalidChangeKey  <br/> |Este error se produce cuando un consumidor pasa una carpeta o un identificador de elemento con una clave de cambio que no se puede analizar. Por ejemplo, podría ser contenido Base64 no válido o una cadena vacía.  <br/> |
|ErrorInvalidClientSecurityContext  <br/> |Este error indica que se produjo un error interno cuando se intentó resolver la identidad del autor de la llamada.  <br/> |
|ErrorInvalidCompleteDate  <br/> |Este error se devuelve cuando se realiza un intento de establecer el valor del elemento [CompleteDate](completedate.md) de una tarea en una hora en el futuro. Cuando se convierte a la hora local del servidor de acceso de cliente, el [CompleteDate](completedate.md) de una tarea no se puede establecer en un valor que sea posterior a la hora local en el servidor de acceso de cliente.  <br/> |
|ErrorInvalidContactEmailAddress  <br/> |Este error indica que se proporcionó una dirección de correo electrónico no válida para un contacto.  <br/> |
|ErrorInvalidContactEmailIndex  <br/> |Este error indica que se proporcionó un valor de índice de correo electrónico no válido para una entrada de correo electrónico.  <br/> |
|ErrorInvalidCrossForestCredentials  <br/> |Este error se produce cuando las credenciales que se usan para redirigir una solicitud a otro bosque del servicio de directorio producen errores de autenticación.  <br/> |
|ErrorInvalidDelegatePermission  <br/> |Este error indica que los permisos de carpeta especificados no son válidos.  <br/> |
|ErrorInvalidDelegateUserId  <br/> |Este error indica que el identificador de usuario del delegado especificado no es válido.  <br/> |
|ErrorInvalidExchangeImpersonationHeaderData  <br/> |Este error se produce durante la suplantación de Exchange cuando una persona que llama no especifica un UPN, una dirección de correo electrónico o un SID de usuario. Esto también ocurrirá si el autor de la llamada especifica uno o varios de estos y los valores están vacíos.  <br/> |
|ErrorInvalidExcludesRestriction  <br/> |Este error se produce cuando no se puede analizar la máscara de la máscara que se ha pasado en una restricción del elemento [Exclude](excludes.md) .  <br/> |
|ErrorInvalidExpressionTypeForSubFilter  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidExtendedProperty  <br/> | Este error se produce cuando se producen los eventos siguientes: <br/> <br/>-El autor de la llamada intenta usar una propiedad extendida que no es compatible con los servicios Web de Exchange.  <br/>-El autor de la llamada pasa una combinación no válida de valores de atributo para una propiedad extendida. Esto también ocurre si no se pasan atributos. Solo se permiten determinadas combinaciones.  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |Este error se produce cuando la sección Value de una propiedad extendida no coincide con el tipo de la propiedad. <br/><br/>Por ejemplo, si se establece una propiedad extendida que tiene PropertyType = "String" en una matriz de enteros, se producirá este error. Cualquier representación de cadena que no sea convertible en el tipo especificado para la propiedad extendida proporcionará este error.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |Este error indica que el remitente de la invitación de uso compartido no ha creado los metadatos de la invitación para uso compartido.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |Este error indica que un mensaje para compartir no está destinado al autor de la llamada.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |Este error indica que los objetos de Federación de la organización del solicitante no están correctamente configurados.  <br/> |
|ErrorInvalidFolderId  <br/> |Este error se produce cuando el identificador de la carpeta está dañado.  <br/> |
|ErrorInvalidFolderTypeForOperation  <br/> |Este error indica que el tipo de carpeta especificado no es válido para la operación actual. Por ejemplo, no puede crear una carpeta de búsqueda en una carpeta pública.  <br/> |
|ErrorInvalidFractionalPagingParameters  <br/> | Este error se produce en la paginación fraccionada cuando el usuario ha especificado una de las siguientes opciones: <br/> <br/>-Un numerador que es mayor que el denominador  <br/>-Un numerador que es menor que cero  <br/>-Un denominador que sea menor o igual que cero  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |Este error indica que ambos elementos [DataType](datatype.md) y ShareFolderId están presentes en una solicitud.  <br/> |
|ErrorInvalidFreeBusyViewType  <br/> |Este error se produce cuando se llama a la [operación GetUserAvailability](getuseravailability-operation.md) con un [FreeBusyViewType](freebusyviewtype.md) de ninguno.  <br/> |
|ErrorInvalidId  <br/> |Este error indica que el identificador o la clave de cambio están mal formados.  <br/> |
|ErrorInvalidIdEmpty  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **ID** vacío.  <br/> |
|ErrorInvalidLikeRequest  <br/> |Este error se produce cuando no se puede gustar el elemento. Las versiones de Exchange que comienzan con el número de compilación 15.00.0913.09 incluyen este valor.  <br/> |
|ErrorInvalidIdMalformed  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **ID** que tiene un formato incorrecto.  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |Este error indica que se ha especificado un identificador de elemento o carpeta que usa el formato de Exchange 2007 para una solicitud con una versión de Exchange 2007 SP1 o posterior. No puede usar identificadores de Exchange 2007 en solicitudes de Exchange 2007 SP1 o posteriores. Debe usar la [operación ConvertId](convertid-operation.md) para convertirlos primero.  <br/> |
|ErrorInvalidIdMonikerTooLong  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **ID** demasiado largo.  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |Este error se devuelve cuando se pasa un identificador que no es un identificador de datos adjuntos al elemento a un método de servicio Web que espera un identificador de datos adjuntos.  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |Este error se produce cuando un contacto del buzón está dañado.  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **ID** demasiado largo.  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |Este error se devuelve cuando la jerarquía de datos adjuntos de un elemento supera el máximo de 255 niveles de profundidad.  <br/> |
|ErrorInvalidIdXml  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidImContactId  <br/> |Este error se devuelve cuando el identificador de contacto de mensajería instantánea especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidImDistributionGroupSmtpAddress  <br/> |Este error se devuelve cuando el identificador de dirección SMTP del grupo de distribución de mi especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidImGroupId  <br/> |Este error se devuelve cuando el identificador de grupo de mensajería instantánea especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidIndexedPagingParameters  <br/> |Este error se produce si el desplazamiento para la paginación indizada es negativo.  <br/> |
|ErrorInvalidInternetHeaderChildNodes  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidItemForOperationArchiveItem  <br/> |Indica que el elemento no era válido para una operación **ArchiveItem** .  <br/> |
|ErrorInvalidItemForOperationAcceptItem  <br/> |Este error se produce cuando se intenta usar un objeto de respuesta AcceptItem para un tipo de elemento que no sea una convocatoria de reunión o un elemento de calendario, o cuando se realiza un intento de aceptar una ocurrencia de un elemento de calendario que se encuentra en la carpeta elementos eliminados.  <br/> |
|ErrorInvalidItemForOperationCancelItem  <br/> |Este error se produce cuando se intenta usar un objeto de respuesta CancelItem en un tipo de elemento que no sea un elemento de calendario.  <br/> |
|ErrorInvalidItemForOperationCreateItemAttachment  <br/> | Este error se devuelve cuando se realiza un intento de crear un elemento adjunto de un tipo no admitido.  <br/><br/>  Los tipos de elementos admitidos para los datos adjuntos de elementos incluyen los siguientes objetos:  <br/><br/>- [Punto](item.md) <br/>- [Mensaje](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Tareas](task.md) <br/>- [Contact](contact.md) <br/> <br/> Por ejemplo, si intenta crear un archivo adjunto de [MeetingMessage](meetingmessage.md) , encontrará este código de respuesta.  <br/> |
|ErrorInvalidItemForOperationCreateItem  <br/> | Este error se devuelve desde una [operación CreateItem](createitem-operation.md) si la solicitud contiene un tipo de elemento no admitido. <br/><br/>Los elementos admitidos incluyen los siguientes objetos:<br/>  <br/>- [Punto](item.md) <br/>- [Mensaje](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Tareas](task.md) <br/>- [Contact](contact.md) <br/><br/>  Ciertos tipos se crean como un efecto secundario de hacer otra cosa. Los mensajes de reunión se crean, por ejemplo, cuando se envía un elemento de calendario a los asistentes; no se crean explícitamente.  <br/> |
|ErrorInvalidItemForOperationDeclineItem  <br/> |Este error se produce cuando se intenta usar un objeto de respuesta de DeclineItem para un tipo de elemento que no sea una convocatoria de reunión o un elemento de calendario, o cuando se realiza un intento de rechazar una ocurrencia del elemento de calendario que se encuentra en la carpeta elementos eliminados.  <br/> |
|ErrorInvalidItemForOperationExpandDL  <br/> |Este error indica que la [operación ExpandDL](expanddl-operation.md) es válida sólo para listas de distribución privadas.  <br/> |
|ErrorInvalidItemForOperationRemoveItem  <br/> |Este error se devuelve desde un objeto de respuesta RemoveItem si la solicitud especifica un elemento que no es un elemento de cancelación de reunión.  <br/> |
|ErrorInvalidItemForOperationSendItem  <br/> |Este error se devuelve desde una [operación SendItem](senditem-operation.md) si la solicitud especifica un elemento que no es un elemento de mensaje.  <br/> |
|ErrorInvalidItemForOperationTentative  <br/> |Este error se produce cuando se intenta usar [TentativelyAcceptItem](tentativelyacceptitem.md) para un tipo de elemento que no sea una convocatoria de reunión o un elemento de calendario, o cuando se realiza un intento de aceptar provisionalmente una ocurrencia del elemento de calendario que se encuentra en la carpeta elementos eliminados.  <br/> |
|ErrorInvalidLogonType  <br/> |Este error es solo para uso interno. Este error no se devuelve.  <br/> |
|ErrorInvalidMailbox  <br/> |Este error indica que se produjo un error en la operación [CreateItem](createitem-operation.md) o en la [operación UpdateItem](updateitem-operation.md) al crear o actualizar una lista de distribución personal.  <br/> |
|ErrorInvalidManagedFolderProperty  <br/> |Este error se produce cuando la estructura de la carpeta administrada está dañada y no se puede representar.  <br/> |
|ErrorInvalidManagedFolderQuota  <br/> |Este error se produce cuando la cuota que se establece en la carpeta administrada es menor que cero, lo que indica una carpeta administrada dañada.  <br/> |
|ErrorInvalidManagedFolderSize  <br/> |Este error se produce cuando el tamaño establecido en la carpeta administrada es menor que cero, lo que indica una carpeta administrada dañada.  <br/> |
|ErrorInvalidMergedFreeBusyInterval  <br/> |Este error se produce cuando el valor interno de disponibilidad combinado proporcionado no es válido. El valor mínimo predeterminado es de 5 minutos. El valor máximo predeterminado es de 1440 minutos.  <br/> |
|ErrorInvalidNameForNameResolution  <br/> |Este error se produce cuando el nombre no es válido para la [operación ResolveNames](resolvenames-operation.md). Por ejemplo, una cadena de longitud cero, un solo espacio, una coma y un guión son nombres no válidos.  <br/> |
|ErrorInvalidNetworkServiceContext  <br/> |Este error indica un error en la cuenta de servicio de red en el servidor de acceso de cliente.  <br/> |
|ErrorInvalidOofParameter  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidOperation  <br/> | Se trata de un error general que se usa cuando la operación solicitada no es válida. <br/><br/>Por ejemplo, no puede hacer lo siguiente: <br/> <br/>-Realice un recorrido "profundo" mediante la [operación FindFolder](findfolder-operation.md) en una carpeta pública.  <br/>-Mueva o copie la raíz de la carpeta pública.  <br/>-Elimine un elemento asociado mediante cualquier modo excepto la eliminación "hard".  <br/>: Mover o copiar un elemento asociado.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |Este error indica que el autor de la llamada ha solicitado información de disponibilidad para un usuario de otra organización, pero la relación de la organización no tiene la disponibilidad habilitada.  <br/> |
|ErrorInvalidPagingMaxRows  <br/> |Este error se produce cuando un consumidor pasa un cero o un valor negativo para el número máximo de filas que se van a devolver.  <br/> |
|ErrorInvalidParentFolder  <br/> |Este error se produce cuando un consumidor pasa una carpeta principal no válida para una operación. Por ejemplo, se devuelve este error si intenta crear una carpeta dentro de una carpeta de búsqueda.  <br/> |
|ErrorInvalidPercentCompleteValue  <br/> |Este error se devuelve cuando se realiza un intento de establecer un porcentaje de finalización de tarea en un valor no válido. El valor debe estar entre 0 y 100 (inclusive).  <br/> |
|ErrorInvalidPermissionSettings  <br/> |Este error indica que el nivel de permisos es incoherente con la configuración de los permisos.  <br/> |
|ErrorInvalidPhoneCallId  <br/> |Este error indica que el identificador del autor de la llamada no es válido.  <br/> |
|ErrorInvalidPhoneNumber  <br/> |Este error indica que el número de teléfono no es correcto o no se ajusta a las reglas del plan de marcado.  <br/> |
|ErrorInvalidPropertyAppend  <br/> | Este error se produce cuando la propiedad que está intentando anexar no admite la anexión. <br/><br/>Las siguientes son las únicas propiedades que admiten la anexión: <br/> <br/>-Colecciones de destinatarios (ToRecipients, CcRecipients, BccRecipients)  <br/>-Collections Attendee (RequiredAttendees, OptionalAttendees, recursos)  <br/>-Body  <br/>-ReplyTo  <br/><br/>  Además, este error se produce cuando se anexa un cuerpo del mensaje si el formato especificado en la solicitud no coincide con el formato del elemento del almacén.  <br/> |
|ErrorInvalidPropertyDelete  <br/> |Este error se produce si la operación de eliminación se especifica en una [operación UpdateItem](updateitem-operation.md) o en una llamada a la [operación UpdateFolder](updatefolder-operation.md) para una propiedad que no admite la operación de eliminación. Por ejemplo, no se puede eliminar el elemento [Itemid](itemid.md) del objeto de [elemento](item.md) .  <br/> |
|ErrorInvalidPropertyForExists  <br/> |Este error se produce si el consumidor pasa una de las propiedades de la marca en un filtro [EXISTS](exists.md) . Por ejemplo, este error se produce si se especifican las marcas [IsRead](isread.md) o [IsFromMe](isfromme.md) en el elemento [EXISTS](exists.md) . En su lugar, la solicitud debe usar el elemento [IsEqualTo](isequalto.md) , ya que son marcas y, por lo tanto, parte de una única propiedad.  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |Este error se produce cuando la propiedad que está intentando manipular no admite la operación que se está realizando.  <br/> |
|ErrorInvalidPropertyRequest  <br/> | Este error se produce si una propiedad especificada en la solicitud no está disponible para el tipo de elemento. Por ejemplo, este error se devuelve si una propiedad que solo está disponible en los elementos del calendario se solicita en una llamada de [operación de GetItem](getitem-operation.md) para un mensaje o se actualiza en una llamada de [operación UpdateItem](updateitem-operation.md) para un mensaje. <br/> <br/>  Esto ocurre en las siguientes operaciones: <br/> <br/>- [GetItem Operation](getitem-operation.md) <br/>- [GetFolder Operation](getfolder-operation.md) <br/>- [Operación UpdateItem](updateitem-operation.md) <br/>- [Operación UpdateFolder](updatefolder-operation.md) <br/> |
|ErrorInvalidPropertySet  <br/> |Este error indica que la propiedad que está intentando manipular no es compatible con la operación que se está realizando. Por ejemplo, este error se devuelve si la propiedad que está intentando establecer es de sólo lectura.  <br/> |
|ErrorInvalidPropertyUpdateSentMessage  <br/> | Este error se produce durante una [operación de UpdateItem](updateitem-operation.md) cuando un cliente intenta actualizar determinadas propiedades de un mensaje que ya se ha enviado.<br/><br/> Por ejemplo, las siguientes propiedades no se pueden actualizar en un mensaje enviado: <br/> <br/>- [IsReadReceiptRequested](isreadreceiptrequested.md) <br/>- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |
|ErrorInvalidProxySecurityContext  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidPullSubscriptionId  <br/> |Este error se produce si se llama a la [operación GetEvents](getevents-operation.md) o a la [operación unsubscribe](unsubscribe-operation.md) mediante un identificador de suscripción de inserción. Para cancelar la suscripción a una suscripción de inserción, debe responder a una solicitud de inserción con una respuesta de cancelación de suscripción o desconectar el servicio Web y esperar a que las notificaciones de inserción superen el tiempo de espera.  <br/> |
|ErrorInvalidPushSubscriptionUrl  <br/> | Este error lo devuelve la [operación subscribe](subscribe-operation.md) cuando crea una suscripción "push" e indica que la dirección URL que se incluye en la solicitud no es válida.<br/><br/>Para que los servicios Web de Exchange acepten la dirección URL, se deben cumplir las siguientes condiciones: <br/> <br/>-Longitud de la cadena \> 0 y \< 2083.  <br/> -Protocol es http o https.  <br/>-La clase URI puede analizar la dirección URL de Microsoft .NET Framework.  <br/> |
|ErrorInvalidRecipients  <br/> |Este error indica que la colección de destinatarios de su mensaje o de la colección de asistentes en el elemento de calendario no es válida. Por ejemplo, se devolverá este error cuando se intente enviar un elemento que no tenga destinatarios.  <br/> |
|ErrorInvalidRecipientSubfilter  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que los servicios web Exchange no pueden representar. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterComparison  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que los servicios web Exchange no pueden representar. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterOrder  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que los servicios web Exchange no pueden representar. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterTextFilter  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que los servicios web Exchange no pueden representar. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidReferenceItem  <br/> | Este error se devuelve desde la [operación CreateItem](createitem-operation.md) para los objetos Response y reply Response en los siguientes escenarios:<br/>  <br/>-El identificador de elemento al que se hace referencia no es un [mensaje](message-ex15websvcsotherref.md), un [CalendarItem](calendaritem.md)o un descendiente de un **mensaje** o **CalendarItem**.  <br/>-El identificador de elemento de referencia es para un **CalendarItem** y el organizador está intentando responder o responder a responder a sí mismo.  <br/>-El mensaje es un borrador y reply o ReplyAll está seleccionado.  <br/>-El elemento de referencia, para [SuppressReadReceipt](suppressreadreceipt.md), no es un **mensaje** o un descendiente de un **mensaje**.  <br/> |
|ErrorInvalidRequest  <br/> |Este error se produce cuando la solicitud SOAP tiene un encabezado de acción SOAP, pero no hay nada en el cuerpo SOAP. Tenga en cuenta que el encabezado de acción SOAP no es necesario, ya que los servicios Web de Exchange pueden determinar el método al que llamar desde el nombre local del elemento raíz del cuerpo SOAP.  <br/> |
|ErrorInvalidRestriction  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidRetentionTagTypeMismatch  <br/> |Este error se devuelve cuando la etiqueta de retención especificada tiene asociada una acción incorrecta. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInvisible  <br/> |Este error se devuelve cuando se realiza un intento de establecer una etiqueta inexistente o invisible en una propiedad **PolicyTag** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInheritance  <br/> |Este error se devuelve cuando se realiza un intento de establecer una etiqueta implícita en la propiedad **PolicyTag** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagIdGuid  <br/> |Indica que el GUID de etiqueta de retención no es válido.  <br/> |
|ErrorInvalidRoutingType  <br/> |Este error se produce si el tipo de enrutamiento que se pasa para un elemento [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) no es válido. Normalmente, el tipo de enrutamiento se establece en Protocolo simple de transferencia de correo (SMTP).  <br/> |
|ErrorInvalidScheduledOofDuration  <br/> |Este error se produce si la hora de finalización de la duración especificada no es mayor que la hora de inicio o si la hora de finalización no se produce en el futuro.  <br/> |
|ErrorInvalidSchemaVersionForMailboxVersion  <br/> |Este error indica que una solicitud de proxy que se envió a otro servidor no puede atender la solicitud debido a un error de coincidencia de versiones.  <br/> |
|ErrorInvalidSecurityDescriptor  <br/> |Este error indica que el descriptor de seguridad de Exchange en la carpeta del calendario del almacén está dañado.  <br/> |
|ErrorInvalidSendItemSaveSettings  <br/> |Este error se produce al intentar enviar un elemento en el que se especifica [SavedItemFolderId](saveditemfolderid.md) en la solicitud, pero la propiedad **SaveItemToFolder** se establece en **false**.  <br/> |
|ErrorInvalidSerializedAccessToken  <br/> |Este error indica que el token que se pasó en el encabezado tiene un formato incorrecto, que no hace referencia a una cuenta válida del directorio o falta el grupo principal **ConnectingSID**.  <br/> |
|ErrorInvalidSharingData  <br/> |Este error indica que los metadatos de uso compartido no son válidos. Esto puede deberse a XML no válido.  <br/> |
|ErrorInvalidSharingMessage  <br/> |Este error indica que el mensaje para compartir no es válido. Esto puede deberse a que falta una propiedad.  <br/> |
|ErrorInvalidSid  <br/> |Este error se produce cuando se pasa un SID no válido en una solicitud.  <br/> |
|ErrorInvalidSIPUri  <br/> |Este error indica que el nombre SIP, el plan de marcado o el número de teléfono son URI SIP no válidos.  <br/> |
|ErrorInvalidServerVersion  <br/> |Este error indica que se ha especificado una versión de servidor de solicitudes no válida en la solicitud.  <br/> |
|ErrorInvalidSmtpAddress  <br/> |Este error se produce cuando no se puede analizar la dirección SMTP.  <br/> |
|ErrorInvalidSubfilterType  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidSubfilterTypeNotAttendeeType  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidSubfilterTypeNotRecipientType  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidSubscription  <br/> |Este error indica que la suscripción ya no es válida. Esto puede deberse a que el servidor de acceso de cliente se está reiniciando o a que la suscripción ha expirado.  <br/> |
|ErrorInvalidSubscriptionRequest  <br/> |Este error indica que la solicitud subscribe incluye varios identificadores de carpetas públicas. Una suscripción puede incluir varias carpetas del mismo buzón o un identificador de carpeta pública.  <br/> |
|ErrorInvalidSyncStateData  <br/> |[SyncFolderItems](syncfolderitems.md) o [SyncFolderHierarchy](syncfolderhierarchy.md) devuelve este error si los datos de [SyncState](syncstate-ex15websvcsotherref.md) que se pasan no son válidos. Para solucionar este error, debe volver a sincronizar sin el estado de sincronización. Asegúrese de que, si va a conservar los blobs de estado de sincronización, no trunque accidentalmente el BLOB.  <br/> |
|ErrorInvalidTimeInterval  <br/> |Este error indica que el intervalo de tiempo especificado no es válido. La hora de inicio debe ser superior o igual a la hora de finalización.  <br/> |
|ErrorInvalidUserInfo  <br/> |Este error indica que se especificó un [userid](userid.md) incoherente internamente para una operación de permisos. Por ejemplo, si se especifica un identificador de usuario distintivo (predeterminado o anónimo), se devuelve este error si también intenta especificar un SID o una dirección SMTP principal o nombre para mostrar para este usuario.  <br/> |
|ErrorInvalidUserOofSettings  <br/> |Este error indica que la configuración del usuario fuera de la oficina (OOF) no es válida debido a que falta una respuesta interna o externa.  <br/> |
|ErrorInvalidUserPrincipalName  <br/> |Este error se produce durante la suplantación de Exchange. El autor de la llamada pasó un UPN no válido en el encabezado SOAP que no era accesible en el directorio.  <br/> |
|ErrorInvalidUserSid  <br/> |Este error se produce cuando se pasa un SID no válido en una solicitud.  <br/> |
|ErrorInvalidUserSidMissingUPN  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidValueForProperty  <br/> |Este error indica que el valor de comparación de la restricción no es válido para la propiedad con la que se está comparando.<br/><br/> Por ejemplo, el valor de comparación de [DateTimeCreated](datetimecreated.md)  >  **true** devolvería este código de respuesta. <br/><br/>Este código de respuesta también se devuelve si se especifica una propiedad de enumeración en la comparación, pero el valor que se está comparando no es un valor válido para esa enumeración.  <br/> |
|ErrorInvalidWatermark  <br/> |Este error se debe a una marca de agua no válida.  <br/> |
|ErrorIPGatewayNotFound  <br/> |Este error indica que no hay disponible una puerta de enlace VoIP válida.  <br/> |
|ErrorIrresolvableConflict  <br/> |Este error indica que la resolución de conflictos no ha podido resolver los cambios de las propiedades. Los elementos de la tienda pueden haber cambiado y deben actualizarse. Recupere la clave de cambio actualizada y vuelva a intentarlo.  <br/> |
|ErrorItemCorrupt  <br/> |Este error indica que el estado del objeto está dañado y no se puede recuperar. Cuando se recupera un elemento, solo algunos elementos estarán en este estado, como [Body](body.md) y [MimeContent](mimecontent.md). Omita estos elementos y vuelva a intentar la operación.  <br/> |
|ErrorItemNotFound  <br/> |Este error se produce cuando no se encuentra el elemento o no tiene permiso para obtener acceso al elemento.  <br/> |
|ErrorItemPropertyRequestFailed  <br/> |Este error se produce si se produce un error en una solicitud de propiedad de un elemento. La propiedad puede existir, pero no se pudo recuperar.  <br/> |
|ErrorItemSave  <br/> |Este error se produce cuando se produce un error al intentar guardar el elemento o carpeta.  <br/> |
|ErrorItemSavePropertyError  <br/> |Este error se produce cuando se producen errores en los intentos de guardar el elemento o la carpeta debido a valores de propiedad no válidos. El código de respuesta incluye la ruta de acceso de las propiedades no válidas.  <br/> |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorLocalServerObjectNotFound  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorLogonAsNetworkServiceFailed  <br/> |Este error indica que el servicio de disponibilidad no ha podido iniciar sesión como servicio de red para el proxy de las solicitudes a los sitios o bosques apropiados. Esta respuesta suele indicar un error de configuración.  <br/> |
|ErrorMailboxConfiguration  <br/> |Este error indica que la información de buzón de correo en AD DS está configurada incorrectamente.  <br/> |
|ErrorMailboxDataArrayEmpty  <br/> |Este error indica que el elemento [MailboxDataArray](mailboxdataarray.md) de la solicitud está vacío. Debe proporcionar al menos un identificador de buzón.  <br/> |
|ErrorMailboxDataArrayTooBig  <br/> |Este error se produce cuando se proporcionan más de 100 entradas en un elemento [MailboxDataArray](mailboxdataarray.md) .  <br/> |
|ErrorMailboxFailover  <br/> |Este error indica que se produjo un error al intentar obtener acceso a un buzón porque el buzón está en un proceso de conmutación por error.  <br/> |
|ErrorMailboxHoldNotFound  <br/> |Indica que no se encontró la retención de buzones.  <br/> |
|ErrorMailboxLogonFailed  <br/> |Este error se produce cuando se produce un error en la conexión al buzón para obtener la información de la vista de calendario.  <br/> |
|ErrorMailboxMoveInProgress  <br/> | Este error indica que el buzón de correo se está moviendo a un servidor o almacén de buzones diferente. Este error también puede indicar que el buzón de correo está en otra base de datos de servidor o de buzones de correo.  <br/> |
|ErrorMailboxStoreUnavailable  <br/> | Este error indica que se produjo una de las siguientes condiciones de error:  <br/><br/>-El almacén del buzón está dañado.  <br/>-Se está deteniendo el almacén del buzón.  <br/>-El almacén del buzón está sin conexión.  <br/>-Se produjo un error de red cuando se intentó obtener acceso al almacén del buzón.  <br/>-El almacén del buzón está sobrecargado y no puede aceptar más conexiones.  <br/>-Se ha pausado el almacén de buzones.  <br/> |
|ErrorMailRecipientNotFound  <br/> |Este error se produce si la información del elemento [MailboxData](mailboxdata.md) no se puede asignar a una cuenta de buzón de correo válida.  <br/> |
|ErrorMailTipsDisabled  <br/> |Este error indica que las sugerencias de correo están deshabilitadas.  <br/> |
|ErrorManagedFolderAlreadyExists  <br/> |Este error se produce si la carpeta administrada que está intentando crear ya existe en un buzón.  <br/> |
|ErrorManagedFolderNotFound  <br/> |Este error se produce cuando el nombre de la carpeta que se especificó en la solicitud no se asigna a una definición de carpeta administrada en AD DS. Solo se pueden crear instancias de carpetas administradas para carpetas definidas en AD DS. Compruebe el nombre y vuelva a intentarlo.  <br/> |
|ErrorManagedFoldersRootFailure  <br/> |Este error indica que la raíz de carpetas administradas se eliminó del buzón o que existe una carpeta en la misma carpeta principal que tiene el nombre de la raíz de la carpeta administrada. Esto también ocurrirá si se produce un error al intentar crear la carpeta administrada raíz.  <br/> |
|ErrorMeetingSuggestionGenerationFailed  <br/> |Este error indica que el motor de sugerencias detectó un problema al intentar generar las sugerencias.  <br/> |
|ErrorMessageDispositionRequired  <br/> | Este error se produce si no se ha establecido el atributo **MessageDisposition** .<br/><br/> Este atributo es necesario para lo siguiente: <br/> <br/>-La [operación CreateItem](createitem-operation.md) y la [operación UpdateItem](updateitem-operation.md) cuando el elemento que se va a crear o actualizar es un [mensaje](message-ex15websvcsotherref.md).  <br/>- Objetos de respuesta [CancelCalendarItem](cancelcalendaritem.md), [AcceptItem](acceptitem.md), [DeclineItem](declineitem.md)o [TentativelyAcceptItem](tentativelyacceptitem.md) .  <br/> |
|ErrorMessageSizeExceeded  <br/> |Este error indica que el mensaje que está intentando enviar supera los límites permitidos.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |Este error indica que no se encuentra el dominio especificado.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |Este error indica que el servicio de seguimiento de mensajes no puede realizar el seguimiento del mensaje.  <br/> |
| ErrorMessageTrackingTransientError  <br/> |Este error indica que el servicio de seguimiento de mensajes está desactivado o no está disponible. Este código de error indica un error transitorio. Los clientes pueden volver a intentar conectarse al servidor cuando se recibe este error.  <br/> |
|ErrorMimeContentConversionFailed  <br/> |Este error se produce cuando el contenido MIME no es un iCal válido para una [operación CreateItem](createitem-operation.md). Para una [operación GetItem](getitem-operation.md), esta respuesta indica que no se pudo generar el contenido MIME.  <br/> |
|ErrorMimeContentInvalid  <br/> |Este error se produce cuando el contenido MIME no es válido.  <br/> |
|ErrorMimeContentInvalidBase64String  <br/> |Este error se produce cuando el contenido MIME de la solicitud no es una cadena base 64 válida.  <br/> |
|ErrorMissingArgument  <br/> |Este error indica que falta un argumento obligatorio en la solicitud. El texto del mensaje de respuesta indica el argumento que se va a comprobar.  <br/> |
|ErrorMissingEmailAddress  <br/> |Este error indica que ha especificado un identificador de carpeta distintivo en la solicitud, pero la cuenta que ha realizado la solicitud no tiene un buzón de correo en el sistema. En ese caso, debe proporcionar un subelemento [Mailbox](mailbox.md) en [DistinguishedFolderId](distinguishedfolderid.md).  <br/> |
|ErrorMissingEmailAddressForManagedFolder  <br/> |Este error indica que ha especificado un identificador de carpeta distintivo en la solicitud, pero la cuenta que ha realizado la solicitud no tiene un buzón de correo en el sistema. En ese caso, debe proporcionar un subelemento [Mailbox](mailbox.md) en [DistinguishedFolderId](distinguishedfolderid.md). Esta respuesta se devuelve desde la [operación CreateManagedFolder](createmanagedfolder-operation.md).  <br/> |
|ErrorMissingInformationEmailAddress  <br/> |Este error se produce si falta el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) .  <br/> |
|ErrorMissingInformationReferenceItemId  <br/> |Este error se produce si falta la [ReferenceItemId](referenceitemid.md) .  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |Este código de error no se devuelve nunca.  <br/> |
|ErrorMissingItemForCreateItemAttachment  <br/> |Este error se devuelve cuando se realiza un intento de no incluir el elemento item en el elemento **ItemAttachment** de una solicitud de [operación CreateAttachment](createattachment-operation.md) .  <br/> |
|ErrorMissingManagedFolderId  <br/> |Este error se produce cuando falta la propiedad IDs de Directiva, etiqueta de propiedad 0x6732, de la carpeta. Debe tener en cuenta que esta carpeta está dañada.  <br/> |
|ErrorMissingRecipients  <br/> |Este error indica que ha intentado enviar un elemento sin incluir a los destinatarios. Tenga en cuenta que si llama a la [operación CreateItem](createitem-operation.md) con una disposición de mensajes que provoque el envío del mensaje, obtendrá el siguiente código de respuesta: **ErrorInvalidRecipients**.  <br/> |
|ErrorMissingUserIdInformation  <br/> |Este error indica que no se ha especificado completamente un [userid](userid.md) en un conjunto de permisos.  <br/> |
|ErrorMoreThanOneAccessModeSpecified  <br/> |Este error indica que ha especificado más de un valor de elemento [ExchangeImpersonation](exchangeimpersonation.md) dentro de una solicitud.  <br/> |
|ErrorMoveCopyFailed  <br/> |Este error indica que no se pudo realizar la operación de mover o copiar. La operación de mover se produce en la [operación CreateItem](createitem-operation.md) cuando acepta una convocatoria de reunión que se encuentra en la carpeta elementos eliminados. Además, si rechaza una convocatoria de reunión, cancela un elemento de calendario o quita una reunión del calendario, ésta se mueve a la carpeta elementos eliminados.  <br/> |
|ErrorMoveDistinguishedFolder  <br/> |Este error se produce si intenta mover una carpeta distintiva.  <br/> |
|ErrorMultiLegacyMailboxAccess  <br/> |Este error se produce cuando una solicitud intenta acceder a varios servidores de buzones de correo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorNameResolutionMultipleResults  <br/> |Este error se produce si la [operación ResolveNames](resolvenames-operation.md) devuelve más de un resultado o el nombre ambiguo que ha especificado coincide con más de un objeto del directorio. El código de respuesta incluye los nombres coincidentes en los datos de la respuesta.  <br/> |
|ErrorNameResolutionNoMailbox  <br/> |Este error indica que el autor de la llamada no tiene un buzón de correo en el sistema. La [operación ResolveNames](resolvenames-operation.md) o [ExpandDL](expanddl-operation.md) no es válida para conectar un usuario sin un buzón.  <br/> |
|ErrorNameResolutionNoResults  <br/> |Este error indica que la [operación ResolveNames](resolvenames-operation.md) no devuelve ningún resultado.  <br/> |
|ErrorNoApplicableProxyCASServersAvailable  <br/> |Este código de error debe devolverse cuando el servicio Web no encuentra un servidor para administrar la solicitud.  <br/> |
|ErrorNoCalendar  <br/> |Este error se produce si no hay ninguna carpeta de calendario para el buzón.  <br/> |
|ErrorNoDestinationCASDueToKerberosRequirements  <br/> |Este error indica que la solicitud hacía referencia a un buzón en otro sitio de Active Directory, pero que no hay servidores de acceso de cliente en el sitio de destino configurados para la autenticación de Windows y, por lo tanto, la solicitud no se pudo enviar por proxy.  <br/> |
|ErrorNoDestinationCASDueToSSLRequirements  <br/> |Este error indica que la solicitud hacía referencia a un buzón en otro sitio de Active Directory, pero ningún servidor de acceso de cliente en el sitio de destino se configuró para conexiones SSL y, por lo tanto, la solicitud no se pudo enviar por proxy.  <br/> |
|ErrorNoDestinationCASDueToVersionMismatch  <br/> |Este error indica que la solicitud hacía referencia a un buzón en otro sitio de Active Directory, pero ningún servidor de acceso de cliente en el sitio de destino tenía una versión de producto aceptable para recibir la solicitud y, por tanto, la solicitud no se pudo enviar por proxy.  <br/> |
|ErrorNoFolderClassOverride  <br/> |Este error se produce si se establece el elemento [FolderClass](folderclass.md) al crear un elemento que no sea una carpeta genérica. Para las carpetas con tipo como [hubiera](calendarfolder.md) y [hubiera](tasksfolder.md), la clase de carpeta está implícita. Si se establece la clase Folder en un tipo de carpeta diferente mediante la [operación UpdateFolder](updatefolder-operation.md) , se obtiene la respuesta **ErrorObjectTypeChanged** . En su lugar, use un tipo de carpeta genérico, pero establezca la clase Folder en el valor que necesite. Los servicios web Exchange crearán la carpeta con establecimiento inflexible de tipos correcta.  <br/> |
|ErrorNoFreeBusyAccess  <br/> |Este error indica que el autor de la llamada no tiene derechos de visualización de disponibilidad en la carpeta de calendario en cuestión.  <br/> |
|ErrorNonExistentMailbox  <br/> | Este error se produce en las siguientes situaciones: <br/> <br/>-La dirección de correo electrónico está vacía en [CreateManagedFolder](createmanagedfolder.md).  <br/>-La dirección de correo electrónico no hace referencia a una cuenta válida en una solicitud que toma una dirección de correo electrónico en el cuerpo o en el encabezado SOAP, como en una llamada de suplantación de Exchange.  <br/> |
|ErrorNonPrimarySmtpAddress  <br/> |Este error se produce cuando una persona que llama pasa una dirección SMTP no principal. La respuesta incluye la dirección SMTP correcta que se va a usar.  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |Este error indica que las etiquetas de propiedad no pueden hacer referencia a las propiedades MAPI del intervalo personalizado, 0x8000 o superior. Debe usar la propiedad [PropertySetId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)de la API administrada de EWS o el elemento [ExtendedFieldURI](extendedfielduri.md) de EWS con el atributo PropertySetId.  <br/> |
|ErrorNoPublicFolderReplicaAvailable  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorNoPublicFolderServerAvailable  <br/> |Este código de error debe devolverse si no hay ningún servidor de carpetas públicas disponible o si el autor de la llamada no tiene un servidor público local.  <br/> |
|ErrorNoRespondingCASInDestinationSite  <br/> |Este error indica que la solicitud se refiere a un buzón en otro sitio de Active Directory, pero ninguno de los servidores de acceso de cliente de ese sitio respondió y, por lo tanto, la solicitud no se pudo enviar por proxy.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |Este error indica que el autor de la llamada intentó conceder permisos en su calendario o carpeta de contactos a un usuario de otra organización y se produjo un error al intentar.  <br/> |
|ErrorNotDelegate  <br/> |Este error indica que el usuario no es un delegado para el buzón. Lo devuelve la [operación GetDelegate](getdelegate-operation.md), la [operación RemoveDelegate](removedelegate-operation.md)y la [operación UpdateDelegate](updatedelegate-operation.md) cuando el usuario delegado especificado no se encuentra en la lista de delegados.  <br/> |
|ErrorNotEnoughMemory  <br/> |Este error indica que la operación no se pudo completar debido a memoria insuficiente.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |Este error indica que no se admite el mensaje para compartir.  <br/> |
|ErrorObjectTypeChanged  <br/> |Este error se produce si cambia el tipo de objeto.  <br/> |
|ErrorOccurrenceCrossingBoundary  <br/> |Este error se produce cuando la hora de [Inicio](start.md) o [finalización](end-ex15websvcsotherref.md) de una ocurrencia se actualiza para que la ocurrencia se programe para que se produzca antes o después de la ocurrencia correspondiente anterior o siguiente.  <br/> |
|ErrorOccurrenceTimeSpanTooBig  <br/> |Este error indica que la asignación de tiempo para una ocurrencia dada se superpone con otra ocurrencia del mismo elemento periódico. Esta respuesta también se produce cuando la longitud en minutos de una ocurrencia determinada es mayor que Int32. MaxValue.  <br/> |
|ErrorOperationNotAllowedWithPublicFolderRoot  <br/> |Este error indica que la operación actual no es válida para la raíz de la carpeta pública.  <br/> |
|ErrorOrganizationNotFederated  <br/> |Este error indica que la organización del solicitante no está federada, por lo que el solicitante no puede crear mensajes de uso compartido para enviar a un usuario externo o no puede aceptar mensajes compartidos recibidos de un usuario externo.  <br/> |
|ErrorParentFolderIdRequired  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorParentFolderNotFound  <br/> |Este error se produce en la [operación CreateFolder](createfolder-operation.md) cuando no se encuentra la carpeta principal.  <br/> |
|ErrorPasswordChangeRequired  <br/> |Este error indica que debe cambiar la contraseña para poder tener acceso a este buzón de correo. Esto ocurre cuando se ha creado una nueva cuenta y el administrador indicó que el usuario debe cambiar la contraseña en el primer inicio de sesión. No puede actualizar la contraseña con los servicios web Exchange. Debe usar una herramienta como Microsoft Office Outlook Web App para cambiar la contraseña.  <br/> |
|ErrorPasswordExpired  <br/> |Este error indica que la contraseña ha expirado. No puede cambiar la contraseña con los servicios web Exchange. Debe usar una herramienta como Outlook Web App para cambiar la contraseña.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |Este error indica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la Directiva de uso compartido asignada al solicitante indica que el nivel de permisos solicitado es superior al que permite la Directiva de uso compartido.  <br/> |
|ErrorPhoneNumberNotDialable  <br/> |Este error indica que el número de teléfono no estaba en el formato correcto.  <br/> |
|ErrorPropertyUpdate  <br/> |Este error indica que se produjo un error en la actualización debido a valores de propiedad no válidos. El mensaje de respuesta incluye las rutas de propiedad no válidas.  <br/> |
|ErrorPromptPublishingOperationFailed  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorPropertyValidationFailure  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorProxiedSubscriptionCallFailure  <br/> |Este error indica que la solicitud hacía referencia a una suscripción que existe en otro servidor de acceso de cliente, pero se produjo un error al intentar proxy la solicitud en ese servidor de acceso de cliente.  <br/> |
|ErrorProxyCallFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorProxyGroupSidLimitExceeded  <br/> |Este error indica que la solicitud se refiere a un buzón en otro sitio de Active Directory, y el autor de la llamada original es miembro de más de 3.000 grupos.  <br/> |
|ErrorProxyRequestNotAllowed  <br/> |Este error indica que la solicitud que envían los servicios web Exchange a otro servidor de acceso de cliente al intentar cumplir una solicitud de [GetUserAvailabilityRequest](getuseravailabilityrequest.md) no era válida. Este código de respuesta suele indicar que se ha producido un error de configuración o de derechos, o que alguien ha tratado sin éxito a imitar una solicitud de proxy de disponibilidad.  <br/> |
|ErrorProxyRequestProcessingFailed  <br/> |Este error indica que los servicios Web de Exchange intentaron redirigir una solicitud de disponibilidad a otro servidor de acceso de cliente para su cumplimiento, pero se produjo un error en la solicitud. Esta respuesta puede deberse a problemas de conectividad de red o a problemas de tiempo de espera de solicitud.  <br/> |
|ErrorProxyServiceDiscoveryFailed  <br/> |Este código de error debe devolverse si el servicio Web no puede determinar si la solicitud se va a ejecutar en el servidor de destino o si se va a enviar un proxy a otro servidor.  <br/> |
|ErrorProxyTokenExpired  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorPublicFolderMailboxDiscoveryFailed  <br/> |Este error se produce cuando no se encuentra la URL de buzón de la carpeta pública. Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorPublicFolderOperationFailed  <br/> |Este error se produce cuando se intenta obtener acceso a una carpeta pública y el intento no se realiza correctamente. Este error se introdujo en Exchange 2013Cuadro Server 2013.  <br/> |
|ErrorPublicFolderRequestProcessingFailed  <br/> |Este error se produce cuando el destinatario que se pasó a la [operación GetUserAvailability](getuseravailability-operation.md) se encuentra en un equipo que ejecuta una versión de Exchange Server anterior a Exchange 2007 y se produce un error en la solicitud para recuperar la información de disponibilidad del destinatario del servidor de carpetas públicas.  <br/> |
|ErrorPublicFolderServerNotFound  <br/> |Este error se produce cuando el destinatario que se pasó a la [operación GetUserAvailability](getuseravailability-operation.md) se encuentra en un equipo que ejecuta una versión de Exchange Server anterior a Exchange 2007 y se produce un error en la solicitud para recuperar la información de disponibilidad del destinatario del servidor de carpetas públicas porque la unidad organizativa no tenía un servidor de carpetas públicas asociado.  <br/> |
|ErrorPublicFolderSyncException  <br/> |Este error se produce cuando una operación de sincronización se realiza correctamente en el buzón de correo de carpeta pública principal pero no en el buzón de la carpeta pública secundaria. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorQueryFilterTooLong  <br/> |Este error indica que la restricción de la carpeta de búsqueda puede ser válida, pero EWS no la admite. Los servicios web Exchange limitan las restricciones para contener un máximo de 255 expresiones de filtro. Si intenta enlazar a una carpeta de búsqueda existente que supera 255, se devuelve este código de respuesta.  <br/> |
|ErrorQuotaExceeded  <br/> |Este error se produce cuando se supera la cuota del buzón.  <br/> |
|ErrorReadEventsFailed  <br/> |Este error lo devuelve la [operación GetEvents](getevents-operation.md) o las notificaciones de inserción cuando se produce un error al recuperar información de eventos. Cuando se devuelve este error, la suscripción se elimina. Vuelva a crear la sincronización de eventos en función de una última marca de agua conocida.  <br/> |
|ErrorReadReceiptNotPending  <br/> |Este error lo devuelve la [operación CreateItem](createitem-operation.md) si se ha intentado suprimir una confirmación de lectura cuando el remitente del mensaje no solicitó una confirmación de lectura en el mensaje o si el mensaje está en la carpeta correo electrónico no deseado.  <br/> |
|ErrorRecurrenceEndDateTooBig  <br/> |Este error se produce cuando la fecha de finalización de la periodicidad es posterior a 9/1/4500.  <br/> |
|ErrorRecurrenceHasNoOccurrence  <br/> |Este error se produce cuando la periodicidad especificada no tiene ninguna instancia del intervalo especificado.  <br/> |
|ErrorRemoveDelegatesFailed  <br/> |Este error indica que no se pudo guardar la lista de delegados una vez quitados los delegados.  <br/> |
|ErrorRequestAborted  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorRequestStreamTooBig  <br/> | Este error se produce cuando el flujo de la solicitud es superior a 400 KB.  <br/> |
|ErrorRequiredPropertyMissing  <br/> |Este error se devuelve cuando falta una propiedad necesaria en una solicitud de [operación CreateAttachment](createattachment-operation.md) . El URI de la propiedad que falta se incluye en la respuesta.  <br/> |
|ErrorResolveNamesInvalidFolderType  <br/> |Este error indica que el autor de la llamada ha especificado una carpeta que no es una carpeta de contactos para la [operación ResolveNames](resolvenames-operation.md).  <br/> |
|ErrorResolveNamesOnlyOneContactsFolderAllowed  <br/> |Este error indica que el autor de la llamada ha especificado más de una carpeta de contactos para la [operación ResolveNames](resolvenames-operation.md).  <br/> |
|ErrorResponseSchemaValidation  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorRestrictionTooLong  <br/> |Este error se produce si la restricción contiene más de 255 nodos.  <br/> |
|ErrorRestrictionTooComplex  <br/> |Este error se produce cuando los servicios Web de Exchange no pueden evaluar la restricción.  <br/> |
|ErrorResultSetTooBig  <br/> |Este error indica que el número de entradas de calendario para un destinatario dado supera el límite permitido de 1000. Reduzca la ventana y vuelva a intentarlo.  <br/> |
|ErrorSavedItemFolderNotFound  <br/> |Este error se produce cuando no se encuentra el [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
|ErrorSchemaValidation  <br/> | Este error se produce cuando la solicitud no se puede validar en el esquema.  <br/> |
|ErrorSearchFolderNotInitialized  <br/> |Este error indica que la carpeta de búsqueda se creó, pero los criterios de búsqueda nunca se establecieron en la carpeta. Esto sólo ocurre cuando se tiene acceso a las carpetas de búsqueda dañadas creadas mediante otra API o cliente. Para solucionar este error, use la [operación UpdateFolder](updatefolder-operation.md) para establecer el elemento [SearchParameters](searchparameters.md) para incluir la restricción que debe estar en la carpeta.  <br/> |
|ErrorSendAsDenied  <br/> | Este error se produce cuando se cumplen las dos condiciones siguientes: <br/> <br/>-A un usuario se le han concedido permisos de CanActAsOwner, pero no tiene derechos de delegado en el buzón de la entidad de identidad.  <br/>-El mismo usuario intenta crear y enviar un mensaje de correo electrónico en el buzón de la entidad de identidad mediante la opción SendAndSaveCopy.<br/>  <br/>  El resultado es un error de ErrorSendAsDenied y la creación del mensaje de correo electrónico en la carpeta Borradores de la entidad de la identidad.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Este error lo devuelve la [operación DeleteItem](deleteitem-operation.md) si el atributo **SendMeetingCancellations** falta en la solicitud y el elemento para eliminar es un elemento de calendario.  <br/> |
|ErrorSendMeetingInvitationsOrCancellationsRequired  <br/> |Este error lo devuelve la [operación UpdateItem](updateitem-operation.md) si falta el atributo **SendMeetingInvitationsOrCancellations** en la solicitud y el elemento que se va a actualizar es un elemento de calendario.  <br/> |
|ErrorSendMeetingInvitationsRequired  <br/> |Este error lo devuelve la [operación CreateItem](createitem-operation.md) si falta el atributo **SendMeetingInvitations** de la solicitud y el elemento que se va a crear es un elemento de calendario.  <br/> |
|ErrorSentMeetingRequestUpdate  <br/> |Este error indica que después de que el organizador envíe una convocatoria de reunión, la solicitud no se puede actualizar. Para modificar la reunión, modifique el elemento de calendario, no la convocatoria de reunión.  <br/> |
|ErrorSentTaskRequestUpdate  <br/> |Este error indica que después de que el iniciador de la tarea envíe una solicitud de tarea, no se puede actualizar la solicitud.  <br/> |
|ErrorServerBusy  <br/> |Este error se produce cuando el servidor está ocupado.  <br/> |
|ErrorServiceDiscoveryFailed  <br/> |Este error indica que los servicios Web de Exchange intentaron redirigir una solicitud de disponibilidad de usuario al bosque adecuado para el destinatario, pero no pudo determinar dónde enviar la solicitud debido a un error de detección de servicios.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |Este error indica que no se ha establecido la propiedad de dirección URL externa en la base de datos de Active Directory.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> |Este error indica que se produjo un error al intentar sincronizar una carpeta de uso compartido. <br/><br/>Este código de error se devuelve cuando se produce lo siguiente:<br/><br/>-No se encuentra la suscripción para una carpeta de uso compartido.<br/>-No se encuentra la carpeta de uso compartido.<br/>-No se encuentra el usuario de directorio correspondiente.<br/>-El usuario ya no existe.<br/>-La cita no es válida.<br/>-El elemento de contacto no es válido.<br/>-Error de comunicación con el servidor remoto.  <br/> |
|ErrorStaleObject  <br/> |Este error se produce en una [operación UpdateItem](updateitem-operation.md) o en una [operación SendItem](senditem-operation.md) cuando la clave Change no está actualizada o no se ha proporcionado. Llame a la [operación GetItem](getitem-operation.md) para recuperar una clave de cambio actualizada y, a continuación, vuelva a intentar la operación.  <br/> |
|ErrorSubmissionQuotaExceeded  <br/> |Este error indica que un usuario no puede enviar más solicitudes inmediatamente porque se ha alcanzado la cuota de envío.  <br/> |
|ErrorSubscriptionAccessDenied  <br/> |Este error se produce cuando intenta obtener acceso a una suscripción con una cuenta que no ha creado dicha suscripción. Solo el creador de la suscripción puede tener acceso a cada suscripción.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Este error indica que no se puede crear una suscripción si no es el propietario o no tiene acceso de propietario al buzón.  <br/> |
|ErrorSubscriptionNotFound  <br/> |Este error se produce si no se encuentra la suscripción que corresponde al [SubscriptionId especificado (GetEvents)](subscriptionid-getevents.md) . Es posible que la suscripción haya expirado, que el proceso de servicios web Exchange se haya reiniciado o que se haya pasado una suscripción no válida. Si la suscripción era válida, vuelva a crear la suscripción con la marca de agua más reciente. Esto lo devuelve la [operación de cancelación de suscripción](unsubscribe-operation.md) o las respuestas de la [operación GetEvents](getevents-operation.md) .  <br/> |
|ErrorSubscriptionUnsubsribed  <br/> |Este código de error debe devolverse cuando se realiza una solicitud de una suscripción cuyo suscripción se ha cancelado.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Este error lo devuelve la [operación SyncFolderItems](syncfolderitems-operation.md) si no se encuentra la carpeta principal especificada.  <br/> |
|ErrorTeamMailboxNotFound  <br/> |Este error indica que no se ha encontrado un buzón de equipo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxNotLinkedToSharePoint  <br/> |Este error indica que se ha encontrado un buzón de equipo pero que no está vinculado a un servidor de SharePoint. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxUrlValidationFailed  <br/> |Este error indica que se ha encontrado un buzón de equipo pero que el vínculo al servidor de SharePoint no es válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxNotAuthorizedOwner  <br/> |Este código de error no se usa. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxActiveToPendingDelete  <br/> |Este código de error no se usa. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxFailedSendingNotifications  <br/> |Este error indica que no se pudo realizar correctamente un intento de enviar una notificación a los propietarios del buzón de grupo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxErrorUnknown  <br/> |Este error indica un error general que puede producirse al intentar obtener acceso a un buzón de equipo. Intente enviar la solicitud en un momento posterior. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTimeIntervalTooBig  <br/> |Este error indica que la ventana de tiempo que se especificó es mayor que el límite permitido. De forma predeterminada, el límite permitido es 42.  <br/> |
|ErrorTimeoutExpired  <br/> | Este error se produce cuando no hay tiempo suficiente para completar el procesamiento de la solicitud.  <br/> |
|ErrorTimeZone  <br/> |Este error indica que hay un error de zona horaria.  <br/> |
|ErrorToFolderNotFound  <br/> |Este error indica que la carpeta de destino no existe.  <br/> |
|ErrorTokenSerializationDenied  <br/> |Este error se produce si el autor de la llamada intenta realizar una solicitud de serialización de token, pero no tiene el MS-Exch-EPI-TokenSerialization derecho en el servidor de acceso de cliente.  <br/> |
|ErrorTooManyObjectsOpened  <br/> |Este error se produce cuando se ha superado el límite interno de los objetos abiertos.  <br/> |
|ErrorUnifiedMessagingDialPlanNotFound  <br/> |Este error indica que el plan de marcado de un usuario no está disponible.  <br/> |
|ErrorUnifiedMessagingReportDataNotFound  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnifiedMessagingPromptNotFound  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnifiedMessagingRequestFailed  <br/> |Este error indica que no se pudo encontrar al usuario.  <br/> |
|ErrorUnifiedMessagingServerNotFound  <br/> |Este error indica que se puede encontrar un servidor válido para el plan de marcado para controlar la solicitud.  <br/> |
|ErrorUnableToGetUserOofSettings  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorUnableToRemoveImContactFromGroup  <br/> |Este error se produce cuando se realiza un intento incorrecto de quitar un contacto de mensajería instantánea de un grupo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnsupportedCulture  <br/> |Este error se produce cuando se intenta establecer la propiedad **Culture** en un valor que no se puede analizar mediante la clase **System. Globalization. CultureInfo** .  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |Este error se produce cuando una persona que llama intenta usar propiedades extendidas de tipos Object, matriz de objetos, error o null.  <br/> |
|ErrorUnsupportedMimeConversion  <br/> |Este error se produce cuando se intenta recuperar o establecer contenido MIME para un elemento que no sea un objeto [PostItem](postitem.md), [Message](message-ex15websvcsotherref.md)o [CalendarItem](calendaritem.md) .  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |Este error se produce cuando el autor de la llamada pasa una propiedad que no es válida para una consulta. Esto puede ocurrir cuando se usan propiedades calculadas.  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |Este error se produce cuando el autor de la llamada pasa una propiedad que no es válida para una ordenación o un grupo por propiedad. Esto puede ocurrir cuando se usan propiedades calculadas.  <br/> |
|ErrorUnsupportedPropertyDefinition  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorUnsupportedQueryFilter  <br/> |Este error indica que la restricción de la carpeta de búsqueda puede ser válida, pero EWS no la admite.  <br/> |
|ErrorUnsupportedRecurrence  <br/> |Este error indica que la periodicidad especificada no es compatible con las tareas.  <br/> |
|ErrorUnsupportedSubFilter  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |Este error indica que los servicios Web de Exchange han encontrado un tipo de propiedad en el almacén, pero no pueden generar XML para el tipo de propiedad.  <br/> |
|ErrorUpdateDelegatesFailed  <br/> |Este error indica que no se pudo guardar la lista de delegados después de que se actualizaron los delegados.  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |Este error se produce cuando la ruta de acceso de propiedad única que aparece en la descripción de un cambio no coincide con la propiedad que se está configurando dentro del objeto de [elemento](item.md) o [carpeta](folder.md) real.  <br/> |
|ErrorUserNotUnifiedMessagingEnabled  <br/> |Este error indica que el solicitante no está habilitado.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |Este error indica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la Directiva de uso compartido asignada al solicitante indica que el dominio del usuario externo no aparece en la Directiva.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Indica que la organización del solicitante tiene un conjunto de dominios federados, pero la organización del solicitante no tiene ninguna dirección proxy SMTP con uno de los dominios federados.  <br/> |
|ErrorValueOutOfRange  <br/> |Este error indica que la fecha de inicio o la fecha de finalización de la vista de calendario se estableció en 1/1/0001 12:00:00 A.M. o 12/31/9999 11:59:59 P.M.  <br/> |
|ErrorVirusDetected  <br/> |Este error indica que el almacén de Exchange ha detectado un virus en el mensaje.  <br/> |
|ErrorVirusMessageDeleted  <br/> |Este error indica que el almacén de Exchange ha detectado un virus en el mensaje y lo ha eliminado.  <br/> |
|ErrorVoiceMailNotImplemented  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWebRequestInInvalidState  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWin32InteropError  <br/> |Este error indica que se produjo un error interno durante la comunicación con el código no administrado.  <br/> |
|ErrorWorkingHoursSaveFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWorkingHoursXmlMalformed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWrongServerVersion  <br/> |Este error indica que solo se puede realizar una solicitud en un servidor que tenga la misma versión que el servidor de buzones de correo.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Este error indica que un delegado realizó una solicitud que tiene una versión de servidor distinta a la del servidor de buzones de correo de la entidad de la identidad.  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |Este código de error no se devuelve nunca.  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |Especifica que hay encabezados SOAP duplicados.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> | Especifica que se produjo un error al intentar sincronizar una carpeta de uso compartido.<br/><br/> Este código de error debe devolverse cuando:<br/><br/>-No se encuentra la suscripción para una carpeta de uso compartido.  <br/>-No se encontró la carpeta de uso compartido.  <br/>-No se ha encontrado el usuario de directorio correspondiente.  <br/>-El usuario ya no existe.  <br/>-La cita no es válida.  <br/>-El elemento de contacto no es válido.  <br/>-Se produjo un error de comunicación con el servidor remoto.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |Especifica que no se ha establecido la propiedad de dirección URL externa en la base de datos de Active Directory. Este código de error debe devolverse si no se ha establecido la propiedad de dirección URL externa en la base de datos de Active Directory.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |Especifica que se ha alcanzado el número máximo de miembros del grupo para obtener información de disponibilidad para una lista de distribución. Este error debe devolverse cuando se ha alcanzado el número máximo de miembros del grupo para obtener información de disponibilidad para una lista de distribución.  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |Especifica que el elemento DataType y ShareFolderId están presentes en una solicitud. Este código de error debe devolverse si los elementos DataType y ShareFolderId están presentes en una solicitud.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |Especifica que el autor de la llamada intentó conceder permisos en su calendario o carpeta de contactos a un usuario de otra organización y se produjo un error en el intento. Este código de error debe devolverse cuando la Directiva de uso compartido está deshabilitada para el autor de la llamada o cuando la Directiva de uso compartido asignada al autor de la llamada no permite el uso compartido para el nivel solicitado o el tipo de carpeta solicitada.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |Especifica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la Directiva de uso compartido asignada al solicitante especifica que el dominio del usuario externo no aparece en la Directiva.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |Especifica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la Directiva de uso compartido asignada al solicitante especifica que el nivel de permisos solicitado es mayor que el que permite la Directiva de uso compartido.  <br/> |
|ErrorOrganizationNotFederated  <br/> |Especifica que la organización del solicitante no está federada para que el solicitante no pueda crear mensajes de uso compartido para enviar a un usuario externo o no puede aceptar mensajes de uso compartido recibidos de un usuario externo. Este código de error debe devolverse si la organización del solicitante no está federada.  <br/> |
|ErrorMailboxFailover  <br/> |Especifica que se produjo un error al intentar obtener acceso a un buzón porque el buzón está en un proceso de conmutación por error.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |Especifica que el remitente de la invitación de uso compartido no ha creado los metadatos de la invitación para uso compartido. Este código de error debe devolverse si el remitente de la invitación de uso compartido no ha creado los metadatos de la invitación para uso compartido.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |Especifica que el servicio de seguimiento de mensajes no puede realizar el seguimiento del mensaje.  <br/> |
|ErrorMessageTrackingTransientError  <br/> |Especifica que el servicio de seguimiento de mensajes está desactivado o no está disponible. Este código de error especifica un error transitorio. Los clientes pueden volver a intentar conectarse al servidor cuando se recibe este error.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |Especifica que no se encuentra el dominio especificado.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Especifica que la organización del solicitante tiene un conjunto de dominios federados, pero que la organización del solicitante no tiene ninguna dirección proxy SMTP con uno de los dominios federados.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |Especifica que el autor de la llamada solicitó la información de disponibilidad de un usuario de otra organización, pero la relación de la organización no tiene la disponibilidad habilitada.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |Especifica que los objetos de Federación de la organización del solicitante no están correctamente configurados.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |Especifica que un mensaje para compartir no está destinado al autor de la llamada.  <br/> |
|ErrorInvalidSharingData  <br/> |Especifica que los metadatos de uso compartido no son válidos. Esto puede deberse a XML no válido.  <br/> |
|ErrorInvalidSharingMessage  <br/> |Especifica que el mensaje para compartir no es válido. Esto puede deberse a que falta una propiedad.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |Especifica que no se admite el mensaje para compartir.  <br/> |
|ErrorApplyConversationActionFailed  <br/> |Este error se debe devolver si no se puede aplicar una acción a uno o más elementos de la conversación.  <br/> |
|ErrorInboxRulesValidationError  <br/> |Este error se debe devolver si no se valida ninguna regla.  <br/> |
|ErrorOutlookRuleBlobExists  <br/> |Este error debe devolverse cuando se produce un intento de administrar las reglas de la bandeja de entrada después de que otro cliente haya tenido acceso a las reglas de la bandeja de entrada.  <br/> |
|ErrorRulesOverQuota  <br/> |Este error debe devolverse cuando se ha superado la cuota de la regla de un usuario.  <br/> |
|ErrorNewEventStreamConnectionOpened  <br/> |Este error se debe devolver a la primera conexión de suscripción si se abre una segunda conexión de suscripción.  <br/> |
|ErrorMissedNotificationEvents  <br/> |Este error se debe devolver cuando se pierden las notificaciones de eventos.  <br/> |
|ErrorDuplicateLegacyDistinguishedName  <br/> |Este error se devuelve cuando hay nombres distintivos heredados duplicados en servicios de dominio de Active Directory (AD DS). Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidClientAccessTokenRequest  <br/> |Este error indica que una solicitud para obtener un token de acceso de cliente no era válida. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorNoSpeechDetected  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUMServerUnavailable  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorRecipientNotFound  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorRecognizerNotInstalled  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSpeechGrammarError  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidManagementRoleHeader  <br/> |Este error se devuelve si el encabezado [ManagementRole](managementrole.md) en el encabezado SOAP es incorrecto. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesDisabled  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesRequestTimedOut  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesRequestFailed  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesInvalidRequest  <br/> |Este error está destinado exclusivamente para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorWeatherServiceDisabled  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorMailboxScopeNotAllowedWithoutQueryString  <br/> |Este error se devuelve cuando se realiza un intento de búsqueda con ámbito sin usar un elemento [QueryString (String)](querystring-string.md) para una búsqueda de indización de contenido. Esto es aplicable a las operaciones **SearchMailboxes** y **FindConversation** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorArchiveMailboxSearchFailed  <br/> |Este error se devuelve cuando una búsqueda de buzón de archivo no se realiza correctamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |Este error se devuelve cuando no se detecta la dirección URL de un buzón de archivo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorGetRemoteArchiveFolderFailed  <br/> |Este error se produce cuando se produce un error en la operación de obtención de la carpeta del buzón de archivo remoto.  <br/> |
|ErrorFindRemoteArchiveFolderFailed  <br/> |Este error se produce cuando se produce un error en la operación de búsqueda de la carpeta del buzón de archivo remoto.  <br/> |
|ErrorGetRemoteArchiveItemFailed  <br/> |Este error se produce cuando se produce un error en la operación para obtener el elemento de buzón de archivo remoto.  <br/> |
|ErrorExportRemoteArchiveItemsFailed  <br/> |Este error se produce cuando se produce un error en la operación de exportación de elementos del buzón de archivo remoto.  <br/> |
|ErrorInvalidPhotoSize  <br/> |Este error se devuelve si se solicita un tamaño de foto no válido desde el servidor. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSearchQueryHasTooManyKeywords  <br/> |Este error se devuelve cuando se solicita un tamaño de foto inesperado en una solicitud de operación **GetUserPhoto** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSearchTooManyMailboxes  <br/> |Este error se devuelve cuando una solicitud de operación de **SearchMailboxes** contiene demasiados buzones para buscar. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagNone  <br/> |Este error indica que no se ha encontrado ninguna etiqueta de retención para este usuario. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorDiscoverySearchesDisabled  <br/> |Este error se devuelve cuando las búsquedas de detección están deshabilitadas en un inquilino o servidor. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorCalendarSeekToConditionNotSupported  <br/> |Este error se produce al intentar invocar la [operación FindItem](finditem-operation.md) con una [SeekToConditionPageItemView](seektoconditionpageitemview.md) para recuperar los elementos del calendario, que no se admiten.  <br/> |
|ErrorCalendarIsGroupMailboxForAccept  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorCalendarIsGroupMailboxForDecline  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorCalendarIsGroupMailboxForTentative  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt  <br/> |Este error está destinado exclusivamente para uso interno.  <br/> |
|ErrorOrganizationAccessBlocked  <br/> |El inquilino está marcado para su eliminación.  <br/> |
|ErrorInvalidLicense  <br/> |El usuario no tiene una licencia válida.  <br/> |
|ErrorMessagePerFolderCountReceiveQuotaExceeded  <br/> |Se ha superado la cuota de recepción de mensajes por carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento no es obligatorio y no se incluye en todas las respuestas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


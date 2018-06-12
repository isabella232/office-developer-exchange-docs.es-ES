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
description: El elemento ResponseCode proporciona información de estado acerca de la solicitud.
ms.openlocfilehash: 7baeb0ab87ffb43ba9d6b4016477888aa4ed613e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837294"
---
# <a name="responsecode"></a>ResponseCode

El elemento **ResponseCode** proporciona información de estado acerca de la solicitud. 
  
- [ResponseMessage](responsemessage.md) 
- [ResponseCode](responsecode.md)
  
```XML
<ResponseCode/>
```

**ResponseCodeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|Elemento|Descripción|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Proporciona información descriptiva sobre el estado de respuesta.<br/><br/>  Los siguientes son las expresiones de XPath posibles para este elemento:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación DeleteItem](deleteitem-operation.md) .  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [la operación de SendItem](senditem-operation.md) .  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación DeleteFolder](deletefolder-operation.md) .  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación DeleteAttachment](deleteattachment-operation.md) .  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación de cancelación de suscripción](unsubscribe-operation.md) .  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetFolder](getfolder-operation.md) .  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación UpdateFolder](updatefolder-operation.md) .  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación MoveFolder](movefolder-operation.md) .  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CopyFolder](copyfolder-operation.md).  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateManagedFolder](createmanagedfolder-operation.md) .  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación FindFolder](findfolder-operation.md) .  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud [CreateItem operation](createitem-operation.md) .  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud [GetItem operation](getitem-operation.md) .  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación UpdateItem](updateitem-operation.md) .  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación MoveItem](moveitem-operation.md) .  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CopyItem](copyitem-operation.md) .  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateAttachment](createattachment-operation.md) .  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetAttachment](getattachment-operation.md) .  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación FindItem](finditem-operation.md) .  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación ResolveNames](resolvenames-operation.md) .  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [la operación de ExpandDL](expanddl-operation.md) .  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud [Subscribe operación](subscribe-operation.md) .  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetEvents](getevents-operation.md) .  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de operación SendNotification.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación SyncFolderHierarchy](syncfolderhierarchy-operation.md) .  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación SyncFolderItems](syncfolderitems-operation.md) .  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación AddDelegate](adddelegate-operation.md) .  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación RemoveDelegate](removedelegate-operation.md) .  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación UpdateDelegate](updatedelegate-operation.md) .  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetServerTimeZones](getservertimezones-operation.md) .  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Define una respuesta a una solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación RefreshSharingFolder](refreshsharingfolder-operation.md) .  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud de [operación RefreshSharingFolder](refreshsharingfolder-operation.md) .  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Contiene el estado y los resultados de una respuesta de [la operación FindConversation](findconversation-operation.md) .  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud de [operación ApplyConversationAction](applyconversationaction-operation.md) .  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud [EmptyFolder operación](emptyfolder-operation.md) .  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Contiene un estado y el resultado de una solicitud de [operación UpdateInboxRules](updateinboxrules-operation.md) .  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contiene un estado y el resultado de una solicitud de [operación UploadItems](uploaditems-operation.md) .  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Contiene una respuesta a una [operación GetInboxRules](getinboxrules-operation.md) *** solicitud.  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Contiene una respuesta a una solicitud de [operación GetServiceConfiguration](getserviceconfiguration-operation.md) .  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene la configuración del servicio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto. En la siguiente tabla se describe los valores que se devuelven con este elemento.
  
|Value|Descripción|
|:-----|:-----|
|NoError  <br/> |Se ha producido ningún error para la solicitud.  <br/> |
|ErrorAccessDenied  <br/> |Este error se produce cuando la cuenta que realiza la llamada no tiene los derechos para llevar a cabo la acción solicitada.  <br/> |
|ErrorAccessModeSpecified  <br/> |Este error es sólo para uso interno. Este error no se devuelve.  <br/> |
|ErrorAccountDisabled  <br/> |Este error se produce cuando se ha deshabilitado la cuenta en cuestión.  <br/> |
|ErrorAddDelegatesFailed  <br/> |Este error se produce cuando no se puede guardar una lista con los delegados se ha agregado.  <br/> |
|ErrorAddressSpaceNotFound  <br/> |Este error se produce cuando no se pudo encontrar el registro del espacio de dirección o el nombre de dominio del sistema de nombres de dominio (DNS), de disponibilidad entre bosques en la base de datos de Active Directory.  <br/> |
|ErrorADOperation  <br/> |Este error se produce cuando la operación ha fallado debido a problemas de comunicación con los servicios de dominio de Active Directory (AD DS).  <br/> |
|ErrorADSessionFilter  <br/> |Este error se devuelve cuando una solicitud de operación **ResolveNames** especifica un nombre que no es válido.  <br/> |
|ErrorADUnavailable  <br/> |Este error se produce cuando AD DS no está disponible. Inténtelo de nuevo más tarde.  <br/> |
|ErrorAffectedTaskOccurrencesRequired  <br/> |Este error indica que no se ha especificado el atributo **AffectedTaskOccurrences** . Cuando se usa el elemento [DeleteItem](deleteitem.md) para eliminar al menos un elemento que es una tarea e independientemente de si esa tarea es periódica o no, el atributo **AffectedTaskOccurrences** debe especificarse para que pueda determinar **DeleteItem** si Para eliminar la aparición actual o toda la serie.  <br/> |
|ErrorArchiveFolderPathCreation  <br/> |Indica un error en la creación de ruta de acceso de carpeta de archivo.  <br/> |
|ErrorArchiveMailboxNotEnabled  <br/> |Indica que el buzón de archivo no se ha habilitado.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |Indica un error que detección de servicios de buzón de correo de archivo.  <br/> |
|ErrorAttachmentNestLevelLimitExceeded  <br/> |Especifica que se ha intentado crear un elemento con datos adjuntos anidados más de 10. Este valor se introdujo en Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|ErrorAttachmentSizeLimitExceeded  <br/> |El elemento [CreateAttachment](createattachment.md) devuelve este error si intenta crear un archivo adjunto con tamaño superior a Int32.MaxValue, en bytes.  <br/> El elemento [GetAttachment](getattachment.md) devuelve este error si intenta recuperar un archivo adjunto existente con tamaño superior a Int32.MaxValue, en bytes.  <br/> |
|ErrorAutoDiscoverFailed  <br/> |Este error indica que los servicios Web Exchange intentó determinar la ubicación de un equipo entre bosques que ejecuta Exchange 2010 que tiene el rol de servidor de acceso de cliente instalado con el servicio de detección automática, pero la llamada al servicio de detección automática no se pudo.  <br/> |
|ErrorAvailabilityConfigNotFound  <br/> |Este error indica que falta la información de configuración de disponibilidad para el bosque local de AD DS.  <br/> |
|ErrorBatchProcessingStopped  <br/> | Este error indica que se produjo una excepción al procesar un elemento y la excepción es probable que se produzcan para los elementos que le siguen. Las solicitudes pueden incluir varios elementos; Por ejemplo, una solicitud de operación GetItem puede incluir varios identificadores. En general, los elementos son procesan uno a la vez. Si se produce una excepción al procesar un elemento y es probable que se produzcan para los elementos que sigan excepción, no se procesarán los elementos que le siguen.  <br/><br/>  Los siguientes son ejemplos de errores que dejará de procesar para los elementos siguientes:<br/>  <br/>-ErrorAccessDenied  <br/>-ErrorAccountDisabled  <br/>-ErrorADUnavailable  <br/>-ErrorADOperation  <br/>-ErrorConnectionFailed  <br/>-ErrorMailboxStoreUnavailable  <br/>-ErrorMailboxMoveInProgress  <br/>-ErrorPasswordChangeRequired  <br/>-ErrorPasswordExpired  <br/>-ErrorQuotaExceeded  <br/>-ErrorInsufficientResources  <br/> |
|ErrorCalendarCannotMoveOrCopyOccurrence  <br/> |Este error se produce cuando se realiza un intento para mover o copiar una aparición de un elemento periódico del calendario.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> | Este error se produce cuando se realiza un intento para actualizar un elemento de calendario que se encuentra en la carpeta Elementos eliminados y cuando son actualizaciones de reunión o cancelaciones se envíen según el valor del atributo **SendMeetingInvitationsOrCancellations** . <br/><br/>Los siguientes son los valores posibles para este atributo:  <br/><br/>-SendToAllAndSaveCopy  <br/>-SendToChangedAndSaveCopy  <br/>-SendOnlyToAll  <br/>-SendOnlyToChanged  <br/>  <br/>Sin embargo, una de estas actualizaciones sólo se permiten cuando el valor de este atributo se establece en SendToNone.  <br/> |
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |Este error se produce cuando se llama a la operación UpdateItem, GetItem, DeleteItem, MoveItem, CopyItem o SendItem y el identificador que se ha especificado no es un identificador de la aparición de cualquier elemento de calendario periódico.  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |Este error se produce cuando se llama a la operación **UpdateItem**, **GetItem**, **DeleteItem**, **MoveItem**, **CopyItem**o **SendItem** y el identificador que se ha especificado no es un identificador de cualquier elemento maestro periódico.  <br/> |
|ErrorCalendarDurationIsTooLong  <br/> |Este error se produce durante una operación **CreateItem** o **UpdateItem** cuando una duración de elemento de calendario es mayor que el máximo permitido, que actualmente es 5 años.  <br/> |
|ErrorCalendarEndDateIsEarlierThanStartDate  <br/> |Este error se produce cuando se establece una hora de finalización del calendario al mismo tiempo o después de la hora de inicio.  <br/> |
|ErrorCalendarFolderIsInvalidForCalendarView  <br/> |Este error se produce cuando la carpeta especificada para una operación de **FindItem** con un elemento [CalendarView](calendarview.md) no es del tipo de carpeta de calendario.  <br/> |
|ErrorCalendarInvalidAttributeValue  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorCalendarInvalidDayForTimeChangePattern  <br/> |Este error se produce durante una operación **CreateItem** o **UpdateItem** cuando los valores no válidos de día, WeekendDay y Weekday se usan para definir el patrón de cambio de tiempo.  <br/> |
|ErrorCalendarInvalidDayForWeeklyRecurrence  <br/> |Este error se produce durante una operación **CreateItem** o **UpdateItem** cuando los valores no válidos de día, semana y WeekendDay se utilizan para especificar la periodicidad semanal.  <br/> |
|ErrorCalendarInvalidPropertyState  <br/> |Este error se produce cuando el estado de un calendario elemento periodicidad objeto binario grande (BLOB) en el almacén de Exchange no es válido.  <br/> |
|ErrorCalendarInvalidPropertyValue  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorCalendarInvalidRecurrence  <br/> |Este error se produce cuando no se puede crear la periodicidad especificada.  <br/> |
|ErrorCalendarInvalidTimeZone  <br/> |Este error se produce cuando se detecta una zona horaria no válida.  <br/> |
|ErrorCalendarIsCancelledForAccept  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForDecline  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForRemove  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForTentative  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsDelegatedForAccept  <br/> |Este error indica que el elemento de [AcceptItem](acceptitem.md) no es válido para una convocatoria de reunión o elemento de calendario en un escenario de delegados.  <br/> |
|ErrorCalendarIsDelegatedForDecline  <br/> |Este error indica que el elemento de [DeclineItem](declineitem.md) no es válido para una convocatoria de reunión o elemento de calendario en un escenario de delegados.  <br/> |
|ErrorCalendarIsDelegatedForRemove  <br/> |Este error indica que el elemento de [RemoveItem](removeitem.md) no es válido para la cancelación de la reunión en un escenario de delegados.  <br/> |
|ErrorCalendarIsDelegatedForTentative  <br/> |Este error indica que el elemento de [TentativelyAcceptItem](tentativelyacceptitem.md) no es válido para una convocatoria de reunión o elemento de calendario en un escenario de delegados.  <br/> |
|ErrorCalendarIsNotOrganizer  <br/> |Este error indica que la operación (actualmente CancelItem) en el elemento de calendario no es válida para un asistente. Sólo el organizador de la reunión puede cancelar la reunión.  <br/> |
|ErrorCalendarIsOrganizerForAccept  <br/> |Este error indica que [AcceptItem](acceptitem.md) no es válida para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarIsOrganizerForDecline  <br/> |Este error indica que [DeclineItem](declineitem.md) no es válida para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarIsOrganizerForRemove  <br/> |Este error indica que no es válido para el elemento de calendario del organizador [RemoveItem](removeitem.md) . Para quitar una reunión desde el calendario, el organizador debe usar CancelCalendarItem.  <br/> |
|ErrorCalendarIsOrganizerForTentative  <br/> |Este error indica que [TentativelyAcceptItem](tentativelyacceptitem.md) no es válida para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarMeetingRequestIsOutOfDate  <br/> |Este error indica que una convocatoria de reunión está obsoleta y no se puede actualizar.  <br/> |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange  <br/> |Este error indica que el índice de aparición no apunta a una aparición dentro de la periodicidad de la actual. Por ejemplo, si el patrón de periodicidad define un conjunto de tres repeticiones de la reunión e intenta obtener acceso a la quinta repetición, se producirá este código de respuesta.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Este error indica que cualquier operación en una aparición eliminada (dirigida a través de índice maestro periódico de identificador y repetición) no es válida.  <br/> |
|ErrorCalendarOutOfRange  <br/> |Este error se produce en las operaciones de CreateItem y UpdateItem para elementos de calendario o propiedades de periodicidad de la tarea cuando el valor de la propiedad está fuera del intervalo. Por ejemplo, especificar la semana del mes decimoquinta dará como resultado de este código de respuesta.  <br/> |
|ErrorCalendarViewRangeTooBig  <br/> |Este error se produce cuando se inicia al intervalo final para el elemento [CalendarView](calendarview.md) es mayor que el máximo permitido, actualmente 2 años.  <br/> |
|ErrorCallerIsInvalidADAccount  <br/> |Este error indica que la cuenta del solicitante no es una cuenta válida en la base de datos de Active directory.  <br/> |
|ErrorCannotArchiveCalendarContactTaskFolderException  <br/> |Indica que se ha intentado archivar una carpeta de contactos de tareas de calendario.  <br/> |
|ErrorCannotArchiveItemsInPublicFolders  <br/> |Indica que se ha intentado archivar elementos en carpetas públicas.  <br/> |
|ErrorCannotArchiveItemsInArchiveMailbox  <br/> |Indica que se ha intentado archive los elementos en el buzón de archivo.  <br/> |
|ErrorCannotCreateCalendarItemInNonCalendarFolder  <br/> |Este error se produce cuando se crea un elemento de calendario y el atributo **SavedItemFolderId** hace referencia a una carpeta de calendario no.  <br/> |
|ErrorCannotCreateContactInNonContactFolder  <br/> |Este error se produce cuando se crea un contacto y el atributo **SavedItemFolderId** hace referencia a una carpeta que no sean contactos.  <br/> |
|ErrorCannotCreatePostItemInNonMailFolder  <br/> |Este error indica que no se puede crear un elemento para exponer en una carpeta que no sea una carpeta de correo, como calendario, contactos, tareas, notas y así sucesivamente.  <br/> |
|ErrorCannotCreateTaskInNonTaskFolder  <br/> |Este error se produce cuando se crea una tarea y el atributo **SavedItemFolderId** hace referencia a una carpeta de tareas comunes.  <br/> |
|ErrorCannotDeleteObject  <br/> |Este error se produce cuando no se puede eliminar el elemento o la carpeta que se va a eliminar.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |La [operación DeleteItem](deleteitem-operation.md) devuelve este error cuando se produce un error al eliminar la aparición actual de una tarea periódica. Esto sólo puede ocurrir si se ha establecido el atributo de **AffectedTaskOccurrences** a SpecifiedOccurrenceOnly.  <br/> |
|ErrorCannotDisableMandatoryExtension  <br/> |Indica que se ha intentado deshabilitar una extensión de mandatorty.  <br/> |
|ErrorCannotEmptyFolder  <br/> |Este error se debe devolver cuando el servidor no puede vaciar una carpeta.  <br/> |
|ErrorCannotGetSourceFolderPath  <br/> |Indica que no se pudo recuperar la ruta de acceso de la carpeta de origen.  <br/> |
|ErrorCannotGetExternalEcpUrl  <br/> |Especifica que el servidor no pudo recuperar la dirección URL externa para las opciones de Outlook Web App.  <br/> |
|ErrorCannotOpenFileAttachment  <br/> |La operación **GetAttachment** devuelve este error si no se puede recuperar el cuerpo de un archivo adjunto.  <br/> |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder  <br/> |Este error indica que el llamador intentó establecer permisos del calendario en una carpeta de calendario no.  <br/> |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder  <br/> |Este error indica que el llamador intentó establecer permisos de calendario no en una carpeta de calendario.  <br/> |
|ErrorCannotSetPermissionUnknownEntries  <br/> |Este error indica que no se puede establecer permisos desconocidos en un conjunto de permisos.  <br/> |
|ErrorCannotSpecifySearchFolderAsSourceFolder  <br/> |Indica que se ha intentado especificar la carpeta de búsqueda como la carpeta de origen.  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |Este error se produce cuando una solicitud que requiere un identificador de elemento se proporciona un identificador de la carpeta.  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |Este error se produce cuando una solicitud que requiera un identificador de la carpeta no se proporciona un identificador de elemento.  <br/> |
|ErrorChangeKeyRequired  <br/> |Este código de respuesta se ha reemplazado por **ErrorChangeKeyRequiredForWriteOperations** <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |Este error se devuelve cuando la clave de cambio para un elemento falta o está obsoleto. <br/><br/>Para las operaciones de SendItem, UpdateItem y UpdateFolder, debe pasar el autor de la llamada en una clave de cambio correcta y actual para el elemento. Tenga en cuenta que esto es el caso con UpdateItem incluso cuando se establece la resolución de conflictos para sobrescribir siempre.  <br/> |
|ErrorClientDisconnected  <br/> |Especifica que el cliente se desconectó.  <br/> |
|ErrorClientIntentInvalidStateDefinition  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorClientIntentNotFound  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorConnectionFailed  <br/> |Este error se produce cuando los servicios Web Exchange no puede conectar con el buzón de correo.  <br/> |
|ErrorContainsFilterWrongType  <br/> |Este error indica que la propiedad que se puede inspeccionar para un filtro de Contains no es un tipo de cadena.  <br/> |
|ErrorContentConversionFailed  <br/> |La operación **GetItem** devuelve este error cuando los servicios Web Exchange es no se puede recuperar el contenido MIME para el elemento solicitado. <br/><br/>La operación **CreateItem** devuelve este error cuando los servicios Web Exchange es no se puede crear el elemento desde el contenido MIME proporcionado. Normalmente, esto es una indicación de que la propiedad item es dañada o truncada.  <br/> |
|ErrorContentIndexingNotEnabled  <br/> |Este error se produce cuando se realiza una solicitud de búsqueda mediante la opción de cadena de consulta y la indización de contenido no está habilitada para el buzón de destino.  <br/> |
|ErrorCorruptData  <br/> |Este error se produce cuando los datos está dañados y no se puede procesar.  <br/> |
|ErrorCreateItemAccessDenied  <br/> |Este error se produce cuando el autor de la llamada no tiene permiso para crear el elemento.  <br/> |
|ErrorCreateManagedFolderPartialCompletion  <br/> |Este error se produce cuando uno o más de las carpetas administradas que se han especificado en la solicitud de operación CreateManagedFolder no pudieron crearse. Búsqueda para cada carpeta determinar qué carpetas se crearon y las carpetas que no existen.  <br/> |
|ErrorCreateSubfolderAccessDenied  <br/> |Este error se produce cuando la cuenta que realiza la llamada no tiene los permisos necesarios para crear la subcarpeta.  <br/> |
|ErrorCrossMailboxMoveCopy  <br/> |Este error se produce cuando se realiza un intento para mover un elemento o carpeta de un buzón de correo a otra. Si el buzón de origen y el buzón de destino son diferentes, se producirá este error.  <br/> |
|ErrorCrossSiteRequest  <br/> |Este error indica que no se permite la solicitud porque el servidor de acceso de cliente que debe atender la solicitud se encuentra en un sitio diferente.  <br/> |
|ErrorDataSizeLimitExceeded  <br/> |Este error puede producirse en los siguientes escenarios:<br/>  <br/>-Está intentado tener acceso o escribir una propiedad en un elemento y el valor de la propiedad es demasiado grande.<br/>-El base64 codificado de longitud dentro de la solicitud XML supera el límite de contenido MIME.<br/>-El tamaño del cuerpo de un cuerpo de elemento existente supera el límite.<br/>-El consumidor intenta establecer un cuerpo HTML o texto cuya longitud (o longitud combinada en el caso de append) supera el límite. |
|ErrorDataSourceOperation  <br/> |Este error se produce cuando se produce un error en el proveedor de datos subyacente completar la operación.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Este error se produce en una operación **AddDelegate** cuando el usuario especificado ya existe en la lista de delegados.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Este error se produce en una operación **AddDelegate** cuando el usuario especificado que se va a agregar es el propietario del buzón.  <br/> |
|ErrorDelegateMissingConfiguration  <br/> |Este error se produce en una operación de **GetDelegate** cuando no hay ninguna información de delegado en el mensaje FreeBusy local o ningún delegado público de Active Directory (no hay "delegado público" o ninguna entrada "Enviar en nombre de" en AD DS).  <br/> |
|ErrorDelegateNoUser  <br/> |Este error se produce cuando un usuario especificado no se puede asignar a un usuario en AD DS.  <br/> |
|ErrorDelegateValidationFailed  <br/> |Este error se produce en la operación de **AddDelegate** cuando un usuario se ha agregado un delegado no es válido.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Este error se produce cuando se realiza un intento para eliminar una carpeta distintivo.  <br/> |
|ErrorDeleteItemsFailed  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorDeleteUnifiedMessagingPromptFailed  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorDistinguishedUserNotSupported  <br/> |Este error indica que un identificador de usuario distintivo no es válido para la operación. **DistinguishedUserType** no debe estar presente en la solicitud.  <br/> |
|ErrorDistributionListMemberNotExist  <br/> |Este error indica que un miembro de lista de distribución de solicitud no existe en la lista de distribución.  <br/> |
|ErrorDuplicateInputFolderNames  <br/> |Este error se produce cuando los nombres de carpeta duplicados se especifican dentro del elemento de [los nombres de carpetas](foldernames.md) de la solicitud de operación **CreateManagedFolder** .  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |Este error indica que no hay encabezados SOAP duplicados.  <br/> |
|ErrorDuplicateUserIdsSpecified  <br/> |Este error indica que se ha encontrado un identificador de usuario duplicados en un conjunto de permisos predeterminado o anónima se establecen más de una vez, o no hay duplicados SID o los destinatarios.  <br/> |
|ErrorEmailAddressMismatch  <br/> |Este error se produce cuando una solicitud intenta crear o actualizar los parámetros de búsqueda de una carpeta de búsqueda. Por ejemplo, esto puede ocurrir cuando se crea una carpeta de búsqueda en el buzón de correo, pero la carpeta de búsqueda se dirige al buscar en otro buzón.  <br/> |
|ErrorEventNotFound  <br/> |Este error se produce cuando se elimina el evento que está asociado con una marca de agua antes de devolver el evento. Cuando se devuelve este error, también se eliminará la suscripción.  <br/> |
|ErrorExceededConnectionCount  <br/> |Este error - indica que hay más usuarios simultáneo solicita contra el servidor de los permitidos por la directiva de un usuario.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |Este error indica que un usuario de la limitación de directiva se ha superado el número máximo de suscripciones.  <br/> |
|ErrorExceededFindCountLimit  <br/> |Este error indica que una llamada de la operación de búsqueda ha superado el número total de elementos que se pueden devolver.  <br/> |
|ErrorExpiredSubscription  <br/> |Este error se produce si se llama a la [operación GetEvents](getevents-operation.md) tal y como se va a eliminar una suscripción debido a que ha caducado.  <br/> |
|ErrorExtensionNotFound  <br/> |Indica que no se encontró la extensión.  <br/> |
|ErrorFolderCorrupt  <br/> |Este error se produce cuando la carpeta está dañada y no se pueden guardar.  <br/> |
|ErrorFolderExists  <br/> |Este error se produce cuando se realiza un intento para crear una carpeta que tiene el mismo nombre que otra carpeta en el mismo elemento primario. No se permiten los nombres de carpeta duplicados.  <br/> |
|ErrorFolderNotFound  <br/> |Este error indica que el identificador de la carpeta que se ha especificado no corresponde a una carpeta válida, o que el delegado no tiene permiso para tener acceso a la carpeta.  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |Este error indica que no se pudo recuperar la propiedad solicitada. Esto no indica que la propiedad no existe, pero que la propiedad se ha dañado de alguna manera para que la recuperación no se pudo.  <br/> |
|ErrorFolderSave  <br/> |Este error indica que la carpeta no se pudo creada o actualizada debido a un estado no válido.  <br/> |
|ErrorFolderSaveFailed  <br/> |Este error indica que la carpeta no se pudo creada o actualizada debido a un estado no válido.  <br/> |
|ErrorFolderSavePropertyError  <br/> |Este error indica que la carpeta no se pudo creada o actualizada debido a los valores de propiedad no válido. El código de respuesta enumera las propiedades que la causa del problema.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |Este error indica que se ha alcanzado el recuento de miembros de grupo máximo para obtener información de libre/ocupado de una lista de distribución.  <br/> |
|ErrorFreeBusyGenerationFailed  <br/> |Este error se devuelve cuando no se puede recuperar la información de disponibilidad debido a un error de intermedio.  <br/> |
|ErrorGetServerSecurityDescriptorFailed  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorImContactLimitReached  <br/> |Este error se devuelve cuando no se puede agregar la nueva instantánea (IM) contactos de mensajería porque se ha alcanzado el número máximo de contactos. Este error se introdujo en Exchange Server 2013.  <br/> |
|ErrorImGroupDisplayNameAlreadyExists  <br/> |Este error se devuelve cuando se realiza un intento para agregar un nombre para mostrar del grupo cuando un grupo existente ya tiene el mismo nombre para mostrar. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorImGroupLimitReached  <br/> |Este error se devuelve cuando no se puede agregar nuevos grupos de mensajería instantánea porque se ha alcanzado el número máximo de grupos. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorImpersonateUserDenied  <br/> |Se devuelve el error en el caso de autorización de servidor a servidor para la suplantación de Exchange cuando el autor de la llamada no tiene los derechos adecuados para suplantar al usuario específico en cuestión. Este error se asigna a la ms-Exch-EPI-May-Impersonate extendido derecha de Active Directory.  <br/> |
|ErrorImpersonationDenied  <br/> |Este error se devuelve en la autorización de servidor a servidor para la suplantación de Exchange cuando el autor de la llamada no tiene los derechos adecuados para suplantar a través del servidor de acceso de cliente que están realizando la solicitud con. Se asigna a la ms-Exch-EPI-Impersonation extendido derecha de Active Directory.  <br/> |
|ErrorImpersonationFailed  <br/> |Este error indica que se ha producido un error inesperado cuando se ha intentado realizar la autenticación de servidor a servidor. Este código de respuesta suele indica que la cuenta de servicio que está ejecutando los servicios Web de Exchange no está configurado correctamente, grupo de aplicaciones que no se puede hablar con servicios Web de Exchange en el directorio, o que una relación de confianza entre bosques no está correctamente configurado.  <br/> |
|ErrorIncorrectSchemaVersion  <br/> |Este error indica que la solicitud era válida para la versión actual de Exchange Server, pero no es válida para la versión de servidor de solicitud que se ha especificado.  <br/> |
|ErrorIncorrectUpdatePropertyCount  <br/> |Este error indica que la descripción de cada cambio en los elementos [UpdateItem](updateitem.md) o [UpdateFolder](updatefolder.md) debe enumerar sólo una propiedad que se debe actualizar.  <br/> |
|ErrorIndividualMailboxLimitReached  <br/> |Este error se produce cuando la solicitud contiene demasiados asistentes para resolver. De forma predeterminada, el número máximo de asistentes para resolver es 100.  <br/> |
|ErrorInsufficientResources  <br/> |Este error se produce cuando el servidor de buzón de correo está sobrecargado. Inténtelo de nuevo más tarde.  <br/> |
|ErrorInternalServerError  <br/> |Este error indica que los servicios Web Exchange detectó un error que no se pudo recuperarse y no existe un código de respuesta más específico que está asociado con el error que se produjo.  <br/> |
|ErrorInternalServerTransientError  <br/> |Este error indica que se ha producido un error interno del servidor y que debe intentar la solicitud de nuevo más tarde.  <br/> |
|ErrorInvalidAccessLevel  <br/> |Este error indica que el nivel de acceso que el autor de la llamada tiene en los datos de disponibilidad no es válido.  <br/> |
|ErrorInvalidArgument  <br/> |Este error indica un error causado por todos los argumentos no válidos que se pasan a la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).<br/><br/> Este error se devuelve en los siguientes escenarios: <br/><br/>-El usuario especificado en el _Enviar-como_ parámetro no existe en el directorio. <br/>-El usuario especificado en el _Enviar-como_ parámetro no es único en el directorio. <br/>-El _Enviar-como_ dirección está vacía.<br/>-El _Enviar-como_ dirección no es una dirección de correo electrónico válida.  <br/> |
|ErrorInvalidAttachmentId  <br/> |Este error es devuelto por la [operación GetAttachment](getattachment-operation.md) o no se encuentra la [operación DeleteAttachment](deleteattachment-operation.md) cuando un objeto attachment que se corresponde con el identificador especificado.  <br/> |
|ErrorInvalidAttachmentSubfilter  <br/> |Este error se produce cuando se intenta enlazar a una carpeta de búsqueda existente mediante el uso de una restricción de tabla de datos adjuntos de tipo complejo. Servicios Web de Exchange sólo admite simple contiene filtros contra la tabla de datos adjuntos. Si se intenta enlazar a una carpeta de búsqueda existente tiene una restricción de tabla de datos adjuntos (un subfiltro) más compleja, servicios Web de Exchange no se puede representar el XML para ese filtro y devuelve este código de respuesta. <br/><br/>Tenga en cuenta que aún puede llamar a la operación GetFolder en la carpeta, pero no se solicitan el elemento [SearchParameters](searchparameters.md) .  <br/> |
|ErrorInvalidAttachmentSubfilterTextFilter  <br/> |Este error se produce cuando se intenta enlazar a una carpeta de búsqueda existente mediante el uso de una restricción de tabla de datos adjuntos de tipo complejo. Servicios Web de Exchange sólo admite simple contiene filtros contra la tabla de datos adjuntos. <br/><br/>Si se intenta enlazar a una carpeta de búsqueda existente que tiene una restricción de tabla de datos adjuntos más compleja, servicios Web de Exchange no se puede representar el XML para ese filtro. En este caso, el subfiltro datos adjuntos contiene un filtro de texto, pero no es mirar el nombre para mostrar de los datos adjuntos.<br/><br/> Tenga en cuenta que aún puede llamar a la operación GetFolder en la carpeta, pero no se solicitan el elemento [SearchParameters](searchparameters.md) .  <br/> |
|ErrorInvalidAuthorizationContext  <br/> | Este error indica que no se pudieron el procedimiento de autorización para el solicitante.  <br/> |
|ErrorInvalidChangeKey  <br/> |Este error se produce cuando un consumidor pasa en una carpeta o un identificador de elemento con una clave de cambio que no se puede analizar. Por ejemplo, esto podría ser contenido base64 no válida o una cadena vacía.  <br/> |
|ErrorInvalidClientSecurityContext  <br/> |Este error indica que se ha producido un error interno cuando se ha intentado resolver la identidad del autor de la llamada.  <br/> |
|ErrorInvalidCompleteDate  <br/> |Este error se devuelve cuando se realiza un intento de establecer el valor del elemento [CompleteDate](completedate.md) de una tarea en una hora en el futuro. Cuando se convierte a la hora local del servidor de acceso de cliente, la [CompleteDate](completedate.md) de una tarea no se puede establecer en un valor que es posterior a la hora local en el servidor de acceso de cliente.  <br/> |
|ErrorInvalidContactEmailAddress  <br/> |Este error indica que se proporcionó una dirección de correo electrónico no válida para un contacto.  <br/> |
|ErrorInvalidContactEmailIndex  <br/> |Este error indica que se proporcionó un valor de índice no válido de correo electrónico para una entrada de correo electrónico.  <br/> |
|ErrorInvalidCrossForestCredentials  <br/> |Este error se produce cuando las credenciales que se usan para el proxy de una solicitud a un bosque del servicio de directorio diferente producirá un error en la autenticación.  <br/> |
|ErrorInvalidDelegatePermission  <br/> |Este error indica que los permisos de la carpeta especificada no son válidos.  <br/> |
|ErrorInvalidDelegateUserId  <br/> |Este error indica que el identificador de usuario delegado especificado no es válido.  <br/> |
|ErrorInvalidExchangeImpersonationHeaderData  <br/> |Este error se produce durante la suplantación de Exchange cuando un autor de la llamada no especifica un UPN, una dirección de correo electrónico o un SID de usuario. Esto también se producirá si el autor de la llamada especifica uno o varios de los y los valores están vacíos.  <br/> |
|ErrorInvalidExcludesRestriction  <br/> |Este error se produce cuando la máscara de bits que se pasó a una restricción de elemento [excluye](excludes.md) no puede que deben ser analizados.  <br/> |
|ErrorInvalidExpressionTypeForSubFilter  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidExtendedProperty  <br/> | Este error se produce cuando los siguientes eventos tienen lugar: <br/> <br/>-El autor de la llamada intenta utilizar una propiedad extendida que no es compatible con los servicios Web Exchange.  <br/>-El autor de la llamada se pasa en una combinación de valores de atributo para una propiedad extendida no válida. Esto también se produce si no se pasan atributos. Se permiten solo determinadas combinaciones.  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |Este error se produce cuando la sección de valor de una propiedad extendida no coincide con el tipo de la propiedad. <br/><br/>Por ejemplo, se establece una propiedad extendida que tiene PropertyType = "Cadena" a una matriz de números enteros, se producirá este error. Cualquier representación de cadena que no se pueda convertir en el tipo especificado para la propiedad extendida generará este error.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |Este error indica que el remitente de la invitación de uso compartido no ha creado los metadatos de la invitación para compartir.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |Este error indica que un mensaje para compartir no está pensado para el autor de la llamada.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |Este error indica que los objetos de federación de la organización del solicitante no están configurados correctamente.  <br/> |
|ErrorInvalidFolderId  <br/> |Este error se produce cuando el identificador de la carpeta está dañado.  <br/> |
|ErrorInvalidFolderTypeForOperation  <br/> |Este error indica que el tipo de la carpeta especificada no es válido para la operación actual. Por ejemplo, no se puede crear una carpeta de búsqueda en una carpeta pública.  <br/> |
|ErrorInvalidFractionalPagingParameters  <br/> | Este error se produce en paginación fraccionaria cuando el usuario ha especificado una de las siguientes: <br/> <br/>-Un numerador que es mayor que el denominador  <br/>-Un numerador que es menor que cero  <br/>-Un denominador que es menor o igual que cero  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |Este error indica que los elementos de [tipo de datos](datatype.md) y ShareFolderId son ambos presente en una solicitud.  <br/> |
|ErrorInvalidFreeBusyViewType  <br/> |Este error se produce cuando se llama a la [operación GetUserAvailability](getuseravailability-operation.md) con un [FreeBusyViewType](freebusyviewtype.md) de ninguno.  <br/> |
|ErrorInvalidId  <br/> |Este error indica que la clave de identificador o el cambio es incorrecta.  <br/> |
|ErrorInvalidIdEmpty  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **Id** que está vacío.  <br/> |
|ErrorInvalidLikeRequest  <br/> |Este error se produce cuando el elemento no puede estar vinculado. Las versiones de Exchange, comenzando por el número de compilación 15.00.0913.09 incluyen este valor.  <br/> |
|ErrorInvalidIdMalformed  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **Id** que tiene un formato incorrecto.  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |Este error indica que un identificador de elemento o la carpeta que está usando el formato de Exchange 2007 se ha especificado para una solicitud con una versión de Exchange 2007 SP1 o posterior. No se puede usar los identificadores de 2007 de Exchange en Exchange 2007 SP1 o posterior solicitudes. Se debe usar la [operación de ConvertId](convertid-operation.md) para convertirlos en primer lugar.  <br/> |
|ErrorInvalidIdMonikerTooLong  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **Id** que es demasiado largo.  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |Este error se devuelve cada vez que un identificador que no es datos adjuntos de elemento que identificador se pasa a un método de servicio Web que espera un identificador de datos adjuntos.  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |Este error se produce cuando un contacto en su buzón de correo está dañado.  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |Este error se produce cuando el autor de la llamada especifica un atributo **Id** que es demasiado largo.  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |Este error se devuelve cuando la jerarquía de los datos adjuntos en un elemento supera el máximo de 255 niveles de profundidad.  <br/> |
|ErrorInvalidIdXml  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidImContactId  <br/> |Este error se devuelve cuando el identificador de contacto de mensajería instantánea especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidImDistributionGroupSmtpAddress  <br/> |Este error se devuelve cuando el identificador de dirección SMTP especificado del grupo de distribución mensajería instantánea no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidImGroupId  <br/> |Este error se devuelve cuando el identificador de grupo de mensajería instantánea especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidIndexedPagingParameters  <br/> |Este error se produce si el desplazamiento de paginación indizado es negativo.  <br/> |
|ErrorInvalidInternetHeaderChildNodes  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidItemForOperationArchiveItem  <br/> |Indica que el elemento no es válido para una operación de **ArchiveItem** .  <br/> |
|ErrorInvalidItemForOperationAcceptItem  <br/> |Este error se produce cuando se realiza un intento de usar un objeto de respuesta AcceptItem para un tipo de elemento que no sea una convocatoria de reunión o un elemento de calendario, o cuando se realiza un intento para aceptar una repetición del elemento de calendario que se encuentra en la carpeta Elementos eliminados.  <br/> |
|ErrorInvalidItemForOperationCancelItem  <br/> |Este error se produce cuando se realiza un intento de usar un objeto de respuesta CancelItem en un tipo de elemento que no sea un elemento de calendario.  <br/> |
|ErrorInvalidItemForOperationCreateItemAttachment  <br/> | Este error se devuelve cuando se realiza un intento para crear un elemento de datos adjuntos de un tipo no admitido.  <br/><br/>  Tipos de elemento admitidos para los datos adjuntos de elemento incluyen los siguientes objetos:  <br/><br/>- [Elemento](item.md) <br/>- [Mensaje](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Tarea](task.md) <br/>- [Contacto](contact.md) <br/> <br/> Por ejemplo, si se intenta crear un dato adjunto de [MeetingMessage](meetingmessage.md) , se producirá este código de respuesta.  <br/> |
|ErrorInvalidItemForOperationCreateItem  <br/> | Este error se devuelve desde una [operación CreateItem](createitem-operation.md) si la solicitud contiene un tipo de elemento no compatible. <br/><br/>Elementos admitidos incluyen los siguientes objetos:<br/>  <br/>- [Elemento](item.md) <br/>- [Mensaje](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Tarea](task.md) <br/>- [Contacto](contact.md) <br/><br/>  Ciertos tipos de se crean como un efecto secundario de hacer algo más. Por ejemplo, los mensajes de la reunión, se crean al enviar un elemento de calendario a los asistentes; no se crean explícitamente.  <br/> |
|ErrorInvalidItemForOperationDeclineItem  <br/> |Este error se produce cuando se realiza un intento de usar un objeto de respuesta DeclineItem para un tipo de elemento que no sea una convocatoria de reunión o un elemento de calendario, o cuando se realiza un intento para rechazar una repetición del elemento de calendario que se encuentra en la carpeta Elementos eliminados.  <br/> |
|ErrorInvalidItemForOperationExpandDL  <br/> |Este error indica que la [operación de ExpandDL](expanddl-operation.md) sólo es válido para las listas de distribución privadas.  <br/> |
|ErrorInvalidItemForOperationRemoveItem  <br/> |Este error es devuelto desde un objeto de respuesta de RemoveItem si la solicitud especifica un elemento que no es una reunión de elemento de cancelación.  <br/> |
|ErrorInvalidItemForOperationSendItem  <br/> |Este error se devuelve desde una [operación de SendItem](senditem-operation.md) si la solicitud especifica un elemento que no es un elemento de mensaje.  <br/> |
|ErrorInvalidItemForOperationTentative  <br/> |Este error se produce cuando se realiza un intento de usar [TentativelyAcceptItem](tentativelyacceptitem.md) para un tipo de elemento que no sea una convocatoria de reunión o un elemento de calendario, o cuando se realiza un intento para aceptar provisionalmente una repetición del elemento de calendario que se encuentra en la carpeta Elementos eliminados.  <br/> |
|ErrorInvalidLogonType  <br/> |Este error es sólo para uso interno. Este error no se devuelve.  <br/> |
|ErrorInvalidMailbox  <br/> |Este error indica que la [operación CreateItem](createitem-operation.md) o la [operación UpdateItem](updateitem-operation.md) error al crear o actualizar una lista de distribución personal.  <br/> |
|ErrorInvalidManagedFolderProperty  <br/> |Este error se produce cuando la estructura de la carpeta administrada está dañada y no se puede representar.  <br/> |
|ErrorInvalidManagedFolderQuota  <br/> |Este error se produce cuando la cuota de que se haya establecido en la carpeta administrada es menor que cero, lo que indica una carpeta administrada dañada.  <br/> |
|ErrorInvalidManagedFolderSize  <br/> |Este error se produce cuando el tamaño que se haya establecido en la carpeta administrada es menor que cero, lo que indica una carpeta administrada dañada.  <br/> |
|ErrorInvalidMergedFreeBusyInterval  <br/> |Este error se produce cuando el combinadas libre/ocupado interno valor proporcionado no es válido. El valor mínimo predeterminado es 5 minutos. El valor máximo predeterminado es 1.440 minutos.  <br/> |
|ErrorInvalidNameForNameResolution  <br/> |Este error se produce cuando el nombre no es válido para la [operación ResolveNames](resolvenames-operation.md). Por ejemplo, una cadena de longitud cero, un espacio, una coma y un guión son todos los nombres no válidos.  <br/> |
|ErrorInvalidNetworkServiceContext  <br/> |Este error indica un error en la cuenta de servicio de red en el servidor de acceso de cliente.  <br/> |
|ErrorInvalidOofParameter  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidOperation  <br/> | Éste es un error general que se usa cuando la operación solicitada no es válida. <br/><br/>Por ejemplo, no puede hacer lo siguiente: <br/> <br/>-Realizar un recorrido "Profundo" mediante el uso de la [operación FindFolder](findfolder-operation.md) en una carpeta pública.  <br/>-Mover o copiar la raíz de la carpeta pública.  <br/>-Eliminar un elemento asociado mediante el uso de cualquier modo excepto elimina "Disco duro".  <br/>-Mover o copiar un elemento asociado.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |Este error indica que un autor de la llamada solicitó información de disponibilidad para un usuario de otra organización, pero no tiene la relación organizativa libre/ocupado habilitado.  <br/> |
|ErrorInvalidPagingMaxRows  <br/> |Este error se produce cuando un consumidor pasa un cero o un valor negativo para el número máximo de filas que se va a devolver.  <br/> |
|ErrorInvalidParentFolder  <br/> |Este error se produce cuando un consumidor pasa en una carpeta primaria no es válida para una operación. Por ejemplo, se devuelve este error si se intenta crear una carpeta dentro de una carpeta de búsqueda.  <br/> |
|ErrorInvalidPercentCompleteValue  <br/> |Este error se devuelve cuando se realiza un intento para establecer un porcentaje de finalización de tarea a un valor no válido. El valor debe ser entre 0 y 100 (ambos inclusive).  <br/> |
|ErrorInvalidPermissionSettings  <br/> |Este error indica que el nivel de permiso no es coherente con la configuración de permisos.  <br/> |
|ErrorInvalidPhoneCallId  <br/> |Este error indica que el identificador de autor de la llamada no es válido.  <br/> |
|ErrorInvalidPhoneNumber  <br/> |Este error indica que el número de teléfono no es correcto o no ajusta a las reglas del plan de marcado.  <br/> |
|ErrorInvalidPropertyAppend  <br/> | Este error se produce cuando no admite la propiedad que está intentando anexar a anexar. <br/><br/>Las siguientes son las únicas propiedades que admiten la anexión de: <br/> <br/>-Destinatarios colecciones (ToRecipients, CcRecipients, BccRecipients)  <br/>-Las colecciones de attendee (RequiredAttendees, OptionalAttendees, recursos)  <br/>-Cuerpo  <br/>-ReplyTo  <br/><br/>  Además, este error se produce cuando se anexa el cuerpo de un mensaje si el formato especificado en la solicitud no coincide con el formato del elemento en el almacén.  <br/> |
|ErrorInvalidPropertyDelete  <br/> |Este error se produce si la operación de eliminación está especificada en una llamada de [operación de UpdateItem](updateitem-operation.md) o [UpdateFolder](updatefolder-operation.md) para una propiedad que no es compatible con la operación de eliminación. Por ejemplo, no se puede eliminar el elemento [ItemId](itemid.md) del objeto de [elemento](item.md) .  <br/> |
|ErrorInvalidPropertyForExists  <br/> |Este error se produce si el consumidor pasa en una de las propiedades de marca en un filtro de [Exists](exists.md) . Por ejemplo, este error se produce si se especifican los indicadores [estáleído](isread.md) o [IsFromMe](isfromme.md) en el elemento [Exists](exists.md) . La solicitud debe utilizar el elemento [IsEqualTo](isequalto.md) en su lugar para estos tal y como están marcas y, por tanto, parte de una sola propiedad.  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |Este error se produce cuando la propiedad que está intentando manipular no es compatible con la operación que se lleva a cabo en él.  <br/> |
|ErrorInvalidPropertyRequest  <br/> | Este error se produce si una propiedad que se especifica en la solicitud no está disponible para el tipo de elemento. Por ejemplo, se devuelve este error si se solicita una propiedad que sólo está disponible en los elementos del calendario en una [operación de GetItem](getitem-operation.md) llamar para un mensaje o se actualiza en una [operación de UpdateItem](updateitem-operation.md) llamar para un mensaje. <br/> <br/>  Esto se produce en las siguientes operaciones: <br/> <br/>- [Operación GetItem](getitem-operation.md) <br/>- [Operación GetFolder](getfolder-operation.md) <br/>- [Operación UpdateItem](updateitem-operation.md) <br/>- [Operación UpdateFolder](updatefolder-operation.md) <br/> |
|ErrorInvalidPropertySet  <br/> |Este error indica que la propiedad que está intentando manipular no es compatible con la operación que se lleva a cabo en él. Por ejemplo, se devuelve este error si la propiedad que está intentando establecer es de sólo lectura.  <br/> |
|ErrorInvalidPropertyUpdateSentMessage  <br/> | Este error se produce durante una [operación de UpdateItem](updateitem-operation.md) cuando un cliente intenta actualizar determinadas propiedades de un mensaje que ya se ha enviado.<br/><br/> Por ejemplo, no se puede actualizar las siguientes propiedades en un mensaje enviado: <br/> <br/>- [IsReadReceiptRequested](isreadreceiptrequested.md) <br/>- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |
|ErrorInvalidProxySecurityContext  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidPullSubscriptionId  <br/> |Este error se produce si se llama a la [operación GetEvents](getevents-operation.md) o la [operación de cancelación de suscripción](unsubscribe-operation.md) mediante un identificador de suscripción de inserción. Para anular la suscripción de una suscripción de inserción, debe responder a una solicitud de inserción con una respuesta de cancelación de suscripción, o desconectar el servicio Web y espere a que las notificaciones de inserción para el tiempo de espera.  <br/> |
|ErrorInvalidPushSubscriptionUrl  <br/> | Este error es devuelto por la [operación Suscribir](subscribe-operation.md) cuando se crea una suscripción de "inserción" y se indica que la dirección URL que se incluye en la solicitud no es válida.<br/><br/>Deben cumplirse las siguientes condiciones para que los servicios Web de Exchange Aceptar la dirección URL: <br/> <br/>-Longitud de la cadena \> 0 y \< 2083.  <br/>-Protocolo es http o https.  <br/>-La dirección URL se puede analizar por la clase URI Microsoft .NET Framework.  <br/> |
|ErrorInvalidRecipients  <br/> |Este error indica que la colección de destinatarios en el mensaje o la colección de attendee en el elemento de calendario no es válida. Por ejemplo, se devolverá este error cuando se realiza un intento de enviar un elemento que carece de destinatarios.  <br/> |
|ErrorInvalidRecipientSubfilter  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que no se representan los servicios Web Exchange. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterComparison  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que no se representan los servicios Web Exchange. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterOrder  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que no se representan los servicios Web Exchange. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterTextFilter  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que no se representan los servicios Web Exchange. Para solucionar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidReferenceItem  <br/> | Este error se devuelve desde la [operación CreateItem](createitem-operation.md) para reenviar y responder objetos de respuesta en los siguientes escenarios:<br/>  <br/>-El identificador del elemento que se hace referencia no es un [mensaje](message-ex15websvcsotherref.md), un [CalendarItem](calendaritem.md)o un descendiente de un **mensaje** o **CalendarItem**.  <br/>-El identificador de elemento de referencia es para un **CalendarItem** y el organizador se intenta responder o responder a todos para designar.  <br/>-El mensaje es un borrador y se selecciona responder o responder a todos.  <br/>-El elemento de referencia, para [SuppressReadReceipt](suppressreadreceipt.md), no es un **mensaje** o un descendiente de un **mensaje**.  <br/> |
|ErrorInvalidRequest  <br/> |Este error se produce cuando la solicitud SOAP tiene un encabezado de acción SOAP, pero no hay nada en el cuerpo SOAP. Tenga en cuenta que no se requiere el encabezado de acción SOAP como servicios Web de Exchange puede determinar el método para llamar desde el nombre local del elemento raíz en el cuerpo SOAP.  <br/> |
|ErrorInvalidRestriction  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidRetentionTagTypeMismatch  <br/> |Este error se devuelve cuando la etiqueta de retención especificado tiene asociada una acción incorrecta. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInvisible  <br/> |Este error se devuelve cuando se realiza un intento para establecer una etiqueta que no existe o invisible en una propiedad **PolicyTag** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInheritance  <br/> |Este error se devuelve cuando se realiza un intento para establecer una etiqueta implícita en la propiedad **PolicyTag** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagIdGuid  <br/> |Indica que la etiqueta de retención GUID no es válida.  <br/> |
|ErrorInvalidRoutingType  <br/> |Este error se produce si el tipo de distribución que se pasa de un elemento de [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) no es válido. Normalmente, el tipo de enrutamiento se establece para el protocolo Simple de transferencia de correo (SMTP).  <br/> |
|ErrorInvalidScheduledOofDuration  <br/> |Este error se produce si la hora de finalización de la duración especificada no es mayor que la hora de inicio, o si la hora de finalización no tienen lugar en el futuro.  <br/> |
|ErrorInvalidSchemaVersionForMailboxVersion  <br/> |Este error indica que una solicitud de proxy que se envió a otro servidor no es capaz de atender la solicitud debido a un error de coincidencia del control de versiones.  <br/> |
|ErrorInvalidSecurityDescriptor  <br/> |Este error indica que el descriptor de seguridad de Exchange en la carpeta del calendario en el almacén está dañado.  <br/> |
|ErrorInvalidSendItemSaveSettings  <br/> |Este error se produce durante un intento de enviar un elemento donde el [SavedItemFolderId](saveditemfolderid.md) se especifica en la solicitud, pero la propiedad **SaveItemToFolder** está establecida en **false**.  <br/> |
|ErrorInvalidSerializedAccessToken  <br/> |Este error indica que el símbolo (token) que se ha pasado en el encabezado es incorrecto, no hace referencia a una cuenta válida en el directorio o falta el grupo principal **ConnectingSID**.  <br/> |
|ErrorInvalidSharingData  <br/> |Este error indica que el uso compartido metadatos no están válido. Esto puede deberse a XML no válido.  <br/> |
|ErrorInvalidSharingMessage  <br/> |Este error indica que el mensaje para compartir no es válido. Esto puede deberse a una propiedad que faltan.  <br/> |
|ErrorInvalidSid  <br/> |Este error se produce cuando se pasa el SID en una solicitud no es válida.  <br/> |
|ErrorInvalidSIPUri  <br/> |Este error indica que el nombre de SIP, el plan de marcado o el número de teléfono son los URI de SIP no válido.  <br/> |
|ErrorInvalidServerVersion  <br/> |Este error indica que se ha especificado una versión de servidor de la solicitud no válida en la solicitud.  <br/> |
|ErrorInvalidSmtpAddress  <br/> |Este error se produce cuando no se puede analizar la dirección SMTP.  <br/> |
|ErrorInvalidSubfilterType  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidSubfilterTypeNotAttendeeType  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidSubfilterTypeNotRecipientType  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidSubscription  <br/> |Este error indica que la suscripción ya no es válida. Esto podría ser debido a que se reinicie el servidor de acceso de cliente o porque la suscripción ha expirado.  <br/> |
|ErrorInvalidSubscriptionRequest  <br/> |Este error indica que la solicitud subscribe incluye carpetas públicas varios identificadores. Una suscripción puede incluir varias carpetas desde el mismo buzón o un ID de carpeta pública.  <br/> |
|ErrorInvalidSyncStateData  <br/> |Este error es devuelto por [SyncFolderItems](syncfolderitems.md) o [SyncFolderHierarchy](syncfolderhierarchy.md) si los datos de [estado de sincronización](syncstate-ex15websvcsotherref.md) que se ha pasado no están válidos. Para corregir este error, debe volver a sincronizar sin el estado de sincronización. Asegúrese de que si se encuentra la sincronización de conservación de datos BLOB de estado, es no accidentalmente el truncamiento el BLOB.  <br/> |
|ErrorInvalidTimeInterval  <br/> |Este error indica que el intervalo de tiempo especificado no es válido. La hora de inicio debe ser mayor o igual a la hora de finalización.  <br/> |
|ErrorInvalidUserInfo  <br/> |Este error indica que se ha especificado un incoherente internamente [UserId](userid.md) para una operación de permisos. Por ejemplo, si un identificador de usuario completo es especificado (valor predeterminado o anónimo), se devuelve este error si intenta también especificar un SID, o una dirección SMTP principal o nombre para mostrar para este usuario.  <br/> |
|ErrorInvalidUserOofSettings  <br/> |Este error indica que la configuración de fuera de oficina (OOF) del usuario no es válida debido a una respuesta interna o externa que faltan.  <br/> |
|ErrorInvalidUserPrincipalName  <br/> |Este error se produce durante la suplantación de Exchange. El autor de la llamada se pasa en un UPN no válido en el encabezado SOAP que no estaba accesible en el directorio.  <br/> |
|ErrorInvalidUserSid  <br/> |Este error se produce cuando se pasa el SID en una solicitud no es válida.  <br/> |
|ErrorInvalidUserSidMissingUPN  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorInvalidValueForProperty  <br/> |Este error indica que no es válido para la propiedad con que se compara el valor de comparación en la restricción.<br/><br/> Por ejemplo, el valor de comparación de [DateTimeCreated](datetimecreated.md) > **true** devolvería este código de respuesta. <br/><br/>Este código de respuesta también se devuelve si especifica una propiedad de enumeración en la comparación, pero el valor que se compara con no es un valor válido para ese (enumeración).  <br/> |
|ErrorInvalidWatermark  <br/> |Este error está causado por una marca de agua no válido.  <br/> |
|ErrorIPGatewayNotFound  <br/> |Este error indica que una puerta de enlace VoIP válido no está disponible.  <br/> |
|ErrorIrresolvableConflict  <br/> |Este error indica que pudo resolución de conflictos se resuelven los cambios de las propiedades. Los elementos en el almacén han cambiado y debe actualizarse. Recuperar la clave de cambio actualizada e inténtelo de nuevo.  <br/> |
|ErrorItemCorrupt  <br/> |Este error indica que el estado del objeto está dañado y no se puede recuperar. Al recuperar un elemento, sólo ciertos elementos estará en este estado, como [Body](body.md) y [MimeContent](mimecontent.md). Omitir estos elementos y vuelva a intentar la operación.  <br/> |
|ErrorItemNotFound  <br/> |Este error se produce cuando el elemento no se encontró o no tiene permiso para obtener acceso al elemento.  <br/> |
|ErrorItemPropertyRequestFailed  <br/> |Este error se produce si se produce un error en una solicitud de propiedad en un elemento. Es posible que exista la propiedad, pero no se puede recuperar.  <br/> |
|ErrorItemSave  <br/> |Este error se produce cuando se intenta guardar el elemento o la carpeta producirá un error.  <br/> |
|ErrorItemSavePropertyError  <br/> |Este error se produce cuando se intenta guardar el elemento o la carpeta producirá un error debido a los valores de propiedad no válido. El código de respuesta incluye la ruta de acceso de las propiedades no válidas.  <br/> |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorLocalServerObjectNotFound  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorLogonAsNetworkServiceFailed  <br/> |Este error indica que el servicio de disponibilidad no pudo iniciar sesión como servicio de red para las solicitudes de proxy a los sitios adecuados o bosques. Esta respuesta normalmente indica un error de configuración.  <br/> |
|ErrorMailboxConfiguration  <br/> |Este error indica que la información de buzón de correo en AD DS está configurada incorrectamente.  <br/> |
|ErrorMailboxDataArrayEmpty  <br/> |Este error indica que el elemento [MailboxDataArray](mailboxdataarray.md) en la solicitud está vacío. Debe proporcionar al menos un identificador de buzón de correo.  <br/> |
|ErrorMailboxDataArrayTooBig  <br/> |Este error se produce cuando se proporcionan más de 100 entradas en un elemento [MailboxDataArray](mailboxdataarray.md) ..  <br/> |
|ErrorMailboxFailover  <br/> |Este error indica que debido a que el buzón está en un proceso de conmutación por error, error al intentar tener acceso a un buzón de correo.  <br/> |
|ErrorMailboxHoldNotFound  <br/> |Indica que no se encontró la suspensión de buzón de correo.  <br/> |
|ErrorMailboxLogonFailed  <br/> |Este error se produce cuando falló la conexión con el buzón de correo para obtener la información de la vista de calendario.  <br/> |
|ErrorMailboxMoveInProgress  <br/> | Este error indica que se va a mover el buzón de correo a un servidor o un almacén de buzón diferente. Este error también puede indicar que el buzón se encuentra en otra base de datos de servidor o buzón de correo.  <br/> |
|ErrorMailboxStoreUnavailable  <br/> | Este error indica que uno de los siguiente error producido las condiciones de:  <br/><br/>-El almacén de buzón de correo está dañado.  <br/>-El almacén de buzón de correo se está deteniendo.  <br/>-El almacén de buzón de correo está sin conexión.  <br/>-Error de red al que se ha intentado obtener acceso al almacén de buzón de correo.  <br/>-El almacén de buzón de correo está sobrecargado y no puede aceptar más conexiones.  <br/>-El almacén de buzón de correo se ha pausado.  <br/> |
|ErrorMailRecipientNotFound  <br/> |Este error se produce si la información del elemento [MailboxData](mailboxdata.md) no se puede asignar a una cuenta de buzón de correo válido.  <br/> |
|ErrorMailTipsDisabled  <br/> |Este error indica que las sugerencias de correo están deshabilitadas.  <br/> |
|ErrorManagedFolderAlreadyExists  <br/> |Este error se produce si la carpeta administrada que está intentando crear ya existe en un buzón de correo.  <br/> |
|ErrorManagedFolderNotFound  <br/> |Este error se produce cuando el nombre de la carpeta que se especificó en la solicitud no se asigna a una definición de carpeta administrada en AD DS. Sólo se pueden crear instancias de las carpetas administradas para las carpetas que se definen en AD DS. Compruebe el nombre e inténtelo de nuevo.  <br/> |
|ErrorManagedFoldersRootFailure  <br/> |Este error indica que se ha eliminado la raíz de las carpetas administradas desde el buzón de correo o que existe una carpeta en la misma carpeta primaria que tiene el nombre de la raíz de la carpeta administrada. Esto también se producirá si el intento de crear la raíz administrada carpeta se produce un error.  <br/> |
|ErrorMeetingSuggestionGenerationFailed  <br/> |Este error indica que el motor de sugerencias detectó un problema cuando intentaba generar las sugerencias.  <br/> |
|ErrorMessageDispositionRequired  <br/> | Este error se produce si no se establece el atributo **MessageDisposition** .<br/><br/> Este atributo es necesario para los siguientes elementos: <br/> <br/>-La [operación CreateItem](createitem-operation.md) y la [operación UpdateItem](updateitem-operation.md) cuando se crea o actualiza el elemento es un [mensaje](message-ex15websvcsotherref.md).  <br/>- Objetos de respuesta [CancelCalendarItem](cancelcalendaritem.md), [AcceptItem](acceptitem.md), [DeclineItem](declineitem.md)o [TentativelyAcceptItem](tentativelyacceptitem.md) .  <br/> |
|ErrorMessageSizeExceeded  <br/> |Este error indica que el mensaje que está intentando enviar supera los límites permitidos.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |Este error indica que no se encuentra el dominio especificado.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |Este error indica que el servicio de seguimiento de mensajes no pueden realizar un seguimiento del mensaje.  <br/> |
| ErrorMessageTrackingTransientError  <br/> |Este error indica que el servicio de seguimiento de mensajes es inactivo u ocupado. Este código de error indica un error transitorio. Los clientes pueden Reintentar para conectarse al servidor cuando se recibe este error.  <br/> |
|ErrorMimeContentConversionFailed  <br/> |Este error se produce cuando el contenido MIME no es válida para una [operación CreateItem](createitem-operation.md)iCal. Para una [operación GetItem](getitem-operation.md), esta respuesta indica que no se pudo generar el contenido MIME.  <br/> |
|ErrorMimeContentInvalid  <br/> |Este error se produce cuando el contenido MIME no es válido.  <br/> |
|ErrorMimeContentInvalidBase64String  <br/> |Este error se produce cuando el contenido MIME de la solicitud es no una base 64 cadena válida.  <br/> |
|ErrorMissingArgument  <br/> |Este error indica que faltaba un argumento necesario de la solicitud. El texto del mensaje de respuesta indica el argumento que se va a comprobar.  <br/> |
|ErrorMissingEmailAddress  <br/> |Este error indica que especificó un identificador de la carpeta completo en la solicitud, pero la cuenta que realizó la solicitud no tiene un buzón de correo en el sistema. En ese caso, debe proporcionar un subelemento [buzón de correo](mailbox.md) de [DistinguishedFolderId](distinguishedfolderid.md).  <br/> |
|ErrorMissingEmailAddressForManagedFolder  <br/> |Este error indica que especificó un identificador de la carpeta completo en la solicitud, pero la cuenta que realizó la solicitud no tiene un buzón de correo en el sistema. En ese caso, debe proporcionar un subelemento [buzón de correo](mailbox.md) de [DistinguishedFolderId](distinguishedfolderid.md). Esta respuesta se devuelve desde la [operación CreateManagedFolder](createmanagedfolder-operation.md).  <br/> |
|ErrorMissingInformationEmailAddress  <br/> |Este error se produce si falta el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) .  <br/> |
|ErrorMissingInformationReferenceItemId  <br/> |Este error se produce si falta el [ReferenceItemId](referenceitemid.md) .  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |Nunca se devuelve este código de error.  <br/> |
|ErrorMissingItemForCreateItemAttachment  <br/> |Este error se devuelve cuando se realiza un intento para no incluir el elemento en el elemento **ItemAttachment** de una solicitud de [operación CreateAttachment](createattachment-operation.md) .  <br/> |
|ErrorMissingManagedFolderId  <br/> |Este error se produce cuando la propiedad de los identificadores de directiva, etiqueta de la propiedad 0x6732, para la carpeta falta. Se debe considerar una carpeta dañada.  <br/> |
|ErrorMissingRecipients  <br/> |Este error indica que ha intentado enviar un elemento sin incluir los destinatarios. Tenga en cuenta que si se llama a la [operación CreateItem](createitem-operation.md) con una disposición de mensaje que hace que se envíe el mensaje, recibirá el siguiente código de respuesta: **ErrorInvalidRecipients**.  <br/> |
|ErrorMissingUserIdInformation  <br/> |Este error indica que un [identificador de usuario](userid.md) no se ha especificado completamente en un conjunto de permisos.  <br/> |
|ErrorMoreThanOneAccessModeSpecified  <br/> |Este error indica que ha especificado más de un valor de elemento [ExchangeImpersonation](exchangeimpersonation.md) dentro de una solicitud.  <br/> |
|ErrorMoveCopyFailed  <br/> |Este error indica que ha fallado la operación de mover o copiar. Mover se produce en la [operación CreateItem](createitem-operation.md) cuando acepta una convocatoria de reunión que se encuentra en la carpeta Elementos eliminados. Además, si se rechaza una convocatoria de reunión, cancelar un elemento de calendario o eliminar una reunión de su calendario, se mueve a la carpeta Elementos eliminados.  <br/> |
|ErrorMoveDistinguishedFolder  <br/> |Este error se produce si se intenta mover una carpeta distintivo.  <br/> |
|ErrorMultiLegacyMailboxAccess  <br/> |Este error se produce cuando una solicitud intenta obtener acceso a varios servidores de buzón de correo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorNameResolutionMultipleResults  <br/> |Este error se produce si la [operación ResolveNames](resolvenames-operation.md) devuelve más de un resultado o el nombre ambiguo que especificó coincide con más de un objeto en el directorio. El código de respuesta incluye los nombres coincidentes en los datos de respuesta.  <br/> |
|ErrorNameResolutionNoMailbox  <br/> |Este error indica que el autor de la llamada no tiene un buzón de correo en el sistema. La [operación de ResolveNames](resolvenames-operation.md) o [ExpandDL](expanddl-operation.md) no es válido para la conexión de un usuario sin un buzón de correo.  <br/> |
|ErrorNameResolutionNoResults  <br/> |Este error indica que la [operación ResolveNames](resolvenames-operation.md) no devuelve ningún resultado.  <br/> |
|ErrorNoApplicableProxyCASServersAvailable  <br/> |Este código de error debe devolverse cuando el servicio Web no puede encontrar un servidor para atender la solicitud.  <br/> |
|ErrorNoCalendar  <br/> |Este error se produce si no hay ninguna carpeta de calendario para el buzón de correo.  <br/> |
|ErrorNoDestinationCASDueToKerberosRequirements  <br/> |Este error indica que la solicitud hace referencia a un buzón de correo en otro sitio de Active Directory, pero no hay servidores de acceso de cliente en el sitio de destino se han configurado para la autenticación de Windows y, por lo tanto, la solicitud podría no ser procesadas por el proxy.  <br/> |
|ErrorNoDestinationCASDueToSSLRequirements  <br/> |Este error indica que la solicitud hace referencia a un buzón de correo en otro sitio de Active Directory, pero no hay servidores de acceso de cliente en el sitio de destino se configuraron para las conexiones SSL y, por lo tanto, la solicitud podría no ser procesadas por el proxy.  <br/> |
|ErrorNoDestinationCASDueToVersionMismatch  <br/> |Este error indica que la solicitud hace referencia a un buzón de correo en otro sitio de Active Directory, pero no hay servidores de acceso de cliente en el sitio de destino eran de una versión de producto aceptable para recibir la solicitud y, por lo tanto, la solicitud podría no ser procesadas por el proxy.  <br/> |
|ErrorNoFolderClassOverride  <br/> |Este error se produce si se establece el elemento de [FolderClass](folderclass.md) cuando se crea un elemento que no sea una carpeta genérica. Para las carpetas con tipo como [CalendarFolder](calendarfolder.md) y [TasksFolder](tasksfolder.md), la clase de la carpeta está implícito. Si se establece la clase de carpeta en un tipo de carpeta diferente mediante el uso de los resultados de la [operación UpdateFolder](updatefolder-operation.md) en la respuesta de **ErrorObjectTypeChanged** . En su lugar, use un tipo de carpeta genérico, pero establezca la clase de carpeta en el valor que requiere. Servicios Web Exchange creará la carpeta fuertemente tipada correcta.  <br/> |
|ErrorNoFreeBusyAccess  <br/> |Este error indica que el autor de la llamada no tiene derechos de visualización de disponibilidad en la carpeta de calendario en cuestión.  <br/> |
|ErrorNonExistentMailbox  <br/> | Este error se produce en los siguientes escenarios: <br/> <br/>-Dirección de correo electrónico está vacía en [CreateManagedFolder](createmanagedfolder.md).  <br/>-Dirección de correo electrónico no hace referencia a una cuenta válida en una solicitud que toma una dirección de correo electrónico en el cuerpo o en el encabezado SOAP, por ejemplo, como en una llamada de suplantación de Exchange.  <br/> |
|ErrorNonPrimarySmtpAddress  <br/> |Este error se produce cuando un autor de la llamada pasa una dirección de SMTP no es el principal. La respuesta incluye la dirección SMTP correcta a usar.  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |Este error indica que las propiedades MAPI en el intervalo personalizado, 0 x 8000 y mayor, no se puede hacer referencia a las etiquetas de propiedad. Debe usar la propiedad de la API administrada de EWS [PropertySetId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)o el elemento EWS [ExtendedFieldURI](extendedfielduri.md) con el atributo PropertySetId.  <br/> |
|ErrorNoPublicFolderReplicaAvailable  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorNoPublicFolderServerAvailable  <br/> |Este código de error debe devolverse si no hay ningún servidor de carpetas públicas está disponible o si el autor de la llamada no tiene un servidor principal público.  <br/> |
|ErrorNoRespondingCASInDestinationSite  <br/> |Este error indica que la solicitud a que se refiere a un buzón en otro sitio de Active Directory, pero ninguno de los servidores de acceso de cliente en que ha respondido de sitio y, por lo tanto, la solicitud podría no ser procesadas por el proxy.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |Este error indica que el llamador intentó conceder los permisos de su carpeta Calendario o los contactos a un usuario de otra organización, y el intento produjo un error.  <br/> |
|ErrorNotDelegate  <br/> |Este error indica que el usuario no es un delegado para el buzón de correo. Es devuelto por la [operación de GetDelegate](getdelegate-operation.md), la [operación de RemoveDelegate](removedelegate-operation.md)y la [operación de UpdateDelegate](updatedelegate-operation.md) cuando el usuario delegado especificado no se encuentra en la lista de delegados.  <br/> |
|ErrorNotEnoughMemory  <br/> |Este error indica que no se pudo completar la operación a causa de memoria insuficiente.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |Este error indica que no se admite el mensaje para compartir.  <br/> |
|ErrorObjectTypeChanged  <br/> |Este error se produce si cambia el tipo de objeto.  <br/> |
|ErrorOccurrenceCrossingBoundary  <br/> |Este error se produce cuando se actualiza la hora de [Inicio](start.md) o [finalización](end-ex15websvcsotherref.md) de una ocurrencia para que la aparición está programada para ocurrir anteriormente o posterior a la aparición anterior o siguiente correspondiente.  <br/> |
|ErrorOccurrenceTimeSpanTooBig  <br/> |Este error indica que el tiempo asignado de una repetición dada se superpone a otra repetición del mismo elemento periódico. Esta respuesta también se produce cuando la duración en minutos de una repetición dada es mayor que Int32.MaxValue.  <br/> |
|ErrorOperationNotAllowedWithPublicFolderRoot  <br/> |Este error indica que la operación actual no es válida para la raíz de la carpeta pública.  <br/> |
|ErrorOrganizationNotFederated  <br/> |Este error indica que la organización del solicitante no está federada para que el solicitante no puede crear mensajes de uso compartidos para enviar a un usuario externo o que no puede aceptar el uso compartido de los mensajes recibidos de un usuario externo.  <br/> |
|ErrorParentFolderIdRequired  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorParentFolderNotFound  <br/> |Este error se produce en la [operación de CreateFolder](createfolder-operation.md) cuando no se encuentra la carpeta principal.  <br/> |
|ErrorPasswordChangeRequired  <br/> |Este error indica que debe cambiar la contraseña antes de que puede tener acceso a este buzón de correo. Esto se produce cuando se ha creado una nueva cuenta y el administrador que se indica que el usuario debe cambiar la contraseña en el primer inicio de sesión. No se puede actualizar la contraseña mediante el uso de servicios Web de Exchange. Debe usar una herramienta como Microsoft Office Outlook Web App para cambiar la contraseña.  <br/> |
|ErrorPasswordExpired  <br/> |Este error indica que la contraseña ha expirado. No se puede cambiar la contraseña mediante el uso de servicios Web de Exchange. Debe usar una herramienta como Outlook Web App para cambiar la contraseña.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |Este error indica que el solicitante intentado conceder permisos en su calendario o carpeta de contactos para un usuario externo, pero la directiva de uso compartido asignado al solicitante indica que el nivel de permiso solicitado es mayor que permite que la directiva de uso compartido.  <br/> |
|ErrorPhoneNumberNotDialable  <br/> |Este error indica que el número de teléfono no estaba en el formato correcto.  <br/> |
|ErrorPropertyUpdate  <br/> |Este error indica que la actualización no se pudieron debido a los valores de propiedad no válido. El mensaje de respuesta incluye las rutas de acceso de propiedad no válido.  <br/> |
|ErrorPromptPublishingOperationFailed  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorPropertyValidationFailure  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorProxiedSubscriptionCallFailure  <br/> |Este error indica que la solicitud hace referencia a una suscripción de que existe en otro servidor de acceso de cliente, pero el error en un intento de proxy de la solicitud a ese servidor acceso de cliente.  <br/> |
|ErrorProxyCallFailed  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorProxyGroupSidLimitExceeded  <br/> |Este error indica que la solicitud hace referencia a un buzón de correo en otro sitio de Active Directory, y el autor de la llamada original es un miembro de más de 3.000 grupos.  <br/> |
|ErrorProxyRequestNotAllowed  <br/> |Este error indica que la solicitud de servicios Web de Exchange se envían a otro servidor de acceso de cliente al intentar llevar a cabo una solicitud de [GetUserAvailabilityRequest](getuseravailabilityrequest.md) no es válida. Este código de respuesta normalmente indica que se ha producido un error de configuración o derechos o que alguien ha intentado sin éxito imitar una solicitud de proxy de disponibilidad.  <br/> |
|ErrorProxyRequestProcessingFailed  <br/> |Este error indica que los servicios Web Exchange intentó proxy de una solicitud de disponibilidad a otro servidor de acceso de cliente para el cumplimiento, pero la solicitud falla. Esta respuesta puede deberse a problemas de conectividad de red o problemas de tiempo de espera de solicitud.  <br/> |
|ErrorProxyServiceDiscoveryFailed  <br/> |Este código de error se debe devolver si el servicio Web no puede determinar si la solicitud se procesadas por el proxy a otro servidor o se va a ejecutar en el servidor de destino.  <br/> |
|ErrorProxyTokenExpired  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorPublicFolderMailboxDiscoveryFailed  <br/> |Este error se produce cuando el buzón de correo de carpetas públicas no se encuentra la dirección URL. Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorPublicFolderOperationFailed  <br/> |Este error se produce cuando se realiza un intento para tener acceso a una carpeta pública y el intento se realiza correctamente. Este error se introdujo en Exchange 2013Exchange Server 2013.  <br/> |
|ErrorPublicFolderRequestProcessingFailed  <br/> |Este error se produce cuando el destinatario que se pasó a la [operación GetUserAvailability](getuseravailability-operation.md) se encuentra en un equipo que está ejecutando una versión de Exchange Server que es anterior a Exchange 2007 y la solicitud para recuperar información de libre/ocupado para el no se pudo destinatario desde el servidor de carpetas públicas.  <br/> |
|ErrorPublicFolderServerNotFound  <br/> |Este error se produce cuando el destinatario que se pasó a la [operación GetUserAvailability](getuseravailability-operation.md) se encuentra en un equipo que está ejecutando una versión de Exchange Server que es anterior a Exchange 2007 y la solicitud para recuperar información de libre/ocupado para el no se pudo destinatario desde el servidor de carpetas públicas porque la unidad organizativa no tenía un servidor de carpetas públicas asociado.  <br/> |
|ErrorPublicFolderSyncException  <br/> |Este error se produce cuando una operación de sincronización se ejecuta correctamente en el buzón de correo de la carpeta pública principal pero no se realiza correctamente con el buzón de carpeta pública secundaria. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorQueryFilterTooLong  <br/> |Este error indica que la restricción de la carpeta de búsqueda puede ser válida, pero no se admite por EWS. Servicios Web Exchange limita las restricciones para contener un máximo de 255 expresiones de filtro. Si se intenta enlazar a una carpeta de búsqueda existente que supere los 255, se devuelve este código de respuesta.  <br/> |
|ErrorQuotaExceeded  <br/> |Este error se produce cuando se supera la cuota de buzón de correo.  <br/> |
|ErrorReadEventsFailed  <br/> |Este error es devuelto por la [operación GetEvents](getevents-operation.md) o inserción notificaciones cuando se produzca un error al recuperar la información de evento. Cuando se devuelve este error, se elimina la suscripción. Volver a crear la sincronización de eventos basándose en la última marca de agua conocido.  <br/> |
|ErrorReadReceiptNotPending  <br/> |Este error es devuelto por la [operación CreateItem](createitem-operation.md) si se ha intentado suprimir una confirmación de lectura al remitente del mensaje no ha solicitado una confirmación de lectura en el mensaje o si el mensaje se encuentra en la carpeta correo electrónico no deseado.  <br/> |
|ErrorRecurrenceEndDateTooBig  <br/> |Este error se produce cuando la fecha de finalización de la periodicidad es después de 1/9/4500.  <br/> |
|ErrorRecurrenceHasNoOccurrence  <br/> |Este error se produce cuando la periodicidad especificada no tiene todas las instancias de aparición en el intervalo especificado.  <br/> |
|ErrorRemoveDelegatesFailed  <br/> |Este error indica que la lista de delegados no se pudieron guardar después de que se han eliminado los delegados.  <br/> |
|ErrorRequestAborted  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorRequestStreamTooBig  <br/> | Este error se produce cuando la secuencia de solicitud es superior a 400 KB.  <br/> |
|ErrorRequiredPropertyMissing  <br/> |Este error se devuelve cuando falta una propiedad necesaria en una solicitud de [operación CreateAttachment](createattachment-operation.md) . Falta la propiedad URI se incluye en la respuesta.  <br/> |
|ErrorResolveNamesInvalidFolderType  <br/> |Este error indica que el autor de la llamada ha especificado una carpeta que no es una carpeta de contactos para la [operación ResolveNames](resolvenames-operation.md).  <br/> |
|ErrorResolveNamesOnlyOneContactsFolderAllowed  <br/> |Este error indica que el autor de la llamada ha especificado más de una carpeta de contactos para la [operación ResolveNames](resolvenames-operation.md).  <br/> |
|ErrorResponseSchemaValidation  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorRestrictionTooLong  <br/> |Este error se produce si la restricción contiene más de 255 nodos.  <br/> |
|ErrorRestrictionTooComplex  <br/> |Este error se produce cuando no se puede evaluar la restricción de los servicios Web Exchange.  <br/> |
|ErrorResultSetTooBig  <br/> |Este error indica que el número de entradas de calendario de un destinatario determinado supera el límite permitido de 1000. Reducir la ventana y vuelva a intentarlo.  <br/> |
|ErrorSavedItemFolderNotFound  <br/> |Este error se produce cuando no se encuentra el [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
|ErrorSchemaValidation  <br/> | Este error se produce cuando la solicitud no se puede validar con el esquema.  <br/> |
|ErrorSearchFolderNotInitialized  <br/> |Este error indica que se creó la carpeta de búsqueda, pero nunca se han establecido los criterios de búsqueda en la carpeta. Esto sólo se produce cuando tiene acceso a las carpetas de búsqueda dañado que se crearon con otra API o cliente. Para corregir este error, use la [operación UpdateFolder](updatefolder-operation.md) para establecer el elemento [SearchParameters](searchparameters.md) para incluir la restricción que debería estar en la carpeta.  <br/> |
|ErrorSendAsDenied  <br/> | Este error se produce cuando se produzcan ambas de las siguientes condiciones: <br/> <br/>-Un usuario se han concedido permisos CanActAsOwner pero no se ha concedido permisos de delegado en el buzón de correo de la entidad de seguridad.  <br/>-El mismo usuario intenta crear y enviar un mensaje de correo electrónico en el buzón de la entidad de seguridad mediante la opción SendAndSaveCopy.<br/>  <br/>  El resultado es un error de ErrorSendAsDenied y la creación de un mensaje de correo electrónico en la carpeta Borradores de la entidad de seguridad.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Este error es devuelto por la [operación DeleteItem](deleteitem-operation.md) si falta el atributo **SendMeetingCancellations** de la solicitud y el elemento que desea eliminar es un elemento de calendario.  <br/> |
|ErrorSendMeetingInvitationsOrCancellationsRequired  <br/> |Este error es devuelto por la [operación UpdateItem](updateitem-operation.md) si falta el atributo **SendMeetingInvitationsOrCancellations** de la solicitud y el elemento que se debe actualizar es un elemento de calendario.  <br/> |
|ErrorSendMeetingInvitationsRequired  <br/> |Este error es devuelto por la [operación CreateItem](createitem-operation.md) si falta el atributo **SendMeetingInvitations** de la solicitud y el elemento que se va a crear es un elemento de calendario.  <br/> |
|ErrorSentMeetingRequestUpdate  <br/> |Este error indica que después de que el organizador envía una convocatoria de reunión, la solicitud no se puede actualizar. Para modificar la reunión, modifique el elemento de calendario, no la convocatoria de reunión.  <br/> |
|ErrorSentTaskRequestUpdate  <br/> |Este error indica que después de que el iniciador de tarea envía una solicitud de tarea, dicha solicitud no se puede actualizar.  <br/> |
|ErrorServerBusy  <br/> |Este error se produce cuando el servidor está ocupado.  <br/> |
|ErrorServiceDiscoveryFailed  <br/> |Este error indica que los servicios Web Exchange intentó proxy de una solicitud de disponibilidad del usuario para el bosque adecuado para el destinatario, pero no se pudo determinar dónde enviar la solicitud debido a un error de detección del servicio.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |Este error indica que no se ha establecido la propiedad de dirección URL externa en la base de datos de Active Directory.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> |Este error indica que ha fallado un intento de sincronización de una carpeta para compartir. <br/><br/>Este código de error se devuelve cuando ocurre lo siguiente:<br/><br/>-No se encontró la suscripción de una carpeta para compartir.<br/>-No se encontró la carpeta de uso compartida.<br/>-No se encontró el usuario de Active directory correspondiente.<br/>-El usuario ya no existe.<br/>-La cita no es válida.<br/>-El elemento de contacto no es válido.<br/>-Hay un error de comunicación con el servidor remoto.  <br/> |
|ErrorStaleObject  <br/> |Este error se produce en una [operación de UpdateItem](updateitem-operation.md) o una [operación de SendItem](senditem-operation.md) cuando la clave de cambio no está actualizada o no se ha proporcionado. Llamar a la [operación GetItem](getitem-operation.md) para recuperar una clave de cambio actualizados y, a continuación, vuelva a intentarlo.  <br/> |
|ErrorSubmissionQuotaExceeded  <br/> |Este error indica que un usuario no puede enviar inmediatamente más solicitudes porque se ha alcanzado la cuota de envío.  <br/> |
|ErrorSubscriptionAccessDenied  <br/> |Este error se produce cuando se intenta obtener acceso a una suscripción con una cuenta que no se ha creado la suscripción. Sólo se puede tener acceso a cada suscripción por el creador de la suscripción.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Este error indica que no se puede crear una suscripción si no es el propietario o no tienen acceso de propietario para el buzón de correo.  <br/> |
|ErrorSubscriptionNotFound  <br/> |Este error se produce si no se encuentra la suscripción que se corresponde con el especificado [SubscriptionId (GetEvents)](subscriptionid-getevents.md) . Puede que haya caducado la suscripción, es posible que se haya reiniciado el proceso de servicios Web de Exchange o se ha pasado una suscripción no válida en. Si la suscripción era válida, volver a crear la suscripción con la última marca de agua. Esto es devuelto por la [operación de cancelación de suscripción](unsubscribe-operation.md) o las respuestas de [operación GetEvents](getevents-operation.md) .  <br/> |
|ErrorSubscriptionUnsubsribed  <br/> |Este código de error debe devolverse cuando se realiza una solicitud para una suscripción a que se canceló la suscripción.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Este error es devuelto por la [operación SyncFolderItems](syncfolderitems-operation.md) si no se encuentra la carpeta primaria que se especifica.  <br/> |
|ErrorTeamMailboxNotFound  <br/> |Este error indica que no se encontró un buzón de correo del equipo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxNotLinkedToSharePoint  <br/> |Este error indica que se encontró un buzón de equipo pero que no está vinculado a un servidor de SharePoint. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxUrlValidationFailed  <br/> |Este error indica que se encontró un buzón de equipo pero que el vínculo al servidor de SharePoint no es válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxNotAuthorizedOwner  <br/> |No se usa este código de error. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxActiveToPendingDelete  <br/> |No se usa este código de error. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxFailedSendingNotifications  <br/> |Este error indica que un intento de enviar una notificación a los propietarios de buzón de correo del equipo ha podido realizar. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxErrorUnknown  <br/> |Este error indica un error general que puede surgir al intentar tener acceso a un buzón de correo del equipo. Intente enviar la solicitud en un momento posterior. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTimeIntervalTooBig  <br/> |Este error indica que la ventana de tiempo que se ha especificado es mayor que el límite permitido. De forma predeterminada, el límite permitido es 42.  <br/> |
|ErrorTimeoutExpired  <br/> | Este error se produce cuando no hay suficiente tiempo para completar el procesamiento de la solicitud.  <br/> |
|ErrorTimeZone  <br/> |Este error indica que se ha producido un error de zona horaria.  <br/> |
|ErrorToFolderNotFound  <br/> |Este error indica que no existe la carpeta de destino.  <br/> |
|ErrorTokenSerializationDenied  <br/> |Este error se produce si el autor de la llamada intenta hacer una solicitud de serialización de símbolo (token) pero no tiene ms-Exch-EPI-TokenSerialization a la derecha en el servidor de acceso de cliente.  <br/> |
|ErrorTooManyObjectsOpened  <br/> |Este error se produce cuando se ha superado el límite interno en objetos abiertos.  <br/> |
|ErrorUnifiedMessagingDialPlanNotFound  <br/> |Este error indica que el plan de marcado de un usuario no está disponible.  <br/> |
|ErrorUnifiedMessagingReportDataNotFound  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnifiedMessagingPromptNotFound  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnifiedMessagingRequestFailed  <br/> |Este error indica que no se pudo encontrar el usuario.  <br/> |
|ErrorUnifiedMessagingServerNotFound  <br/> |Este error indica que se puede encontrar un servidor válido para el plan de marcado para controlar la solicitud.  <br/> |
|ErrorUnableToGetUserOofSettings  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorUnableToRemoveImContactFromGroup  <br/> |Este error se produce cuando se realiza un intento incorrecto para quitar un contacto de mensajería instantánea de un grupo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnsupportedCulture  <br/> |Este error se produce cuando se intenta establecer la propiedad de la **referencia cultural** en un valor que no es analizable por la clase **System.Globalization.CultureInfo** .  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |Este error se produce cuando un autor de la llamada intenta usar las propiedades extendidas de objetos de tipos, matriz de objetos, error o null.  <br/> |
|ErrorUnsupportedMimeConversion  <br/> |Este error se produce cuando se intenta recuperar o establecer el contenido MIME para un elemento que no sea un objeto [PostItem](postitem.md), [mensaje](message-ex15websvcsotherref.md)o [CalendarItem](calendaritem.md) .  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |Este error se produce cuando el autor de la llamada pasa una propiedad que no es válida para una consulta. Esto puede ocurrir cuando se usan las propiedades calculadas.  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |Este error se produce cuando el autor de la llamada pasa una propiedad que no es válida para un ordenar o agrupar por propiedad. Esto puede ocurrir cuando se usan las propiedades calculadas.  <br/> |
|ErrorUnsupportedPropertyDefinition  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorUnsupportedQueryFilter  <br/> |Este error indica que la restricción de la carpeta de búsqueda puede ser válida, pero no se admite por EWS.  <br/> |
|ErrorUnsupportedRecurrence  <br/> |Este error indica que no se admite la periodicidad especificada para las tareas.  <br/> |
|ErrorUnsupportedSubFilter  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |Este error indica que los servicios Web Exchange encontró un tipo de propiedad en el almacén pero no puede generar el XML para el tipo de propiedad.  <br/> |
|ErrorUpdateDelegatesFailed  <br/> |Este error indica que la lista de delegados no se pudieron guardar después de que se han actualizado los delegados.  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |Este error se produce cuando la ruta de acceso de propiedad único que aparece en una descripción de cambio no coincide con la única propiedad que se va a establecer en el objeto de [elemento](item.md) o [carpeta](folder.md) real.  <br/> |
|ErrorUserNotUnifiedMessagingEnabled  <br/> |Este error indica que el solicitante no está habilitado.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |Este error indica que el solicitante intentado conceder permisos en su calendario o carpeta de contactos para un usuario externo, pero la directiva de uso compartido asignado al solicitante indica que el dominio del usuario externo no figura en la directiva.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Indica que la organización del solicitante tiene un conjunto de dominios federados, pero la organización del solicitante no tiene ninguna dirección de proxy SMTP con uno de los dominios federados.  <br/> |
|ErrorValueOutOfRange  <br/> |Este error indica que la fecha de inicio de una vista de calendario o fecha de finalización se estableció en 1/1/0001 12:00:00 AM o 31/12/9999 11:59:59 PM.  <br/> |
|ErrorVirusDetected  <br/> |Este error indica que el almacén de Exchange detectó un virus en el mensaje.  <br/> |
|ErrorVirusMessageDeleted  <br/> |Este error indica que el almacén de Exchange detectó un virus en el mensaje y eliminó.  <br/> |
|ErrorVoiceMailNotImplemented  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorWebRequestInInvalidState  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorWin32InteropError  <br/> |Este error indica que se ha producido un error interno durante la comunicación con código no administrado.  <br/> |
|ErrorWorkingHoursSaveFailed  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorWorkingHoursXmlMalformed  <br/> |No se usa este código de respuesta.  <br/> |
|ErrorWrongServerVersion  <br/> |Este error indica que sólo se realiza una solicitud a un servidor que es la misma versión que el servidor de buzones.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Este error indica que se realizó una solicitud por parte de un delegado que tiene una versión de servidor diferente que el servidor de buzón de correo de la entidad de seguridad.  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |Nunca se devuelve este código de error.  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |Especifica que no hay encabezados SOAP duplicados.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> | Especifica que no se pudieron un intento de sincronización de una carpeta para compartir.<br/><br/> Este código de error debe devolverse cuando:<br/><br/>-No se encontró la suscripción de una carpeta para compartir.  <br/>-No se encontró la carpeta de uso compartida.  <br/>-No se encontró el usuario de Active directory correspondiente.  <br/>-El usuario ya no existe.  <br/>-La cita no es válida.  <br/>-El elemento de contacto no es válido.  <br/>-Se produjo un error de comunicación con el servidor remoto.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |Especifica que no se ha establecido la propiedad de dirección URL externa en la base de datos de Active Directory. Este código de error debe devolverse si no se ha establecido la propiedad de dirección URL externa en la base de datos de Active Directory.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |Especifica que se ha alcanzado el recuento de miembros de grupo máximo para obtener información de libre/ocupado de una lista de distribución. Este error se debe devolver cuando se ha alcanzado el recuento de miembros de grupo máximo para obtener información de libre/ocupado de una lista de distribución.  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |Especifica que el elemento de tipo de datos y ShareFolderId están presentes en una solicitud. Este código de error se debe devolver si el elemento de tipo de datos y ShareFolderId está presentes en una solicitud.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |Especifica que el llamador intentó realizar conceder permisos en su carpeta Calendario o los contactos a un usuario en otra organización y el intento de error. Este código de error se debe devolver cuando la directiva de uso compartido está deshabilitada para el autor de la llamada o cuando la directiva de uso compartido asignada al autor de la llamada no permite el uso compartido para el nivel solicitado o el tipo de carpeta solicitada.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |Especifica que el solicitante ha tratado de concesión de permisos de su calendario o carpeta de contactos para un usuario externo, pero la directiva de uso compartido asignado al solicitante especifica que el dominio del usuario externo no figura en la directiva.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |Especifica que el solicitante ha tratado de conceder los permisos de su carpeta Calendario o los contactos a un usuario externo, pero la directiva de uso compartido asignado al solicitante especifica que el nivel de permiso solicitado es superior es que la directiva de qué uso compartida permite.  <br/> |
|ErrorOrganizationNotFederated  <br/> |Especifica que la organización del solicitante no está federado para que el solicitante no puede crear mensajes de uso compartidos para enviar a un usuario externo o no puede aceptar el uso compartido de los mensajes recibidos de un usuario externo. Este código de error se debe devolver si la organización del solicitante no está asociado.  <br/> |
|ErrorMailboxFailover  <br/> |Especifica que debido a que el buzón está en un proceso de conmutación por error, error al intentar tener acceso a un buzón de correo.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |Especifica que el remitente de la invitación de uso compartido no ha creado los metadatos de la invitación para compartir. Este código de error se debe devolver si el remitente de la invitación de uso compartido no ha creado los metadatos de la invitación para compartir.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |Especifica que el servicio de seguimiento de mensajes no pueden realizar un seguimiento del mensaje.  <br/> |
|ErrorMessageTrackingTransientError  <br/> |Especifica que puede ser el servicio de seguimiento de mensaje es inactivo u ocupado. Este código de error especifica un error transitorio. Los clientes pueden Reintentar para conectarse al servidor cuando se recibe este error.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |Especifica que no se encuentra el dominio especificado.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Especifica que la organización del solicitante tiene un conjunto de dominios federados pero organización del solicitante no tiene ninguna dirección de proxy SMTP con uno de los dominios federados.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |Especifica que un autor de la llamada solicitó información de disponibilidad para un usuario de otra organización, pero no tiene la relación organizativa libre/ocupado habilitado.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |Especifica que los objetos de federación de la organización del solicitante no están configurados correctamente.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |Especifica que un mensaje para compartir no está pensado para el autor de la llamada.  <br/> |
|ErrorInvalidSharingData  <br/> |Especifica que los metadatos de uso compartido no están válido. Esto puede deberse a XML no válido.  <br/> |
|ErrorInvalidSharingMessage  <br/> |Especifica que el mensaje para compartir no es válido. Esto puede deberse a una propiedad que faltan.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |Especifica que no se admite el mensaje para compartir.  <br/> |
|ErrorApplyConversationActionFailed  <br/> |Este error se debe devolver si una acción no se puede aplicar a uno o más elementos en la conversación.  <br/> |
|ErrorInboxRulesValidationError  <br/> |Este error se debe devolver si no valida cualquier regla.  <br/> |
|ErrorOutlookRuleBlobExists  <br/> |Este error se debe devolver cuando se produce un intento de administración de reglas de bandeja de entrada después de otro cliente tiene acceso a las reglas de bandeja de entrada.  <br/> |
|ErrorRulesOverQuota  <br/> |Este error se debe devolver cuando se superó la cuota de reglas de un usuario.  <br/> |
|ErrorNewEventStreamConnectionOpened  <br/> |Este error se debe devolver a la primera conexión de suscripción si se abre una segunda conexión de suscripción.  <br/> |
|ErrorMissedNotificationEvents  <br/> |Este error se debe devolver cuando se pierden las notificaciones de eventos.  <br/> |
|ErrorDuplicateLegacyDistinguishedName  <br/> |Este error se devuelve cuando hay duplicados nombres distintivos heredados en servicios de dominio de Active Directory (AD DS). Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidClientAccessTokenRequest  <br/> |Este error indica que una solicitud para obtener un acceso de cliente de símbolo (token) no era válida. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorNoSpeechDetected  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUMServerUnavailable  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorRecipientNotFound  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorRecognizerNotInstalled  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSpeechGrammarError  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidManagementRoleHeader  <br/> |Este error se devuelve si el encabezado de [ManagementRole](managementrole.md) en el encabezado SOAP es incorrecto. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesDisabled  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesRequestTimedOut  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesRequestFailed  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesInvalidRequest  <br/> |Este error está pensado para uso interno únicamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorWeatherServiceDisabled  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorMailboxScopeNotAllowedWithoutQueryString  <br/> |Este error se devuelve cuando se realiza un intento de búsqueda con un ámbito sin usar un elemento de [cadena de consulta (cadena)](querystring-string.md) para un búsqueda de indización de contenido. Esto es aplicable a las operaciones de **SearchMailboxes** y **FindConversation** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorArchiveMailboxSearchFailed  <br/> |Este error se devuelve cuando una búsqueda de archivos de buzón de correo se finalice correctamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |Este error se devuelve cuando la dirección URL de un buzón de archivo no es reconocible. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorGetRemoteArchiveFolderFailed  <br/> |Este error se produce cuando el error en la operación para obtener la carpeta de buzón de correo de archivo remoto.  <br/> |
|ErrorFindRemoteArchiveFolderFailed  <br/> |Este error se produce cuando el error en la operación para buscar la carpeta de buzón de correo de archivo remoto.  <br/> |
|ErrorGetRemoteArchiveItemFailed  <br/> |Este error se produce cuando el error en la operación para obtener el elemento del buzón de correo de archivo remoto.  <br/> |
|ErrorExportRemoteArchiveItemsFailed  <br/> |Este error se produce cuando el error en la operación para exportar elementos de buzón de correo de archivo remoto.  <br/> |
|ErrorInvalidPhotoSize  <br/> |Este error se devuelve si se solicita un tamaño de fotografías no válida desde el servidor. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSearchQueryHasTooManyKeywords  <br/> |Este error se devuelve cuando se solicita un tamaño de foto inesperados en una solicitud de operación **GetUserPhoto** . Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSearchTooManyMailboxes  <br/> |Este error se devuelve cuando una solicitud de operación **SearchMailboxes** contiene demasiados buzones para buscar. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagNone  <br/> |Este error indica que se han encontrado sin etiquetas de retención para este usuario. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorDiscoverySearchesDisabled  <br/> |Este error se devuelve cuando las búsquedas de detección están deshabilitadas en un servidor o inquilino. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorCalendarSeekToConditionNotSupported  <br/> |Este error se produce cuando se intenta invocar la [operación FindItem](finditem-operation.md) con un [SeekToConditionPageItemView](seektoconditionpageitemview.md) para la búsqueda de elementos de calendario, que no es compatible.  <br/> |
|ErrorCalendarIsGroupMailboxForAccept  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorCalendarIsGroupMailboxForDecline  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorCalendarIsGroupMailboxForTentative  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt  <br/> |Este error está pensado para uso interno únicamente.  <br/> |
|ErrorOrganizationAccessBlocked  <br/> |El inquilino se marca para eliminación.  <br/> |
|ErrorInvalidLicense  <br/> |El usuario no tiene una licencia válida.  <br/> |
|ErrorMessagePerFolderCountReceiveQuotaExceeded  <br/> |Recibe el mensaje por carpeta se superó la cuota.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento no es necesario y no se incluye en todas las respuestas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


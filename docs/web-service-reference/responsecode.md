---
title: ResponseCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 4b84d670-74c9-4d6d-84e7-f0a9f76f0d93
description: El elemento ResponseCode proporciona información de estado sobre la solicitud.
ms.openlocfilehash: 9d662ee93870c2aabe045d801222deb881d0a28b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512390"
---
# <a name="responsecode"></a>ResponseCode

El **elemento ResponseCode** proporciona información de estado sobre la solicitud. 
  
- [ResponseMessage](responsemessage.md) 
- [ResponseCode](responsecode.md)
  
```XML
<ResponseCode/>
```

**ResponseCodeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|Elemento|Descripción|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Proporciona información descriptiva sobre el estado de la respuesta.<br/><br/>  Las siguientes son las posibles expresiones XPath de este elemento:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación DeleteItem.](deleteitem-operation.md)  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación SendItem.](senditem-operation.md)  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación DeleteFolder.](deletefolder-operation.md)  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación DeleteAttachment.](deleteattachment-operation.md)  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud [de operación Cancelar suscripción.](unsubscribe-operation.md)  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación CreateFolder.](createfolder-operation.md)  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación GetFolder.](getfolder-operation.md)  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación UpdateFolder.](updatefolder-operation.md)  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación MoveFolder.](movefolder-operation.md)  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación CopyFolder.](copyfolder-operation.md)  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateManagedFolder.](createmanagedfolder-operation.md)  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación FindFolder.](findfolder-operation.md)  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación CreateItem.](createitem-operation.md)  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación GetItem.](getitem-operation.md)  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación UpdateItem.](updateitem-operation.md)  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación MoveItem.](moveitem-operation.md)  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación CopyItem.](copyitem-operation.md)  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de operación [CreateAttachment.](createattachment-operation.md)  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de operación [GetAttachment.](getattachment-operation.md)  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación FindItem.](finditem-operation.md)  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación ResolveNames.](resolvenames-operation.md)  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola [solicitud de operación ExpandDL.](expanddl-operation.md)  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud [de operación Subscribe.](subscribe-operation.md)  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación GetEvents.](getevents-operation.md)  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de operación SendNotification.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación SyncFolderHierarchy.](syncfolderhierarchy-operation.md)  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación SyncFolderItems.](syncfolderitems-operation.md)  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación ConvertId.](convertid-operation.md)  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación AddDelegate.](adddelegate-operation.md)  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación GetDelegate.](getdelegate-operation.md)  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación RemoveDelegate.](removedelegate-operation.md)  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación UpdateDelegate.](updatedelegate-operation.md)  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación GetServerTimeZones.](getservertimezones-operation.md)  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación GetSharingFolder.](getsharingfolder-operation.md)  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Define una respuesta a una [solicitud de operación GetSharingFolder.](getsharingfolder-operation.md)  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación GetSharingMetadata.](getsharingmetadata-operation.md)  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Define una respuesta a una [solicitud de operación GetSharingMetadata.](getsharingmetadata-operation.md)  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación RefreshSharingFolder.](refreshsharingfolder-operation.md)  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Define una respuesta a una [solicitud de operación RefreshSharingFolder.](refreshsharingfolder-operation.md)  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Contiene el estado y los resultados de una respuesta de operación [FindConversation.](findconversation-operation.md)  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |Contiene el estado y los resultados de una [solicitud de operación ApplyConversationAction.](applyconversationaction-operation.md)  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación EmptyFolder.](emptyfolder-operation.md)  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Contiene un estado y el resultado de una [solicitud de operación UpdateInboxRules.](updateinboxrules-operation.md)  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contiene un estado y el resultado de una [solicitud de operación UploadItems.](uploaditems-operation.md)  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Contiene una respuesta a una [solicitud **** de operación GetInboxRules.](getinboxrules-operation.md)  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Contiene una respuesta a una [solicitud de operación GetServiceConfiguration.](getserviceconfiguration-operation.md)  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene opciones de configuración de servicio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto. En la tabla siguiente se describen los valores que se devuelven con este elemento.
  
|Valor|Descripción|
|:-----|:-----|
|NoError  <br/> |No se ha producido ningún error para la solicitud.  <br/> |
|ErrorAccessDenied  <br/> |Este error se produce cuando la cuenta de llamada no tiene los derechos para realizar la acción solicitada.  <br/> |
|ErrorAccessModeSpecified  <br/> |Este error es solo para uso interno. Este error no se devuelve.  <br/> |
|ErrorAccountDisabled  <br/> |Este error se produce cuando se ha deshabilitado la cuenta en cuestión.  <br/> |
|ErrorAddDelegatesFailed  <br/> |Este error se produce cuando no se puede guardar una lista con delegados agregados.  <br/> |
|ErrorAddressSpaceNotFound  <br/> |Este error se produce cuando el registro de espacio de direcciones, o el nombre de dominio del sistema de nombres de dominio (DNS), para la disponibilidad entre bosques no se pudo encontrar en la base de datos de Active Directory.  <br/> |
|ErrorADOperation  <br/> |Este error se produce cuando se produce un error en la operación debido a problemas de comunicación con servicios de dominio de Active Directory (AD DS).  <br/> |
|ErrorADSessionFilter  <br/> |Este error se devuelve cuando una solicitud de operación **ResolveNames** especifica un nombre que no es válido.  <br/> |
|ErrorADUnavailable  <br/> |Este error se produce cuando AD DS no está disponible. Vuelva a intentar la solicitud más adelante.  <br/> |
|ErrorAffectedTaskOccurrencesRequired  <br/> |Este error indica que no se especificó el atributo **AffectedTaskOccurrences.** Cuando se usa el elemento [DeleteItem](deleteitem.md) para eliminar al menos un elemento que es una tarea e independientemente de si esa tarea es periódica o no, el atributo **AffectedTaskOccurrences** debe especificarse para que **DeleteItem** pueda determinar si se va a eliminar la repetición actual o toda la serie.  <br/> |
|ErrorArchiveFolderPathCreation  <br/> |Indica un error en la creación de la ruta de acceso de carpeta de archivo.  <br/> |
|ErrorArchiveMailboxNotEnabled  <br/> |Indica que el buzón de archivo no estaba habilitado.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |Indica que se ha fallado la detección del servicio de buzón de correo de archivo.  <br/> |
|ErrorAttachmentNestLevelLimitExceeded  <br/> |Especifica que se intentó crear un elemento con más de 10 datos adjuntos anidados. Este valor se introdujo en Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|ErrorAttachmentSizeLimitExceeded  <br/> |El [elemento CreateAttachment](createattachment.md) devuelve este error si se intenta crear datos adjuntos con un tamaño superior a Int32.MaxValue, en bytes.  <br/> El [elemento GetAttachment](getattachment.md) devuelve este error si se intenta recuperar datos adjuntos existentes con un tamaño superior a Int32.MaxValue, en bytes.  <br/> |
|ErrorAutoDiscoverFailed  <br/> |Este error indica que Exchange Web Services intentó determinar la ubicación de un equipo entre bosques que ejecuta Exchange 2010 que tiene el rol de servidor acceso de cliente instalado mediante el servicio de detección automática, pero se produjo un error en la llamada al servicio de detección automática.  <br/> |
|ErrorAvailabilityConfigNotFound  <br/> |Este error indica que la información de configuración de disponibilidad para el bosque local falta en AD DS.  <br/> |
|ErrorBatchProcessingStopped  <br/> | Este error indica que se produjo una excepción al procesar un elemento y que es probable que se produzca esa excepción para los elementos siguientes. Las solicitudes pueden incluir varios elementos; por ejemplo, una solicitud de operación GetItem puede incluir varios identificadores. En general, los elementos se procesan uno a la vez. Si se produce una excepción al procesar un elemento y es probable que se produzca esa excepción para los elementos siguientes, los elementos siguientes no se procesarán.  <br/><br/>  A continuación se muestran ejemplos de errores que dejarán de procesarse para los elementos siguientes:<br/>  <br/>- ErrorAccessDenied  <br/>- ErrorAccountDisabled  <br/>- ErrorADUnavailable  <br/>- ErrorADOperation  <br/>- ErrorConnectionFailed  <br/>- ErrorMailboxStoreUnavailable  <br/>- ErrorMailboxMoveInProgress  <br/>- ErrorPasswordChangeRequired  <br/>- ErrorPasswordExpired  <br/>- ErrorQuotaExceeded  <br/>- ErrorInsufficientResources  <br/> |
|ErrorCalendarCannotMoveOrCopyOccurrence  <br/> |Este error se produce cuando se intenta mover o copiar una repetición de un elemento de calendario periódico.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> | Este error se produce cuando se intenta actualizar un elemento de calendario que se encuentra en la carpeta Elementos eliminados y cuando las actualizaciones o cancelaciones de reuniones se envían según el valor del atributo **SendMeetingInvitationsOrCancellations.** <br/><br/>Estos son los valores posibles para este atributo:  <br/><br/>- SendToAllAndSaveCopy  <br/>- SendToChangedAndSaveCopy  <br/>- SendOnlyToAll  <br/>- SendOnlyToChanged  <br/>  <br/>Sin embargo, esta actualización solo se permite cuando el valor de este atributo se establece en SendToNone.  <br/> |
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |Este error se produce cuando se llama a la operación UpdateItem, GetItem, DeleteItem, MoveItem, CopyItem o SendItem y el identificador especificado no es un identificador de repetición de ningún elemento de calendario periódico.  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |Este error se produce cuando se llama a la operación **UpdateItem**, **GetItem**, **DeleteItem**, **MoveItem**, **CopyItem** o **SendItem** y el identificador especificado no es un identificador de ningún elemento maestro periódico.  <br/> |
|ErrorCalendarDurationIsTooLong  <br/> |Este error se produce durante una **operación CreateItem** o **UpdateItem** cuando la duración de un elemento de calendario es mayor que el máximo permitido, que actualmente es de 5 años.  <br/> |
|ErrorCalendarEndDateIsEarlierThanStartDate  <br/> |Este error se produce cuando una hora de finalización del calendario se establece en la misma hora o después de la hora de inicio.  <br/> |
|ErrorCalendarFolderIsInvalidForCalendarView  <br/> |Este error se produce cuando la carpeta especificada para una operación **FindItem** con [un elemento CalendarView](calendarview.md) no es del tipo de carpeta de calendario.  <br/> |
|ErrorCalendarInvalidAttributeValue  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorCalendarInvalidDayForTimeChangePattern  <br/> |Este error se produce durante una **operación CreateItem** o **UpdateItem** cuando se usan valores no válidos de Day, WeekendDay y Weekday para definir el patrón de cambio de hora.  <br/> |
|ErrorCalendarInvalidDayForWeeklyRecurrence  <br/> |Este error se produce durante una **operación CreateItem** o **UpdateItem** cuando se usan valores no válidos de Day, WeekDay y WeekendDay para especificar la periodicidad semanal.  <br/> |
|ErrorCalendarInvalidPropertyState  <br/> |Este error se produce cuando el estado de un objeto binario grande (BLOB) de periodicidad de un elemento de calendario en el Exchange no es válido.  <br/> |
|ErrorCalendarInvalidPropertyValue  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorCalendarInvalidRecurrence  <br/> |Este error se produce cuando no se puede crear la periodicidad especificada.  <br/> |
|ErrorCalendarInvalidTimeZone  <br/> |Este error se produce cuando se encuentra una zona horaria no válida.  <br/> |
|ErrorCalendarIsCancelledForAccept  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForDecline  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForRemove  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsCancelledForTentative  <br/> |Este error indica que se ha cancelado un elemento de calendario.  <br/> |
|ErrorCalendarIsDelegatedForAccept  <br/> |Este error indica que el [elemento AcceptItem](acceptitem.md) no es válido para un elemento de calendario o una solicitud de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsDelegatedForDecline  <br/> |Este error indica que el [elemento DeclineItem](declineitem.md) no es válido para un elemento de calendario o una solicitud de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsDelegatedForRemove  <br/> |Este error indica que el [elemento RemoveItem](removeitem.md) no es válido para una cancelación de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsDelegatedForTentative  <br/> |Este error indica que el [elemento TentativelyAcceptItem](tentativelyacceptitem.md) no es válido para un elemento de calendario o una solicitud de reunión en un escenario delegado.  <br/> |
|ErrorCalendarIsNotOrganizer  <br/> |Este error indica que la operación (actualmente CancelItem) en el elemento de calendario no es válida para un asistente. Solo el organizador de la reunión puede cancelar la reunión.  <br/> |
|ErrorCalendarIsOrganizerForAccept  <br/> |Este error indica que [AcceptItem](acceptitem.md) no es válido para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarIsOrganizerForDecline  <br/> |Este error indica que [DeclineItem](declineitem.md) no es válido para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarIsOrganizerForRemove  <br/> |Este error indica que [RemoveItem](removeitem.md) no es válido para el elemento de calendario del organizador. Para quitar una reunión del calendario, el organizador debe usar CancelCalendarItem.  <br/> |
|ErrorCalendarIsOrganizerForTentative  <br/> |Este error indica que [TentativelyAcceptItem](tentativelyacceptitem.md) no es válido para el elemento de calendario del organizador.  <br/> |
|ErrorCalendarMeetingRequestIsOutOfDate  <br/> |Este error indica que una solicitud de reunión está desactual y no se puede actualizar.  <br/> |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange  <br/> |Este error indica que el índice de ocurrencia no apunta a una repetición dentro de la periodicidad actual. Por ejemplo, si el patrón de periodicidad define un conjunto de tres repeticiones de reunión e intenta obtener acceso a la quinta repetición, se mostrará este código de respuesta.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Este error indica que cualquier operación en una repetición eliminada (dirigida a través del identificador de patrón periódico y el índice de repetición) no es válida.  <br/> |
|ErrorCalendarOutOfRange  <br/> |Este error se notifica en las operaciones CreateItem y UpdateItem para elementos de calendario o propiedades de periodicidad de tareas cuando el valor de la propiedad está fuera del intervalo. Por ejemplo, especificar la decimoquinta semana del mes dará como resultado este código de respuesta.  <br/> |
|ErrorCalendarViewRangeTooBig  <br/> |Este error se produce cuando el intervalo De inicio a fin del elemento [CalendarView](calendarview.md) es superior al máximo permitido, actualmente 2 años.  <br/> |
|ErrorCallerIsInvalidADAccount  <br/> |Este error indica que la cuenta solicitante no es una cuenta válida en la base de datos de directorios.  <br/> |
|ErrorCannotArchiveCalendarContactTaskFolderException  <br/> |Indica que se intentó archivar una carpeta de tareas de contacto de calendario.  <br/> |
|ErrorCannotArchiveItemsInPublicFolders  <br/> |Indica que se intentó archivar elementos en carpetas públicas.  <br/> |
|ErrorCannotArchiveItemsInArchiveMailbox  <br/> |Indica que se intentó archivar elementos en el buzón de archivo.  <br/> |
|ErrorCannotCreateCalendarItemInNonCalendarFolder  <br/> |Este error se produce cuando se crea un elemento de calendario y el atributo **SavedItemFolderId** hace referencia a una carpeta que no es de calendario.  <br/> |
|ErrorCannotCreateContactInNonContactFolder  <br/> |Este error se produce cuando se crea un contacto y el atributo **SavedItemFolderId** hace referencia a una carpeta que no es de contacto.  <br/> |
|ErrorCannotCreatePostItemInNonMailFolder  <br/> |Este error indica que no se puede crear un elemento de publicación en una carpeta que no sea una carpeta de correo, como Calendario, Contacto, Tareas, Notas, entre otras.  <br/> |
|ErrorCannotCreateTaskInNonTaskFolder  <br/> |Este error se produce cuando se crea una tarea y el atributo **SavedItemFolderId** hace referencia a una carpeta que no es de tarea.  <br/> |
|ErrorCannotDeleteObject  <br/> |Este error se produce cuando no se puede eliminar el elemento o la carpeta que se va a eliminar.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |La [operación DeleteItem](deleteitem-operation.md) devuelve este error cuando no se puede eliminar la repetición actual de una tarea periódica. Esto solo puede ocurrir si el atributo **AffectedTaskOccurrences** se ha establecido en SpecifiedOccurrenceOnly.  <br/> |
|ErrorCannotDisableMandatoryExtension  <br/> |Indica que se intentó deshabilitar una extensión obligatoria.  <br/> |
|ErrorCannotEmptyFolder  <br/> |Este error debe devolverse cuando el servidor no puede vaciar una carpeta.  <br/> |
|ErrorCannotGetSourceFolderPath  <br/> |Indica que no se pudo recuperar la ruta de acceso de la carpeta de origen.  <br/> |
|ErrorCannotGetExternalEcpUrl  <br/> |Especifica que el servidor no pudo recuperar la dirección URL externa de Outlook Web App opciones.  <br/> |
|ErrorCannotOpenFileAttachment  <br/> |La **operación GetAttachment** devuelve este error si no puede recuperar el cuerpo de los datos adjuntos de un archivo.  <br/> |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder  <br/> |Este error indica que el autor de la llamada intentó establecer permisos de calendario en una carpeta que no es de calendario.  <br/> |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder  <br/> |Este error indica que el autor de la llamada intentó establecer permisos que no son de calendario en una carpeta de calendario.  <br/> |
|ErrorCannotSetPermissionUnknownEntries  <br/> |Este error indica que no se pueden establecer permisos desconocidos en un conjunto de permisos.  <br/> |
|ErrorCannotSpecifySearchFolderAsSourceFolder  <br/> |Indica que se intentó especificar la carpeta de búsqueda como carpeta de origen.  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |Este error se produce cuando se le da un identificador de carpeta a una solicitud que requiere un identificador de elemento.  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |Este error se produce cuando se le da un identificador de elemento a una solicitud que requiere un identificador de carpeta.  <br/> |
|ErrorChangeKeyRequired  <br/> |Este código de respuesta se ha reemplazado **por ErrorChangeKeyRequiredForWriteOperations** <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |Este error se devuelve cuando falta o está obsoleta la clave de cambio de un elemento. <br/><br/>Para las operaciones SendItem, UpdateItem y UpdateFolder, el autor de la llamada debe pasar una clave de cambio correcta y actual para el elemento. Tenga en cuenta que este es el caso de UpdateItem incluso cuando la resolución de conflictos está establecida en sobrescribir siempre.  <br/> |
|ErrorClientDisconnected  <br/> |Especifica que el cliente se desconectó.  <br/> |
|ErrorClientIntentInvalidStateDefinition  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorClientIntentNotFound  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorConnectionFailed  <br/> |Este error se produce cuando Exchange Web Services no se puede conectar al buzón.  <br/> |
|ErrorContainsFilterWrongType  <br/> |Este error indica que la propiedad que se ha inspeccionado para un filtro Contains no es un tipo de cadena.  <br/> |
|ErrorContentConversionFailed  <br/> |La **operación GetItem** devuelve este error cuando Exchange Web Services no puede recuperar el contenido MIME del elemento solicitado. <br/><br/>La **operación CreateItem** devuelve este error cuando Exchange Web Services no puede crear el elemento a partir del contenido MIME proporcionado. Por lo general, esto indica que la propiedad item está dañada o truncada.  <br/> |
|ErrorContentIndexingNotEnabled  <br/> |Este error se produce cuando se realiza una solicitud de búsqueda mediante la opción QueryString y la indización de contenido no está habilitada para el buzón de destino.  <br/> |
|ErrorCorruptData  <br/> |Este error se produce cuando los datos están dañados y no se pueden procesar.  <br/> |
|ErrorCreateItemAccessDenied  <br/> |Este error se produce cuando el autor de la llamada no tiene permiso para crear el elemento.  <br/> |
|ErrorCreateManagedFolderPartialCompletion  <br/> |Este error se produce cuando no se pudo crear una o varias de las carpetas administradas especificadas en la solicitud de operación CreateManagedFolder. Busque cada carpeta para determinar qué carpetas se crearon y qué carpetas no existen.  <br/> |
|ErrorCreateSubfolderAccessDenied  <br/> |Este error se produce cuando la cuenta de llamada no tiene los permisos necesarios para crear la subcarpeta.  <br/> |
|ErrorCrossMailboxMoveCopy  <br/> |Este error se produce cuando se intenta mover un elemento o carpeta de un buzón a otro. Si el buzón de origen y el buzón de destino son diferentes, recibirá este error.  <br/> |
|ErrorCrossSiteRequest  <br/> |Este error indica que la solicitud no está permitida porque el servidor de acceso de cliente que debe proporcionar servicio a la solicitud se encuentra en un sitio diferente.  <br/> |
|ErrorDataSizeLimitExceeded  <br/> |Este error puede producirse en los siguientes escenarios:<br/>  <br/>- Se intenta obtener acceso o escribir una propiedad en un elemento y el valor de la propiedad es demasiado grande.<br/>- La longitud de contenido MIME codificado en base64 dentro del XML de solicitud supera el límite.<br/>- El tamaño del cuerpo de un cuerpo de elemento existente supera el límite.<br/>- El consumidor intenta establecer un html o cuerpo de texto cuya longitud (o longitud combinada en el caso de append) supere el límite. |
|ErrorDataSourceOperation  <br/> |Este error se produce cuando el proveedor de datos subyacente no puede completar la operación.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Este error se produce en una **operación AddDelegate** cuando el usuario especificado ya existe en la lista de delegados.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Este error se produce en una **operación AddDelegate** cuando el usuario especificado que se va a agregar es el propietario del buzón.  <br/> |
|ErrorDelegateMissingConfiguration  <br/> |Este error se produce en una operación **GetDelegate** cuando no hay información de delegado en el mensaje de FreeBusy local o no hay delegado público de Active Directory (sin entrada "delegado público" o "Enviar en nombre" en AD DS).  <br/> |
|ErrorDelegateNoUser  <br/> |Este error se produce cuando un usuario especificado no se puede asignar a un usuario en AD DS.  <br/> |
|ErrorDelegateValidationFailed  <br/> |Este error se produce en la **operación AddDelegate** cuando un usuario delegado agregado no es válido.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Este error se produce cuando se intenta eliminar una carpeta distinguida.  <br/> |
|ErrorDeleteItemsFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorDeleteUnifiedMessagingPromptFailed  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorDistinguishedUserNotSupported  <br/> |Este error indica que un identificador de usuario distintivo no es válido para la operación. **DistinguishedUserType** no debe estar presente en la solicitud.  <br/> |
|ErrorDistributionListMemberNotExist  <br/> |Este error indica que un miembro de la lista de distribución de solicitudes no existe en la lista de distribución.  <br/> |
|ErrorDuplicateInputFolderNames  <br/> |Este error se produce cuando se especifican nombres de carpeta duplicados dentro del [elemento FolderNames](foldernames.md) de la solicitud de operación **CreateManagedFolder.**  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |Este error indica que hay encabezados SOAP duplicados.  <br/> |
|ErrorDuplicateUserIdsSpecified  <br/> |Este error indica que se ha encontrado un identificador de usuario duplicado en un conjunto de permisos, ya sea predeterminado o anónimo se establecen más de una vez, o hay SID duplicados o destinatarios.  <br/> |
|ErrorEmailAddressMismatch  <br/> |Este error se produce cuando una solicitud intenta crear o actualizar los parámetros de búsqueda de una carpeta de búsqueda. Por ejemplo, esto puede ocurrir cuando se crea una carpeta de búsqueda en el buzón, pero la carpeta de búsqueda se dirige a buscar en otro buzón.  <br/> |
|ErrorEventNotFound  <br/> |Este error se produce cuando el evento asociado a una marca de agua se elimina antes de que se devuelva el evento. Cuando se devuelve este error, también se elimina la suscripción.  <br/> |
|ErrorExceededConnectionCount  <br/> |Este error -iIndica que hay más solicitudes simultáneas en el servidor de las permitidas por la directiva de un usuario.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |Este error indica que se ha superado el número máximo de suscripciones de la directiva de limitación de un usuario.  <br/> |
|ErrorExceededFindCountLimit  <br/> |Este error indica que una llamada a una operación de búsqueda ha excedido el número total de elementos que se pueden devolver.  <br/> |
|ErrorExpiredSubscription  <br/> |Este error se produce si se llama a la operación [GetEvents](getevents-operation.md) cuando se elimina una suscripción porque ha expirado.  <br/> |
|ErrorExtensionNotFound  <br/> |Indica que no se encontró la extensión.  <br/> |
|ErrorFolderCorrupt  <br/> |Este error se produce cuando la carpeta está dañada y no se puede guardar.  <br/> |
|ErrorFolderExists  <br/> |Este error se produce cuando se intenta crear una carpeta que tenga el mismo nombre que otra carpeta del mismo elemento primario. No se permiten nombres de carpeta duplicados.  <br/> |
|ErrorFolderNotFound  <br/> |Este error indica que el identificador de carpeta especificado no corresponde a una carpeta válida o que el delegado no tiene permiso para tener acceso a la carpeta.  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |Este error indica que no se pudo recuperar la propiedad solicitada. Esto no indica que la propiedad no existe, pero que la propiedad se ha dañado de alguna manera para que la recuperación falle.  <br/> |
|ErrorFolderSave  <br/> |Este error indica que no se pudo crear o actualizar la carpeta debido a un estado no válido.  <br/> |
|ErrorFolderSaveFailed  <br/> |Este error indica que no se pudo crear o actualizar la carpeta debido a un estado no válido.  <br/> |
|ErrorFolderSavePropertyError  <br/> |Este error indica que no se pudo crear o actualizar la carpeta debido a valores de propiedad no válidos. El código de respuesta enumera las propiedades que provocaron el problema.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |Este error indica que se ha alcanzado el número máximo de miembros del grupo para obtener información de disponibilidad para una lista de distribución.  <br/> |
|ErrorFreeBusyGenerationFailed  <br/> |Este error se devuelve cuando no se puede recuperar la información de disponibilidad debido a un error que interviene.  <br/> |
|ErrorGetServerSecurityDescriptorFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorImContactLimitReached  <br/> |Este error se devuelve cuando no se pueden agregar nuevos contactos de mensajería instantánea (MI) porque se ha alcanzado el número máximo de contactos. Este error se introdujo en Exchange Server 2013.  <br/> |
|ErrorImGroupDisplayNameAlreadyExists  <br/> |Este error se devuelve cuando se intenta agregar un nombre para mostrar de grupo cuando un grupo existente ya tiene el mismo nombre para mostrar. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorImGroupLimitReached  <br/> |Este error se devuelve cuando no se pueden agregar nuevos grupos de mensajería instantánea porque se ha alcanzado el número máximo de grupos. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorImpersonateUserDenied  <br/> |El error se devuelve en el caso de autorización de servidor a servidor para la suplantación de Exchange cuando el autor de la llamada no tiene los derechos adecuados para suplantar al usuario específico en cuestión. Este error se asigna a ms-Exch-EPI-May-Suplantar la derecha extendida de Active Directory.  <br/> |
|ErrorImpersonationDenied  <br/> |Este error se devuelve en la autorización de servidor a servidor para la suplantación de Exchange cuando el autor de la llamada no tiene los derechos adecuados para suplantar a través del servidor de acceso de cliente en el que realiza la solicitud. Esto se asigna a la derecha extendida de Active Directory ms-Exch-EPI-Impersonation.  <br/> |
|ErrorImpersonationFailed  <br/> |Este error indica que hubo un error inesperado cuando se intentó realizar la autenticación de servidor a servidor. Este código de respuesta normalmente indica que la cuenta de servicio que ejecuta el grupo de aplicaciones de servicios web de Exchange está configurada incorrectamente, que Exchange Web Services no puede hablar con el directorio o que una confianza entre bosques no está configurada correctamente.  <br/> |
|ErrorIncorrectSchemaVersion  <br/> |Este error indica que la solicitud era válida para la versión Exchange Server actual, pero no era válida para la versión del servidor de solicitudes especificada.  <br/> |
|ErrorIncorrectUpdatePropertyCount  <br/> |Este error indica que cada descripción de cambio en los [elementos UpdateItem](updateitem.md) o [UpdateFolder](updatefolder.md) debe enumerar solo una propiedad para actualizar.  <br/> |
|ErrorIndividualMailboxLimitReached  <br/> |Este error se produce cuando la solicitud contiene demasiados asistentes para resolver. De forma predeterminada, el número máximo de asistentes para resolver es 100.  <br/> |
|ErrorInsufficientResources  <br/> |Este error se produce cuando el servidor de buzones de correo está sobrecargado. Vuelva a intentar la solicitud más adelante.  <br/> |
|ErrorInternalServerError  <br/> |Este error indica que Exchange Web Services encontró un error del que no pudo recuperarse y no existe un código de respuesta más específico asociado al error que se produjo.  <br/> |
|ErrorInternalServerTransientError  <br/> |Este error indica que se ha producido un error de servidor interno y que debe volver a intentar la solicitud más adelante.  <br/> |
|ErrorInvalidAccessLevel  <br/> |Este error indica que el nivel de acceso que el autor de la llamada tiene en los datos de disponibilidad no es válido.  <br/> |
|ErrorInvalidArgument  <br/> |Este error indica un error causado por todos los argumentos no válidos pasados a la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).<br/><br/> Este error se devuelve en los siguientes escenarios: <br/><br/>- El usuario especificado en el  _parámetro sending-as_ no existe en el directorio. <br/>- El usuario especificado en el  _parámetro sending-as_ no es único en el directorio. <br/>- La  _dirección de envío está_ vacía.<br/>- La  _dirección de envío como_ no es una dirección de correo electrónico válida.  <br/> |
|ErrorInvalidAttachmentId  <br/> |La operación [GetAttachment](getattachment-operation.md) o la operación [DeleteAttachment](deleteattachment-operation.md) devuelven este error cuando no se encuentra ningún dato adjunto que corresponda al identificador especificado.  <br/> |
|ErrorInvalidAttachmentSubfilter  <br/> |Este error se produce cuando se intenta enlazar a una carpeta de búsqueda existente mediante una restricción de tabla de datos adjuntos compleja. Exchange Los servicios web solo admiten simples contiene filtros en la tabla de datos adjuntos. Si intenta enlazar a una carpeta de búsqueda existente que tiene una restricción de tabla de datos adjuntos más compleja (un subfiltro), Exchange Web Services no puede representar el XML de ese filtro y devuelve este código de respuesta. <br/><br/>Tenga en cuenta que todavía puede llamar a la operación GetFolder en la carpeta, pero no solicite el [elemento SearchParameters.](searchparameters.md)  <br/> |
|ErrorInvalidAttachmentSubfilterTextFilter  <br/> |Este error se produce cuando se intenta enlazar a una carpeta de búsqueda existente mediante una restricción de tabla de datos adjuntos compleja. Exchange Los servicios web solo admiten simples contiene filtros en la tabla de datos adjuntos. <br/><br/>Si intenta enlazar a una carpeta de búsqueda existente que tiene una restricción de tabla de datos adjuntos más compleja, Exchange Web Services no puede representar el XML para ese filtro. En este caso, el subfiltro de datos adjuntos contiene un filtro de texto, pero no está mirando el nombre para mostrar de los datos adjuntos.<br/><br/> Tenga en cuenta que todavía puede llamar a la operación GetFolder en la carpeta, pero no solicite el [elemento SearchParameters.](searchparameters.md)  <br/> |
|ErrorInvalidAuthorizationContext  <br/> | Este error indica que se produjo un error en el procedimiento de autorización del solicitante.  <br/> |
|ErrorInvalidChangeKey  <br/> |Este error se produce cuando un consumidor pasa una carpeta o un identificador de elemento con una clave de cambio que no se puede analizar. Por ejemplo, podría ser contenido base64 no válido o una cadena vacía.  <br/> |
|ErrorInvalidClientSecurityContext  <br/> |Este error indica que hubo un error interno cuando se intentó resolver la identidad del autor de la llamada.  <br/> |
|ErrorInvalidCompleteDate  <br/> |Este error se devuelve cuando se intenta establecer el valor del elemento [CompleteDate](completedate.md) de una tarea en una hora en el futuro. Cuando se convierte a la hora local del servidor de acceso de cliente, [el CompleteDate](completedate.md) de una tarea no se puede establecer en un valor posterior a la hora local en el servidor de acceso de cliente.  <br/> |
|ErrorInvalidContactEmailAddress  <br/> |Este error indica que se proporcionó una dirección de correo electrónico no válida para un contacto.  <br/> |
|ErrorInvalidContactEmailIndex  <br/> |Este error indica que se proporcionó un valor de índice de correo electrónico no válido para una entrada de correo electrónico.  <br/> |
|ErrorInvalidCrossForestCredentials  <br/> |Este error se produce cuando las credenciales que se usan para proxy de una solicitud en un bosque de servicio de directorio diferente fallan en la autenticación.  <br/> |
|ErrorInvalidDelegatePermission  <br/> |Este error indica que los permisos de carpeta especificados no son válidos.  <br/> |
|ErrorInvalidDelegateUserId  <br/> |Este error indica que el identificador de usuario delegado especificado no es válido.  <br/> |
|ErrorInvalidExchangeImpersonationHeaderData  <br/> |Este error se produce durante Exchange suplantación cuando un autor de la llamada no especifica un UPN, una dirección de correo electrónico o un SID de usuario. Esto también se producirá si el autor de la llamada especifica una o varias de ellas y los valores están vacíos.  <br/> |
|ErrorInvalidExcludesRestriction  <br/> |Este error se produce cuando la máscara de bits que se pasó a una restricción del elemento [Excludes](excludes.md) no se puede analizar.  <br/> |
|ErrorInvalidExpressionTypeForSubFilter  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidExtendedProperty  <br/> | Este error se produce cuando se producen los siguientes eventos: <br/> <br/>- El autor de la llamada intenta usar una propiedad extendida que no es compatible con Exchange Web Services.  <br/>- El autor de la llamada pasa una combinación no válida de valores de atributo para una propiedad extendida. Esto también se produce si no se pasan atributos. Solo se permiten determinadas combinaciones.  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |Este error se produce cuando la sección de valor de una propiedad extendida no coincide con el tipo de la propiedad. <br/><br/>Por ejemplo, al establecer una propiedad extendida que tenga PropertyType="String" en una matriz de enteros, se producirá este error. Cualquier representación de cadena que no sea coerciible en el tipo especificado para la propiedad extendida dará este error.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |Este error indica que el remitente de la invitación para compartir no ha creado los metadatos de invitación para compartir.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |Este error indica que un mensaje de uso compartido no está pensado para el autor de la llamada.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |Este error indica que los objetos de federación de organización del solicitante no están configurados correctamente.  <br/> |
|ErrorInvalidFolderId  <br/> |Este error se produce cuando el identificador de carpeta está dañado.  <br/> |
|ErrorInvalidFolderTypeForOperation  <br/> |Este error indica que el tipo de carpeta especificado no es válido para la operación actual. Por ejemplo, no puede crear una carpeta de búsqueda en una carpeta pública.  <br/> |
|ErrorInvalidFractionalPagingParameters  <br/> | Este error se produce en la paginación fraccional cuando el usuario ha especificado una de las siguientes opciones: <br/> <br/>- Un numerador mayor que el denominador  <br/>- Un numerador que es menor que cero  <br/>- Un denominador que es menor o igual que cero  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |Este error indica que los [elementos DataType](datatype.md) y ShareFolderId están presentes en una solicitud.  <br/> |
|ErrorInvalidFreeBusyViewType  <br/> |Este error se produce cuando se llama a la operación [GetUserAvailability](getuseravailability-operation.md) con [un FreeBusyViewType](freebusyviewtype.md) de None.  <br/> |
|ErrorInvalidId  <br/> |Este error indica que el identificador o la clave de cambio están malformados.  <br/> |
|ErrorInvalidIdEmpty  <br/> |Este error se produce cuando el autor de la llamada especifica un **atributo Id** que está vacío.  <br/> |
|ErrorInvalidLikeRequest  <br/> |Este error se produce cuando no se puede gustar al elemento. Las versiones Exchange a partir del número de compilación 15.00.0913.09 incluyen este valor.  <br/> |
|ErrorInvalidIdMalformed  <br/> |Este error se produce cuando el autor de la llamada especifica un **atributo Id** que está malformado.  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |Este error indica que se especificó un identificador de carpeta o elemento que usa el formato Exchange 2007 para una solicitud con una versión de Exchange 2007 SP1 o posterior. No puede usar Exchange 2007 IDs en Exchange 2007 SP1 o solicitudes posteriores. Debe usar la operación [ConvertId para](convertid-operation.md) convertirlos primero.  <br/> |
|ErrorInvalidIdMonikerTooLong  <br/> |Este error se produce cuando el autor de la llamada especifica un **atributo Id** que es demasiado largo.  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |Este error se devuelve siempre que se pasa un identificador que no es un identificador de datos adjuntos de elemento a un método de servicio web que espera un identificador de datos adjuntos.  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |Este error se produce cuando un contacto del buzón está dañado.  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |Este error se produce cuando el autor de la llamada especifica un **atributo Id** que es demasiado largo.  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |Este error se devuelve cuando la jerarquía de datos adjuntos de un elemento supera el máximo de 255 niveles de profundidad.  <br/> |
|ErrorInvalidIdXml  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidImContactId  <br/> |Este error se devuelve cuando el identificador de contacto de MI especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidImDistributionGroupSmtpAddress  <br/> |Este error se devuelve cuando el identificador de dirección SMTP del grupo de distribución de mensajería instantánea especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidImGroupId  <br/> |Este error se devuelve cuando el identificador de grupo de mensajería instantánea especificado no representa un identificador válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidIndexedPagingParameters  <br/> |Este error se produce si el desplazamiento de la paginación indizada es negativo.  <br/> |
|ErrorInvalidInternetHeaderChildNodes  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidItemForOperationArchiveItem  <br/> |Indica que el elemento no era válido para una **operación ArchiveItem.**  <br/> |
|ErrorInvalidItemForOperationAcceptItem  <br/> |Este error se produce cuando se intenta usar un objeto de respuesta AcceptItem para un tipo de elemento que no sea una solicitud de reunión o un elemento de calendario, o cuando se intenta aceptar una repetición de elemento de calendario que se encuentra en la carpeta Elementos eliminados.  <br/> |
|ErrorInvalidItemForOperationCancelItem  <br/> |Este error se produce cuando se intenta usar un objeto de respuesta CancelItem en un tipo de elemento distinto de un elemento de calendario.  <br/> |
|ErrorInvalidItemForOperationCreateItemAttachment  <br/> | Este error se devuelve cuando se intenta crear datos adjuntos de elementos de un tipo no compatible.  <br/><br/>  Entre los tipos de elementos admitidos para los datos adjuntos de elementos se incluyen los siguientes objetos:  <br/><br/>- [Elemento](item.md) <br/>- [Mensaje](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Tarea](task.md) <br/>- [Contacto](contact.md) <br/> <br/> Por ejemplo, si intenta crear datos adjuntos [de MeetingMessage,](meetingmessage.md) encontrará este código de respuesta.  <br/> |
|ErrorInvalidItemForOperationCreateItem  <br/> | Este error se devuelve de una [operación CreateItem](createitem-operation.md) si la solicitud contiene un tipo de elemento no admitido. <br/><br/>Los elementos admitidos incluyen los siguientes objetos:<br/>  <br/>- [Elemento](item.md) <br/>- [Mensaje](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Tarea](task.md) <br/>- [Contacto](contact.md) <br/><br/>  Ciertos tipos se crean como un efecto secundario de hacer otra cosa. Los mensajes de reunión, por ejemplo, se crean al enviar un elemento de calendario a los asistentes; no se crean explícitamente.  <br/> |
|ErrorInvalidItemForOperationDeclineItem  <br/> |Este error se produce cuando se intenta usar un objeto de respuesta DeclineItem para un tipo de elemento que no sea una solicitud de reunión o un elemento de calendario, o cuando se intenta rechazar una aparición de elemento de calendario que se encuentra en la carpeta Elementos eliminados.  <br/> |
|ErrorInvalidItemForOperationExpandDL  <br/> |Este error indica que la operación [ExpandDL](expanddl-operation.md) solo es válida para listas de distribución privadas.  <br/> |
|ErrorInvalidItemForOperationRemoveItem  <br/> |Este error se devuelve de un objeto de respuesta RemoveItem si la solicitud especifica un elemento que no es un elemento de cancelación de reunión.  <br/> |
|ErrorInvalidItemForOperationSendItem  <br/> |Este error se devuelve de una [operación SendItem](senditem-operation.md) si la solicitud especifica un elemento que no es un elemento de mensaje.  <br/> |
|ErrorInvalidItemForOperationTentative  <br/> |Este error se produce cuando se intenta usar [TentativelyAcceptItem](tentativelyacceptitem.md) para un tipo de elemento que no sea una solicitud de reunión o un elemento de calendario, o cuando se intenta aceptar provisionalmente una aparición de elementos de calendario que se encuentra en la carpeta Elementos eliminados.  <br/> |
|ErrorInvalidLogonType  <br/> |Este error es solo para uso interno. Este error no se devuelve.  <br/> |
|ErrorInvalidMailbox  <br/> |Este error indica que la operación [CreateItem](createitem-operation.md) o [la operación UpdateItem](updateitem-operation.md) fallaron al crear o actualizar una lista de distribución personal.  <br/> |
|ErrorInvalidManagedFolderProperty  <br/> |Este error se produce cuando la estructura de la carpeta administrada está dañada y no se puede representar.  <br/> |
|ErrorInvalidManagedFolderQuota  <br/> |Este error se produce cuando la cuota que se establece en la carpeta administrada es menor que cero, lo que indica una carpeta administrada dañada.  <br/> |
|ErrorInvalidManagedFolderSize  <br/> |Este error se produce cuando el tamaño establecido en la carpeta administrada es menor que cero, lo que indica una carpeta administrada dañada.  <br/> |
|ErrorInvalidMergedFreeBusyInterval  <br/> |Este error se produce cuando el valor interno de disponibilidad combinado proporcionado no es válido. El valor mínimo predeterminado es 5 minutos. El valor máximo predeterminado es 1440 minutos.  <br/> |
|ErrorInvalidNameForNameResolution  <br/> |Este error se produce cuando el nombre no es válido para la [operación ResolveNames](resolvenames-operation.md). Por ejemplo, una cadena de longitud cero, un solo espacio, una coma y un guión son nombres no válidos.  <br/> |
|ErrorInvalidNetworkServiceContext  <br/> |Este error indica un error en la cuenta de servicio de red en el servidor de acceso de cliente.  <br/> |
|ErrorInvalidOofParameter  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidOperation  <br/> | Se trata de un error general que se usa cuando la operación solicitada no es válida. <br/><br/>Por ejemplo, no puede hacer lo siguiente: <br/> <br/>- Realizar un recorrido "profundo" mediante la operación [FindFolder](findfolder-operation.md) en una carpeta pública.  <br/>- Mover o copiar la raíz de carpeta pública.  <br/>- Eliminar un elemento asociado mediante cualquier modo excepto la eliminación "Dura".  <br/>- Mover o copiar un elemento asociado.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |Este error indica que un autor de la llamada solicitó información de disponibilidad para un usuario de otra organización, pero la relación organizativa no tiene habilitada la disponibilidad.  <br/> |
|ErrorInvalidPagingMaxRows  <br/> |Este error se produce cuando un consumidor pasa un valor cero o negativo para las filas máximas que se devolverán.  <br/> |
|ErrorInvalidParentFolder  <br/> |Este error se produce cuando un consumidor pasa una carpeta principal no válida para una operación. Por ejemplo, este error se devuelve si intenta crear una carpeta dentro de una carpeta de búsqueda.  <br/> |
|ErrorInvalidPercentCompleteValue  <br/> |Este error se devuelve cuando se intenta establecer un porcentaje de finalización de tareas en un valor no válido. El valor debe estar entre 0 y 100 (ambos inclusive).  <br/> |
|ErrorInvalidPermissionSettings  <br/> |Este error indica que el nivel de permisos es incoherente con la configuración de permisos.  <br/> |
|ErrorInvalidPhoneCallId  <br/> |Este error indica que el identificador de autor de la llamada no es válido.  <br/> |
|ErrorInvalidPhoneNumber  <br/> |Este error indica que el número de teléfono no es correcto o no se ajusta a las reglas del plan de marcado.  <br/> |
|ErrorInvalidPropertyAppend  <br/> | Este error se produce cuando la propiedad a la que está intentando anexar no admite anexar. <br/><br/>Las siguientes son las únicas propiedades que admiten anexar: <br/> <br/>- Colecciones de destinatarios (ToRecipients, CcRecipients, BccRecipients)  <br/>- Colecciones de asistentes (RequiredAttendees, OptionalAttendees, Resources)  <br/>- Body  <br/>- ReplyTo  <br/><br/>  Además, este error se produce cuando se anexa un cuerpo del mensaje si el formato especificado en la solicitud no coincide con el formato del elemento del almacén.  <br/> |
|ErrorInvalidPropertyDelete  <br/> |Este error se produce si la operación de eliminación se especifica en una operación [UpdateItem](updateitem-operation.md) o una llamada de operación [UpdateFolder](updatefolder-operation.md) para una propiedad que no admite la operación de eliminación. Por ejemplo, no puede eliminar el [elemento ItemId](itemid.md) del [objeto Item.](item.md)  <br/> |
|ErrorInvalidPropertyForExists  <br/> |Este error se produce si el consumidor pasa una de las propiedades de marca en un [filtro Exists.](exists.md) Por ejemplo, este error se produce si las marcas [IsRead](isread.md) o [IsFromMe](isfromme.md) se especifican en el [elemento Exists.](exists.md) La solicitud debe usar el [elemento IsEqualTo](isequalto.md) en su lugar para estos, ya que son marcas y, por lo tanto, forman parte de una sola propiedad.  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |Este error se produce cuando la propiedad que está intentando manipular no admite la operación que se está realizando en ella.  <br/> |
|ErrorInvalidPropertyRequest  <br/> | Este error se produce si una propiedad especificada en la solicitud no está disponible para el tipo de elemento. Por ejemplo, este error se devuelve si se solicita una propiedad que solo está disponible en elementos de calendario en una llamada de operación [GetItem](getitem-operation.md) para un mensaje o si se actualiza en una llamada de operación [UpdateItem](updateitem-operation.md) para un mensaje. <br/> <br/>  Esto se produce en las siguientes operaciones: <br/> <br/>- [Operación GetItem](getitem-operation.md) <br/>- [Operación GetFolder](getfolder-operation.md) <br/>- [Operación UpdateItem](updateitem-operation.md) <br/>- [Operación UpdateFolder](updatefolder-operation.md) <br/> |
|ErrorInvalidPropertySet  <br/> |Este error indica que la propiedad que está intentando manipular no admite la operación que se está realizando en ella. Por ejemplo, este error se devuelve si la propiedad que está intentando establecer es de solo lectura.  <br/> |
|ErrorInvalidPropertyUpdateSentMessage  <br/> | Este error se produce durante una [operación UpdateItem](updateitem-operation.md) cuando un cliente intenta actualizar determinadas propiedades de un mensaje que ya se ha enviado.<br/><br/> Por ejemplo, las siguientes propiedades no se pueden actualizar en un mensaje enviado: <br/> <br/>- [IsReadReceiptRequested](isreadreceiptrequested.md) <br/>- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |
|ErrorInvalidProxySecurityContext  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidPullSubscriptionId  <br/> |Este error se produce si se llama a la operación [GetEvents](getevents-operation.md) o a la operación [Cancelar](unsubscribe-operation.md) suscripción mediante un identificador de suscripción de inserción. Para cancelar la suscripción a una suscripción de inserción, debe responder a una solicitud de inserción con una respuesta de cancelación de suscripción o desconectar el servicio web y esperar a que las notificaciones de inserción se desasoyen.  <br/> |
|ErrorInvalidPushSubscriptionUrl  <br/> | La operación [Subscribe](subscribe-operation.md) devuelve este error cuando crea una suscripción "push" e indica que la dirección URL que se incluye en la solicitud no es válida.<br/><br/>Se deben cumplir las siguientes condiciones para que Exchange Web Services acepte la dirección URL: <br/> <br/>- Longitud de \> cadena 0 \< 2083.  <br/> y- El protocolo es http o https.  <br/>- La dirección URL se puede analizar mediante el URI de la .NET Framework Microsoft.  <br/> |
|ErrorInvalidRecipients  <br/> |Este error indica que la colección de destinatarios del mensaje o la colección de asistentes en el elemento de calendario no es válida. Por ejemplo, este error se devolverá cuando se intente enviar un elemento que no tenga destinatarios.  <br/> |
|ErrorInvalidRecipientSubfilter  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que Exchange los servicios web no pueden representar. Para evitar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterComparison  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que Exchange los servicios web no pueden representar. Para evitar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterOrder  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que Exchange los servicios web no pueden representar. Para evitar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidRecipientSubfilterTextFilter  <br/> |Este error indica que la carpeta de búsqueda tiene un filtro de tabla de destinatarios que Exchange los servicios web no pueden representar. Para evitar este error, recupere la carpeta sin solicitar los parámetros de búsqueda.  <br/> |
|ErrorInvalidReferenceItem  <br/> | Este error se devuelve de la [operación CreateItem](createitem-operation.md) para objetos de respuesta Forward y Reply en los siguientes escenarios:<br/>  <br/>- El identificador de elemento al que se hace referencia no es [un Message](message-ex15websvcsotherref.md), [un CalendarItem](calendaritem.md)o un descendiente de **un Message** o **CalendarItem**.  <br/>- El identificador de elemento de referencia es para **un CalendarItem** y el organizador está intentando responder o responderle a sí mismo.  <br/>- El mensaje es un borrador y Reply o ReplyAll está seleccionado.  <br/>- El elemento de referencia, [para SuppressReadReceipt](suppressreadreceipt.md), no es un **mensaje** o un descendiente de un **mensaje**.  <br/> |
|ErrorInvalidRequest  <br/> |Este error se produce cuando la solicitud SOAP tiene un encabezado de acción SOAP, pero no hay nada en el cuerpo SOAP. Tenga en cuenta que el encabezado acción SOAP no es necesario, ya que Exchange Web Services puede determinar el método al que llamar desde el nombre local del elemento raíz en el cuerpo SOAP.  <br/> |
|ErrorInvalidRestriction  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidRetentionTagTypeMismatch  <br/> |Este error se devuelve cuando la etiqueta de retención especificada tiene asociada una acción incorrecta. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInvisible  <br/> |Este error se devuelve cuando se intenta establecer una etiqueta inexistente o invisible en una **propiedad PolicyTag.** Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInheritance  <br/> |Este error se devuelve cuando se intenta establecer una etiqueta implícita en la **propiedad PolicyTag.** Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagIdGuid  <br/> |Indica que el GUID de la etiqueta de retención no era válido.  <br/> |
|ErrorInvalidRoutingType  <br/> |Este error se produce si el tipo de enrutamiento que se pasa para un [elemento RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) no es válido. Normalmente, el tipo de enrutamiento se establece en Protocolo simple de transferencia de correo (SMTP).  <br/> |
|ErrorInvalidScheduledOofDuration  <br/> |Este error se produce si la duración especificada no es mayor que la hora de inicio o si la hora de finalización no se produce en el futuro.  <br/> |
|ErrorInvalidSchemaVersionForMailboxVersion  <br/> |Este error indica que una solicitud de proxy que se envió a otro servidor no puede dar servicio a la solicitud debido a un error de coincidencia de versiones.  <br/> |
|ErrorInvalidSecurityDescriptor  <br/> |Este error indica que el descriptor Exchange de seguridad de la carpeta Calendario del almacén está dañado.  <br/> |
|ErrorInvalidSendItemSaveSettings  <br/> |Este error se produce durante un intento de enviar un elemento donde se especifica [SavedItemFolderId](saveditemfolderid.md) en la solicitud, pero la propiedad **SaveItemToFolder** se establece en **false**.  <br/> |
|ErrorInvalidSerializedAccessToken  <br/> |Este error indica que el token que se pasó en el encabezado está malformado, no hace referencia a una cuenta válida en el directorio o falta el grupo principal **ConnectingSID**.  <br/> |
|ErrorInvalidSharingData  <br/> |Este error indica que los metadatos de uso compartido no son válidos. Esto puede deberse a XML no válido.  <br/> |
|ErrorInvalidSharingMessage  <br/> |Este error indica que el mensaje de uso compartido no es válido. Esto puede deberse a una propiedad que falta.  <br/> |
|ErrorInvalidSid  <br/> |Este error se produce cuando se pasa un SID no válido en una solicitud.  <br/> |
|ErrorInvalidSIPUri  <br/> |Este error indica que el nombre SIP, el plan de marcado o el número de teléfono son URI SIP no válidos.  <br/> |
|ErrorInvalidServerVersion  <br/> |Este error indica que se especificó una versión del servidor de solicitudes no válida en la solicitud.  <br/> |
|ErrorInvalidSmtpAddress  <br/> |Este error se produce cuando no se puede analizar la dirección SMTP.  <br/> |
|ErrorInvalidSubfilterType  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidSubfilterTypeNotAttendeeType  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidSubfilterTypeNotRecipientType  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidSubscription  <br/> |Este error indica que la suscripción ya no es válida. Esto puede deberse a que el servidor de acceso de cliente se está reiniciando o porque la suscripción ha expirado.  <br/> |
|ErrorInvalidSubscriptionRequest  <br/> |Este error indica que la solicitud de suscripción incluía varios IDs de carpetas públicas. Una suscripción puede incluir varias carpetas del mismo buzón o un identificador de carpeta pública.  <br/> |
|ErrorInvalidSyncStateData  <br/> |[SyncFolderItems](syncfolderitems.md) o [SyncFolderHierarchy](syncfolderhierarchy.md) devuelven este error si los datos [SyncState](syncstate-ex15websvcsotherref.md) que se pasan no son válidos. Para corregir este error, debe volver a sincronizar sin el estado de sincronización. Asegúrese de que si conserva los BLOB de estado de sincronización, no trunca accidentalmente el BLOB.  <br/> |
|ErrorInvalidTimeInterval  <br/> |Este error indica que el intervalo de tiempo especificado no es válido. La hora de inicio debe ser mayor o igual que la hora de finalización.  <br/> |
|ErrorInvalidUserInfo  <br/> |Este error indica que se especificó un [UserId](userid.md) incoherente internamente para una operación de permisos. Por ejemplo, si se especifica un identificador de usuario distintivo (predeterminado o anónimo), este error se devuelve si también intenta especificar un SID o una dirección SMTP principal o un nombre para mostrar para este usuario.  <br/> |
|ErrorInvalidUserOofSettings  <br/> |Este error indica que la configuración del usuario fuera de Office (OOF) no es válida debido a que falta una respuesta interna o externa.  <br/> |
|ErrorInvalidUserPrincipalName  <br/> |Este error se produce durante Exchange suplantación. El autor de la llamada pasó un UPN no válido en el encabezado SOAP que no era accesible en el directorio.  <br/> |
|ErrorInvalidUserSid  <br/> |Este error se produce cuando se pasa un SID no válido en una solicitud.  <br/> |
|ErrorInvalidUserSidMissingUPN  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorInvalidValueForProperty  <br/> |Este error indica que el valor de comparación de la restricción no es válido para la propiedad con la que se compara.<br/><br/> Por ejemplo, el valor de comparación [de DateTimeCreated](datetimecreated.md)  >  **true** devolvería este código de respuesta. <br/><br/>Este código de respuesta también se devuelve si especifica una propiedad de enumeración en la comparación, pero el valor con el que se compara no es un valor válido para esa enumeración.  <br/> |
|ErrorInvalidWatermark  <br/> |Este error se debe a una marca de agua no válida.  <br/> |
|ErrorIPGatewayNotFound  <br/> |Este error indica que una puerta de enlace VoIP válida no está disponible.  <br/> |
|ErrorIrresolvableConflict  <br/> |Este error indica que la resolución de conflictos no pudo resolver los cambios de las propiedades. Es posible que los elementos de la tienda se hayan cambiado y tengan que actualizarse. Recupere la clave de cambio actualizada e inténtelo de nuevo.  <br/> |
|ErrorItemCorrupt  <br/> |Este error indica que el estado del objeto está dañado y no se puede recuperar. Al recuperar un elemento, solo ciertos elementos estarán en este estado, como [Body](body.md) y [MimeContent](mimecontent.md). Omita estos elementos y vuelva a intentar la operación.  <br/> |
|ErrorItemNotFound  <br/> |Este error se produce cuando no se encontró el elemento o no tiene permiso para tener acceso al elemento.  <br/> |
|ErrorItemPropertyRequestFailed  <br/> |Este error se produce si se produce un error en una solicitud de propiedad en un elemento. La propiedad puede existir, pero no se pudo recuperar.  <br/> |
|ErrorItemSave  <br/> |Este error se produce cuando se producen errores al intentar guardar el elemento o la carpeta.  <br/> |
|ErrorItemSavePropertyError  <br/> |Este error se produce cuando se produce un error al intentar guardar el elemento o carpeta debido a valores de propiedad no válidos. El código de respuesta incluye la ruta de acceso de las propiedades no válidas.  <br/> |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorLocalServerObjectNotFound  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorLogonAsNetworkServiceFailed  <br/> |Este error indica que el servicio de disponibilidad no pudo iniciar sesión como servicio de red para las solicitudes de proxy en los sitios o bosques adecuados. Esta respuesta suele indicar un error de configuración.  <br/> |
|ErrorMailboxConfiguration  <br/> |Este error indica que la información del buzón en AD DS está configurada incorrectamente.  <br/> |
|ErrorMailboxDataArrayEmpty  <br/> |Este error indica que el [elemento MailboxDataArray](mailboxdataarray.md) de la solicitud está vacío. Debe proporcionar al menos un identificador de buzón.  <br/> |
|ErrorMailboxDataArrayTooBig  <br/> |Este error se produce cuando se proporcionan más de 100 entradas en un [elemento MailboxDataArray.](mailboxdataarray.md)  <br/> |
|ErrorMailboxFailover  <br/> |Este error indica que se produjo un error al intentar obtener acceso a un buzón porque el buzón está en un proceso de conmutación por error.  <br/> |
|ErrorMailboxHoldNotFound  <br/> |Indica que no se encontró la retención del buzón.  <br/> |
|ErrorMailboxLogonFailed  <br/> |Este error se produce cuando se produce un error en la conexión al buzón para obtener la información de vista de calendario.  <br/> |
|ErrorMailboxMoveInProgress  <br/> | Este error indica que el buzón se mueve a un servidor o almacén de buzones diferente. Este error también puede indicar que el buzón está en otro servidor o base de datos de buzones.  <br/> |
|ErrorMailboxStoreUnavailable  <br/> | Este error indica que se produjo una de las siguientes condiciones de error:  <br/><br/>- El almacén de buzones está dañado.  <br/>- Se detiene el almacén de buzones.  <br/>- El almacén de buzones está sin conexión.  <br/>- Se produjo un error de red cuando se intentó obtener acceso al almacén de buzones.  <br/>- El almacén de buzones está sobrecargado y no puede aceptar más conexiones.  <br/>- El almacén de buzones se ha pausado.  <br/> |
|ErrorMailRecipientNotFound  <br/> |Este error se produce si la información del [elemento MailboxData](mailboxdata.md) no se puede asignar a una cuenta de buzón válida.  <br/> |
|ErrorMailTipsDisabled  <br/> |Este error indica que las sugerencias de correo están deshabilitadas.  <br/> |
|ErrorManagedFolderAlreadyExists  <br/> |Este error se produce si la carpeta administrada que está intentando crear ya existe en un buzón.  <br/> |
|ErrorManagedFolderNotFound  <br/> |Este error se produce cuando el nombre de carpeta especificado en la solicitud no se asigna a una definición de carpeta administrada en AD DS. Solo puede crear instancias de carpetas administradas para carpetas definidas en AD DS. Compruebe el nombre e inténtelo de nuevo.  <br/> |
|ErrorManagedFoldersRootFailure  <br/> |Este error indica que la raíz de carpetas administradas se eliminó del buzón o que existe una carpeta en la misma carpeta primaria que tiene el nombre de la raíz de carpeta administrada. Esto también se producirá si se produce un error en el intento de crear la carpeta administrada raíz.  <br/> |
|ErrorMeetingSuggestionGenerationFailed  <br/> |Este error indica que el motor de sugerencias encontró un problema cuando intentaba generar las sugerencias.  <br/> |
|ErrorMessageDispositionRequired  <br/> | Este error se produce si no se establece el atributo **MessageDisposition.**<br/><br/> Este atributo es necesario para lo siguiente: <br/> <br/>- La [operación CreateItem y](createitem-operation.md) [la operación UpdateItem](updateitem-operation.md) cuando se crea o actualiza el elemento es un [mensaje](message-ex15websvcsotherref.md).  <br/>- [CancelCalendarItem](cancelcalendaritem.md), [AcceptItem](acceptitem.md), [DeclineItem](declineitem.md)o [TentativelyAcceptItem objetos](tentativelyacceptitem.md) de respuesta.  <br/> |
|ErrorMessageSizeExceeded  <br/> |Este error indica que el mensaje que intenta enviar supera los límites permitidos.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |Este error indica que no se puede encontrar el dominio determinado.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |Este error indica que el servicio de seguimiento de mensajes no puede realizar un seguimiento del mensaje.  <br/> |
| ErrorMessageTrackingTransientError  <br/> |Este error indica que el servicio de seguimiento de mensajes está abajo o ocupado. Este código de error indica un error transitorio. Los clientes pueden volver a intentar conectarse al servidor cuando se recibe este error.  <br/> |
|ErrorMimeContentConversionFailed  <br/> |Este error se produce cuando el contenido MIME no es un iCal válido para una [operación CreateItem](createitem-operation.md). Para una [operación GetItem,](getitem-operation.md)esta respuesta indica que no se pudo generar el contenido MIME.  <br/> |
|ErrorMimeContentInvalid  <br/> |Este error se produce cuando el contenido MIME no es válido.  <br/> |
|ErrorMimeContentInvalidBase64String  <br/> |Este error se produce cuando el contenido MIME de la solicitud no es una cadena base 64 válida.  <br/> |
|ErrorMissingArgument  <br/> |Este error indica que faltaba un argumento necesario en la solicitud. El texto del mensaje de respuesta indica el argumento que se va a comprobar.  <br/> |
|ErrorMissingEmailAddress  <br/> |Este error indica que especificó un identificador de carpeta distintivo en la solicitud, pero la cuenta que realizó la solicitud no tiene un buzón en el sistema. En ese caso, debe proporcionar un sub elemento [Mailbox](mailbox.md) en [DistinguishedFolderId](distinguishedfolderid.md).  <br/> |
|ErrorMissingEmailAddressForManagedFolder  <br/> |Este error indica que especificó un identificador de carpeta distintivo en la solicitud, pero la cuenta que realizó la solicitud no tiene un buzón en el sistema. En ese caso, debe proporcionar un sub elemento [Mailbox](mailbox.md) en [DistinguishedFolderId](distinguishedfolderid.md). Esta respuesta se devuelve de la [operación CreateManagedFolder](createmanagedfolder-operation.md).  <br/> |
|ErrorMissingInformationEmailAddress  <br/> |Este error se produce si falta el [elemento EmailAddress (NonEmptyStringType).](emailaddress-nonemptystringtype.md)  <br/> |
|ErrorMissingInformationReferenceItemId  <br/> |Este error se produce si [falta ReferenceItemId.](referenceitemid.md)  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |Este código de error nunca se devuelve.  <br/> |
|ErrorMissingItemForCreateItemAttachment  <br/> |Este error se devuelve cuando se intenta no incluir el elemento item en el **elemento ItemAttachment** de una solicitud de operación [CreateAttachment.](createattachment-operation.md)  <br/> |
|ErrorMissingManagedFolderId  <br/> |Este error se produce cuando falta la propiedad de identificadores de directiva, la etiqueta de 0x6732 de la carpeta. Debe considerar esto como una carpeta dañada.  <br/> |
|ErrorMissingRecipients  <br/> |Este error indica que intentó enviar un elemento sin incluir destinatarios. Tenga en cuenta que si llama a la operación [CreateItem](createitem-operation.md) con una disposición de mensaje que hace que se envíe el mensaje, recibirá el siguiente código de respuesta: **ErrorInvalidRecipients**.  <br/> |
|ErrorMissingUserIdInformation  <br/> |Este error indica que un [UserId](userid.md) no se ha especificado completamente en un conjunto de permisos.  <br/> |
|ErrorMoreThanOneAccessModeSpecified  <br/> |Este error indica que ha especificado más de un valor de elemento [ExchangeImpersonation](exchangeimpersonation.md) dentro de una solicitud.  <br/> |
|ErrorMoveCopyFailed  <br/> |Este error indica que se produjo un error en la operación de movimiento o copia. El movimiento se produce en [la operación CreateItem](createitem-operation.md) cuando se acepta una solicitud de reunión que se encuentra en la carpeta Elementos eliminados. Además, si rechaza una solicitud de reunión, cancela un elemento de calendario o quita una reunión del calendario, se mueve a la carpeta Elementos eliminados.  <br/> |
|ErrorMoveDistinguishedFolder  <br/> |Este error se produce si intenta mover una carpeta distinguida.  <br/> |
|ErrorMultiLegacyMailboxAccess  <br/> |Este error se produce cuando una solicitud intenta obtener acceso a varios servidores de buzones de correo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorNameResolutionMultipleResults  <br/> |Este error se produce si la operación [ResolveNames](resolvenames-operation.md) devuelve más de un resultado o si el nombre ambiguo especificado coincide con más de un objeto del directorio. El código de respuesta incluye los nombres coincidentes en los datos de respuesta.  <br/> |
|ErrorNameResolutionNoMailbox  <br/> |Este error indica que el autor de la llamada no tiene un buzón en el sistema. La [operación ResolveNames o](resolvenames-operation.md) la operación [ExpandDL](expanddl-operation.md) no son válidas para conectar a un usuario sin un buzón.  <br/> |
|ErrorNameResolutionNoResults  <br/> |Este error indica que la [operación ResolveNames](resolvenames-operation.md) no devuelve ningún resultado.  <br/> |
|ErrorNoApplicableProxyCASServersAvailable  <br/> |Este código de error DEBE devolverse cuando el servicio web no puede encontrar un servidor que controle la solicitud.  <br/> |
|ErrorNoCalendar  <br/> |Este error se produce si no hay ninguna carpeta Calendar para el buzón.  <br/> |
|ErrorNoDestinationCASDueToKerberosRequirements  <br/> |Este error indica que la solicitud hacía referencia a un buzón en otro sitio de Active Directory, pero no se configuró ningún servidor de acceso de cliente en el sitio de destino para la autenticación de Windows y, por lo tanto, no se pudo realizar el proxy de la solicitud.  <br/> |
|ErrorNoDestinationCASDueToSSLRequirements  <br/> |Este error indica que la solicitud hacía referencia a un buzón en otro sitio de Active Directory, pero no se configuró ningún servidor de acceso de cliente en el sitio de destino para las conexiones SSL y, por lo tanto, la solicitud no se pudo proxy.  <br/> |
|ErrorNoDestinationCASDueToVersionMismatch  <br/> |Este error indica que la solicitud hacía referencia a un buzón de otro sitio de Active Directory, pero ningún servidor de acceso de cliente en el sitio de destino era de una versión de producto aceptable para recibir la solicitud y, por lo tanto, no se pudo proxy.  <br/> |
|ErrorNoFolderClassOverride  <br/> |Este error se produce si establece el [elemento FolderClass](folderclass.md) al crear un elemento que no sea una carpeta genérica. Para las carpetas con tipo, [como CalendarFolder](calendarfolder.md) y [TasksFolder,](tasksfolder.md)la clase de carpeta está implícita. Al establecer la clase de carpeta en un tipo de carpeta diferente mediante la operación [UpdateFolder,](updatefolder-operation.md) se produce la respuesta **ErrorObjectTypeChanged.** En su lugar, use un tipo de carpeta genérica, pero establezca la clase de carpeta en el valor que necesite. Exchange Los servicios web crearán la carpeta correcta fuertemente escribeda.  <br/> |
|ErrorNoFreeBusyAccess  <br/> |Este error indica que el autor de la llamada no tiene derechos de visualización de disponibilidad en la carpeta Calendario en cuestión.  <br/> |
|ErrorNonExistentMailbox  <br/> | Este error se produce en los siguientes escenarios: <br/> <br/>- La dirección de correo electrónico está vacía [en CreateManagedFolder](createmanagedfolder.md).  <br/>- La dirección de correo electrónico no hace referencia a una cuenta válida en una solicitud que toma una dirección de correo electrónico en el cuerpo o en el encabezado SOAP, como en una llamada Exchange suplantación de identidad.  <br/> |
|ErrorNonPrimarySmtpAddress  <br/> |Este error se produce cuando un autor de la llamada pasa una dirección SMTP no principal. La respuesta incluye la dirección SMTP correcta que se usará.  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |Este error indica que las propiedades MAPI del intervalo personalizado, 0x8000 y superiores, no se pueden hacer referencia mediante etiquetas de propiedades. Debe usar la propiedad [PropertySetId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)de la API administrada ews o el elemento EWS [ExtendedFieldURI](extendedfielduri.md) con el atributo PropertySetId.  <br/> |
|ErrorNoPublicFolderReplicaAvailable  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorNoPublicFolderServerAvailable  <br/> |Este código de error DEBE devolverse si no hay ningún servidor de carpetas públicas disponible o si el autor de la llamada no tiene un servidor público principal.  <br/> |
|ErrorNoRespondingCASInDestinationSite  <br/> |Este error indica que la solicitud hacía referencia a un buzón en otro sitio de Active Directory, pero ninguno de los servidores de acceso de cliente de ese sitio respondió y, por lo tanto, no se pudo realizar el proxy de la solicitud.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |Este error indica que el autor de la llamada intentó conceder permisos en su calendario o carpeta de contactos a un usuario de otra organización y se produjo un error en el intento.  <br/> |
|ErrorNotDelegate  <br/> |Este error indica que el usuario no es un delegado para el buzón. Se devuelve mediante la operación [GetDelegate](getdelegate-operation.md), la operación [RemoveDelegate](removedelegate-operation.md)y la operación [UpdateDelegate](updatedelegate-operation.md) cuando el usuario delegado especificado no se encuentra en la lista de delegados.  <br/> |
|ErrorNotEnoughMemory  <br/> |Este error indica que la operación no se pudo completar debido a la falta de memoria.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |Este error indica que no se admite el mensaje de uso compartido.  <br/> |
|ErrorObjectTypeChanged  <br/> |Este error se produce si el tipo de objeto cambió.  <br/> |
|ErrorOccurrenceCrossingBoundary  <br/> |Este error se [](start.md) produce [](end-ex15websvcsotherref.md) cuando se actualiza la hora de inicio o finalización de una repetición para que la repetición se programe antes o después de la repetición anterior o siguiente correspondiente.  <br/> |
|ErrorOccurrenceTimeSpanTooBig  <br/> |Este error indica que la asignación de tiempo para una repetición determinada se superpone con otra repetición del mismo elemento periódico. Esta respuesta también se produce cuando la longitud en minutos de una repetición determinada es mayor que Int32.MaxValue.  <br/> |
|ErrorOperationNotAllowedWithPublicFolderRoot  <br/> |Este error indica que la operación actual no es válida para la raíz de la carpeta pública.  <br/> |
|ErrorOrganizationNotFederated  <br/> |Este error indica que la organización del solicitante no está federada, por lo que el solicitante no puede crear mensajes de uso compartido para enviarlos a un usuario externo o no puede aceptar mensajes compartidos recibidos de un usuario externo.  <br/> |
|ErrorParentFolderIdRequired  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorParentFolderNotFound  <br/> |Este error se produce en la [operación CreateFolder](createfolder-operation.md) cuando no se encuentra la carpeta primaria.  <br/> |
|ErrorPasswordChangeRequired  <br/> |Este error indica que debe cambiar la contraseña para poder acceder a este buzón. Esto ocurre cuando se ha creado una nueva cuenta y el administrador ha indicado que el usuario debe cambiar la contraseña al iniciar sesión. No puede actualizar la contraseña mediante Exchange Web Services. Debes usar una herramienta como Microsoft Office Outlook Web App para cambiar la contraseña.  <br/> |
|ErrorPasswordExpired  <br/> |Este error indica que la contraseña ha expirado. No puede cambiar la contraseña mediante Exchange Web Services. Debe usar una herramienta como Outlook Web App para cambiar la contraseña.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |Este error indica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la directiva de uso compartido asignada al solicitante indica que el nivel de permisos solicitado es superior al que permite la directiva de uso compartido.  <br/> |
|ErrorPhoneNumberNotDialable  <br/> |Este error indica que el número de teléfono no estaba en el formulario correcto.  <br/> |
|ErrorPropertyUpdate  <br/> |Este error indica que se produjo un error en la actualización debido a valores de propiedad no válidos. El mensaje de respuesta incluye las rutas de acceso de propiedad no válidas.  <br/> |
|ErrorPromptPublishingOperationFailed  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorPropertyValidationFailure  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorProxiedSubscriptionCallFailure  <br/> |Este error indica que la solicitud hace referencia a una suscripción que existe en otro servidor de acceso de cliente, pero se produjo un error al intentar proxy de la solicitud en ese servidor de acceso de cliente.  <br/> |
|ErrorProxyCallFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorProxyGroupSidLimitExceeded  <br/> |Este error indica que la solicitud hace referencia a un buzón en otro sitio de Active Directory y que el autor de la llamada original es miembro de más de 3.000 grupos.  <br/> |
|ErrorProxyRequestNotAllowed  <br/> |Este error indica que la solicitud que Exchange servicios web enviados a otro servidor de acceso de cliente al intentar cumplir una solicitud [GetUserAvailabilityRequest](getuseravailabilityrequest.md) no era válida. Este código de respuesta normalmente indica que se ha producido un error de configuración o derechos, o que alguien intentó imitar sin éxito una solicitud de proxy de disponibilidad.  <br/> |
|ErrorProxyRequestProcessingFailed  <br/> |Este error indica que Exchange Web Services intentó proxy de una solicitud de disponibilidad en otro servidor de acceso de cliente para su cumplimiento, pero se produjo un error en la solicitud. Esta respuesta puede deberse a problemas de conectividad de red o a problemas de tiempo de espera de solicitud.  <br/> |
|ErrorProxyServiceDiscoveryFailed  <br/> |Este código de error debe devolverse si el servicio web no puede determinar si la solicitud se va a ejecutar en el servidor de destino o si se va a usar como proxy en otro servidor.  <br/> |
|ErrorProxyTokenExpired  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorPublicFolderMailboxDiscoveryFailed  <br/> |Este error se produce cuando no se encuentra la dirección URL del buzón de carpetas públicas. Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorPublicFolderOperationFailed  <br/> |Este error se produce cuando se intenta obtener acceso a una carpeta pública y el intento no se realiza correctamente. Este error se introdujo en Exchange 2013Exchange Server 2013.  <br/> |
|ErrorPublicFolderRequestProcessingFailed  <br/> |Este error se produce cuando el destinatario que se pasó a la operación [GetUserAvailability](getuseravailability-operation.md) se encuentra en un equipo que ejecuta una versión de Exchange Server anterior a Exchange 2007 y se produjo un error en la solicitud para recuperar información de disponibilidad para el destinatario del servidor de carpetas públicas.  <br/> |
|ErrorPublicFolderServerNotFound  <br/> |Este error se produce cuando el destinatario que se pasó a la operación [GetUserAvailability](getuseravailability-operation.md) se encuentra en un equipo que ejecuta una versión de Exchange Server anterior a Exchange 2007 y la solicitud para recuperar información de disponibilidad del destinatario del servidor de carpetas públicas produjo un error porque la unidad organizativa no tenía un servidor de carpetas públicas asociado.  <br/> |
|ErrorPublicFolderSyncException  <br/> |Este error se produce cuando una operación de sincronización se realiza correctamente en el buzón de carpetas públicas principal, pero no se realiza correctamente en el buzón de carpetas públicas secundaria. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorQueryFilterTooLong  <br/> |Este error indica que la restricción de carpeta de búsqueda puede ser válida, pero EWS no la admite. Exchange Los servicios web limitan las restricciones para que contengan un máximo de 255 expresiones de filtro. Si intenta enlazar a una carpeta de búsqueda existente que supere 255, se devuelve este código de respuesta.  <br/> |
|ErrorQuotaExceeded  <br/> |Este error se produce cuando se supera la cuota de buzón.  <br/> |
|ErrorReadEventsFailed  <br/> |La operación [GetEvents](getevents-operation.md) o las notificaciones de inserción devuelven este error cuando se produce un error al recuperar información del evento. Cuando se devuelve este error, se elimina la suscripción. Vuelva a crear la sincronización de eventos basándose en una última marca de agua conocida.  <br/> |
|ErrorReadReceiptNotPending  <br/> |La operación [CreateItem](createitem-operation.md) devuelve este error si se intentó suprimir una confirmación de lectura cuando el remitente del mensaje no solicitó una confirmación de lectura en el mensaje o si el mensaje se encuentra en la carpeta Correo electrónico no deseado.  <br/> |
|ErrorRecurrenceEndDateTooBig  <br/> |Este error se produce cuando la fecha de finalización de la periodicidad es después del 1/9/4500.  <br/> |
|ErrorRecurrenceHasNoOccurrence  <br/> |Este error se produce cuando la periodicidad especificada no tiene instancias de repetición en el intervalo especificado.  <br/> |
|ErrorRemoveDelegatesFailed  <br/> |Este error indica que la lista de delegados no se pudo guardar después de quitar los delegados.  <br/> |
|ErrorRequestAborted  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorRequestStreamTooBig  <br/> | Este error se produce cuando la secuencia de solicitudes es mayor que 400 KB.  <br/> |
|ErrorRequiredPropertyMissing  <br/> |Este error se devuelve cuando falta una propiedad necesaria en una solicitud de operación [CreateAttachment.](createattachment-operation.md) El URI de la propiedad que falta se incluye en la respuesta.  <br/> |
|ErrorResolveNamesInvalidFolderType  <br/> |Este error indica que el autor de la llamada ha especificado una carpeta que no es una carpeta de contactos para la [operación ResolveNames](resolvenames-operation.md).  <br/> |
|ErrorResolveNamesOnlyOneContactsFolderAllowed  <br/> |Este error indica que el autor de la llamada ha especificado más de una carpeta de contactos para la [operación ResolveNames](resolvenames-operation.md).  <br/> |
|ErrorResponseSchemaValidation  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorRestrictionTooLong  <br/> |Este error se produce si la restricción contiene más de 255 nodos.  <br/> |
|ErrorRestrictionTooComplex  <br/> |Este error se produce cuando la restricción no puede ser evaluada por Exchange Web Services.  <br/> |
|ErrorResultSetTooBig  <br/> |Este error indica que el número de entradas de calendario de un destinatario determinado supera el límite permitido de 1000. Reduzca la ventana e inténtelo de nuevo.  <br/> |
|ErrorSavedItemFolderNotFound  <br/> |Este error se produce cuando no se encuentra [SavedItemFolderId.](saveditemfolderid.md)  <br/> |
|ErrorSchemaValidation  <br/> | Este error se produce cuando la solicitud no se puede validar en el esquema.  <br/> |
|ErrorSearchFolderNotInitialized  <br/> |Este error indica que se creó la carpeta de búsqueda, pero los criterios de búsqueda nunca se han establecido en la carpeta. Esto solo se produce cuando se tiene acceso a carpetas de búsqueda dañadas que se crearon mediante otra API o cliente. Para corregir este error, use la [operación UpdateFolder](updatefolder-operation.md) para establecer el elemento [SearchParameters](searchparameters.md) para incluir la restricción que debe estar en la carpeta.  <br/> |
|ErrorSendAsDenied  <br/> | Este error se produce cuando se producen las dos condiciones siguientes: <br/> <br/>- A un usuario se le han concedido permisos CanActAsOwner, pero no se le conceden derechos de delegado en el buzón de la entidad de seguridad.  <br/>- El mismo usuario intenta crear y enviar un mensaje de correo electrónico en el buzón de la entidad de seguridad mediante la opción SendAndSaveCopy.<br/>  <br/>  El resultado es un error ErrorSendAsDenied y la creación del mensaje de correo electrónico en la carpeta Borradores de la entidad de seguridad.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |La operación [DeleteItem](deleteitem-operation.md) devuelve este error si falta el atributo **SendMeetingCancellations** de la solicitud y el elemento que se va a eliminar es un elemento de calendario.  <br/> |
|ErrorSendMeetingInvitationsOrCancellationsRequired  <br/> |La operación [UpdateItem](updateitem-operation.md) devuelve este error si el atributo **SendMeetingInvitationsOrCancellations** falta en la solicitud y el elemento que se va a actualizar es un elemento de calendario.  <br/> |
|ErrorSendMeetingInvitationsRequired  <br/> |La operación [CreateItem](createitem-operation.md) devuelve este error si falta el atributo **SendMeetingInvitations** de la solicitud y el elemento que se va a crear es un elemento de calendario.  <br/> |
|ErrorSentMeetingRequestUpdate  <br/> |Este error indica que después de que el organizador envía una solicitud de reunión, la solicitud no se puede actualizar. Para modificar la reunión, modifique el elemento de calendario, no la solicitud de reunión.  <br/> |
|ErrorSentTaskRequestUpdate  <br/> |Este error indica que después de que el iniciador de tareas envíe una solicitud de tarea, esa solicitud no se puede actualizar.  <br/> |
|ErrorServerBusy  <br/> |Este error se produce cuando el servidor está ocupado.  <br/> |
|ErrorServiceDiscoveryFailed  <br/> |Este error indica que Exchange Web Services intentó proxy de una solicitud de disponibilidad de usuario en el bosque adecuado para el destinatario, pero no pudo determinar dónde enviar la solicitud debido a un error de detección de servicio.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |Este error indica que la propiedad url externa no se ha establecido en la base de datos de Active Directory.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> |Este error indica que se produjo un error al intentar sincronizar una carpeta de uso compartido. <br/><br/>Este código de error se devuelve cuando se produce lo siguiente:<br/><br/>- No se encuentra la suscripción a una carpeta de uso compartido.<br/>- No se encuentra la carpeta de uso compartido.<br/>- No se encuentra el usuario de directorio correspondiente.<br/>- El usuario ya no existe.<br/>- La cita no es válida.<br/>- El elemento de contacto no es válido.<br/>- Hay un error de comunicación con el servidor remoto.  <br/> |
|ErrorStaleObject  <br/> |Este error se produce en una [operación UpdateItem](updateitem-operation.md) o en una operación [SendItem](senditem-operation.md) cuando la clave de cambio no está actualizada o no se suministró. Llame a [la operación GetItem](getitem-operation.md) para recuperar una clave de cambio actualizada y, a continuación, vuelva a intentar la operación.  <br/> |
|ErrorSubmissionQuotaExceeded  <br/> |Este error indica que un usuario no puede enviar inmediatamente más solicitudes porque se ha alcanzado la cuota de envío.  <br/> |
|ErrorSubscriptionAccessDenied  <br/> |Este error se produce cuando intenta obtener acceso a una suscripción mediante una cuenta que no hizo esa suscripción. El creador de la suscripción solo puede acceder a cada suscripción.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Este error indica que no puede crear una suscripción si no es el propietario o no tiene acceso de propietario al buzón.  <br/> |
|ErrorSubscriptionNotFound  <br/> |Este error se produce si no se encuentra la suscripción que corresponde al [Objeto SubscriptionId (GetEvents)](subscriptionid-getevents.md) especificado. Es posible que la suscripción haya expirado, que Exchange proceso de servicios web se haya reiniciado o que se haya pasado una suscripción no válida. Si la suscripción era válida, vuelve a crear la suscripción con la marca de agua más reciente. Esto lo devuelve la operación [Unsubscribe o](unsubscribe-operation.md) las respuestas de la operación [GetEvents.](getevents-operation.md)  <br/> |
|ErrorSubscriptionUnsubsribed  <br/> |Este código de error debe devolverse cuando se realiza una solicitud para una suscripción que se ha cancelado.  <br/> |
|ErrorSyncFolderNotFound  <br/> |La operación [SyncFolderItems](syncfolderitems-operation.md) devuelve este error si no se encuentra la carpeta primaria especificada.  <br/> |
|ErrorTeamMailboxNotFound  <br/> |Este error indica que no se encontró un buzón de equipo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxNotLinkedToSharePoint  <br/> |Este error indica que se encontró un buzón de equipo, pero que no está vinculado a un servidor SharePoint servidor. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxUrlValidationFailed  <br/> |Este error indica que se encontró un buzón de equipo, pero que el vínculo al servidor SharePoint no es válido. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxNotAuthorizedOwner  <br/> |Este código de error no se usa. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxActiveToPendingDelete  <br/> |Este código de error no se usa. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxFailedSendingNotifications  <br/> |Este error indica que un intento de enviar una notificación a los propietarios de buzones de equipo no se ha producido correctamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTeamMailboxErrorUnknown  <br/> |Este error indica un error general que puede producirse al intentar obtener acceso a un buzón de equipo. Pruebe a enviar la solicitud más adelante. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorTimeIntervalTooBig  <br/> |Este error indica que la ventana de tiempo especificada es mayor que el límite permitido. De forma predeterminada, el límite permitido es 42.  <br/> |
|ErrorTimeoutExpired  <br/> | Este error se produce cuando no hay tiempo suficiente para completar el procesamiento de la solicitud.  <br/> |
|ErrorTimeZone  <br/> |Este error indica que hay un error de zona horaria.  <br/> |
|ErrorToFolderNotFound  <br/> |Este error indica que la carpeta de destino no existe.  <br/> |
|ErrorTokenSerializationDenied  <br/> |Este error se produce si el autor de la llamada intenta realizar una solicitud de serialización de tokens, pero no tiene el derecho ms-Exch-EPI-TokenSerialization en el servidor de acceso de cliente.  <br/> |
|ErrorTooManyObjectsOpened  <br/> |Este error se produce cuando se ha superado el límite interno de objetos abiertos.  <br/> |
|ErrorUnifiedMessagingDialPlanNotFound  <br/> |Este error indica que el plan de marcado de un usuario no está disponible.  <br/> |
|ErrorUnifiedMessagingReportDataNotFound  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnifiedMessagingPromptNotFound  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnifiedMessagingRequestFailed  <br/> |Este error indica que no se pudo encontrar al usuario.  <br/> |
|ErrorUnifiedMessagingServerNotFound  <br/> |Este error indica que se puede encontrar un servidor válido para el plan de marcado para controlar la solicitud.  <br/> |
|ErrorUnableToGetUserOofSettings  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorUnableToRemoveImContactFromGroup  <br/> |Este error se produce cuando se realiza un intento fallido de quitar un contacto de mensajería instantánea de un grupo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUnsupportedCulture  <br/> |Este error se produce cuando se intenta establecer la propiedad **Culture** en un valor que la clase **System.Globalization.CultureInfo** no puede analizar.  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |Este error se produce cuando un autor de la llamada intenta usar propiedades extendidas de tipos de objeto, matriz de objetos, error o null.  <br/> |
|ErrorUnsupportedMimeConversion  <br/> |Este error se produce cuando se intenta recuperar o establecer contenido MIME para un elemento distinto de un [objeto PostItem](postitem.md), [Message](message-ex15websvcsotherref.md)o [CalendarItem.](calendaritem.md)  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |Este error se produce cuando el autor de la llamada pasa una propiedad que no es válida para una consulta. Esto puede ocurrir cuando se usan propiedades calculadas.  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |Este error se produce cuando el autor de la llamada pasa una propiedad que no es válida para una ordenación o un grupo por propiedad. Esto puede ocurrir cuando se usan propiedades calculadas.  <br/> |
|ErrorUnsupportedPropertyDefinition  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorUnsupportedQueryFilter  <br/> |Este error indica que la restricción de carpeta de búsqueda puede ser válida, pero EWS no la admite.  <br/> |
|ErrorUnsupportedRecurrence  <br/> |Este error indica que la periodicidad especificada no es compatible con las tareas.  <br/> |
|ErrorUnsupportedSubFilter  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |Este error indica que Exchange Web Services encontró un tipo de propiedad en el almacén, pero no puede generar XML para el tipo de propiedad.  <br/> |
|ErrorUpdateDelegatesFailed  <br/> |Este error indica que la lista de delegados no se pudo guardar después de actualizar los delegados.  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |Este error se produce cuando la ruta de acceso de una sola propiedad que aparece en una descripción de cambio no coincide con la única propiedad que se establece dentro del [objeto Item](item.md) o [Folder](folder.md) real.  <br/> |
|ErrorUserNotUnifiedMessagingEnabled  <br/> |Este error indica que el solicitante no está habilitado.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |Este error indica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la directiva de uso compartido asignada al solicitante indica que el dominio del usuario externo no aparece en la directiva.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Indica que la organización del solicitante tiene un conjunto de dominios federados, pero la organización del solicitante no tiene ninguna dirección proxy SMTP con uno de los dominios federados.  <br/> |
|ErrorValueOutOfRange  <br/> |Este error indica que una fecha de inicio o finalización de la vista de calendario se estableció en 1/1/0001 12:00:00 AM o 12/31/9999 11:59:59 PM.  <br/> |
|ErrorVirusDetected  <br/> |Este error indica que el Exchange detectó un virus en el mensaje.  <br/> |
|ErrorVirusMessageDeleted  <br/> |Este error indica que el Exchange detectó un virus en el mensaje y lo eliminó.  <br/> |
|ErrorVoiceMailNotImplemented  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWebRequestInInvalidState  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWin32InteropError  <br/> |Este error indica que hubo un error interno durante la comunicación con código no administrado.  <br/> |
|ErrorWorkingHoursSaveFailed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWorkingHoursXmlMalformed  <br/> |Este código de respuesta no se usa.  <br/> |
|ErrorWrongServerVersion  <br/> |Este error indica que solo se puede realizar una solicitud a un servidor que tenga la misma versión que el servidor de buzones de correo.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Este error indica que un delegado realizó una solicitud que tiene una versión de servidor diferente a la del servidor de buzones de correo de la entidad de seguridad.  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |Este código de error nunca se devuelve.  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |Especifica que hay encabezados SOAP duplicados.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> | Especifica que se ha fallado un intento de sincronización de una carpeta de uso compartido.<br/><br/> Este código de error DEBE devolverse cuando:<br/><br/>- No se encuentra la suscripción a una carpeta de uso compartido.  <br/>- No se encontró la carpeta de uso compartido.  <br/>- No se encontró el usuario de directorio correspondiente.  <br/>- El usuario ya no existe.  <br/>- La cita no es válida.  <br/>- El elemento de contacto no es válido.  <br/>- Hubo un error de comunicación con el servidor remoto.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |Especifica que la propiedad url externa no se ha establecido en la base de datos de Active Directory. Este código de error DEBE devolverse si la propiedad url externa no se ha establecido en la base de datos de Active Directory.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |Especifica que se ha alcanzado el número máximo de miembros del grupo para obtener información de disponibilidad para una lista de distribución. Este error DEBE devolverse cuando se haya alcanzado el número máximo de miembros del grupo para obtener información de disponibilidad para una lista de distribución.  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |Especifica que el elemento DataType y ShareFolderId están presentes en una solicitud. Este código de error DEBE devolverse si el elemento DataType y ShareFolderId están presentes en una solicitud.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |Especifica que el autor de la llamada intentó conceder permisos en su calendario o carpeta de contactos a un usuario de otra organización y el intento falló. Este código de error DEBE devolverse cuando la directiva de uso compartido está deshabilitada para el autor de la llamada o cuando la directiva de uso compartido asignada al autor de la llamada no permite el uso compartido para el nivel solicitado o el tipo de carpeta solicitado.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |Especifica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la directiva de uso compartido asignada al solicitante especifica que el dominio del usuario externo no aparece en la directiva.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |Especifica que el solicitante intentó conceder permisos en su calendario o carpeta de contactos a un usuario externo, pero la directiva de uso compartido asignada al solicitante especifica que el nivel de permisos solicitado es mayor que lo que permite la directiva de uso compartido.  <br/> |
|ErrorOrganizationNotFederated  <br/> |Especifica que la organización del solicitante no está federada, por lo que el solicitante no puede crear mensajes de uso compartido para enviarlos a un usuario externo o no puede aceptar mensajes compartidos recibidos de un usuario externo. Este código de error DEBE devolverse si la organización del solicitante no está federada.  <br/> |
|ErrorMailboxFailover  <br/> |Especifica que se ha fallado un intento de acceso a un buzón porque el buzón está en un proceso de conmutación por error.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |Especifica que el remitente de la invitación para compartir no ha creado los metadatos de invitación para compartir. Este código de error DEBE devolverse si el remitente de la invitación para compartir no ha creado los metadatos de invitación para compartir.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |Especifica que el servicio de seguimiento de mensajes no puede realizar un seguimiento del mensaje.  <br/> |
|ErrorMessageTrackingTransientError  <br/> |Especifica que el servicio de seguimiento de mensajes está abajo o ocupado. Este código de error especifica un error transitorio. Los clientes pueden volver a intentar conectarse al servidor cuando se recibe este error.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |Especifica que no se puede encontrar el dominio especificado.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Especifica que la organización del solicitante tiene un conjunto de dominios federados, pero la organización del solicitante no tiene ninguna dirección proxy SMTP con uno de los dominios federados.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |Especifica que un autor de la llamada solicitó información de disponibilidad para un usuario de otra organización, pero la relación organizativa no tiene habilitada la disponibilidad.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |Especifica que los objetos de federación de organización del solicitante no están configurados correctamente.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |Especifica que un mensaje de uso compartido no está pensado para el autor de la llamada.  <br/> |
|ErrorInvalidSharingData  <br/> |Especifica que los metadatos de uso compartido no son válidos. Esto puede deberse a XML no válido.  <br/> |
|ErrorInvalidSharingMessage  <br/> |Especifica que el mensaje de uso compartido no es válido. Esto puede deberse a una propiedad que falta.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |Especifica que no se admite el mensaje de uso compartido.  <br/> |
|ErrorApplyConversationActionFailed  <br/> |Este error DEBE devolverse si no se puede aplicar una acción a uno o varios elementos de la conversación.  <br/> |
|ErrorInboxRulesValidationError  <br/> |Este error DEBE devolverse si alguna regla no valida.  <br/> |
|ErrorOutlookRuleBlobExists  <br/> |Este error DEBE devolverse cuando se produce un intento de administrar reglas de bandeja de entrada después de que otro cliente haya accedido a las reglas de la Bandeja de entrada.  <br/> |
|ErrorRulesOverQuota  <br/> |Este error DEBE devolverse cuando se ha excedido la cuota de regla de un usuario.  <br/> |
|ErrorNewEventStreamConnectionOpened  <br/> |Este error DEBE devolverse a la primera conexión de suscripción si se abre una segunda conexión de suscripción.  <br/> |
|ErrorMissedNotificationEvents  <br/> |Este error DEBE devolverse cuando se pierden las notificaciones de eventos.  <br/> |
|ErrorDuplicateLegacyDistinguishedName  <br/> |Este error se devuelve cuando hay nombres distintivos heredados duplicados en Servicios de dominio de Active Directory (AD DS). Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidClientAccessTokenRequest  <br/> |Este error indica que una solicitud para obtener un token de acceso de cliente no era válida. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorNoSpeechDetected  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorUMServerUnavailable  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorRecipientNotFound  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorRecognizerNotInstalled  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSpeechGrammarError  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidManagementRoleHeader  <br/> |Este error se devuelve si el [encabezado ManagementRole](managementrole.md) del encabezado SOAP es incorrecto. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesDisabled  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesRequestTimedOut  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesRequestFailed  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorLocationServicesInvalidRequest  <br/> |Este error está diseñado solo para uso interno. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorWeatherServiceDisabled  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorMailboxScopeNotAllowedWithoutQueryString  <br/> |Este error se devuelve cuando se realiza un intento de búsqueda con ámbito sin usar un [elemento QueryString (String)](querystring-string.md) para una búsqueda de indización de contenido. Esto es aplicable a las **operaciones SearchMailboxes** y **FindConversation.** Este error se introdujo en Exchange 2013.  <br/> |
|ErrorArchiveMailboxSearchFailed  <br/> |Este error se devuelve cuando una búsqueda de buzón de archivo no se realiza correctamente. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |Este error se devuelve cuando no se puede detectar la dirección URL de un buzón de archivo. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorGetRemoteArchiveFolderFailed  <br/> |Este error se produce cuando se produce un error en la operación para obtener la carpeta de buzón de archivo remoto.  <br/> |
|ErrorFindRemoteArchiveFolderFailed  <br/> |Este error se produce cuando se produce un error en la operación para buscar la carpeta de buzón de archivo remoto.  <br/> |
|ErrorGetRemoteArchiveItemFailed  <br/> |Este error se produce cuando se produce un error en la operación para obtener el elemento de buzón de archivo remoto.  <br/> |
|ErrorExportRemoteArchiveItemsFailed  <br/> |Este error se produce cuando se produjo un error en la operación para exportar elementos de buzón de archivo remoto.  <br/> |
|ErrorInvalidPhotoSize  <br/> |Este error se devuelve si se solicita un tamaño de foto no válido del servidor. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSearchQueryHasTooManyKeywords  <br/> |Este error se devuelve cuando se solicita un tamaño de foto inesperado en una **solicitud de operación GetUserPhoto.** Este error se introdujo en Exchange 2013.  <br/> |
|ErrorSearchTooManyMailboxes  <br/> |Este error se devuelve cuando una solicitud de operación **SearchMailboxes** contiene demasiados buzones para buscar. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagNone  <br/> |Este error indica que no se encontraron etiquetas de retención para este usuario. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorDiscoverySearchesDisabled  <br/> |Este error se devuelve cuando las búsquedas de detección están deshabilitadas en un inquilino o servidor. Este error se introdujo en Exchange 2013.  <br/> |
|ErrorCalendarSeekToConditionNotSupported  <br/> |Este error se produce al intentar invocar la operación [FindItem](finditem-operation.md) con [seekToConditionPageItemView para](seektoconditionpageitemview.md) capturar elementos de calendario, que no se admiten.  <br/> |
|ErrorCalendarIsGroupMailboxForAccept  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorCalendarIsGroupMailboxForDecline  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorCalendarIsGroupMailboxForTentative  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt  <br/> |Este error está diseñado solo para uso interno.  <br/> |
|ErrorOrganizationAccessBlocked  <br/> |El espacio empresarial está marcado para su eliminación.  <br/> |
|ErrorInvalidLicense  <br/> |El usuario no tiene una licencia válida.  <br/> |
|ErrorMessagePerFolderCountReceiveQuotaExceeded  <br/> |Se ha superado la cuota de recepción del mensaje por carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento no es necesario y no se incluye en todas las respuestas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


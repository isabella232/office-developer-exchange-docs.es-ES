---
title: MessageText
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageText
api_type:
- schema
ms.assetid: 59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1
description: El elemento MessageText proporciona una descripción de texto del estado de la respuesta.
ms.openlocfilehash: 1503bbf211544797f56e7da661f38824a87a1196
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523862"
---
# <a name="messagetext"></a>MessageText

El **elemento MessageText** proporciona una descripción de texto del estado de la respuesta. 
  
```XML
<MessageText/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Proporciona información descriptiva sobre el estado de la respuesta.  <br/> <br/> Estas son algunas de las posibles expresiones XPath de este elemento: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/> <br/> `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud DeleteItem.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud SendItem.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud DeleteFolder.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud DeleteAttachment.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de cancelación de suscripción.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateFolder.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetFolder.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud UpdateFolder.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud MoveFolder.  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CopyFolder.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateManagedFolder.  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud FindFolder.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateItem.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetItem.  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud UpdateItem.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud MoveItem.  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CopyItem.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateAttachment.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetAttachment.  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud FindItem.  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud ResolveNames.  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud ExpandDL.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud subscribe.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetEvents.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud SendNotification.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud SyncFolderHierarchy.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud SyncFolderItems.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud ConvertId.  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud AddDelegate.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud GetServerTimeZones.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud GetSharingFolder.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud GetSharingFolder.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud GetSharingMetadata.  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Define una respuesta a una solicitud GetSharingMetadata.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud RefreshSharingFolder.  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud RefreshSharingFolder.  <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |Representa un destinatario no válido para una solicitud GetSharingMetadata.  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Contiene el estado y los resultados de una **respuesta FindConversation.**  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola **solicitud EmptyFolder.**  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Contiene una respuesta a una **solicitud UpdateInboxRules.**  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Contiene una respuesta a una **solicitud GetInboxRules.**  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Contiene una respuesta a una **solicitud GetServiceConfiguration.**  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene opciones de configuración de servicio.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento no es necesario y no se incluye en todas las respuestas. Este elemento se incluye cuando se devuelven mensajes de error. 
  
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


---
title: ResponseMessages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 2071bed8-ea66-4627-aa4f-a1d9a025cf3d
description: El elemento ResponseMessages contiene los mensajes de respuesta de una Exchange de servicios web.
ms.openlocfilehash: 23fa25b29cec0377d83ecf56a094da86af6c5213
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516394"
---
# <a name="responsemessages"></a>ResponseMessages

El **elemento ResponseMessages** contiene los mensajes de respuesta de una Exchange de servicios web. 
  
```XML
<ResponseMessages>
   <CreateItemResponseMessage/>
</ResponseMessages>
```

```xml
<ResponseMessages>
   <DeleteItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SendItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <EmptyFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <FindFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <MoveFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CopyFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UploadItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ExportItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <FindItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <MoveItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CopyItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ResolveNamesResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ExpandDLResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetServerTimeZonesResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetEventsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetStreamingEventsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SubscribeResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UnsubscribeResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SendNotificationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SyncFolderHierarchyResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SyncFolderItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateManagedFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ConvertIdResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetSharingMetadataResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <RefreshSharingFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetSharingFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRoomListsResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRoomsResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRemindersResponse/>
</ResponseMessages
```

```xml 
<ResponseMessages>
   <PerformReminderActionResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ApplyConversationActionResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetPasswordExpirationDateResponse />
</ResponseMessages>
```


**ArrayOfResponseMessagesType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CopyFolder.  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CopyItem.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateAttachment.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateFolder.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateItem.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud CreateManagedFolder.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud DeleteAttachment.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud DeleteFolder.  <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud DeleteItem.  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola [solicitud EmptyFolder.](emptyfolder.md)  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud ExpandDL.  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud FindFolder.  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud FindItem.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetAttachment.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una única solicitud UploadItems.  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una única solicitud ExportItems.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetEvents.  <br/> |
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetStreamingEvents.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetFolder.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetItem.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud MoveFolder.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud MoveItem.  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud ResolveNames.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud SendItem.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud SendNotification.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud subscribe.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud SyncFolderHierarchy.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud SyncFolderItems.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de cancelación de suscripción.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud UpdateFolder.  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud UpdateItem.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud ConvertId.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud GetSharingMetadata.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud RefreshSharingFolder.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud GetSharingFolder.  <br/> |
|[CreateUserConfigurationResponseMessage](createuserconfigurationresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud CreateUserConfiguration.  <br/> |
|[DeleteUserConfigurationResponseMessage](deleteuserconfigurationresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud DeleteUserConfiguration.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud GetUserConfiguration.  <br/> |
|[UpdateUserConfigurationResponseMessage](updateuserconfigurationresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud UpdateUserConfiguration.  <br/> |
|[GetRoomListsResponse](getroomlistsresponse.md) <br/> |Contiene el estado y los resultados de una solicitud GetRoomLists.  <br/> |
|[GetRoomsResponse](getroomsresponse.md) <br/> |Contiene el estado y los resultados de una solicitud GetRooms.  <br/> |
|[GetRemindersResponse](getremindersresponse.md) <br/> |Contiene el estado y los resultados de una solicitud GetReminders.  <br/> |
|[PerformReminderActionResponse](performreminderactionresponse.md) <br/> |Contiene el estado y los resultados de una solicitud PerformReminderAction.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetServerTimeZones.  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |Contiene el estado y los resultados de una [solicitud de operación ApplyConversationAction.](applyconversationaction-operation.md)  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopyFolderResponse](copyfolderresponse.md) <br/> |Define una respuesta a una solicitud CopyFolder.  <br/> |
|[CopyItemResponse](copyitemresponse.md) <br/> |Define una respuesta a una solicitud CopyItem.  <br/> |
|[CreateAttachmentResponse](createattachmentresponse.md) <br/> |Define una respuesta a una solicitud CreateAttachment.  <br/> |
|[CreateFolderResponse](createfolderresponse.md) <br/> |Define una respuesta a una solicitud CreateFolder.  <br/> |
|[CreateItemResponse](createitemresponse.md) <br/> |Define una respuesta a una solicitud CreateItem.  <br/> |
|[CreateManagedFolderResponse](createmanagedfolderresponse.md) <br/> |Define una respuesta a una solicitud CreateManagedFolder.  <br/> |
|[DeleteAttachmentResponse](deleteattachmentresponse.md) <br/> |Define una respuesta a una solicitud DeleteAttachment.  <br/> |
|[DeleteFolderResponse](deletefolderresponse.md) <br/> |Define una respuesta a una solicitud DeleteFolder.  <br/> |
|[DeleteItemResponse](deleteitemresponse.md) <br/> |Define una respuesta a una solicitud DeleteItem.  <br/> |
|[EmptyFolderResponse](emptyfolderresponse.md) <br/> |Define una respuesta a una solicitud EmptyFolder.  <br/> |
|[ExpandDLResponse](expanddlresponse.md) <br/> |Define una respuesta a una solicitud ExpandDL.  <br/> |
|[ExportItemsResponse](exportitemsresponse.md) <br/> |Representa la respuesta a una única solicitud ExportItems.  <br/> |
|[FindFolderResponse](findfolderresponse.md) <br/> |Define una respuesta a una solicitud FindFolder.  <br/> |
|[FindItemResponse](finditemresponse.md) <br/> |Define una respuesta a una solicitud FindItem.  <br/> |
|[GetAttachmentResponse](getattachmentresponse.md) <br/> |Define una respuesta a una solicitud GetAttachment.  <br/> |
|[GetEventsResponse](geteventsresponse.md) <br/> |Define una respuesta a una solicitud GetEvents.  <br/> |
|[GetStreamingEventsResponse](getstreamingeventsresponse.md) <br/> |Define una respuesta a una solicitud GetStreamingEvents.  <br/> |
|[GetFolderResponse](getfolderresponse.md) <br/> |Define una respuesta a una solicitud GetFolder.  <br/> |
|[GetItemResponse](getitemresponse.md) <br/> |Define una respuesta a una solicitud GetItem.  <br/> |
|[MoveFolderResponse](movefolderresponse.md) <br/> |Define una respuesta a una solicitud MoveFolder.  <br/> |
|[MoveItemResponse](moveitemresponse.md) <br/> |Define una respuesta a una solicitud MoveItem.  <br/> |
|[ResolveNamesResponse](resolvenamesresponse.md) <br/> |Define una respuesta a una solicitud ResolveNames.  <br/> |
|[SendItemResponse](senditemresponse.md) <br/> |Define una respuesta a una solicitud SendItem.  <br/> |
|[SendNotificationResult](sendnotificationresult.md) <br/> |Define una respuesta a una solicitud SendNotification.  <br/> |
|[SubscribeResponse](subscriberesponse.md) <br/> |Define una respuesta a una solicitud subscribe.  <br/> |
|[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md) <br/> |Define una respuesta a una solicitud SyncFolderHierarchy.  <br/> |
|[SyncFolderItemsResponse](syncfolderitemsresponse.md) <br/> |Define una respuesta a una solicitud SyncFolderItems.  <br/> |
|[UnsubscribeResponse](unsubscriberesponse.md) <br/> |Define una respuesta a una solicitud de cancelación de suscripción.  <br/> |
|[UpdateFolderResponse](updatefolderresponse.md) <br/> |Define una respuesta a una solicitud UpdateFolder.  <br/> |
|[UpdateItemResponse](updateitemresponse.md) <br/> |Define una respuesta a una solicitud UpdateItem.  <br/> |
|[ConvertIdResponse](convertidresponse.md) <br/> |Contiene una respuesta a una solicitud ConvertId.  <br/> |
|[GetServerTimeZonesResponse](getservertimezonesresponse.md) <br/> |Define una respuesta a una solicitud GetServerTimeZones.  <br/> |
|[CreateUserConfigurationResponse](createuserconfigurationresponse.md) <br/> |Define una respuesta a una solicitud CreateUserConfiuration.  <br/> |
|[DeleteUserConfigurationResponse](deleteuserconfigurationresponse.md) <br/> |Define una respuesta a una solicitud DeleteUserConfiguration.  <br/> |
|[GetUserConfigurationResponse](getuserconfigurationresponse.md) <br/> |Define una respuesta a una solicitud GetUserConfiguration.  <br/> |
|[UpdateUserConfigurationResponse](updateuserconfigurationresponse.md) <br/> |Define una respuesta a una solicitud UpdateUserConfiguration.  <br/> |
|[ApplyConversationActionResponse](applyconversationactionresponse.md) <br/> |Define una respuesta a una [solicitud de operación ApplyConversationAction.](applyconversationaction-operation.md)  <br/> |
|[GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md) <br/> |Define una respuesta a una [solicitud de operación GetPasswordExpirationDate.](getpasswordexpirationdate-operation.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ExportItems](exportitems-operation.md) 
- [Operación UploadItems](uploaditems-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


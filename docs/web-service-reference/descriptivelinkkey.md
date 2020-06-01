---
title: DescriptiveLinkKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DescriptiveLinkKey
api_type:
- schema
ms.assetid: f7f36749-00f3-4915-b17c-e3caa0af6e67
description: El elemento DescriptiveLinkKey está actualmente no en uso y está reservado para uso futuro. Contiene un valor de 0.
ms.openlocfilehash: e078d4ef4a629ea06bab0c2eb02b4f67b4fbf651
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467875"
---
# <a name="descriptivelinkkey"></a>DescriptiveLinkKey

El elemento **DescriptiveLinkKey** está actualmente no en uso y está reservado para uso futuro. Contiene un valor de 0. 
  
```XML
<DescriptiveLinkKey/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Proporciona información descriptiva sobre el estado de la respuesta.  <br/><br/>A continuación, se enumeran algunas de las posibles expresiones de XPath de este elemento:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>`/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>`/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **DeleteItem** .  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **SendItem** .  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **DeleteFolder** .  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **DeleteAttachment** .  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de **cancelación de suscripción** .  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud **CreateFolder** .  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **GetFolder** .  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **UpdateFolder** .  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **MoveFolder** .  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **CopyFolder** .  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **CreateManagedFolder** .  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **FindFolder** .  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **CreateItem** .  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud **GetItem** .  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **UpdateItem** .  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud **MoveItem** .  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud **CopyItem** .  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **CreateAttachment** .  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **GetAttachment** .  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **FindItem** .  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **ResolveNames** .  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **ExpandDL** .  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de **suscripción** .  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **GetEvents** .  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **SendNotification** .  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **SyncFolderHierarchy** .  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **SyncFolderItems** .  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **ConvertId** .  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud **AddDelegate** .  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **GetServerTimeZones** .  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **GetSharingFolder** .  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud **GetSharingFolder** .  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **GetSharingMetadata** .  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Define una respuesta a una solicitud **GetSharingMetadata** .  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **RefreshSharingFolder** .  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Define una respuesta a una solicitud **RefreshSharingFolder** .  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Contiene el estado y los resultados de una respuesta **FindConversation** .  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud **EmptyFolder** .  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Contiene el estado y el resultado de una solicitud **UpdateInboxRules** .  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud **UploadItemsResponse** .  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Contiene una respuesta a una solicitud de **GetInboxRules** .  <br/> |
|GetServiceConfigurationResponse  <br/> |Contiene una respuesta a una solicitud de **GetServiceConfiguration** .  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene las opciones de configuración del servicio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Es necesario un valor de texto si se usa este elemento. Este elemento es de sólo lectura.
  
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

- [Referencia EWS para Exchange](ews-reference-for-exchange.md) 
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


---
title: StreamingSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StreamingSubscriptionRequest
api_type:
- schema
ms.assetid: d18f3b60-ebb6-4133-b895-a6ec8942d039
description: El elemento StreamingSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos de streaming.
ms.openlocfilehash: 9789329f3f59cb543861dca0232207669f0711b8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544552"
---
# <a name="streamingsubscriptionrequest"></a>StreamingSubscriptionRequest

El **elemento StreamingSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos de streaming. 
  
[Subscribe](subscribe.md)
  
[StreamingSubscriptionRequest](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 **StreamingSubscriptionRequest**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Indica si el servidor se suscribirá a todas las carpetas del buzón del usuario. Un valor de **true** indica que el servidor se suscribirá.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usan para identificar carpetas para supervisar las notificaciones de eventos.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Contiene una colección de notificaciones de eventos que se usan para crear una suscripción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Subscribe](subscribe.md) <br/> |Contiene las propiedades que se usan para crear suscripciones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación GetStreamingEvents](getstreamingevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)


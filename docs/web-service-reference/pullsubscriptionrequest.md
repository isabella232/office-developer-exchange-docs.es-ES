---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: El elemento PullSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos basada en extracción.
ms.openlocfilehash: fb9712c9e1481678c2821ee344052783d5c25bf9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468869"
---
# <a name="pullsubscriptionrequest"></a>PullSubscriptionRequest

El elemento **PullSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos basada en extracción. 
  
[Suscribirse](subscribe.md)
  
[PullSubscriptionRequest](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 **PullSubscriptionRequestType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Indica si se va a suscribir a todas las carpetas disponibles. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a supervisar para las notificaciones de eventos.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Contiene una colección de notificaciones de eventos que se usan para crear una suscripción.  <br/> |
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos del buzón. Se usa para crear una suscripción que comienza en un evento que está representado por la marca de agua. Si no se encuentra la marca de agua de una solicitud de suscripción, se devolverá una respuesta de error al cliente. Este error puede producirse si la marca de agua es superior a 30 días o si la marca de agua nunca estaba presente en el buzón.  <br/> |
|[Timeout](timeout.md) <br/> |Representa la duración, en minutos, que la suscripción puede permanecer inactiva sin una solicitud GetEvents del cliente.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Suscribirse](subscribe.md) <br/> |Contiene las propiedades que se usan para crear suscripciones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[Operación subscribe](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación unsubscribe](unsubscribe-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


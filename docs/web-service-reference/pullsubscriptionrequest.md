---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: El elemento PullSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos basada en extracción.
ms.openlocfilehash: f1a527dff0c81262cac01a905293af1155acbf1c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540604"
---
# <a name="pullsubscriptionrequest"></a>PullSubscriptionRequest

El **elemento PullSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos basada en extracción. 
  
[Subscribe](subscribe.md)
  
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
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usan para identificar carpetas para supervisar las notificaciones de eventos.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Contiene una colección de notificaciones de eventos que se usan para crear una suscripción.  <br/> |
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos del buzón. Esto se usa para crear una suscripción que comience en un evento representado por la marca de agua. Si no se encuentra la marca de agua de una solicitud Subscribe, se devolverá una respuesta de error al cliente. Este error puede producirse si la marca de agua tiene más de 30 días o si la marca de agua nunca estuvo presente en el buzón.  <br/> |
|[Timeout](timeout.md) <br/> |Representa la duración, en minutos, de que la suscripción puede permanecer inactiva sin una solicitud GetEvents del cliente.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Subscribe](subscribe.md) <br/> |Contiene las propiedades que se usan para crear suscripciones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


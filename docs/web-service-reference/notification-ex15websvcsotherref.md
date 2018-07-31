---
title: Notification
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: El elemento de notificación contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.
ms.openlocfilehash: 942ec18521fc484a7a3aa1385fb54f480ce9d11f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354354"
---
# <a name="notification"></a>Notification

El elemento de **notificación** contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación. 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CreatedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <DeletedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <ModifiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <MovedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <NewMailEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <StatusEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <FreeBusyChangedEvent/>
</Notification>
```

**NotificationType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SubscriptionId (GetEvents)](subscriptionid-getevents.md) <br/> |Representa el identificador para una suscripción a.  <br/> |
|[PreviousWatermark](previouswatermark.md) <br/> |Representa la marca de agua del evento más reciente que se ha comunicado correctamente al cliente para la suscripción.  <br/> |
|[MoreEvents](moreevents.md) <br/> |Indica si hay más eventos en la cola para entregar al cliente.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento en el que se crea una carpeta o elemento.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento en el que se elimina un elemento o carpeta.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento en el que se modifica una carpeta o elemento.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento que se desencadena por un nuevo elemento de correo en un buzón de correo.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo.  <br/> |
|[FreeBusyChangedEvent](freebusychangedevent.md) <br/> |Representa un evento en el que se ha cambiado el tiempo de disponibilidad de un elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud GetEvents.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de SendNotification.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación Subscribe](subscribe-operation.md) 
- [Operación GetEvents](getevents-operation.md) 
- [Operación GetStreamingEvents](getstreamingevents-operation.md) 
- [Operación Unsubscribe](unsubscribe-operation.md)


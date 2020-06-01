---
title: Watermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: El elemento marca de agua representa un marcador de evento en la cola de eventos del buzón.
ms.openlocfilehash: a717196101fea698b0b8c66f92a3d420fda9a421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459766"
---
# <a name="watermark"></a>Watermark

El elemento **marca de agua** representa un marcador de evento en la cola de eventos del buzón. 
  
```xml
<Watermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en extracción.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en inserción.  <br/> |
|[GetEvents](getevents.md) <br/> |Representa la operación usada por los clientes de extracción para solicitar notificaciones del servidor.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o una carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento en el que se crea un elemento o una carpeta.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento en el que se elimina un elemento o carpeta.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento en el que se modifica un elemento o una carpeta.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento desencadenado por un nuevo elemento de correo en un buzón.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Representa una notificación de que no se ha producido ninguna actividad nueva en el buzón.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud subscribe.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto puede ser obligatorio u opcional en función de cómo se use este elemento.
  
## <a name="remarks"></a>Comentarios

Si una solicitud de suscripción contiene una marca de agua, la suscripción se crea desde la marca de agua hacia delante. Si la solicitud de suscripción contiene una marca de agua que no se encuentra en la tabla de eventos del buzón de correo, `ErrorInvalidWatermark` se devuelve un error a la aplicación cliente. Esto puede ocurrir si la marca de agua es demasiado antigua y se ha quitado de la ventana de 30 días de la tabla eventos o si la marca de agua no se ha puesto en alguna ocasión en la tabla eventos. Esto puede ocurrir, por ejemplo, si se obtiene una marca de agua de una suscripción diferente para un buzón de una base de datos diferente. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación subscribe](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación unsubscribe](unsubscribe-operation.md)


---
title: Watermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: El elemento Watermark representa un marcador de evento en la cola de eventos del buzón.
ms.openlocfilehash: 959ae7369195a164d257b8805a8c985f1fdca53b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524408"
---
# <a name="watermark"></a>Watermark

El **elemento Watermark** representa un marcador de evento en la cola de eventos del buzón. 
  
```xml
<Watermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en extracción.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en inserción.  <br/> |
|[GetEvents](getevents.md) <br/> |Representa la operación usada por los clientes de extracción para solicitar notificaciones desde el servidor.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento donde se copia un elemento o carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento donde se crea un elemento o carpeta.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento donde se elimina un elemento o una carpeta.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento donde se modifica un elemento o carpeta.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que se mueve un elemento o una carpeta de una carpeta primaria a otra carpeta primaria.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento desencadenado por un nuevo elemento de correo en un buzón.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Representa una notificación de que no se ha producido ninguna nueva actividad en el buzón.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud subscribe.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto puede ser necesario u opcional según cómo se utilice este elemento.
  
## <a name="remarks"></a>Comentarios

Si una solicitud Subscribe contiene una marca de agua, la suscripción se crea a partir de la marca de agua hacia delante. Si la solicitud Subscribe contiene una marca de agua que no se encuentra en la tabla de eventos de buzón de correo, se devuelve  `ErrorInvalidWatermark` un error a la aplicación cliente. Esto puede ocurrir si la marca de agua es demasiado antigua y se ha quitado de la ventana de 30 días de la tabla de eventos o si la marca de agua nunca estuvo presente en la tabla de eventos. Esto puede suceder, por ejemplo, si se obtiene una marca de agua de una suscripción diferente para un buzón de correo en una base de datos diferente. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)


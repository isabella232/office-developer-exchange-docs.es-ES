---
title: Marca de agua
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
description: El elemento de marca de agua representa un marcador de evento en la cola de eventos de buzón de correo.
ms.openlocfilehash: 1867aa781bc24f5eb3bdb4648fa494a2a7ea396a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840975"
---
# <a name="watermark"></a>Marca de agua

El elemento de **marca de agua** representa un marcador de evento en la cola de eventos de buzón de correo. 
  
```xml
<Watermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basado en la extracción.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de evento basada en inserción.  <br/> |
|[GetEvents](getevents.md) <br/> |Representa la operación usada por los clientes de extracción para las notificaciones de solicitud desde el servidor.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento donde se copia una carpeta o elemento.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento que se crea una carpeta o elemento.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento que se elimina un elemento o carpeta.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento que se modifica una carpeta o elemento.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento donde una carpeta o elemento se mueve desde la carpeta principal de una a otra carpeta primaria.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento activado por un nuevo elemento de correo en un buzón de correo.  <br/> |
|[Objeto StatusEvent](statusevent.md) <br/> |Representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud Subscribe.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto puede ser obligatorio u opcional dependiendo de cómo se usa este elemento.
  
## <a name="remarks"></a>Notas

Si una solicitud Subscribe contiene una marca de agua, se crea la suscripción de la marca de agua. Si la solicitud Subscribe contiene una marca de agua que no se encuentra en la tabla de eventos de buzón de correo, un `ErrorInvalidWatermark` error se devuelve a la aplicación cliente. Esto puede ocurrir si la marca de agua es demasiado antigua y se ha quitado de la ventana de 30 días de la tabla de eventos o si la marca de agua no fue nunca presentes en la tabla eventos. Esto puede suceder, por ejemplo, si se obtiene una marca de agua de una suscripción a diferente para un buzón de correo en una base de datos diferente. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)


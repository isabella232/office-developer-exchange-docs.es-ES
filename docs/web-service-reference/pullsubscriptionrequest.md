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
description: El elemento PullSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos basado en la extracción.
ms.openlocfilehash: 5f757bf1f79f7e2a00fb886db50e6ea0eaed1a4a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836932"
---
# <a name="pullsubscriptionrequest"></a>PullSubscriptionRequest

El elemento **PullSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos basado en la extracción. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Indica si se debe suscribirse a todas las carpetas disponibles. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para supervisar las notificaciones de eventos.  <br/> |
|[Debe establecer](eventtypes.md) <br/> |Contiene una colección de las notificaciones de eventos que se usan para crear una suscripción.  <br/> |
|[Marca de agua](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos de buzón de correo. Esto se usa para crear una suscripción que se inicia en un evento que está representado por la marca de agua. Si no se encuentra la marca de agua de una solicitud Subscribe, se devolverá una respuesta de error al cliente. Este error puede producirse si la marca de agua es más antiguo que 30 días o si la marca de agua nunca estaba presente en el buzón de correo.  <br/> |
|[Timeout](timeout.md) <br/> |Representa la duración, en minutos, que puede permanecer inactiva sin una solicitud GetEvents desde el cliente de la suscripción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Suscribirse](subscribe.md) <br/> |Contiene las propiedades que se usan para crear las suscripciones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


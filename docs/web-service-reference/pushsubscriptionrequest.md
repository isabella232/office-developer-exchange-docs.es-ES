---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: El elemento PushSubscriptionRequest representa una suscripción a una suscripción de notificación de evento basada en inserción.
ms.openlocfilehash: 34717d37b8e5bb50c927e57088299fbcb18a2514
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836929"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

El elemento **PushSubscriptionRequest** representa una suscripción a una suscripción de notificación de evento basada en inserción. 
  
[Suscribirse](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 **PushSubscriptionRequestType**
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
|[Marca de agua](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos de buzón de correo. Esto se usa para crear una suscripción a partir de un evento representado por la marca de agua. Si no se encuentra la marca de agua de una solicitud Subscribe, se devolverá una respuesta de error al cliente. Esto puede ocurrir si la marca de agua es más antiguo que 30 días o si la marca de agua nunca estaba presente en el buzón de correo.  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |Representa la frecuencia, en minutos, en la notificación que los mensajes se enviarán al cliente cuando no se ha producido ningún evento.  <br/> |
|[Dirección URL](url-ex15websvcsotherref.md) <br/> |Representa la ubicación del cliente de servicio Web para las notificaciones de inserción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Suscribirse](subscribe.md) <br/> |Contiene las propiedades usadas para crear las suscripciones.  <br/> |
   
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



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)


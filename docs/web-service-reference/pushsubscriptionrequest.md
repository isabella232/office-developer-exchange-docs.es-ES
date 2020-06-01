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
description: El elemento PushSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos basada en inserción.
ms.openlocfilehash: dcdb767ed175468aa4ec940f3147c164e4707e40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465516"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

El elemento **PushSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos basada en inserción. 
  
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
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos del buzón. Se usa para crear una suscripción que empieza en un evento representado por la marca de agua. Si no se encuentra la marca de agua de una solicitud de suscripción, se devolverá una respuesta de error al cliente. Esto puede ocurrir si la marca de agua es superior a 30 días o si la marca de agua nunca estaba presente en el buzón.  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |Representa la frecuencia, especificada en minutos, a la que se enviarán los mensajes de notificación al cliente cuando no se ha producido ningún evento.  <br/> |
|[Dirección URL](url-ex15websvcsotherref.md) <br/> |Representa la ubicación del servicio Web de cliente para las notificaciones de inserción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Suscribirse](subscribe.md) <br/> |Contiene las propiedades utilizadas para crear suscripciones.  <br/> |
   
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



[Operación subscribe](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación unsubscribe](unsubscribe-operation.md)


---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: El elemento StatusEvent representa una notificación de que no se ha producido ninguna actividad nueva en el buzón.
ms.openlocfilehash: 8158a47937a810be2ea22346384b4e61da56ac48
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468260"
---
# <a name="statusevent"></a>StatusEvent

El elemento **StatusEvent** representa una notificación de que no se ha producido ninguna actividad nueva en el buzón. 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 **BaseNotificationEventType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa la última marca de agua válida para una suscripción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **StatusEvent** se devuelve en una notificación por una de las siguientes razones: 
  
- Un cliente de extracción emite una solicitud GetEvents en una suscripción que no tiene actividad.
    
- Un cliente de inserción no tiene eventos en la cola cuando se ha alcanzado el [StatusFrequency](statusfrequency.md) . 
    
La **StatusEvent**[marca de agua](watermark.md) StatusEvent se usa en una aplicación cliente de la misma manera que las marcas de agua de otro tipo de evento. Sin embargo, la marca de agua de **StatusEvent** no es la misma que las marcas de agua usadas para otros eventos. Por ejemplo, una suscripción tiene eventos con marcas de agua de 1, 2 y 3, y estos eventos se han comunicado correctamente en una notificación. Se produce un período de inactividad y se envía una solicitud **GetEvents** . El servidor de acceso de cliente (CAS) devuelve un evento status e incluye la última marca de agua, 3, como [PreviousWatermark](previouswatermark.md) y la [marca de agua](watermark.md)actual.
  
La marca de agua no seguirá siendo la misma en todos los casos. Las entradas del evento se mantienen durante 30 días. Para mantener una suscripción activa, las entidades de certificación actualizan periódicamente las marcas de agua de las colas de suscripción. Las marcas de agua actualizadas se envían a los clientes para mantener una suscripción activa.
  
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


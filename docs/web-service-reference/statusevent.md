---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: El elemento StatusEvent representa una notificación de que no se ha producido ninguna nueva actividad en el buzón.
ms.openlocfilehash: 777d5cd22e47fea6e7bf7432e58e5d58d1ef67a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543978"
---
# <a name="statusevent"></a>StatusEvent

El **elemento StatusEvent** representa una notificación de que no se ha producido ninguna nueva actividad en el buzón. 
  
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

El **elemento StatusEvent** se devuelve en una notificación por uno de los siguientes motivos: 
  
- Un cliente de extracción emite una solicitud GetEvents en una suscripción que no tiene actividad.
    
- Un cliente de inserción no tiene eventos en la cola cuando se ha alcanzado [statusFrequency.](statusfrequency.md) 
    
La marca de [agua](watermark.md) **StatusEvent** la usa una aplicación cliente de la misma manera que las marcas de agua del otro tipo de evento. Sin embargo, la marca de agua **de StatusEvent** no es la misma que las marcas de agua usadas para otros eventos. Por ejemplo, una suscripción tiene eventos con marcas de agua 1, 2 y 3 y esos eventos se han comunicado correctamente en una notificación. Se produce un período de inactividad y se envía una solicitud **GetEvents.** El servidor de acceso de cliente (CAS) devuelve un evento de estado e incluye la última marca de agua, 3, como [previousWatermark](previouswatermark.md) y la marca de agua [actual.](watermark.md)
  
La marca de agua no seguirá siendo la misma en todos los casos. Las entradas de evento se mantienen durante 30 días. Para mantener una suscripción activa, el CAS actualiza periódicamente las marcas de agua para las colas de suscripción. Las marcas de agua actualizadas se envían a los clientes para mantener una suscripción activa.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)


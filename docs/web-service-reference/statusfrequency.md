---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: El elemento StatusFrequency representa el valor de tiempo de espera máximo, en minutos, en el que el servidor intenta realizar reintentos.
ms.openlocfilehash: f0359bab58167bbe7be5cce8c250240bebc7cc08
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525536"
---
# <a name="statusfrequency"></a>StatusFrequency

El **elemento StatusFrequency** representa el valor de tiempo de espera máximo, en minutos, en el que el servidor intenta realizar reintentos. 
  
[Subscribe](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[StatusFrequency](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 **SubscriptionStatusFrequencyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en inserción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto que representa un número entero. Los valores posibles para este elemento son de 1 a 1440, ambos incluidos. Este elemento es opcional. El valor predeterminado es de 30 minutos.
  
## <a name="remarks"></a>Comentarios

El servidor usa el valor **StatusFrequency** para reintentar una notificación de inserción cuando no recibe una respuesta a una notificación de inserción o un ping de estado del cliente. Si el servidor no recibe una respuesta, vuelve a enviar la notificación varias veces antes de que deje de enviar la notificación. En EWS, el intervalo de reintentos predeterminado es de 30 segundos y los reintentos posteriores siempre duplican el tiempo del último intervalo de reintentos. Los tiempos de reintento no son exactos, ya que se pueden retrasar debido a otras cargas en el servidor. En la tabla siguiente se muestra cómo se producen los intervalos de reintentos en los 30 minutos asignados por el valor **statusfrequency** predeterminado (suponiendo que el servidor no haya encontrado retrasos). 
  
|**Reintentar**|**Segundos**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |Sincronización inicial  <br/> |
|1  <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4   <br/> |240  <br/> |04:00  <br/> |
|5  <br/> |480  <br/> |08:00  <br/> |
|6   <br/> |960  <br/> |16:00  <br/> |
|7   <br/> |1920  <br/> |32:00: **valor predeterminado StatusFrequency** de 30 superado, reintento no enviado  <br/> |
   
Si el cliente no recibe mensajes de notificación del servidor durante un período de tiempo que supera el doble del tiempo especificado por **StatusFrequency,** el cliente debe realizar una acción como volver a crear la suscripción. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
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
  
[Watermark](watermark.md)


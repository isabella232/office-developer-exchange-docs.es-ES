---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: El elemento StatusFrequency representa el valor de tiempo de espera máximo, en minutos, en el que el servidor intenta realizar reintentos.
ms.openlocfilehash: db14ecfd54584188b3da16bb369db6c8089c70f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468246"
---
# <a name="statusfrequency"></a>StatusFrequency

El elemento **StatusFrequency** representa el valor de tiempo de espera máximo, en minutos, en el que el servidor intenta realizar reintentos. 
  
[Suscribirse](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[StatusFrequency](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 **SubscriptionStatusFrequencyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en inserción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Es necesario un valor de texto que representa un entero si se usa este elemento. Los valores posibles para este elemento son de 1 a 1440, ambos incluidos. Este elemento es opcional. El valor predeterminado es de 30 minutos.
  
## <a name="remarks"></a>Comentarios

El servidor usa el valor **StatusFrequency** para volver a intentar una notificación de inserción cuando no recibe una respuesta a una notificación de inserción o ping de estado del cliente. Si el servidor no recibe una respuesta, vuelve a intentar enviar la notificación varias veces antes de dejar de enviar la notificación. En EWS, el intervalo de reintento predeterminado es de 30 segundos y los reintentos siguientes siempre se duplican en el momento del último intervalo de reintento. Las horas de reintento no son exactas, ya que se pueden retrasar debido a otras cargas en el servidor. En la tabla siguiente se muestra cómo se producen los intervalos de reintento en los 30 minutos asignados por el valor de **StatusFrequency** predeterminado (si el servidor no ha encontrado ningún retraso). 
  
|**Reintentar**|**Segundos**|**Time**|
|:-----|:-----|:-----|
|comprendi  <br/> |comprendi  <br/> |Sincronización inicial  <br/> |
|1   <br/> |semestre  <br/> |00:30  <br/> |
|segundo  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4   <br/> |240  <br/> |04:00  <br/> |
|5   <br/> |480  <br/> |08:00  <br/> |
|6   <br/> |960  <br/> |16:00  <br/> |
|7   <br/> |1920  <br/> |32:00- **StatusFrequency** valor predeterminado de 30 superado, reintentar no enviado  <br/> |
   
Si el cliente no recibe mensajes de notificación del servidor durante un período de tiempo superior al doble del tiempo especificado por **StatusFrequency**, el cliente debe realizar una acción, como volver a crear la suscripción. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
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
  
[Watermark](watermark.md)


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
description: El elemento StatusFrequency representa el valor de tiempo de espera máximo, en minutos, en el que se ha tratado de reintentos por el servidor.
ms.openlocfilehash: 402f8978c0ec6b377dfa020f23595c8954509a07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837589"
---
# <a name="statusfrequency"></a>StatusFrequency

El elemento **StatusFrequency** representa el valor de tiempo de espera máximo, en minutos, en el que se ha tratado de reintentos por el servidor. 
  
[Suscribirse](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[StatusFrequency](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 **SubscriptionStatusFrequencyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de evento basada en inserción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, es necesario un valor de texto que representa un número entero. Los valores posibles para este elemento son 1 y 1440, ambos inclusive. Este elemento es opcional. El valor predeterminado es 30 minutos.
  
## <a name="remarks"></a>Comentarios

El valor de **StatusFrequency** se usa en el servidor para volver a intentar una notificación de inserción cuando no recibe una respuesta a una notificación de inserción o ping de estado desde el cliente. Si el servidor no recibe una respuesta, reintentos enviar la notificación de varias veces antes de que ésta detiene el envío de la notificación. En EWS, el intervalo de reintento de forma predeterminada es de 30 segundos y reintentos subsiguientes siempre son doble a la hora de último intervalo de reintento. Número de reintentos no es exacto como que se pueden retrasar debido a otras cargas que hay en el servidor. En la tabla siguiente se muestra cómo se producen los intervalos de reintento en los 30 minutos máximo permitidos por el valor de **StatusFrequency** predeterminado (suponiendo que el servidor no encuentra la los retrasos). 
  
|**Reintentar**|**Segundos**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |Sincronización inicial  <br/> |
|1  <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4  <br/> |240  <br/> |04:00  <br/> |
|5  <br/> |480  <br/> |08:00  <br/> |
|6  <br/> |960  <br/> |16:00  <br/> |
|7  <br/> |1920  <br/> |32:00 - **StatusFrequency** valor de predeterminado de 30 superado, reintento no enviado  <br/> |
   
Si el cliente no recibe los mensajes de notificación desde el servidor durante un período de tiempo que supere los dos veces el tiempo especificado por **StatusFrequency**, el cliente debe realizar una acción como volver a crear la suscripción. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)
  
[Marca de agua](watermark.md)


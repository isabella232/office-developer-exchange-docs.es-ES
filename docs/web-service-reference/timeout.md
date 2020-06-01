---
title: Timeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Timeout
api_type:
- schema
ms.assetid: c2e1ca5a-6667-4f6f-aac4-89de33bddc54
description: El elemento timeout representa la duración, en minutos, que la suscripción puede permanecer inactiva sin una solicitud GetEvents del cliente.
ms.openlocfilehash: 6f3228cd480bf0eaf259c4f321bc74d0845b9bba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459899"
---
# <a name="timeout"></a>Timeout

El elemento **timeout** representa la duración, en minutos, que la suscripción puede permanecer inactiva sin una solicitud GetEvents del cliente. 
  
```xml
<Timeout/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en extracción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Es necesario un valor de texto que representa un entero si se usa este elemento. Los valores posibles para este elemento son de 1 a 1440, ambos incluidos. Se requiere este elemento.
  
## <a name="remarks"></a>Comentarios

Una solicitud GetEvents correcta restablece el temporizador de tiempo de espera de la suscripción.
  
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


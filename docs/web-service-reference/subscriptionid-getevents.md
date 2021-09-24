---
title: SubscriptionId (GetEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SubscriptionId
api_type:
- schema
ms.assetid: 77c0abab-69e8-428e-8c20-22258e4ef71b
description: El elemento SubscriptionId representa el identificador de una suscripción.
ms.openlocfilehash: c24ae8dc61fa98716efc38d7a2500cab503760b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522589"
---
# <a name="subscriptionid-getevents"></a>SubscriptionId (GetEvents)

El **elemento SubscriptionId** representa el identificador de una suscripción. 
  
```xml
<SubscriptionId/>
```

 **SubscriptionIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetEvents](getevents.md) <br/> |Representa la operación usada por los clientes de extracción para solicitar notificaciones desde el servidor.  <br/> |
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud subscribe.  <br/> |
|[Unsubscribe](unsubscribe.md) <br/> |Contiene las propiedades usadas para cancelar la suscripción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto es un GUID.
  
## <a name="remarks"></a>Comentarios

El servidor de acceso de cliente genera el GUID que representa el identificador de suscripción cuando se crea la suscripción.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)


---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: El elemento MoreEvents indica si hay más eventos en la cola que se entregarán al cliente.
ms.openlocfilehash: 7a19349e406a7e55e52c8a8cf0c3febba0a7301b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521812"
---
# <a name="moreevents"></a>MoreEvents

El **elemento MoreEvents** indica si hay más eventos en la cola que se entregarán al cliente. 
  
```xml
<MoreEvents/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un valor booleano. Un valor **true** indica que hay más eventos en la cola. Un valor de **false** indica que no hay más eventos en la cola. Esta propiedad es de sólo lectura. 
  
## <a name="remarks"></a>Comentarios

En el caso de las notificaciones de extracción, un valor **verdadero** en este elemento indica al cliente que se debe emitir otra solicitud GetEvents para obtener los eventos restantes. Suponiendo que las especificaciones del cliente requieren una latencia mínima para las notificaciones de eventos, las solicitudes GetEvents deben continuar en una sucesión continua hasta que se devuelva un **valor** **False MoreEvents.** 
  
En el caso de las  notificaciones push, un valor verdadero para **MoreEvents** indica al cliente que se enviará otra solicitud de notificación al cliente para entregar los eventos restantes. Al igual que con las notificaciones de extracción, estas solicitudes de seguimiento continuarán en continua sucesión hasta que la cola de eventos del servidor de acceso de cliente esté vacía. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)


---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: El elemento MoreEvents indica si hay más eventos en la cola que se entreguen al cliente.
ms.openlocfilehash: fd12dd2e2e64ce1711e553ba5eb29bd0eb64c892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462734"
---
# <a name="moreevents"></a>MoreEvents

El elemento **MoreEvents** indica si hay más eventos en la cola que se entreguen al cliente. 
  
```xml
<MoreEvents/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un valor booleano. Un valor de **true** indica que hay más eventos en la cola. Un valor de **false** indica que no hay más eventos en la cola. Esta propiedad es de sólo lectura. 
  
## <a name="remarks"></a>Comentarios

En el caso de las notificaciones de extracción, un valor **true** en este elemento indica al cliente que se debe emitir otra solicitud GetEvents para obtener los eventos restantes. Si se supone que las especificaciones de cliente requieren una latencia mínima para las notificaciones de eventos, las solicitudes GetEvents deben continuar en una sucesión continua hasta que se devuelva un valor **MoreEvents** **falso** . 
  
En el caso de las notificaciones de inserción, un valor **true** para **MoreEvents** indica al cliente que se enviará al cliente otra solicitud de notificación para entregar los eventos restantes. De forma similar a las notificaciones de extracción, estas solicitudes de seguimiento continuarán en sucesión continuas hasta que la cola de eventos del servidor de acceso de cliente esté vacía. 
  
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


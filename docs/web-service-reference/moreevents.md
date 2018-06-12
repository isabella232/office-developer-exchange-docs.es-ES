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
description: El elemento MoreEvents indica si hay más eventos en la cola para entregar al cliente.
ms.openlocfilehash: cc3f7ed3b4b5f5ce27a9d45d508506bfa62e5086
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836489"
---
# <a name="moreevents"></a>MoreEvents

El elemento **MoreEvents** indica si hay más eventos en la cola para entregar al cliente. 
  
```xml
<MoreEvents/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un valor de tipo Boolean. Un valor de **true** indica que son más eventos en la cola. Un valor de **false** indica que no hay más eventos están en la cola. Esta propiedad es de sólo lectura. 
  
## <a name="remarks"></a>Notas

En el caso de las notificaciones de extracción, un valor **true** en este elemento indica al cliente que se debe emitir otra solicitud GetEvents para obtener los eventos restantes. Suponiendo que las especificaciones de cliente necesitan la latencia mínima para las notificaciones de eventos, Solicitudes GetEvents deberían seguir en una sucesión continua hasta que se devuelve **false** el valor de **MoreEvents** . 
  
En el caso de las notificaciones de inserción, indica un valor **true** para **MoreEvents** al cliente que otra solicitud de notificación se enviarán al cliente para ofrecer los eventos restantes. Al igual que las notificaciones de extracción, estas solicitudes seguimiento continuará en sucesión continua hasta que la cola de eventos en el servidor de acceso de cliente está vacía. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)


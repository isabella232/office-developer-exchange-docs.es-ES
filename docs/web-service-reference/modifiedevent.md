---
title: ModifiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: El elemento ModifiedEvent representa un evento en el que se modifica una carpeta o elemento.
ms.openlocfilehash: 2e9fb870396d49efb5cdf307a502b4111c2e507e
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353815"
---
# <a name="modifiedevent"></a>ModifiedEvent

El elemento **ModifiedEvent** representa un evento en el que se modifica una carpeta o elemento. 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/> 
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

**ModifiedEventType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos de buzón de correo.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Representa la marca de hora de un evento de buzón de carpeta o elemento modificado.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta modificada.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento modificado.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal de la carpeta o el elemento modificado.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Representa el recuento de elementos no leídos dentro de una carpeta determinada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

Se generan dos eventos modificados para cada modificación de un elemento en una carpeta. Un evento es relevante para el elemento que ha cambiado. El otro evento es relevante para la carpeta principal del elemento. Esto es la misma carpeta que se creó la suscripción contra. El evento que está asociado a la carpeta se usa para comunicarse un cambio posible para la propiedad [UnreadCount](unreadcount.md) en la carpeta. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación Subscribe](subscribe-operation.md)  
- [Operación GetEvents](getevents-operation.md)  
- [Operación Unsubscribe](unsubscribe-operation.md)


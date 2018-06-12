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
ms.openlocfilehash: fb464fb0a270d8ca7d33d40e5425e260970b2f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836482"
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

 **ModifiedEventType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Marca de agua](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos de buzón de correo.  <br/> |
|[Marca de tiempo](timestamp.md) <br/> |Representa la marca de hora de un evento de buzón de carpeta o elemento modificado.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta modificada.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento modificado.  <br/> |
|[Id](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal de la carpeta o el elemento modificado.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Representa el recuento de elementos no leídos dentro de una carpeta determinada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Notas

Se generan dos eventos modificados para cada modificación de un elemento en una carpeta. Un evento es relevante para el elemento que ha cambiado. El otro evento es relevante para la carpeta principal del elemento. Esto es la misma carpeta que se creó la suscripción contra. El evento que está asociado a la carpeta se usa para comunicarse un cambio posible para la propiedad [UnreadCount](unreadcount.md) en la carpeta. 
  
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


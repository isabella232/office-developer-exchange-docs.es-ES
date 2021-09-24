---
title: ModifiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: El elemento ModifiedEvent representa un evento en el que se modifica un elemento o carpeta.
ms.openlocfilehash: 92002c2824168687e6984913dbf46ee85da921e7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539363"
---
# <a name="modifiedevent"></a>ModifiedEvent

El **elemento ModifiedEvent** representa un evento en el que se modifica un elemento o carpeta. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos del buzón.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Representa la marca de tiempo de un elemento modificado o un evento de buzón de carpeta.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta modificada.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento modificado.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal del elemento o carpeta modificado.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Representa el recuento de elementos no leídos dentro de una carpeta determinada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

Se generan dos eventos modificados para cada modificación de un elemento de una carpeta. Un evento es relevante para el elemento que ha cambiado. El otro evento es relevante para la carpeta principal del elemento. Esta es la misma carpeta en la que se creó la suscripción. El evento asociado a la carpeta se usa para comunicar un posible cambio a la [propiedad UnreadCount](unreadcount.md) de la carpeta. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación de suscripción](subscribe-operation.md)  
- [Operación GetEvents](getevents-operation.md)  
- [Operación Darse de baja](unsubscribe-operation.md)


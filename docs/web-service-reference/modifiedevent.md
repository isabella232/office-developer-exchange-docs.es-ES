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
description: El elemento ModifiedEvent representa un evento en el que se modifica un elemento o una carpeta.
ms.openlocfilehash: 1a798773601a0857b9064c7fa6a532a7a36517ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468554"
---
# <a name="modifiedevent"></a>ModifiedEvent

El elemento **ModifiedEvent** representa un evento en el que se modifica un elemento o una carpeta. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos del buzón.  <br/> |
|[Marca](timestamp.md) <br/> |Representa la marca de hora de un elemento modificado o un evento de buzón de carpeta.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta modificada.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento modificado.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal del elemento o carpeta que se ha modificado.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Representa el número de elementos no leídos dentro de una carpeta determinada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

Se generan dos eventos modificados para cada modificación de un elemento en una carpeta. Un evento es relevante para el elemento que ha cambiado. El otro evento es relevante para la carpeta principal del elemento. Se trata de la misma carpeta en la que se creó la suscripción. El evento asociado a la carpeta se usa para comunicar un cambio potencial a la propiedad [UnreadCount](unreadcount.md) de la carpeta. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación subscribe](subscribe-operation.md)  
- [Operación GetEvents](getevents-operation.md)  
- [Operación unsubscribe](unsubscribe-operation.md)


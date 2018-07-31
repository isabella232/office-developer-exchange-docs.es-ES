---
title: MovedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: El elemento MovedEvent representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.
ms.openlocfilehash: 07f9c02ea194187a9fdfb1e27b19eb311392f51f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353262"
---
# <a name="movedevent"></a>MovedEvent

El elemento **MovedEvent** representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria. 
  
```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</MovedEvent>
```

```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</MovedEvent>
```


**MovedCopiedEventType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa un marcador de eventos en la tabla de eventos de buzón de correo.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Representa la marca de hora de un evento de mover el buzón de correo elemento o carpeta.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta que se ha movido.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento que se ha movido.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta que contiene el elemento que se ha movido o la carpeta.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Contiene el identificador de la carpeta de la carpeta original antes de se ha movido o copiado.  <br/> |
|[OldItemId](olditemid.md) <br/> |Contiene el identificador único del elemento original antes de que se ha movido.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Contiene el identificador de la carpeta principal original de un elemento o carpeta que se ha movido.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

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


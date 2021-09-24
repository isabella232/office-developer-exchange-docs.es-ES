---
title: MovedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: El elemento MovedEvent representa un evento en el que se mueve un elemento o carpeta de una carpeta primaria a otra carpeta primaria.
ms.openlocfilehash: 4e0795fc3f335139e22fb51a4cf215a870ec62c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518137"
---
# <a name="movedevent"></a>MovedEvent

El **elemento MovedEvent** representa un evento en el que se mueve un elemento o carpeta de una carpeta primaria a otra carpeta primaria. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa un marcador de eventos en la tabla de eventos de buzón.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Representa la marca de tiempo de un evento de buzón de correo de elemento de movimiento o carpeta.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta movida.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento movido.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta que contiene el elemento o carpeta movido.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Contiene el identificador de carpeta de la carpeta original antes de moverla o copiarla.  <br/> |
|[OldItemId](olditemid.md) <br/> |Contiene el identificador único del elemento original antes de moverlo.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Contiene el identificador de la carpeta principal original de un elemento o carpeta que se movió.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

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


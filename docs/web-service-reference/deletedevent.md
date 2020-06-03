---
title: DeletedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedEvent
api_type:
- schema
ms.assetid: c4565eb4-b537-466c-b1ff-11602533812b
description: El elemento DeletedEvent representa un evento en el que se elimina un elemento o una carpeta.
ms.openlocfilehash: 5eb0c947aacc592f81c595da2cc00bf4874f300b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526945"
---
# <a name="deletedevent"></a>DeletedEvent

El elemento **DeletedEvent** representa un evento en el que se elimina un elemento o una carpeta. 
  
```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
</DeletedEvent>
```

**BaseObjectChangedEventType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos del buzón.  <br/> |
|[Marca](timestamp.md) <br/> |Representa la marca de hora de un evento de elemento o buzón de carpeta eliminado.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta eliminada.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento eliminado.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal del elemento o carpeta eliminados antes de su eliminación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

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


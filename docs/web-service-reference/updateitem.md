---
title: UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: El elemento UpdateItem define una solicitud para actualizar un elemento en un buzón.
ms.openlocfilehash: 544ccfb8c42b2a4d4f69ae04d383233203c235b8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542794"
---
# <a name="updateitem"></a>UpdateItem

El **elemento UpdateItem** define una solicitud para actualizar un elemento en un buzón. 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 **UpdateItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ConflictResolution** <br/> |Identifica el tipo de resolución de conflictos que se debe intentar durante una actualización. El valor predeterminado es AutoResolve.  <br/> |
|**MessageDisposition** <br/> |Describe cómo se controlará el elemento después de actualizarlo. El **atributo MessageDisposition** es necesario para los elementos del mensaje, incluidos los mensajes de reunión, como cancelaciones de reuniones, solicitudes de reunión y respuestas de reunión.  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |Describe cómo se comunican las actualizaciones de reuniones después de actualizar un elemento de calendario. Este atributo es necesario para los elementos de calendario y las repeticiones de elementos de calendario.  <br/> |
|**SuppressReadReceipts** <br/> |Indica si se deben suprimir las confirmaciones de lectura del elemento actualizado. Un valor de texto **de true** indica que se deben suprimir las confirmaciones de lectura. Un valor de **false** indica que las confirmaciones de lectura se enviarán al remitente. Este atributo es opcional.  <br/> Este atributo se introdujo en Exchange Server 2013 SP1.  <br/> |
   
#### <a name="conflictresolution-attribute"></a>Atributo ConflictResolution

|**Valor**|**Descripción**|
|:-----|:-----|
|NeverOverwrite  <br/> |Si hay un conflicto, se produce un error en la operación de actualización y se devuelve un error.  <br/> |
|AutoResolve  <br/> |La operación de actualización resuelve automáticamente cualquier conflicto.  <br/> |
|AlwaysOverwrite  <br/> |Si hay un conflicto, la operación de actualización sobrescribirá la información.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>Atributo MessageDisposition

|**Valor**|**Descripción**|
|:-----|:-----|
|SaveOnly  <br/> |El elemento se actualiza y se guarda de nuevo en su carpeta actual.  <br/> |
|SendOnly  <br/> |El elemento se actualiza y se envía, pero no se guarda ninguna copia.  <br/> |
|SendAndSaveCopy  <br/> |El elemento se actualiza y se guarda una copia en la carpeta identificada por el [elemento SavedItemFolderId.](saveditemfolderid.md)  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>Atributo SendMeetingInvitationsOrCancellations

|**Valor**|**Descripción**|
|:-----|:-----|
|SendToNone  <br/> |El elemento de calendario se actualiza, pero las actualizaciones no se envían a los asistentes.  <br/> |
|SendOnlyToAll  <br/> |El elemento de calendario se actualiza y la actualización de la reunión se envía a todos los asistentes, pero no se guarda en la carpeta Elementos enviados.  <br/> |
|SendOnlyToChanged  <br/> |El elemento de calendario se actualiza y la actualización de la reunión se envía solo a los asistentes que se ven afectados por el cambio en la reunión.  <br/> |
|SendToAllAndSaveCopy  <br/> |El elemento de calendario se actualiza, la actualización de la reunión se envía a todos los asistentes y se guarda una copia en la carpeta Elementos enviados.  <br/> |
|SendToChangedAndSaveCopy  <br/> |El elemento de calendario se actualiza, la actualización de la reunión se envía a todos los asistentes que se ven afectados por el cambio en la reunión y se guarda una copia en la carpeta Elementos enviados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el Exchange almacén.  <br/> |
|[ItemChanges](itemchanges.md) <br/> |Contiene una matriz de [elementos ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se deben aplicar a los elementos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación UpdateItem](updateitem-operation.md)


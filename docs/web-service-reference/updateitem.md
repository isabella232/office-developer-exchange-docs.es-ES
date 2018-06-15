---
title: UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: El elemento UpdateItem define una solicitud para actualizar un elemento en un buzón de correo.
ms.openlocfilehash: 7b9b5f1dcffb95eb127572cb91f92d961c05a77e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19840845"
---
# <a name="updateitem"></a>UpdateItem

El elemento **UpdateItem** define una solicitud para actualizar un elemento en un buzón de correo. 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 **UpdateItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ConflictResolution** <br/> |Identifica el tipo de resolución de conflictos para probar durante una actualización. El valor predeterminado es resolver automáticamente.  <br/> |
|**MessageDisposition** <br/> |Describe cómo se controlarán el elemento después de que se actualice. El atributo **MessageDisposition** es obligatorio para los elementos de mensaje, incluidos los mensajes de reunión como cancelaciones de reunión, convocatorias de reunión y respuestas a la reunión.  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |Describe cómo se comunican las actualizaciones de la reunión después de actualiza un elemento de calendario. Este atributo es necesario para los elementos de calendario y las apariciones del elemento de calendario.  <br/> |
|**SuppressReadReceipts** <br/> |Indica si se deben suprimir confirmaciones de lectura para el elemento actualizado. Un valor de texto de **true** indica que se deben suprimir confirmaciones de lectura. Un valor de **false** indica que se enviarán las confirmaciones de lectura al remitente. Este atributo es opcional.  <br/> Este atributo se introdujo en Exchange Server 2013 SP1.  <br/> |
   
#### <a name="conflictresolution-attribute"></a>Atributo ConflictResolution

|**Valor**|**Descripción**|
|:-----|:-----|
|NeverOverwrite  <br/> |Si hay un conflicto, se produce un error en la operación de actualización y se devuelve un error.  <br/> |
|Resolver automáticamente  <br/> |La operación de actualización resuelve automáticamente cualquier conflicto.  <br/> |
|AlwaysOverwrite  <br/> |Si hay un conflicto, la operación de actualización sobrescribirá información.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>Atributo MessageDisposition

|**Valor**|**Descripción**|
|:-----|:-----|
|SaveOnly  <br/> |El elemento se actualiza y se vuelve a guardar en su carpeta actual.  <br/> |
|SendOnly  <br/> |El elemento se actualiza y se envía, pero ninguna copia se guarda.  <br/> |
|SendAndSaveCopy  <br/> |El elemento se actualiza y se guarda una copia en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>Atributo SendMeetingInvitationsOrCancellations

|**Valor**|**Descripción**|
|:-----|:-----|
|SendToNone  <br/> |El elemento de calendario se actualiza pero no se envían las actualizaciones a los asistentes.  <br/> |
|SendOnlyToAll  <br/> |El elemento de calendario se actualiza y se envía a todos los asistentes de la actualización de la reunión pero no se guarda en la carpeta Elementos enviados.  <br/> |
|SendOnlyToChanged  <br/> |Se actualiza el elemento de calendario y la actualización de la reunión sólo se envía a los asistentes que se ven afectados por el cambio en la reunión.  <br/> |
|SendToAllAndSaveCopy  <br/> |Se actualiza el elemento de calendario, la actualización de la reunión se envía a todos los asistentes y se guarda una copia en la carpeta Elementos enviados.  <br/> |
|SendToChangedAndSaveCopy  <br/> |Se actualiza el elemento de calendario, la actualización de la reunión se envía a todos los asistentes que se ven afectados por el cambio de la reunión y se guarda una copia en la carpeta Elementos enviados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.  <br/> |
|[ItemChanges](itemchanges.md) <br/> |Contiene una matriz de elementos de [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se debe aplicar a los elementos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación UpdateItem](updateitem-operation.md)


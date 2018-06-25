---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: El elemento DeleteItem define una solicitud para eliminar un elemento de un buzón en el almacén de Exchange.
ms.openlocfilehash: de64787750c88c8a47bb69daddc0a1d2ebe8bde9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764106"
---
# <a name="deleteitem"></a>DeleteItem

El elemento **DeleteItem** define una solicitud para eliminar un elemento de un buzón en el almacén de Exchange. 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 **DeleteItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**DeleteType** <br/> |Describe cómo se elimina un elemento. Este atributo es necesario.  <br/> |
|**SendMeetingCancellations** <br/> |Describe si una eliminación del elemento de calendario se comunica a los asistentes. Este atributo es necesario cuando se eliminan los elementos de calendario. Este atributo es opcional si los elementos de calendario no se eliminan.  <br/> |
|**AffectedTaskOccurrences** <br/> |Describe si se elimina una instancia de la tarea o un patrón de tarea por una [operación DeleteItem](deleteitem-operation.md). Este atributo es necesario cuando se eliminan las tareas. Este atributo es opcional cuando se eliminan los elementos de tarea que no sean.  <br/> |
|**SuppressReadReceipts** <br/> |Indica si se suprimen las confirmaciones de lectura para el elemento eliminado. Un valor de texto **es true**, indica que se suprimen las confirmaciones de lectura. Un valor de **false** indica que se envían las confirmaciones de lectura al remitente. Este atributo es opcional.  <br/> |
   
#### <a name="deletetype-attribute"></a>Atributo DeleteType

|**Valor**|**Descripción**|
|:-----|:-----|
|HardDelete  <br/> |Un elemento se quitará permanentemente el almacén.  <br/> |
|SoftDelete  <br/> |Un elemento se mueve al volcado de archivos si el volcado de archivos está habilitado.  <br/> |
|MoveToDeletedItems  <br/> |Un elemento se mueve a la carpeta Elementos eliminados.  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>Atributo SendMeetingCancellations

|**Valor**|**Descripción**|
|:-----|:-----|
|SendToNone  <br/> |Se elimina un elemento de calendario sin enviar un mensaje de cancelación.  <br/> |
|SendOnlyToAll  <br/> |Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes.  <br/> |
|SendToAllAndSaveCopy  <br/> |Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes. En la carpeta Elementos enviados, se guarda una copia del mensaje de cancelación.  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>Atributo AffectedTaskOccurrences

|**Valor**|**Descripción**|
|:-----|:-----|
|AllOccurrences  <br/> |Una solicitud de elemento delete Elimina la tarea principal y, por lo tanto, todas las tareas repetitivas que están asociados con la tarea principal.  <br/> |
|SpecifiedOccurrenceOnly  <br/> |Una solicitud de elemento delete elimina sólo las apariciones específicas de una tarea.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemId](itemids.md) <br/> |Contiene una matriz de elementos, elementos de repetición y periódica maestra para eliminar de un buzón en el almacén de Exchange. La [operación DeleteItem](deleteitem-operation.md) puede realizarse en cualquier tipo de elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las opciones **MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que el tiempo de una llamada al servicio Web completa, la base de datos ha movido el elemento a la carpeta Elementos eliminados o quita permanentemente el elemento de la base de datos de Exchange. Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010. 
  
La opción **SoftDelete** funciona de manera diferente para las versiones de destino diferente de Exchange. **SoftDelete** para Exchange 2007 establece un bit en el elemento que se indica a la base de datos de Exchange que se moverá el elemento para el volcado de archivos carpeta en un momento indeterminado en el futuro. **SoftDelete** para Exchange 2010 mueve inmediatamente el elemento para el volcado de archivos. **SoftDelete** no es una opción de eliminación de la carpeta. **SoftDelete** búsquedas de recorrido de elementos y carpetas no devolverá ningún resultado. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [DeleteItemResponse](deleteitemresponse.md)  
- [Operación DeleteItem](deleteitem-operation.md)


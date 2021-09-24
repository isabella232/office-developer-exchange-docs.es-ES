---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: El elemento DeleteItem define una solicitud para eliminar un elemento de un buzón en el Exchange almacén.
ms.openlocfilehash: aa421de447126a22c1f01b3a0dc7498ff5b74a65
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528890"
---
# <a name="deleteitem"></a>DeleteItem

El **elemento DeleteItem** define una solicitud para eliminar un elemento de un buzón en el Exchange almacén. 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 **DeleteItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**DeleteType** <br/> |Describe cómo se elimina un elemento. Este atributo es obligatorio.  <br/> |
|**SendMeetingCancellations** <br/> |Describe si se comunica una eliminación de elementos de calendario a los asistentes. Este atributo es necesario cuando se eliminan los elementos del calendario. Este atributo es opcional si se eliminan elementos que no son de calendario.  <br/> |
|**AffectedTaskOccurrences** <br/> |Describe si una instancia de tarea o un patrón de tareas se elimina mediante una [operación DeleteItem](deleteitem-operation.md). Este atributo es necesario cuando se eliminan las tareas. Este atributo es opcional cuando se eliminan elementos que no son de tarea.  <br/> |
|**SuppressReadReceipts** <br/> |Indica si se suprimen las confirmaciones de lectura del elemento eliminado. Un valor de texto **de true**, indica que se suprimen las confirmaciones de lectura. Un valor de **false** indica que las confirmaciones de lectura se envían al remitente. Este atributo es opcional.  <br/> |
   
#### <a name="deletetype-attribute"></a>Atributo DeleteType

|**Valor**|**Descripción**|
|:-----|:-----|
|HardDelete  <br/> |Un elemento se quita permanentemente del almacén.  <br/> |
|SoftDelete  <br/> |Un elemento se mueve al contenedor si el contenedor está habilitado.  <br/> |
|MoveToDeletedItems  <br/> |Se mueve un elemento a la carpeta Elementos eliminados.  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>Atributo SendMeetingCancellations

|**Valor**|**Descripción**|
|:-----|:-----|
|SendToNone  <br/> |Un elemento de calendario se elimina sin enviar un mensaje de cancelación.  <br/> |
|SendOnlyToAll  <br/> |Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes.  <br/> |
|SendToAllAndSaveCopy  <br/> |Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes. Se guarda una copia del mensaje de cancelación en la carpeta Elementos enviados.  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>Atributo AffectedTaskOccurrences

|**Valor**|**Descripción**|
|:-----|:-----|
|AllOccurrences  <br/> |Una solicitud de eliminación de elementos elimina la tarea maestra y, por lo tanto, todas las tareas periódicas asociadas a la tarea maestra.  <br/> |
|SpecifiedOccurrenceOnly  <br/> |Una solicitud de eliminación de elementos elimina solo las repeticiones específicas de una tarea.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Contiene una matriz de elementos, elementos de repetición y elementos maestros periódicos que se eliminarán de un buzón del Exchange almacén. La [operación DeleteItem](deleteitem-operation.md) se puede realizar en cualquier tipo de elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las **opciones MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que cuando finaliza una llamada de servicio web, la base de datos ha movido el elemento a la carpeta Elementos eliminados o ha quitado permanentemente el elemento de la base de datos Exchange. Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010. 
  
La **opción SoftDelete** funciona de forma diferente para diferentes versiones de destino de Exchange. **SoftDelete** para Exchange 2007 establece un bit en el elemento que indica a la base de datos de Exchange que el elemento se trasladará a la carpeta del contenedor en un momento indeterminado en el futuro. **SoftDelete** para Exchange 2010 mueve inmediatamente el elemento al contenedor. **SoftDelete** no es una opción para eliminar carpetas. **Las búsquedas** transversales de SoftDelete para elementos y carpetas no devolverán ningún resultado. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [DeleteItemResponse](deleteitemresponse.md)  
- [Operación DeleteItem](deleteitem-operation.md)


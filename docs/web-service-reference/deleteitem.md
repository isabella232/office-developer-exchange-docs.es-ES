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
description: El elemento DeleteItem define una solicitud para eliminar un elemento de un buzón de correo en el almacén de Exchange.
ms.openlocfilehash: ed13ee32b487f49740aed80e8705257d3e2e6938
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529206"
---
# <a name="deleteitem"></a>DeleteItem

El elemento **DeleteItem** define una solicitud para eliminar un elemento de un buzón de correo en el almacén de Exchange. 
  
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
|**SendMeetingCancellations** <br/> |Describe si la eliminación de un elemento de calendario se comunica a los asistentes. Este atributo es necesario cuando se eliminan elementos de calendario. Este atributo es opcional si se eliminan elementos que no son de calendario.  <br/> |
|**AffectedTaskOccurrences** <br/> |Describe si una [operación DeleteItem](deleteitem-operation.md)elimina una instancia de tarea o un patrón de tareas. Este atributo es necesario cuando se eliminan tareas. Este atributo es opcional cuando se eliminan elementos que no son de tarea.  <br/> |
|**SuppressReadReceipts** <br/> |Indica si se suprimen las confirmaciones de lectura del elemento eliminado. Un valor de texto de **true**, indica que se suprimen las confirmaciones de lectura. Un valor de **false** indica que las confirmaciones de lectura se envían al remitente. Este atributo es opcional.  <br/> |
   
#### <a name="deletetype-attribute"></a>Atributo DeleteType

|**Valor**|**Descripción**|
|:-----|:-----|
|HardDelete  <br/> |Un elemento se elimina de forma permanente de la tienda.  <br/> |
|SoftDelete  <br/> |Si el contenedor está habilitado, se mueve un elemento al contenedor.  <br/> |
|MoveToDeletedItems  <br/> |Se mueve un elemento a la carpeta Elementos eliminados.  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>Atributo SendMeetingCancellations

|**Valor**|**Descripción**|
|:-----|:-----|
|SendToNone  <br/> |Se elimina un elemento de calendario sin enviar un mensaje de cancelación.  <br/> |
|SendOnlyToAll  <br/> |Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes.  <br/> |
|SendToAllAndSaveCopy  <br/> |Se elimina un elemento de calendario y se envía un mensaje de cancelación a todos los asistentes. Se guarda una copia del mensaje de cancelación en la carpeta elementos enviados.  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>Atributo AffectedTaskOccurrences

|**Valor**|**Descripción**|
|:-----|:-----|
|AllOccurrences  <br/> |Una solicitud de eliminación de elemento elimina la tarea maestra y, por tanto, todas las tareas periódicas que están asociadas a la tarea maestra.  <br/> |
|SpecifiedOccurrenceOnly  <br/> |Una solicitud de eliminación de elementos elimina solo las ocurrencias específicas de una tarea.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Contiene una matriz de elementos, elementos de ocurrencia y elementos maestros periódicos para eliminarlos de un buzón de correo en el almacén de Exchange. La [operación DeleteItem](deleteitem-operation.md) puede realizarse en cualquier tipo de elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las opciones **MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que cuando se completa una llamada de servicio Web, la base de datos movió el elemento a la carpeta elementos eliminados o quitó permanentemente el elemento de la base de datos de Exchange. Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010. 
  
La opción **SoftDelete** funciona de forma diferente para las distintas versiones de Exchange de destino. **SoftDelete** para Exchange 2007 establece un bit en el elemento que indica a la base de datos de Exchange que el elemento se moverá a la carpeta del contenedor a una hora indeterminada en el futuro. **SoftDelete** para Exchange 2010 inmediatamente mueve el elemento al contenedor. **SoftDelete** no es una opción para la eliminación de carpetas. **SoftDelete** búsquedas transversales de elementos y carpetas no devolverán ningún resultado. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [DeleteItemResponse](deleteitemresponse.md)  
- [Operación DeleteItem](deleteitem-operation.md)


---
title: Update (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: El elemento de actualización identifica un solo elemento que se debe actualizar en el almacén de cliente local.
ms.openlocfilehash: bf560f18184151a3f17d7016d05cdb725db934ae
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353633"
---
# <a name="update-itemsync"></a>Update (ItemSync)

El elemento **Update** identifica un solo elemento que se debe actualizar en el almacén de cliente local. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md)  
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)  
- [Changes (Items)](changes-items.md)  
- [Update (ItemSync)](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

```xml
<Update>
   <MeetingRequest/>
</Update>
```

```xml
<Update>
   <MeetingCancellation/>
</Update>
```

```xml
<Update>
   <Task/>
</Update>
```

```xml
<Update>
   <CalendarItem/>
</Update>
```

```xml
<Update>
   <MeetingResponse/>
</Update>
```

```xml
<Update>
   <Message/>
</Update>
```

```xml
<Update>
   <DistributionList/>
</Update>
```

```xml
<Update>
   <MeetingMessage/>
</Update>
```

```xml
<Update>
   <Contact/> 
</Update>
```

**SyncFolderItemsCreateOrUpdateType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento de Exchange genérico que se debe actualizar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange para actualizar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange para actualizar.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange para actualizar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución que se debe actualizar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión que se debe actualizar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión que se debe actualizar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión que se debe actualizar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión que se debe actualizar.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea que se debe actualizar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Changes (Items)](changes-items.md) <br/> |Contiene una matriz de secuencia de tipos de cambio que representan el tipo de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.  <br/> |
   
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

- [Operación SyncFolderItems](syncfolderitems-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


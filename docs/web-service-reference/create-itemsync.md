---
title: Create (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: cb5e64a2-66a5-4447-921e-7c13efb8f6bf
description: El elemento Create identifica un solo elemento para crear en el almacén de cliente local.
ms.openlocfilehash: d49e54c64f7bd53dcb296d998a856c20570d81be
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353948"
---
# <a name="create-itemsync"></a>Create (ItemSync)

El elemento **Create** identifica un solo elemento para crear en el almacén de cliente local. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) 
- [Changes (Items)](changes-items.md) 
- [Create (ItemSync)](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

```xml
<Create>
   <Task/> 
</Create>
```

```xml
<Create>
   <MeetingResponse/>
</Create>
```

```xml
<Create>
   <CalendarItem/>
</Create>
```

```xml
<Create>
   <MeetingMessage/>
</Create>
```

```xml
<Create>
   <DistributionList/>
</Create>
```

```xml
<Create>
   <MeetingCancellation/>
</Create>
```

```xml
<Create>
   <MeetingRequest/> 
</Create>
```

```xml
<Create>
   <Message/> 
</Create>
```

```xml
<Create>
   <Contact/> 
</Create>
```

**SyncFolderItemsCreateOrUpdateType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento genérico de Exchange para crear.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange para crear.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange para crear.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange para crear.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución para crear.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión para crear.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión para crear.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión para crear.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión para crear.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea a crear.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Changes (Items)](changes-items.md) <br/> |Contiene una matriz de secuencia de tipos de cambios que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.  <br/> |
   
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


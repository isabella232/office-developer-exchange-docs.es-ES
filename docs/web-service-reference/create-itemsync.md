---
title: Crear (ItemSync)
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
description: El elemento Create identifica un solo elemento que se va a crear en el almacén de cliente local.
ms.openlocfilehash: b9c0f28333594a6c17ee9581a227fc4773874fd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460802"
---
# <a name="create-itemsync"></a>Crear (ItemSync)

El elemento **Create** identifica un solo elemento que se va a crear en el almacén de cliente local. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) 
- [Cambios (elementos)](changes-items.md) 
- [Crear (ItemSync)](create-itemsync.md)
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento de Exchange genérico que se va a crear.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange que se va a crear.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange que se va a crear.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange que se va a crear.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución que se va a crear.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión que se va a crear.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión que se va a crear.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión que se va a crear.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión que se va a crear.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea que se va a crear.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Cambios (elementos)](changes-items.md) <br/> |Contiene una matriz de secuencias de tipos de cambio que representan los tipos de diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.  <br/> |
   
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

- [Operación SyncFolderItems](syncfolderitems-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


---
title: ParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 258f4b1f-367e-4c7d-9c29-eb775a2398c7
description: El elemento ParentFolderId representa el identificador de la carpeta principal que contiene el elemento o carpeta.
ms.openlocfilehash: 3bad638aa21019472df8f487f1e065d2e725e750
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465754"
---
# <a name="parentfolderid"></a>ParentFolderId

El elemento **ParentFolderId** representa el identificador de la carpeta principal que contiene el elemento o carpeta. 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

**FolderIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Contiene una cadena que identifica una carpeta en el almacén de Exchange. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Contiene una cadena que identifica una versión de una carpeta identificada por el atributo **ID** . Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario en un buzón.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto en un buzón.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o una carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento en el que se crea un elemento o una carpeta.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento en el que se elimina un elemento o una carpeta.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución privada en un buzón.  <br/> |
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento de Exchange genérico.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un solo elemento que se va a cargar en un buzón.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en un buzón.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en un buzón.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en un buzón.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en un buzón.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico en un buzón.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento en el que se modifica un elemento o una carpeta.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento desencadenado por un nuevo elemento de correo en un buzón.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta de aceptación para una convocatoria de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta provisional a una convocatoria de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de rechazo a una convocatoria de reunión.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento del almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa un elemento de tarea en un buzón.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al creador de un elemento en el almacén de Exchange.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
   
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

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


---
title: Id
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
description: El elemento ID representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.
ms.openlocfilehash: 3f60e8adb62fbf464a58af4169fbcd83910877cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836687"
---
# <a name="parentfolderid"></a>Id

El elemento **ID** representa el identificador de la carpeta primaria que contiene el elemento o la carpeta. 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

**FolderIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Contiene una cadena que identifica una carpeta en el almacén de Exchange. Este atributo es necesario.  <br/> |
|**ChangeKey** <br/> |Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo **Id** . Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta del calendario en un buzón de correo.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario en un buzón de correo.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto en un buzón de correo.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón de correo.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento en el que se crea una carpeta o elemento.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento en el que se elimina un elemento o carpeta.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución privada en un buzón de correo.  <br/> |
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón de correo.  <br/> |
|[Item](item.md) <br/> |Representa un elemento genérico de Exchange.  <br/> |
|[Elemento (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un solo elemento va a cargar en un buzón de correo.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en un buzón de correo.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en un buzón de correo.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en un buzón de correo.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en un buzón de correo.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico en un buzón de correo.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento en el que se modifica una carpeta o elemento.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento que se desencadena por un nuevo elemento de correo en un buzón de correo.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta a Aceptar a una convocatoria de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa un provisional responde a una convocatoria de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de rechazo a una convocatoria de reunión.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento desde el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa un elemento de tarea en un buzón de correo.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta para el creador de un elemento en el almacén de Exchange.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un elemento del almacén de Exchange reenviar a los destinatarios.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón de correo.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón de correo.  <br/> |
   
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

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


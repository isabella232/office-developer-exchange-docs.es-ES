---
title: Asunto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subject
api_type:
- schema
ms.assetid: c140d6c2-deb1-4f67-a908-9397197c4ae7
description: El elemento Subject representa la propiedad Subject de los elementos del almacén de Exchange. El asunto está limitado a 255 caracteres.
ms.openlocfilehash: c4d7c21ab70c21ceb63e53d008d25aebf8e22270
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458974"
---
# <a name="subject"></a>Subject

El elemento **Subject** representa la propiedad Subject de los elementos del almacén de Exchange. El asunto está limitado a 255 caracteres. 
  
```XML
<Subject/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa un objeto de respuesta de elemento de calendario de cancelación.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Especifica los criterios para los tipos de mensajes que se van a buscar.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Representa un objeto de respuesta inteligente de elemento de reenvío.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un correo electrónico en el almacén de Exchange.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contiene un solo mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contiene un único resultado de mensaje para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .  <br/> |
|[RemoveItem](removeitem.md) <br/> |Representa un objeto de respuesta de quitar elemento.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Representa un objeto de respuesta inteligente responder a todos.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Representa un objeto de respuesta inteligente de respuesta a elemento.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se necesita un valor de texto que contenga el asunto de un elemento de Exchange.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


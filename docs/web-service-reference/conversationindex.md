---
title: ConversationIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationIndex
api_type:
- schema
ms.assetid: fdf47e22-8d93-4ae4-883b-0c9f07f48724
description: El elemento ConversationIndex contiene un identificador binario que representa el subproceso al que pertenece el mensaje.
ms.openlocfilehash: 03874c6462be6380e34c999bc2354c376a462882
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461439"
---
# <a name="conversationindex"></a>ConversationIndex

El elemento **ConversationIndex** contiene un identificador binario que representa el subproceso al que pertenece el mensaje. 
  
```xml
<ConversationIndex/>
```

 **Base64Binary**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RemoveItem](removeitem.md) <br/> |Quita un elemento del almacén de Exchange.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta de aceptación para una convocatoria de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta aceptada provisionalmente a una convocatoria de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de rechazo a una convocatoria de reunión.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al creador de un elemento en el almacén de Exchange.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento post en el almacén de Exchange. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un identificador binario en formato **Base64Binary** . 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del servidor de Exchange que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


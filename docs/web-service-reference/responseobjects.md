---
title: ResponseObjects
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseObjects
api_type:
- schema
ms.assetid: ad29e064-3f3d-4b7b-aa4c-9ec27326381d
description: El elemento ResponseObjects contiene una colección de todos los objetos de respuesta asociados con un elemento del Exchange almacén.
ms.openlocfilehash: 65676bba6a78ce4533eb4dabab51106f9799d625
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544804"
---
# <a name="responseobjects"></a>ResponseObjects

El **elemento ResponseObjects** contiene una colección de todos los objetos de respuesta asociados con un elemento del Exchange almacén. 
  
```XML
<ResponseObjects>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <ProposeNewTime>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</ResponseObjects>
```

 **NonEmptyArrayOfResponseObjectsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta Accept a una solicitud de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta provisional a una solicitud de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de declinación a una solicitud de reunión.  <br/> |
|[ProposeNewTime](proposenewtime.md) <br/> |Indica que el asistente a la reunión puede proponer una nueva hora de reunión. Este elemento se introdujo en Microsoft Exchange Server 2013 Service Pack 1 (SP1).  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al creador de un elemento en el Exchange almacén.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un Exchange almacén para reenviar a los destinatarios.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta a todos los destinatarios identificados de un elemento en el Exchange almacén.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta usado para cancelar una reunión.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Contiene una respuesta a un elemento de publicación. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[SuppressReadReceipt](suppressreadreceipt.md) <br/> |Se usa para suprimir las solicitudes de recibo de lectura.  <br/> |
|[AcceptSharingInvitation](acceptsharinginvitation.md) <br/> |Se usa para aceptar una invitación que permite el acceso a los datos de calendario o contactos de otro usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


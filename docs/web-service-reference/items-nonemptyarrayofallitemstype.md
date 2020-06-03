---
title: Elementos (NonEmptyArrayOfAllItemsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: d61ef1cc-ddfc-480a-9625-7b436cb33ae0
description: El elemento items contiene un conjunto de elementos que se van a crear.
ms.openlocfilehash: 0f70f1fe4348b5b74cef6be6414618af1e3de260
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459857"
---
# <a name="items-nonemptyarrayofallitemstype"></a>Elementos (NonEmptyArrayOfAllItemsType)

El elemento **Items** contiene un conjunto de elementos que se van a crear. 
  
```XML
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</Items>
```

 **NonEmptyArrayOfAllItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al remitente de un elemento en el almacén de Exchange.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta al remitente y a todos los destinatarios identificados de un elemento en el almacén de Exchange.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta de aceptación para una convocatoria de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta provisional a una convocatoria de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de rechazo a una convocatoria de reunión.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Representa un objeto Response que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Contiene una respuesta a un elemento post.  <br/> |
|[SuppressReadReceipt](suppressreadreceipt.md) <br/> |Se usa para suprimir las confirmaciones de lectura.  <br/> |
|[AcceptSharingInvitation](acceptsharinginvitation.md) <br/> |Se usa para aceptar una invitación que permite el acceso al calendario o los datos de contactos de otro usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Define la solicitud para crear un elemento en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:`/CreateItem` <br/> |
|[ConversationNode](conversationnode.md) <br/> |Identifica un solo nodo en una conversación.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación CreateFolder](createfolder-operation.md)
  
[Operación CreateItem](createitem-operation.md)


[Creación de carpetas (servicios Web de Exchange)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)


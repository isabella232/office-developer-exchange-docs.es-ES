---
title: Items (NonEmptyArrayOfAllItemsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Items
api_type:
- schema
ms.assetid: d61ef1cc-ddfc-480a-9625-7b436cb33ae0
description: El elemento Items contiene un conjunto de elementos que se crearán.
ms.openlocfilehash: a511fa9e81cdfb4d5c84705edb0d37f75eb76049
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524997"
---
# <a name="items-nonemptyarrayofallitemstype"></a>Items (NonEmptyArrayOfAllItemsType)

El **elemento Items** contiene un conjunto de elementos que se crearán. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al remitente de un elemento en el Exchange almacén.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un Exchange almacén para reenviar a los destinatarios.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta al remitente y a todos los destinatarios identificados de un elemento en el Exchange almacén.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta Accept a una solicitud de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta provisional a una solicitud de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de declinación a una solicitud de reunión.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Contiene una respuesta a un elemento de publicación.  <br/> |
|[SuppressReadReceipt](suppressreadreceipt.md) <br/> |Se usa para suprimir las confirmaciones de lectura.  <br/> |
|[AcceptSharingInvitation](acceptsharinginvitation.md) <br/> |Se usa para aceptar una invitación que permite el acceso a los datos de calendario o contactos de otro usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Define la solicitud para crear un elemento en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/CreateItem` <br/> |
|[ConversationNode](conversationnode.md) <br/> |Identifica un único nodo de una conversación.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateFolder](createfolder-operation.md)
  
[Operación CreateItem](createitem-operation.md)


[Creación de carpetas (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)


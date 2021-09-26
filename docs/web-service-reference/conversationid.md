---
title: ConversationId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConversationId
api_type:
- schema
ms.assetid: d5f1ddb3-9af3-4677-a6ba-111b304a951e
description: El elemento ConversationId contiene el identificador de un elemento o conversación.
ms.openlocfilehash: 345c7c692576abb8c1e1b9848b005ca3d0c0fa0f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547543"
---
# <a name="conversationid"></a>ConversationId

El **elemento ConversationId** contiene el identificador de un elemento o conversación. 
  
```XML
<ConversationId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identifica un elemento específico en el Exchange almacén.  <br/> |
|**ChangeKey** <br/> | Identifica una versión específica de un elemento. Se **requiere un ChangeKey** para los siguientes escenarios:  <br/><br/>- El [elemento UpdateItem](updateitem.md) requiere **una clase ChangeKey** si el atributo **ConflictResolution** está establecido en AutoResolve. AutoResolve es un valor predeterminado. Si no se incluye el atributo **ChangeKey,** la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorChangeKeyRequired**.<br/><br/>- [Los elementos SendItem](senditem.md), [DeleteItem](deleteitem.md)y [DeleteFolder](deletefolder.md) requieren **un ChangeKey** para comprobar si la operación intentada actuará sobre la versión más reciente de un elemento. Si el **atributo ChangeKey** no se incluye en **itemid** o si **la clase ChangeKey** está vacía, la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorStaleObject**.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[ConversationAction](conversationaction.md) <br/> |Representa una sola acción que se aplicará a una sola conversación.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento de publicación en el Exchange almacén.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
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

- [Operación FindConversation](findconversation-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


---
title: HasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasAttachments
api_type:
- schema
ms.assetid: 538b7a85-11d7-4daa-8458-09b540760e8b
description: El elemento HasAttachments representa una propiedad que se establece en true si un elemento tiene al menos un dato adjunto visible o si la conversación contiene al menos un elemento que tiene datos adjuntos. Esta propiedad es de sólo lectura.
ms.openlocfilehash: e76e0ecbb357396540f0d1649cf5062edfb18660
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835801"
---
# <a name="hasattachments"></a>HasAttachments

El elemento **HasAttachments** representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible o si la conversación contiene al menos un elemento que tiene datos adjuntos. Esta propiedad es de sólo lectura. 
  
```XML
<HasAttachments/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla de esa regla.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.  <br/> |
|[Item](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor de tipo Boolean. Un valor de **true** significa que el elemento o la conversación tiene al menos un dato adjunto visible. Un valor de **false** significa que la conversación o el elemento no tiene datos adjuntos o sólo se oculta los datos adjuntos. 
  
## <a name="remarks"></a>Comentarios

La propiedad **HasAttachments** se calcula a partir de la propiedad Boolean MAPI **AllAttachmentsHidden** . Si un elemento no tiene datos adjuntos, la propiedad **AllAttachmentsHidden** no existe. Si se ocultan todos los datos adjuntos en el elemento, la propiedad **AllAttachmentsHidden** es **true**. La propiedad **AllAttachmentsHidden** es **false** si tiene al menos un dato adjunto y al menos uno de los datos adjuntos es visible. Utilice la propiedad **AllAttachmentsHidden** MAPI para realizar búsquedas, agrupar y ordenar los elementos. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
  
[Referencia EWS para Exchange](ews-reference-for-exchange.md)


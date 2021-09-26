---
title: HasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HasAttachments
api_type:
- schema
ms.assetid: 538b7a85-11d7-4daa-8458-09b540760e8b
description: El elemento HasAttachments representa una propiedad establecida en true si un elemento tiene al menos un dato adjunto visible o si una conversación contiene al menos un elemento que tiene datos adjuntos. Esta propiedad es de sólo lectura.
ms.openlocfilehash: dea1ffdc5ae29a0bc7c585e0ebee9ed104143c53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547291"
---
# <a name="hasattachments"></a>HasAttachments

El **elemento HasAttachments** representa una propiedad establecida en **true** si un elemento tiene al menos un dato adjunto visible o si una conversación contiene al menos un elemento que tiene datos adjuntos. Esta propiedad es de sólo lectura. 
  
```XML
<HasAttachments/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla para esa regla.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para la regla bandeja de entrada.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor booleano. Un valor true **significa** que el elemento o la conversación tiene al menos un dato adjunto visible. Un valor de **false** significa que el elemento o la conversación no tiene datos adjuntos o solo tiene datos adjuntos ocultos. 
  
## <a name="remarks"></a>Comentarios

La **propiedad HasAttachments** se calcula a partir de la propiedad BOOLEAN **AllAttachmentsHidden** MAPI. Si un elemento no tiene datos adjuntos, la **propiedad AllAttachmentsHidden** no existe. Si todos los datos adjuntos del elemento están ocultos, la **propiedad AllAttachmentsHidden** es **true**. La **propiedad AllAttachmentsHidden** es **false** si tiene al menos un dato adjunto y al menos uno de los datos adjuntos está visible. Use la **propiedad MAPI AllAttachmentsHidden** para buscar, agrupar y ordenar elementos. 
  
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
  
[Referencia EWS para Exchange](ews-reference-for-exchange.md)


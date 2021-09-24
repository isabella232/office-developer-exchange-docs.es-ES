---
title: Importance
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Importance
api_type:
- schema
ms.assetid: 1557f59a-41f2-43fb-9ded-88f3ec5c76cb
description: El elemento Importance describe la importancia de un elemento o la importancia agregada de todos los elementos de una conversación en la carpeta actual.
ms.openlocfilehash: 38dc05bd08a49d95b7cacd776dde6a07b1a92522
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541143"
---
# <a name="importance"></a>Importance

El **elemento Importance** describe la importancia de un elemento o la importancia agregada de todos los elementos de una conversación en la carpeta actual. 
  
```XML
<Importance/>
```

 **ImportanceChoicesType**
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
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para la regla bandeja de entrada.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Estos son los valores posibles para este elemento:
  
- Bajo
    
- Normal
    
- Alto
    
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


---
title: Importancia
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Importance
api_type:
- schema
ms.assetid: 1557f59a-41f2-43fb-9ded-88f3ec5c76cb
description: El elemento de importancia describe la importancia de un elemento o la importancia agregada de todos los elementos en una conversación en la carpeta actual.
ms.openlocfilehash: 3a58a4da1b26fee0c2aa1d085c3181d7d26f7259
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835891"
---
# <a name="importance"></a>Importancia

El elemento de **importancia** describe la importancia de un elemento o la importancia agregada de todos los elementos en una conversación en la carpeta actual. 
  
```XML
<Importance/>
```

 **ImportanceChoicesType**
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
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.  <br/> |
|[Item](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento desde el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los siguientes son los valores posibles para este elemento:
  
- Low
    
- Importance
    
- High
    
## <a name="remarks"></a>Comentarios

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


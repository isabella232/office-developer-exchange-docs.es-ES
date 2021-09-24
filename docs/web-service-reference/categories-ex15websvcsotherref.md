---
title: Categories
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Categories
api_type:
- schema
ms.assetid: d84d4927-b524-4e62-bf3d-1f12fec8c21a
description: El elemento Categories contiene una colección de cadenas que identifican las categorías a las que pertenece un elemento del buzón.
ms.openlocfilehash: a7d9b42b1ce6a5ec26de76c59c713279c134a15c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518788"
---
# <a name="categories"></a>Categories

El **elemento Categories** contiene una colección de cadenas que identifican las categorías a las que pertenece un elemento del buzón. 
  
```XML
<Categories>
   <String/>
</Categories>
```

 **ArrayOfStringsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[String](string.md) <br/> |Contiene una cadena que identifica una sola categoría.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.  <br/> |
|[ConversationAction](conversationaction.md) <br/> |Contiene una sola acción que se aplicará a una sola conversación.  <br/> |
   
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
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


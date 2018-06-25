---
title: DateTimeCreated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DateTimeCreated
api_type:
- schema
ms.assetid: 42ae0067-4688-49d9-93c5-c4dbeb54cee1
description: El elemento DateTimeCreated representa la fecha y hora en que se creó el elemento en el buzón de correo.
ms.openlocfilehash: 5cfd4e73295bc6823e76d901a21f4745c5fda977
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764037"
---
# <a name="datetimecreated"></a>DateTimeCreated

El elemento **DateTimeCreated** representa la fecha y hora en que se creó el elemento en el buzón de correo. 
  
```xml
<DateTimeCreated/>
```

**DateTime**

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
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Item](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento desde el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la fecha y hora cuando se creó el elemento en el buzón de correo.
  
## <a name="remarks"></a>Comentarios

Uso de objetos de respuesta de calendario actualiza la propiedad [DateTimeCreated](datetimecreated.md) en el elemento de calendario asociado. El comportamiento esperado es para que la propiedad **DateTimeCreated** no se modifican. Por ejemplo, envía el usuario A una reunión de solicitar al usuario B. usuario B acepta la convocatoria de reunión con el identificador de la convocatoria de reunión. Se cambia la propiedad **DateTimeCreated** del elemento de calendario asociado. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


---
title: RecurrenceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: El elemento RecurrenceId se usa para identificar una instancia específica de un elemento de calendario periódico.
ms.openlocfilehash: 863673f7439c12ce4c74e8e0ef4ddea996fb4eb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527567"
---
# <a name="recurrenceid"></a>RecurrenceId

El **elemento RecurrenceId** se usa para identificar una instancia específica de un elemento de calendario periódico. 
  
```xml
<RecurrenceId/>
```

 **dateTime**
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
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un valor de fecha y hora que identifica una aparición de calendario.
  
## <a name="remarks"></a>Comentarios

Esta propiedad se usa con la [propiedad UID](uid.md) para identificar una instancia específica de un elemento de calendario periódico. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


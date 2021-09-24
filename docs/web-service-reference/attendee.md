---
title: Asistente
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: El elemento Attendee representa los asistentes y los recursos de una reunión.
ms.openlocfilehash: d48dcee42292b045ffc7cdcc5fd02f70109b1853
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531197"
---
# <a name="attendee"></a>Asistente

El **elemento Attendee** representa los asistentes y los recursos de una reunión. 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 **AttendeeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica una dirección de correo electrónico totalmente resuelta.  <br/> |
|[ResponseType](responsetype.md) <br/> |Representa el tipo de respuesta de destinatario que se recibe para una reunión. Esta propiedad solo es relevante para el elemento de calendario de un organizador de la reunión.  <br/> |
|[LastResponseTime](lastresponsetime.md) <br/> |Representa la fecha y hora de la respuesta más reciente que se recibe.  <br/> |
|[ProposedStart](proposedstart-attendeetype.md) <br/> |Representa la hora de inicio propuesta por un asistente para una reunión. <br/> |
|[ProposedEnd](proposedend-attendeetype.md) <br/> |Representa la hora de finalización propuesta por un asistente para una reunión. <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RequiredAttendees](requiredattendees.md) <br/> |Representa los asistentes necesarios para asistir a una reunión.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Representa los asistentes que no son necesarios para asistir a una reunión.  <br/> |
|[Recursos](resources.md) <br/> |Representa un recurso programado para una reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


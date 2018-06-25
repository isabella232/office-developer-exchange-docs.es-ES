---
title: ATTENDEE
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: El elemento de Attendee representa los asistentes y los recursos de una reunión.
ms.openlocfilehash: 60cb0839c2f6de69b833c11f4594d40c14cd8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763573"
---
# <a name="attendee"></a>ATTENDEE

El elemento de **Attendee** representa los asistentes y los recursos de una reunión. 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 **AttendeeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Buzón de correo](mailbox.md) <br/> |Identifica una dirección de correo electrónico completa resuelta.  <br/> |
|[ResponseType](responsetype.md) <br/> |Representa el tipo de respuesta de destinatarios que se recibe de una reunión. Esta propiedad sólo es relevante para el elemento de calendario del organizador de una reunión.  <br/> |
|[LastResponseTime](lastresponsetime.md) <br/> |Representa la fecha y hora de la respuesta más reciente que se recibe.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[RequiredAttendees](requiredattendees.md) <br/> |Representa a los asistentes necesarios para asistir a una reunión.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Representa a los asistentes que no sean necesarios para asistir a una reunión.  <br/> |
|[Recursos](resources.md) <br/> |Representa un recurso para una reunión programado.  <br/> |
   
## <a name="remarks"></a>Comentarios

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


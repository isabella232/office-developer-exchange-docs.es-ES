---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: El elemento AttendeeType representa el tipo de asistente que se identifica en el elemento de correo electrónico (EmailAddressType). Este elemento se usa en las solicitudes de sugerencias de reunión.
ms.openlocfilehash: a08532ed78296102ee252c1e0c40beee7ca8ea5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763578"
---
# <a name="attendeetype"></a>AttendeeType

El elemento **AttendeeType** representa el tipo de asistente que se identifica en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) . Este elemento se usa en las solicitudes de sugerencias de reunión. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
- [AttendeeType](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 **MeetingAttendeeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |Representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto es necesario para este elemento. En la siguiente tabla se enumera los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Organizador  <br/> |El usuario del buzón y el asistente que creó el elemento de calendario.  <br/> |
|Obligatorio  <br/> |Un usuario de buzón de correo que sea un asistente necesario a la reunión.  <br/> |
|Opcional  <br/> |Un usuario de buzón de correo que es un asistente opcional para la reunión.  <br/> |
|Salón  <br/> |Una entidad de buzón de correo que representa un recurso de sala utilizado para la reunión.  <br/> |
|Recurso  <br/> |Un recurso, como una TV o proyectores que está programada para su uso en la reunión.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento es un elemento secundario necesario del elemento [MailboxData](mailboxdata.md) . Este elemento sólo puede aparecer una vez en el elemento [MailboxData](mailboxdata.md) . El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
> [!NOTE]
> El tipo de esquema de AttendeeType se usa para representar a los asistentes a un elemento de calendario. No confunda este elemento con elementos del tipo de esquema AttendeeType. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


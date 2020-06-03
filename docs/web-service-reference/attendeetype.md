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
description: El elemento AttendeeType representa el tipo de asistente que se identifica en el elemento email (EmailAddressType). Este elemento se usa en las solicitudes de sugerencias de reunión.
ms.openlocfilehash: 104b9f38cc891310ecb47c0b47837a912ced6ab7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462300"
---
# <a name="attendeetype"></a>AttendeeType

El elemento **AttendeeType** representa el tipo de asistente que se identifica en el elemento [email (EmailAddressType)](email-emailaddresstype.md) . Este elemento se usa en las solicitudes de sugerencias de reunión. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
- [AttendeeType](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 **MeetingAttendeeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |Representa un usuario de buzón individual y opciones para el tipo de datos que se devolverán sobre el usuario del buzón.  <br/> A continuación se encuentra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto para este elemento. En la siguiente tabla se enumeran los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Organizador  <br/> |El usuario del buzón de correo y el asistente que creó el elemento de calendario.  <br/> |
|Obligatorio  <br/> |Un usuario de buzón de correo que es un asistente requerido para la reunión.  <br/> |
|Opcional  <br/> |Un usuario de buzón de correo que es un asistente opcional a la reunión.  <br/> |
|Sala  <br/> |Entidad de buzón de correo que representa un recurso de sala usado para la reunión.  <br/> |
|Resource  <br/> |Un recurso como un televisor o un proyector programados para su uso en la reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es un elemento secundario necesario del elemento [MailboxData](mailboxdata.md) . Este elemento solo puede producirse una vez en el elemento [MailboxData](mailboxdata.md) . El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes. 
  
> [!NOTE]
> El tipo de esquema AttendeeType se usa para representar a los asistentes a un elemento de calendario. No confunda este elemento con los elementos del tipo de esquema AttendeeType. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: El elemento AttendeeType representa el tipo de asistente que se identifica en el elemento Email (EmailAddressType). Este elemento se usa en las solicitudes de sugerencias de reunión.
ms.openlocfilehash: 5bcec50fe6cccc3df48ca9615dbd0d9418211b4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533937"
---
# <a name="attendeetype"></a>AttendeeType

El **elemento AttendeeType** representa el tipo de asistente que se identifica en el [elemento Email (EmailAddressType).](email-emailaddresstype.md) Este elemento se usa en las solicitudes de sugerencias de reunión. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |Representa un usuario de buzón de correo individual y las opciones para el tipo de datos que se devolverán sobre el usuario del buzón.  <br/> A continuación se muestra XPath a este elemento:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto para este elemento. En la tabla siguiente se enumeran los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Organizador  <br/> |El usuario del buzón y el asistente que crearon el elemento de calendario.  <br/> |
|Necesario  <br/> |Un usuario de buzón de correo que es un asistente necesario a la reunión.  <br/> |
|Opcional  <br/> |Un usuario de buzón que es un asistente opcional a la reunión.  <br/> |
|Sala  <br/> |Entidad de buzón que representa un recurso de sala usado para la reunión.  <br/> |
|Recurso  <br/> |Un recurso como un televisor o un proyector que está programado para su uso en la reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es un elemento secundario necesario del [elemento MailboxData.](mailboxdata.md) Este elemento solo puede producirse una vez en el [elemento MailboxData.](mailboxdata.md) El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente. 
  
> [!NOTE]
> El tipo de esquema AttendeeType se usa para representar a los asistentes a un elemento de calendario. No confunda este elemento con elementos del tipo de esquema AttendeeType. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


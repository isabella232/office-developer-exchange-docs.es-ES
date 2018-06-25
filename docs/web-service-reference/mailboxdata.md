---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: El elemento MailboxData representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.
ms.openlocfilehash: df60294e7d83b1459e5cca7d75c2b6b4bb9d931d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836281"
---
# <a name="mailboxdata"></a>MailboxData

El elemento **MailboxData** representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

**MailboxData**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Correo electrónico (EmailAddressType)](email-emailaddresstype.md) <br/> |Representa el usuario del buzón para una consulta GetUserAvailability.  <br/> |
|[AttendeeType](attendeetype.md) <br/> |Representa el tipo de asistente identificado en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) . Se usa en las solicitudes de sugerencias de reunión.  <br/> |
|[ExcludeConflicts](excludeconflicts.md) <br/> |Especifica si se devuelven sugerida veces para tiempos de calendario que entre en conflicto entre los asistentes.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MailboxDataArray](mailboxdataarray.md) <br/> |Contiene una lista de buzones de correo para consultar la información de disponibilidad.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a>Comentarios

Una aplicación cliente puede definir uno a muchos elementos **MailboxData** . 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
## <a name="example"></a>Ejemplo

```xml
<MailboxDataArray>
  <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <Email>
      <Name></Name>
      <Address>someone@ExServer.example.com</Address>
      <RoutingType>SMTP</RoutingType>
    </Email>
    <AttendeeType>Organizer</AttendeeType>
    <ExcludeConflicts>false</ExcludeConflicts>
  </MailboxData>
</MailboxDataArray>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


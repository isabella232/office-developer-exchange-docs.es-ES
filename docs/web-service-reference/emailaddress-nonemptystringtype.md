---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: El elemento EmailAddress define la dirección SMTP principal de un usuario de buzón de correo.
ms.openlocfilehash: fcf2839c1e2e40a22d6b6a856608f52f2c9c2a1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764339"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

El elemento **EmailAddress** define la dirección SMTP principal de un usuario de buzón de correo. 
  
```XML
<EmailAddress/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |Identifique quién envía como el autor de la llamada.  <br/> |
|[Buzón de correo](mailbox.md) <br/> | Identifica una dirección de correo electrónico completa resuelta.  <br/><br/>Las siguientes son algunas expresiones de XPath para este elemento:<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>Los siguientes son elementos de primario adicionales del elemento de buzón de correo:<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [Remitente](sender.md) <br/>- [De](from.md) <br/>- [Organizador](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [Resolución](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [ATTENDEE](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |Identifica una lista de las salas de reuniones por dirección de correo electrónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

El elemento **EmailAddress** puede representar SMTP o distintivos (DN) de Exchange heredado direcciones de nombre (también conocido como DN). El elemento **EmailAddress** es el único elemento necesario de [buzón de correo](mailbox.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   


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
ms.openlocfilehash: fcc3e650d5fc32344022ed6f015d4096a4461f63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463135"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

El elemento **EmailAddress** define la dirección SMTP principal de un usuario de buzón de correo. 
  
```XML
<EmailAddress/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Acciones](actingas.md) <br/> |Identifica quién envía el autor de la llamada.  <br/> |
|[Buzón](mailbox.md) <br/> | Identifica una dirección de correo electrónico completamente resuelta.  <br/><br/>Las siguientes son algunas expresiones XPath de este elemento:<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>Los siguientes son elementos primarios adicionales del elemento Mailbox:<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [Remitente](sender.md) <br/>- [De](from.md) <br/>- [Organizador](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [N](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [Asistente](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |Identifica una lista de salas de reuniones por dirección de correo electrónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se necesita un valor de texto que represente una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

El elemento **EmailAddress** puede representar direcciones SMTP o heredadas de nombres distintivos de Exchange (también conocidos como DN). El elemento **EmailAddress** es el único elemento necesario del [buzón de correo](mailbox.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   


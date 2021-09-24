---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: El elemento EmailAddress define la dirección SMTP principal de un usuario de buzón.
ms.openlocfilehash: 8740f6f7f67269de86aaa7383a7ad8f3cdf07a4a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513005"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

El **elemento EmailAddress** define la dirección SMTP principal de un usuario de buzón. 
  
```XML
<EmailAddress/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |Identifica a quién envía el autor de la llamada.  <br/> |
|[Buzón](mailbox.md) <br/> | Identifica una dirección de correo electrónico totalmente resuelta.  <br/><br/>Las siguientes son algunas expresiones XPath para este elemento:<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>Los siguientes son elementos primarios adicionales del elemento Mailbox:<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [Remitente](sender.md) <br/>- [De](from.md) <br/>- [Organizador](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [Resolución](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [Asistente](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |Identifica una lista de salas de reuniones por dirección de correo electrónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

El **elemento EmailAddress** puede representar SMTP o direcciones Exchange nombre distintivo (también conocido como DN). El **elemento EmailAddress** es el único elemento [Mailbox](mailbox.md) necesario. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   


---
title: Buzón de correo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: El elemento Mailbox identifica un objeto de Active Directory habilitado para correo.
ms.openlocfilehash: 284c3ff6f9fece57611169a4ec41eeaa273c6ad3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468204"
---
# <a name="mailbox"></a>Buzón de correo

El elemento **Mailbox** identifica un objeto de Active Directory habilitado para correo. 
  
```XML
<Mailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Nombre (EmailAddressType)](name-emailaddresstype.md) <br/> |Define el nombre del usuario del buzón de correo. Este elemento es opcional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Define la ruta que se usa para el buzón. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Define el tipo de buzón de un usuario de buzón. Este elemento es opcional.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExpandDL](expanddl.md) <br/> |Define una solicitud para expandir una lista de distribución. <br/> <br/> La siguiente es la expresión XPath a este elemento:` /ExpandDL ` <br/> |
|[ToRecipients](torecipients.md) <br/> |Contiene una matriz de destinatarios de un elemento.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Representa una colección de destinatarios que recibirán una copia del mensaje.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifica una matriz de direcciones de correo electrónico a la que se deben enviar las respuestas.  <br/> |
|[Sender](sender.md) <br/> |Identifica al remitente de un elemento.  <br/> |
|[From](from.md) <br/> |Representa el destinatario del remitente del mensaje.  <br/> |
|[Organizador](organizer.md) <br/> |Representa al organizador de una reunión.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> | Identifica las carpetas predeterminadas de Microsoft Exchange Server 2007.  <br/><br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[Resolución](resolution.md) <br/> |Contiene una única entidad resuelta.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Contiene una matriz de buzones que se encuentran en una lista de distribución.  <br/> |
|[Asistente](attendee.md) <br/> |Representa los asistentes y los recursos de un elemento de calendario.  <br/> |
|[CreateManagedFolder](createmanagedfolder.md) <br/> |Define una solicitud para agregar carpetas administradas a un buzón de correo.  <br/> |
|[AddDelegate](adddelegate.md) <br/> |Define una solicitud para agregar delegados a un buzón.  <br/> |
|[GetDelegate](getdelegate.md) <br/> |Define una solicitud para obtener información acerca de los delegados de un buzón.  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |Define una solicitud para quitar delegados de un buzón.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Define una solicitud para actualizar delegados en un buzón.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Describe el delegado en un escenario de acceso delegado.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Describe la entidad de identidad en un escenario de acceso delegado.  <br/> |
|[Miembro](member-ex15websvcsotherref.md) <br/> |Representa un miembro de una lista de distribución.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los elementos [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) y [Itemid](itemid.md) identifican un buzón o una lista de distribución. 

El elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) identifica un buzón o una lista de distribución por dirección SMTP. 

El elemento [Itemid](itemid.md) identifica un buzón mediante un identificador de elemento, que está asociado a un buzón en particular. 

El elemento [Itemid](itemid.md) no se puede usar para enviar un mensaje a una lista de distribución o un contacto en una carpeta de contactos pública. Se producirá un error si se usa en una operación CreateItem, UpdateItem o SendItem cuando se intenta enviar un mensaje a una lista de distribución o a un contacto en una carpeta pública contactos. Use la operación ExpandDL para obtener la dirección SMTP y, a continuación, envíe el mensaje usando el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en lugar del elemento [Itemid](itemid.md) . 
  
Otro elemento, [Mailbox (Availability)](mailbox-availability.md), proporciona información para las operaciones de disponibilidad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


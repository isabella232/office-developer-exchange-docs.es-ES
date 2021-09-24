---
title: Buzón de correo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: El elemento Mailbox identifica un objeto de Active Directory habilitado para correo.
ms.openlocfilehash: 8065c0472c3b847d538422aa77cd93f75d919a9b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535006"
---
# <a name="mailbox"></a>Buzón de correo

El **elemento Mailbox** identifica un objeto de Active Directory habilitado para correo. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Define el nombre del usuario del buzón. Este elemento es opcional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Define el enrutamiento que se usa para el buzón. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Define el tipo de buzón de correo de un usuario de buzón. Este elemento es opcional.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de una lista de contactos o distribución privada para los destinatarios de la carpeta de contactos de un usuario. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExpandDL](expanddl.md) <br/> |Define una solicitud para expandir una lista de distribución. <br/> <br/> A continuación se muestra la expresión XPath de este elemento: ` /ExpandDL ` <br/> |
|[ToRecipients](torecipients.md) <br/> |Contiene una matriz de destinatarios de un elemento.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Representa una colección de destinatarios que recibirán una copia del mensaje.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Representa una colección de destinatarios para recibir una copia a ciegas (CCO) de un correo electrónico.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifica una matriz de direcciones de correo electrónico a las que se deben enviar respuestas.  <br/> |
|[Sender](sender.md) <br/> |Identifica al remitente de un elemento.  <br/> |
|[From](from.md) <br/> |Representa el destinatario desde el que se envió el mensaje.  <br/> |
|[Organizador](organizer.md) <br/> |Representa el organizador de una reunión.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> | Identifica las carpetas Microsoft Exchange Server 2007 predeterminadas.  <br/><br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[Resolución](resolution.md) <br/> |Contiene una única entidad resuelta.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Contiene una matriz de buzones que se encuentran en una lista de distribución.  <br/> |
|[Attendee](attendee.md) <br/> |Representa los asistentes y los recursos de un elemento de calendario.  <br/> |
|[CreateManagedFolder](createmanagedfolder.md) <br/> |Define una solicitud para agregar carpetas administradas a un buzón.  <br/> |
|[AddDelegate](adddelegate.md) <br/> |Define una solicitud para agregar delegados a un buzón.  <br/> |
|[GetDelegate](getdelegate.md) <br/> |Define una solicitud para obtener información sobre delegados en un buzón.  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |Define una solicitud para quitar delegados de un buzón.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Define una solicitud para actualizar delegados en un buzón.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Describe al delegado en un escenario de acceso delegado.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Describe la entidad de seguridad en un escenario de acceso delegado.  <br/> |
|[Miembro](member-ex15websvcsotherref.md) <br/> |Representa un miembro de una lista de distribución.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los [elementos EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) y [ItemId](itemid.md) identifican un buzón o una lista de distribución. 

El [elemento EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) identifica un buzón o una lista de distribución por dirección SMTP. 

El [elemento ItemId](itemid.md) identifica un buzón mediante un identificador de elemento, que está asociado a un buzón en particular. 

El [elemento ItemId](itemid.md) no se puede usar para enviar un mensaje a una lista de distribución o a un contacto en una carpeta de contactos públicos. Se producirá un error si se usa en una operación CreateItem, UpdateItem o SendItem cuando se intenta enviar un mensaje a una lista de distribución o un contacto en una carpeta pública de contactos. Use la operación ExpandDL para obtener la dirección SMTP y, a continuación, enviar el mensaje mediante el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en lugar del [elemento ItemId.](itemid.md) 
  
Otro elemento, [Mailbox (Availability),](mailbox-availability.md)proporciona información para las operaciones de disponibilidad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


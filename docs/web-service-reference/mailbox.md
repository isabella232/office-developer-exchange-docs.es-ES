---
title: Buz?n de correo
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
description: El elemento de buzón de correo identifica un objeto de Active Directory habilitados para correo.
ms.openlocfilehash: e9fa21f3678249a9ac13d567b88beaf0177f989f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836258"
---
# <a name="mailbox"></a>Buz?n de correo

El elemento de **buzón de correo** identifica un objeto de Active Directory habilitados para correo. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Nombre (EmailAddressType)](name-emailaddresstype.md) <br/> |Define el nombre del usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Define la ruta que se usa para el buzón de correo. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Define el tipo de buzón de correo de un usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ExpandDL](expanddl.md) <br/> |Define una solicitud para expandir una lista de distribución. <br/> <br/> La siguiente es la expresión de XPath para este elemento:` /ExpandDL ` <br/> |
|[ToRecipients](torecipients.md) <br/> |Contiene una matriz de destinatarios de un elemento.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Representa una colección de los destinatarios que recibirán una copia del mensaje.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifica una matriz de direcciones de correo electrónico a la que se deben enviar las respuestas.  <br/> |
|[Sender](sender.md) <br/> |Identifica el remitente de un elemento.  <br/> |
|[From](from.md) <br/> |Representa al destinatario de la que se envió el mensaje.  <br/> |
|[Organizer](organizer.md) <br/> |Representa el organizador de una reunión.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> | Identifica las carpetas predeterminadas de Microsoft Exchange Server 2007.  <br/><br/>  Los siguientes son las expresiones de XPath para este elemento: <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[Resoluci?n](resolution.md) <br/> |Contiene una única entidad resuelta.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Contiene una matriz de los buzones de correo que están contenidos en una lista de distribución.  <br/> |
|[Attendee](attendee.md) <br/> |Representa los asistentes y los recursos para un elemento de calendario.  <br/> |
|[CreateManagedFolder](createmanagedfolder.md) <br/> |Define una solicitud para agregar las carpetas administradas a un buzón de correo.  <br/> |
|[AddDelegate](adddelegate.md) <br/> |Define una solicitud para agregar delegados a un buzón de correo.  <br/> |
|[GetDelegate](getdelegate.md) <br/> |Define una solicitud para obtener información acerca de los delegados a un buzón de correo.  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |Define una solicitud para quitar delegados de un buzón de correo.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Define una solicitud para actualizar los delegados en un buzón de correo.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Describe al delegado en un escenario de acceso delegado.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Describe la entidad de seguridad en un escenario de acceso delegado.  <br/> |
|[Elemento](member-ex15websvcsotherref.md) <br/> |Representa a un miembro de una lista de distribución.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

Los elementos [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) y [ItemId](itemid.md) identifican una buzón de correo o lista de distribución. 

El elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) identifica una buzón de correo o lista de distribución mediante la dirección SMTP. 

El elemento [ItemId](itemid.md) identifica un buzón de correo mediante un identificador de elemento, que está asociado a un buzón determinado. 

El elemento de [ItemId](itemid.md) no puede usarse para enviar un mensaje a una lista de distribución o un contacto en una carpeta pública de contactos. Se producirá un error si se utiliza en una operación CreateItem, UpdateItem o SendItem cuando se realiza un intento para enviar un mensaje a una lista de distribución o un contacto en una carpeta pública de contactos. Use la operación de ExpandDL para obtener la dirección SMTP y, a continuación, envíe el mensaje mediante el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en lugar del elemento [ItemId](itemid.md) . 
  
Otro elemento, [buzón de correo (disponibilidad)](mailbox-availability.md), proporciona información para las operaciones de disponibilidad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


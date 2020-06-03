---
title: Dirección (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: 518641c8-7f6f-496c-86f9-341e7c1bb44c
description: El elemento Address representa una dirección de correo electrónico completamente resuelta.
ms.openlocfilehash: 591bc675165ec80f69407bd8ee19d16c9ddff15a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464906"
---
# <a name="address-emailaddresstype"></a>Dirección (EmailAddressType)

El elemento **Address** representa una dirección de correo electrónico completamente resuelta. 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
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
|[OriginalRecipients](originalrecipients.md) <br/> |Contiene una colección de direcciones de correo electrónico que representan a los destinatarios originales de un mensaje con seguimiento.  <br/> |
|[RoomLists](roomlists.md) <br/> |Contiene una lista de las salas de reuniones de una organización.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Contiene una lista de direcciones de correo electrónico a las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) 
- [Operación GetRoomLists](getroomlists-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


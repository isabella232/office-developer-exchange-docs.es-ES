---
title: Address (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Address
api_type:
- schema
ms.assetid: 518641c8-7f6f-496c-86f9-341e7c1bb44c
description: El elemento Address representa una dirección de correo electrónico totalmente resuelta.
ms.openlocfilehash: ff26a8d6de1e9bf36bb8dff5bc0141974220cf90
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546815"
---
# <a name="address-emailaddresstype"></a>Address (EmailAddressType)

El **elemento Address** representa una dirección de correo electrónico totalmente resuelta. 
  
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
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Define el nombre del usuario del buzón. Este elemento es opcional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Define el enrutamiento que se usa para el buzón. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Define el tipo de buzón de correo de un usuario de buzón. Este elemento es opcional.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de una lista de contactos o distribución privada para los destinatarios de la carpeta Contactos de un usuario. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OriginalRecipients](originalrecipients.md) <br/> |Contiene una colección de direcciones de correo electrónico que representan los destinatarios originales de un mensaje rastreado.  <br/> |
|[RoomLists](roomlists.md) <br/> |Contiene una lista de salas de reuniones de una organización.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Contiene una lista de direcciones de correo electrónico a las que deben enviarse los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) 
- [Operación GetRoomLists](getroomlists-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


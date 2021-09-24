---
title: SendingAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SendingAs
api_type:
- schema
ms.assetid: b43ce19f-9ab0-4946-acb2-c5aafead9d35
description: El elemento SendingAs representa una dirección de correo electrónico que un usuario está intentando enviar como.
ms.openlocfilehash: 6b40b49f80ff995b0b068f2a9bd518f9fda84ba9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517836"
---
# <a name="sendingas"></a>SendingAs

El **elemento SendingAs** representa una dirección de correo electrónico que un usuario está intentando enviar como. 
  
```XML
<SendingAs>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</SendingAs>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Representa el nombre del usuario del buzón. Este elemento es opcional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección principal del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Define el tipo de dirección del buzón. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Representa el tipo de buzón representado por un usuario de correo electrónico. Este elemento es opcional.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de una lista de contactos o distribución privada para los destinatarios de la carpeta Contactos de un usuario. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Contiene los destinatarios y los tipos de sugerencias de correo que se recuperarán.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


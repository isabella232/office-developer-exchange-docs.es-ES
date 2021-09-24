---
title: RoomList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RoomList
api_type:
- schema
ms.assetid: cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2
description: El elemento RoomList representa una dirección de correo electrónico que identifica una lista de salas de reuniones.
ms.openlocfilehash: ae461424b6affbc3dd362d5a7d0a5cc3fdc46fab
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524493"
---
# <a name="roomlist"></a>RoomList

El **elemento RoomList** representa una dirección de correo electrónico que identifica una lista de salas de reuniones. 
  
[GetRooms](getrooms.md)
  
[RoomList](roomlist.md)
  
```XML
<RoomList>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RoomList>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Define el nombre para mostrar de la lista de sala. Este elemento es opcional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección del Protocolo simple de transferencia de correo (SMTP) de una lista de sala. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Define el enrutamiento que se usa para el buzón. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Define el tipo de buzón de correo de un usuario de buzón. Este elemento es opcional.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de una lista de contactos o distribución privada para los destinatarios de la carpeta Contactos de un usuario. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetRooms](getrooms.md) <br/> |Elemento raíz de una solicitud para obtener una lista de salas dentro de una lista de salas determinada.  <br/> |
   
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



[Operación GetRooms](getrooms-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: El elemento MailboxType representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.
ms.openlocfilehash: d7232377951e8d9c8f191ac856058bc28467cadd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836305"
---
# <a name="mailboxtype"></a>MailboxType

El elemento **MailboxType** representa el tipo de buzón de correo que está representada por la dirección de correo electrónico. 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

**MailboxTypeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Buzón de correo](mailbox.md) <br/> |Identifica una dirección de correo electrónico completa resuelta.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifica una lista de las salas de reuniones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **MailboxType** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Buz?n de correo  <br/> |Representa un objeto de Active Directory habilitados para correo.  <br/> |
|PublicDL  <br/> |Representa una lista de distribución públicas.  <br/> |
|PrivateDL  <br/> |Representa una lista de distribución privada en el buzón del usuario.  <br/> |
|Contacto  <br/> |Representa un contacto en el buzón del usuario.  <br/> |
|PublicFolder  <br/> |Representa una carpeta pública.  <br/> |
|Desconocido  <br/> |Representa un tipo desconocido de buzón de correo.  <br/> |
|OneOff  <br/> |Representa a un miembro de uso único de una lista de distribución personal.  <br/> |
|GroupMailbox  <br/> |Representa un buzón de grupo.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


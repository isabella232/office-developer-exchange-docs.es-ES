---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: El elemento MailboxType representa el tipo de buzón representado por la dirección de correo electrónico.
ms.openlocfilehash: f7605bf0e90851352efaaabed09e878be0925581
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524052"
---
# <a name="mailboxtype"></a>MailboxType

El **elemento MailboxType** representa el tipo de buzón representado por la dirección de correo electrónico. 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

**MailboxTypeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica una dirección de correo electrónico totalmente resuelta.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifica una lista de salas de reuniones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores posibles para el **elemento MailboxType.** 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Buzón de correo  <br/> |Representa un objeto de Active Directory habilitado para correo.  <br/> |
|PublicDL  <br/> |Representa una lista de distribución pública.  <br/> |
|PrivateDL  <br/> |Representa una lista de distribución privada en el buzón de un usuario.  <br/> |
|Contacto  <br/> |Representa un contacto en el buzón de un usuario.  <br/> |
|PublicFolder  <br/> |Representa una carpeta pública.  <br/> |
|Unknown  <br/> |Representa un tipo desconocido de buzón.  <br/> |
|OneOff  <br/> |Representa un miembro único de una lista de distribución personal.  <br/> |
|GroupMailbox  <br/> |Representa un buzón de grupo.  <br/> |
   
## <a name="remarks"></a>Comentarios

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


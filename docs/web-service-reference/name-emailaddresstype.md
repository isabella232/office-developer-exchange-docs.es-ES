---
title: Name (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Name
api_type:
- schema
ms.assetid: 98c58c53-9acc-4e89-9fcf-03f1b05abee1
description: El elemento Name representa el nombre de un usuario de buzón.
ms.openlocfilehash: 096b5db4f7bc2de7d1d7355e4e0dba2684bd06d8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515519"
---
# <a name="name-emailaddresstype"></a>Name (EmailAddressType)

El **elemento Name** representa el nombre de un usuario de buzón. 
  
```xml
<Name/>
```

**string**

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

Si se usa este elemento, se requiere un valor de texto que representa una cadena.
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional. El **elemento Name** existe en los tipos **AttachmentType**, **EmailAddressType** y **EmailAddress.** El **elemento Name** del tipo **EmailAddress** se describe en el tema del elemento [Name (EmailAddress).](name-emailaddress.md) 
  
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


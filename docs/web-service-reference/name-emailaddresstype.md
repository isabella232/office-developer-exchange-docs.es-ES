---
title: Nombre (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: 98c58c53-9acc-4e89-9fcf-03f1b05abee1
description: El elemento Name representa el nombre de un usuario de buzón de correo.
ms.openlocfilehash: b140fd46608a04f9aaba17f917cc4171c056dcf2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836504"
---
# <a name="name-emailaddresstype"></a>Nombre (EmailAddressType)

El elemento **Name** representa el nombre de un usuario de buzón de correo. 
  
```xml
<Name/>
```

**string**

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

Si se usa este elemento, es necesario un valor de texto que representa una cadena.
  
## <a name="remarks"></a>Notas

Este elemento es opcional. El elemento **Name** existe en los tipos de **AttachmentType**, **EmailAddressType**y **EmailAddress** . El elemento **nombre** en el tipo de **EmailAddress** se describe en el tema de elemento [nombre (EmailAddress)](name-emailaddress.md) . 
  
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


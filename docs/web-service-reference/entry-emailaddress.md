---
title: Entry (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: El elemento Entry representa una única dirección de correo electrónico para un contacto.
ms.openlocfilehash: 96351a82e113f2c4aa73776e89e1eb7e7a683433
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520671"
---
# <a name="entry-emailaddress"></a>Entry (EmailAddress)

El **elemento Entry** representa una única dirección de correo electrónico para un contacto. 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

**EmailAddressDictionaryEntryType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Clave** <br/> | Identifica la dirección de correo electrónico.<br/><br/>Estos son los valores posibles para este atributo:<br/><br/>- EmailAddress1  <br/>- EmailAddress2  <br/>- EmailAddress3 <br/><br/>  Este atributo es obligatorio.  <br/> |
|**Nombre** <br/> |Define el nombre del usuario del buzón. Este atributo es opcional.  <br/> |
|**RoutingType** <br/> |Define el enrutamiento que se usa para el buzón. El valor predeterminado es SMTP. Este atributo es opcional.  <br/> |
|**MailboxType** <br/> |Define el tipo de buzón de correo de un usuario de buzón. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[EmailAddresses](emailaddresses.md) <br/> |Representa una colección de direcciones de correo electrónico para un contacto.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


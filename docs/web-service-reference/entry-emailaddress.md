---
title: Entrada (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: El elemento entry representa una sola dirección de correo electrónico de un contacto.
ms.openlocfilehash: 766d67cda10b02c07a7677e541fddfc38a4285cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459647"
---
# <a name="entry-emailaddress"></a>Entrada (EmailAddress)

El elemento **entry** representa una sola dirección de correo electrónico de un contacto. 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

**EmailAddressDictionaryEntryType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Key** <br/> | Identifica la dirección de correo electrónico.<br/><br/>A continuación se muestran los valores posibles para este atributo:<br/><br/>- EmailAddress1  <br/>- EmailAddress2  <br/>- EmailAddress3 <br/><br/>  Este atributo es obligatorio.  <br/> |
|**Nombre** <br/> |Define el nombre del usuario del buzón de correo. Este atributo es opcional.  <br/> |
|**RoutingType** <br/> |Define la ruta que se usa para el buzón. El valor predeterminado es SMTP. Este atributo es opcional.  <br/> |
|**MailboxType** <br/> |Define el tipo de buzón de un usuario de buzón. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[EmailAddresses](emailaddresses.md) <br/> |Representa una colección de direcciones de correo electrónico de un contacto.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


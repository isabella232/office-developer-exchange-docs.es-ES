---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: El elemento MailboxSmtpAddress representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada que se va a recuperar o actualizar; o cuya fecha de caducidad de la contraseña se van a recuperar.
ms.openlocfilehash: 60b2c018f2a05e9630e92e28de1054a421b41e52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836303"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

El elemento **MailboxSmtpAddress** representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada que se va a recuperar o actualizar; o cuya fecha de caducidad de la contraseña se van a recuperar. 
  
```XML
<MailboxSmtpAddress/>
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
|[GetInboxRules](getinboxrules.md) <br/> |Define una solicitud para obtener las reglas de bandeja de entrada en un buzón de correo en el almacén del servidor.  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |Define una solicitud para obtener la fecha de caducidad de la contraseña de una cuenta de correo electrónico.  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |Define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El elemento **MailboxSmtpAddress** es un elemento opcional. Si se omite el elemento **MailboxSmtpAddress** , se usa la dirección del usuario que ha iniciado la sesión. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación de GetInboxRules](getinboxrules-operation.md)
- [Operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md)
- [Operación de UpdateInboxRules](updateinboxrules-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


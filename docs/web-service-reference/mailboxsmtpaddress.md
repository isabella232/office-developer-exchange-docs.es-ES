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
description: El elemento MailboxSmtpAddress representa la dirección SMTP del usuario cuyas reglas de la bandeja de entrada se van a recuperar o actualizar; o cuya fecha de expiración de contraseña se va a recuperar.
ms.openlocfilehash: 613e8098210257280bec47f2b22a2d29d04fa07c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530547"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

El elemento **MailboxSmtpAddress** representa la dirección SMTP del usuario cuyas reglas de la bandeja de entrada se van a recuperar o actualizar; o cuya fecha de expiración de contraseña se va a recuperar. 
  
```XML
<MailboxSmtpAddress/>
```

**string**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetInboxRules](getinboxrules.md) <br/> |Define una solicitud para obtener las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |Define una solicitud para obtener la fecha de expiración de la contraseña de una cuenta de correo electrónico.  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |Define una solicitud para actualizar las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El elemento **MailboxSmtpAddress** es un elemento opcional. Si se omite el elemento **MailboxSmtpAddress** , se usa la dirección del usuario que ha iniciado sesión. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación de GetInboxRules](getinboxrules-operation.md)
- [Operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md)
- [Operación de UpdateInboxRules](updateinboxrules-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


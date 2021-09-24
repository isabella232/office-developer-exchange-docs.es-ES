---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: El elemento MailboxSmtpAddress representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada deben recuperarse o actualizarse; o cuya fecha de expiración de contraseña se va a recuperar.
ms.openlocfilehash: 86a39c416b9674e1f48f0a75508c003ad9d620f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511134"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

El **elemento MailboxSmtpAddress** representa la dirección SMTP del usuario cuyas reglas de bandeja de entrada deben recuperarse o actualizarse; o cuya fecha de expiración de contraseña se va a recuperar. 
  
```XML
<MailboxSmtpAddress/>
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
|[GetInboxRules](getinboxrules.md) <br/> |Define una solicitud para obtener las reglas de la Bandeja de entrada en un buzón en el almacén de servidores.  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |Define una solicitud para obtener la fecha de expiración de contraseña de una cuenta de correo electrónico.  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |Define una solicitud para actualizar las reglas de la Bandeja de entrada en un buzón en el almacén del servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El **elemento MailboxSmtpAddress** es un elemento opcional. Si se **omite el elemento MailboxSmtpAddress,** se usa la dirección del usuario que ha iniciado sesión. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación de GetInboxRules](getinboxrules-operation.md)
- [Operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md)
- [Operación de UpdateInboxRules](updateinboxrules-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


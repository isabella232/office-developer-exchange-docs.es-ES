---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: El elemento GetPasswordExpirationDate define una solicitud para obtener la fecha de expiración de contraseña de una cuenta de correo electrónico. Este elemento es el elemento base de la operación GetPasswordExpirationDate.
ms.openlocfilehash: e5c74cc773438780fad0448cd2ae449dae07738f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520517"
---
# <a name="getpasswordexpirationdate"></a>GetPasswordExpirationDate

El **elemento GetPasswordExpirationDate** define una solicitud para obtener la fecha de expiración de contraseña de una cuenta de correo electrónico. Este elemento es el elemento base de la [operación GetPasswordExpirationDate.](getpasswordexpirationdate-operation.md) 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 **GetPasswordExpirationDateType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |Representa la dirección de correo electrónico de la cuenta de correo electrónico para la que se devolverá la fecha de expiración de la contraseña.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


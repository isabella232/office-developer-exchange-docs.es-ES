---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: El elemento GetPasswordExpirationDate define una solicitud para obtener la fecha de caducidad de contraseña para una cuenta de correo electrónico. Este elemento es el elemento base para la operación de la operación de GetPasswordExpirationDate.
ms.openlocfilehash: a9e0955566372f7b99c48c56e62ce2c5025f9f95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764935"
---
# <a name="getpasswordexpirationdate"></a>GetPasswordExpirationDate

El elemento **GetPasswordExpirationDate** define una solicitud para obtener la fecha de caducidad de contraseña para una cuenta de correo electrónico. Este elemento es el elemento base para la operación de la [operación de GetPasswordExpirationDate](getpasswordexpirationdate-operation.md) . 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 **GetPasswordExpirationDateType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |Representa la dirección de correo electrónico de la cuenta de correo electrónico para la que es la fecha de caducidad de contraseña que se va a devolver.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


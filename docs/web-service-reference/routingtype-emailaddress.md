---
title: RoutingType (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: El elemento RoutingType representa el protocolo de enrutamiento del destinatario.
ms.openlocfilehash: cc4d18ff9fa18f0ec2024f15cb6a3bd4199832de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534432"
---
# <a name="routingtype-emailaddress"></a>RoutingType (EmailAddress)

El **elemento RoutingType** representa el protocolo de enrutamiento del destinatario. 
  
```XML
<RoutingType/>
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
|[Email (EmailAddressType)](email-emailaddresstype.md) <br/> |Especifica la dirección de correo electrónico del objeto MailboxData. Este elemento se usa en la [operación GetUserAvailability](getuseravailability-operation.md).  <br/><br/> A continuación se muestra XPath a este elemento:  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Mailbox (Availability)](mailbox-availability.md) <br/> | Representa el usuario del buzón de una solicitud SetUserOofSettings o GetUserOofSettings.  <br/><br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto es opcional. Los valores posibles son los siguientes:

* SMTP
* EX

Si no se proporciona ningún valor, se usa el valor predeterminado de SMTP.
  
## <a name="remarks"></a>Comentarios

Este elemento puede producirse como máximo una vez en el [elemento Email (EmailAddressType).](email-emailaddresstype.md) Este elemento no es necesario. Este elemento existe para la inclusión de protocolos futuros. Otro **elemento RoutingType** se usa para obtener acceso a los elementos del buzón de un usuario. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


---
title: RoutingType (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: El elemento RoutingType representa el protocolo de enrutamiento para el destinatario.
ms.openlocfilehash: a0a6cf312bcb1d4b4818a82bc8d8d3e3f33ad6f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837255"
---
# <a name="routingtype-emailaddress"></a>RoutingType (EmailAddress)

El elemento **RoutingType** representa el protocolo de enrutamiento para el destinatario. 
  
```XML
<RoutingType/>
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
|[Correo electrónico (EmailAddressType)](email-emailaddresstype.md) <br/> |Especifica la dirección de correo electrónico del objeto MailboxData. Este elemento se usa en la [operación GetUserAvailability](getuseravailability-operation.md).  <br/><br/> La siguiente es la expresión de XPath para este elemento:  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Buzón de correo (disponibilidad)](mailbox-availability.md) <br/> | Representa el usuario del buzón para una solicitud SetUserOofSettings o GetUserOofSettings.  <br/><br/>  Los siguientes son las expresiones de XPath para este elemento: <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto es opcional. El único valor válido es SMTP. Si no se proporciona ningún valor, se usa el valor predeterminado de SMTP.
  
## <a name="remarks"></a>Notas

Este elemento puede aparecer como máximo una vez en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) . Este elemento no es necesario. Este elemento existe para la inclusión de protocolos futuros. Otro elemento de **RoutingType** se usa para obtener acceso a los elementos en el buzón del usuario. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


---
title: Address (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: El elemento Address representa la dirección de correo electrónico del usuario del buzón.
ms.openlocfilehash: 839107050f22df5c00cb4dea9c531563df52933d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463646"
---
# <a name="address-string"></a>Address (cadena)

El elemento **Address** representa la dirección de correo electrónico del usuario del buzón. 
  
```xml
<Address>...</Address>
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
|[Correo electrónico (EmailAddressType)](email-emailaddresstype.md) <br/> |Especifica la dirección de correo electrónico del objeto MailboxData. Este elemento se usa en la [operación GetUserAvailability](getuseravailability-operation.md).<br/><br/> A continuación se encuentra la expresión XPath de este elemento:<br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Buzón de correo (disponibilidad)](mailbox-availability.md) <br/> | Representa el usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings.<br/><br/>  Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Valor de texto

Es necesario un valor de texto si se usa este elemento.
  
## <a name="remarks"></a>Comentarios

Este elemento se puede producir al menos una vez en el elemento [email (EmailAddressType)](email-emailaddresstype.md) y en el elemento [Mailbox (Availability)](mailbox-availability.md) . 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Operación GetUserOofSettings](getuseroofsettings-operation.md)
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [GetUserOofSettingsRequest](getuseroofsettingsrequest.md)
- [SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


---
title: Buzón de correo (disponibilidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: El elemento Mailbox representa al usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings.
ms.openlocfilehash: 1bda6e8b90551b86b4e1c2711ac25693a65e5410
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458078"
---
# <a name="mailbox-availability"></a>Buzón de correo (disponibilidad)

El elemento **Mailbox** representa al usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings. 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Nombre (EmailAddress)](name-emailaddress.md) <br/> |Representa el nombre para mostrar del usuario del buzón. Este elemento es opcional en SetUserOofSettingsRequest. GetUserOofSettingsRequest devolverá este elemento.  <br/> |
|[Address (cadena)](address-string.md) <br/> |Representa la dirección de correo electrónico del usuario del buzón. Se requiere este elemento.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Representa el protocolo de enrutamiento para el mensaje. Este elemento es opcional en SetUserOofSettingsRequest. GetUserOofSettingsRequest devolverá este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |Se usa para obtener los mensajes y la configuración de fuera de la oficina (OOF) del usuario de un buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Se usa para establecer los mensajes y la configuración OOF de un usuario de buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Comentarios

La dirección de correo electrónico se usa para identificar la carpeta de calendario que contiene la configuración de OOF. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md)
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)


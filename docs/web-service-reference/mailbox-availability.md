---
title: Mailbox (Availability)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: El elemento Mailbox representa el usuario del buzón de una solicitud SetUserOofSettings o GetUserOofSettings.
ms.openlocfilehash: 5e32c4be807dae92b27df7012caa8eb1b295b26c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522925"
---
# <a name="mailbox-availability"></a>Mailbox (Availability)

El **elemento Mailbox** representa el usuario del buzón de una solicitud SetUserOofSettings o GetUserOofSettings. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Name (EmailAddress)](name-emailaddress.md) <br/> |Representa el nombre para mostrar del usuario del buzón. Este elemento es opcional en SetUserOofSettingsRequest. GetUserOofSettingsRequest devolverá este elemento.  <br/> |
|[Address (cadena)](address-string.md) <br/> |Representa la dirección de correo electrónico del usuario del buzón. Se requiere este elemento.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Representa el protocolo de enrutamiento del mensaje. Este elemento es opcional en SetUserOofSettingsRequest. GetUserOofSettingsRequest devolverá este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |Se usa para obtener la configuración y los mensajes fuera de Office (OOF) de un usuario de buzón de correo.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Se usa para establecer la configuración y los mensajes de OOF de un usuario de buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Comentarios

La dirección de correo electrónico se usa para identificar la carpeta de calendario que contiene la configuración de OOF. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md)
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)


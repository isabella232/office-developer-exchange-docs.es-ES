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
description: El elemento de buzón de correo representa al usuario de buzón de correo para un SetUserOofSettings o solicitar GetUserOofSettings.
ms.openlocfilehash: 2e901ae0df56542f56f247184254294735018468
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836254"
---
# <a name="mailbox-availability"></a>Buzón de correo (disponibilidad)

El elemento de **buzón de correo** representa al usuario de buzón de correo para un SetUserOofSettings o solicitar GetUserOofSettings. 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Nombre (EmailAddress)](name-emailaddress.md) <br/> |Representa el nombre para mostrar del usuario de buzón de correo. Este elemento es opcional en el SetUserOofSettingsRequest. El GetUserOofSettingsRequest devolverá este elemento.  <br/> |
|[Dirección (cadena)](address-string.md) <br/> |Representa la dirección de correo electrónico del usuario de buzón de correo. Se requiere este elemento.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Representa el protocolo de enrutamiento para el mensaje. Este elemento es opcional en el SetUserOofSettingsRequest. El GetUserOofSettingsRequest devolverá este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |Se usa para obtener la configuración de fuera de oficina (OOF) y los mensajes de un usuario de buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Se usa para establecer la configuración de fuera de la oficina y los mensajes de un usuario de buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Notas

La dirección de correo electrónico se usa para identificar la carpeta de calendario que contiene la configuración de fuera de la oficina. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md)
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)


---
title: UserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: El elemento UserConfiguration define un único objeto de configuración de usuario.
ms.openlocfilehash: 1217f5d591570c2d8df49a116b6bf35c243d1e0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468911"
---
# <a name="userconfiguration"></a>UserConfiguration

El elemento **UserConfiguration** define un único objeto de configuración de usuario. 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 **UserConfigurationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. Este elemento debe usarse cuando se crea un objeto de configuración de usuario.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de objeto de configuración de usuario.  <br/> |
|[Diccionario](dictionary.md) <br/> |Define un conjunto de entradas de propiedades de diccionario para un objeto de configuración de usuario.  <br/> |
|[XmlData](xmldata.md) <br/> |Contiene el contenido de la propiedad de datos XML para un objeto de configuración de usuario.  <br/> |
|[BinaryData](binarydata.md) <br/> |Contiene el contenido de la propiedad de datos binarios de un objeto de configuración de usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |Representa una solicitud para crear un objeto de configuración de usuario.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Representa una respuesta que devuelve un objeto de configuración de usuario.  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |Representa una solicitud para actualizar un objeto de configuración de usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


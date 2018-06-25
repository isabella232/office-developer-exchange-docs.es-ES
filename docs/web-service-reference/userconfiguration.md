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
description: El elemento UserConfiguration define un objeto de configuración de usuario único.
ms.openlocfilehash: ce3eaa470ef592c5a8e5a7ef24c377bb2feeca2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840901"
---
# <a name="userconfiguration"></a>UserConfiguration

El elemento **UserConfiguration** define un objeto de configuración de usuario único. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. Este elemento se debe usar al crear un objeto de configuración de usuario.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de objeto de configuración de usuario.  <br/> |
|[Diccionario](dictionary.md) <br/> |Define un conjunto de entradas de diccionario (propiedad) para un objeto de configuración de usuario.  <br/> |
|[Nota](xmldata.md) <br/> |Contiene contenido de propiedad de datos XML para un objeto de configuración de usuario.  <br/> |
|[BinaryData](binarydata.md) <br/> |Contiene el contenido de la propiedad de datos binarios para un objeto de configuración de usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |Representa una solicitud para crear un objeto de configuración de usuario.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Representa una respuesta que devuelve un objeto de configuración de usuario.  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |Representa una solicitud para actualizar un objeto de configuración de usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


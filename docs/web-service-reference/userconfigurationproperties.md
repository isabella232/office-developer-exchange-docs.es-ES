---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: El elemento UserConfigurationProperties especifica los tipos de propiedad para obtener en una operación de GetUserConfiguration.
ms.openlocfilehash: 4f993765bb7c36f28a41a3f2fa7e28698a3f709e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840904"
---
# <a name="userconfigurationproperties"></a>UserConfigurationProperties

El elemento **UserConfigurationProperties** especifica los tipos de propiedad para obtener en una operación de GetUserConfiguration. 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 **UserConfigurationPropertyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Especifica una solicitud para obtener un objeto de configuración de usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **UserConfigurationProperties** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Especifica la propiedad del identificador.  <br/> |
|Dictionary  <br/> |Especifica los tipos de propiedad de diccionario.  <br/> |
|Nota  <br/> |Especifica los tipos de propiedad de datos XML.  <br/> |
|BinaryData  <br/> |Especifica los tipos de datos binarios (propiedad).  <br/> |
|Todos  <br/> |Especifica el identificador, diccionario, datos XML y tipos de datos binarios (propiedad).  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


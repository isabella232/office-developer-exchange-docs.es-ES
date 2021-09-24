---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: El elemento UserConfigurationProperties especifica los tipos de propiedad que se obtienen en una operación GetUserConfiguration.
ms.openlocfilehash: 0aed3ffc680ac881410469fe762349739ba924a1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515008"
---
# <a name="userconfigurationproperties"></a>UserConfigurationProperties

El **elemento UserConfigurationProperties** especifica los tipos de propiedad que se obtienen en una operación GetUserConfiguration. 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 **UserConfigurationPropertyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Especifica una solicitud para obtener un objeto de configuración de usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores posibles para el **elemento UserConfigurationProperties.** 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Especifica la propiedad identifier.  <br/> |
|Dictionary  <br/> |Especifica tipos de propiedades dictionary.  <br/> |
|XmlData  <br/> |Especifica tipos de propiedades de datos XML.  <br/> |
|BinaryData  <br/> |Especifica tipos de propiedades de datos binarios.  <br/> |
|Todo  <br/> |Especifica los tipos de identificador, diccionario, datos XML y propiedades de datos binarios.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


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
description: El elemento UserConfigurationProperties especifica los tipos de propiedad que se van a obtener en una operación GetUserConfiguration.
ms.openlocfilehash: af6bee64516a7410d96ecc7581e8e819f550ddc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466496"
---
# <a name="userconfigurationproperties"></a>UserConfigurationProperties

El elemento **UserConfigurationProperties** especifica los tipos de propiedad que se van a obtener en una operación GetUserConfiguration. 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 **UserConfigurationPropertyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Especifica una solicitud para obtener un objeto de configuración de usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **UserConfigurationProperties** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Especifica la propiedad de identificador.  <br/> |
|Dictionary  <br/> |Especifica los tipos de propiedades de diccionario.  <br/> |
|XmlData  <br/> |Especifica los tipos de propiedades de datos XML.  <br/> |
|BinaryData  <br/> |Especifica los tipos de propiedades de datos binarios.  <br/> |
|Todo  <br/> |Especifica los tipos de propiedad de identificador, diccionario, datos XML y datos binarios.  <br/> |
   
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


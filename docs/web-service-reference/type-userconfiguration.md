---
title: Tipo (UserConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Type
api_type:
- schema
ms.assetid: d09a9621-6950-451a-90dc-920af9cab35c
description: El elemento Type Especifica un tipo de objeto Dictionary.
ms.openlocfilehash: ea196e070279bb809cc2e4c2a51dd2453dd9b331
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458876"
---
# <a name="type-userconfiguration"></a>Tipo (UserConfiguration)

El elemento **Type** especifica un tipo de objeto Dictionary. 
  
```xml
<Type>DateTime or Boolean or Byte or String or Integer32 or UnsignedInteger32 or Integer64 or UnsignedInteger64 or StringArray or ByteArray</Type> 
```

 **UserConfigurationDictionaryObjectTypesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DictionaryKey](dictionarykey.md) <br/> |Especifica la clave de diccionario para una propiedad Dictionary.  <br/> |
|[DictionaryValue](dictionaryvalue.md) <br/> |Especifica el valor de diccionario para una propiedad Dictionary.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **Type** . 
  
**Valores del elemento Type**

|**Valor**|**Descripción**|
|:-----|:-----|
|DateTime  <br/> ||
|Boolean  <br/> ||
|Byte  <br/> ||
|Cadena  <br/> ||
|Integer32  <br/> ||
|UnsignedInteger32  <br/> ||
|Integer64  <br/> ||
|UnsignedInteger64  <br/> ||
|StringArray  <br/> ||
|ByteArray  <br/> ||
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


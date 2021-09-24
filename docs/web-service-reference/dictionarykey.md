---
title: DictionaryKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DictionaryKey
api_type:
- schema
ms.assetid: f331c8ac-f1c7-4248-a570-97701969d5bf
description: El elemento DictionaryKey especifica la clave de diccionario de una propiedad dictionary.
ms.openlocfilehash: feae35d292c212b41394f63c0840ec4d3c3b8800
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519782"
---
# <a name="dictionarykey"></a>DictionaryKey

El **elemento DictionaryKey** especifica la clave de diccionario de una propiedad dictionary. 
  
```xml
<DictionaryKey>
   <Type/>
   <Value/>
</DictionaryKey>
```

 **UserConfigurationDictionaryObjectType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Type (UserConfiguration)](type-userconfiguration.md) <br/> | Especifica un tipo de objeto dictionary.<br/><br/>El tipo puede ser uno de los siguientes valores de cadena:<br/><br/>- DateTime  <br/>- Boolean  <br/>- Byte  <br/>- String  <br/>- Integer32  <br/>- UnsignedInteger32  <br/>- Integer64  <br/>- UnsignedInteger64  <br/>- StringArray  <br/>- ByteArray  <br/> |
|[Value (UserConfiguration)](value-userconfiguration.md) <br/> |Especifica el valor del objeto dictionary como una cadena.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DictionaryEntry](dictionaryentry.md) <br/> |Especifica el contenido de una sola propiedad de entrada de diccionario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


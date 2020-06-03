---
title: DictionaryValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DictionaryValue
api_type:
- schema
ms.assetid: f4089381-826f-4f6a-8c6d-e51b910cbe6d
description: El elemento DictionaryValue especifica el valor de Diccionario de una propiedad Dictionary.
ms.openlocfilehash: 9bad9b8cc7aa80aa071c89a1c22609dc8d44f2b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462146"
---
# <a name="dictionaryvalue"></a>DictionaryValue

El elemento **DictionaryValue** especifica el valor de Diccionario de una propiedad Dictionary. 
  
```xml
<DictionaryValue>
   <Type/>
   <Value/>
</DictionaryValue>
```

 **UserConfigurationDictionaryObjectType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tipo (UserConfiguration)](type-userconfiguration.md) <br/> |Especifica el tipo de objeto Dictionary.  <br/> |
|[Valor (UserConfiguration)](value-userconfiguration.md) <br/> |Especifica el valor del objeto Dictionary como una cadena.  <br/> |
   
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
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


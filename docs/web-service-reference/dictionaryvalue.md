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
description: El elemento DictionaryValue especifica el valor de diccionario para una propiedad de diccionario.
ms.openlocfilehash: 78e4cd7e5d3d8f18276912da56bafb44cda76753
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764160"
---
# <a name="dictionaryvalue"></a>DictionaryValue

El elemento **DictionaryValue** especifica el valor de diccionario para una propiedad de diccionario. 
  
```xml
<DictionaryValue>
   <Type/>
   <Value/>
</DictionaryValue>
```

 **UserConfigurationDictionaryObjectType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Tipo (UserConfiguration)](type-userconfiguration.md) <br/> |Especifica el tipo de objeto de diccionario.  <br/> |
|[Valor (UserConfiguration)](value-userconfiguration.md) <br/> |Especifica el valor del objeto diccionario como una cadena.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DictionaryEntry](dictionaryentry.md) <br/> |Especifica el contenido de una propiedad de entrada único diccionario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


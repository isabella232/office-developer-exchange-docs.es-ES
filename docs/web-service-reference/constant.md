---
title: Constante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: El elemento constante identifica un valor constante en una restricción.
ms.openlocfilehash: 73912bc1981c5d54040f7c4a563ad805916fe721
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763779"
---
# <a name="constant"></a>Constante

El elemento **constante** identifica un valor constante en una restricción. 
  
```xml
<Constant Value="" />
```

 **ConstantValueType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Value** <br/> |Especifica el valor de comparación de la restricción.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Incluye](contains.md) <br/> |Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de cadena en el atributo de **valor** debe ser convertible en el tipo que intenta comparar. Por ejemplo, si se está comparando una propiedad de fecha y hora con respecto a un valor constante, el valor de cadena debe representar un fecha y hora. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


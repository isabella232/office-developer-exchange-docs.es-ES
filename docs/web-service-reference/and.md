---
title: Y
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: El elemento y representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda. Es true si se cumplen todas las expresiones de búsqueda incluidas dentro del elemento y el resultado de la operación AND.
ms.openlocfilehash: d287d57d68aeca7127325dc8fb65fd0190e5b5eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763439"
---
# <a name="and"></a>Y

El elemento **y** representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda. El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 **AndType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Representa la clase base para expresiones dentro de una restricción. Debe haber dos o más expresiones de búsqueda en una operación de And.<br/><br/>  Uno de los siguientes elementos debe ser sustituido para el elemento **SearchExpression** :<ul><li> [Existe](exists.md)</li><li>[Excluye](excludes.md)</li><li>[IsEqualTo](isequalto.md)</li><li>[IsNotEqualTo](isnotequalto.md)</li><li>[IsGreaterThan](isgreaterthan.md)</li><li>[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</li><li>[IsLessThan](islessthan.md)</li><li>[IsLessThanOrEqualTo](islessthanorequalto.md)</li><li>[Incluye](contains.md)</li><li>[No](not.md)</li><li>**And**</li><li>[Or](or.md) </li></ul> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.  <br/> |
|[No](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|**And** <br/> |Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda. El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que se realiza una operación de **OR** lógica en la expresión de búsqueda que contiene. **O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**. **O** debe tener dos o más elementos secundarios.  <br/> |
   
## <a name="remarks"></a>Comentarios

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


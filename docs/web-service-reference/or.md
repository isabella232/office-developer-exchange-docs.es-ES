---
title: O
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: El elemento Or representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene. O bien, devuelve true si cualquiera de sus elementos secundarios devuelven true. O bien, debe tener dos o más elementos secundarios.
ms.openlocfilehash: 46cf031047aeb09e05a385150ab7587968aef345
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836661"
---
# <a name="or"></a>O

El elemento **o** representa una expresión de búsqueda que lleva a cabo una lógica **o** en la expresión de búsqueda que contiene. **O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**. **O** debe tener dos o más elementos secundarios. 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 **OrType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Representa la clase base para expresiones dentro de una restricción. <br/><br/>Uno de los siguientes elementos debe ser sustituido para el elemento **SearchExpression** : <br/> <br/>- [Existe](exists.md) <br/>- [Excluye](excludes.md) <br/>- [IsEqualTo](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [IsGreaterThan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Contiene](contains.md) <br/>- [No](not.md) <br/>- [Y](and.md) <br/>- **O** <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.  <br/> |
|[No](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda. El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .  <br/> |
|**Or** <br/> |Representa una expresión de búsqueda que se realiza una operación de **OR** lógica en la expresión de búsqueda que contiene. **O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**. **O** debe tener dos o más elementos secundarios.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


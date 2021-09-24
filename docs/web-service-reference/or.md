---
title: 'O bien:'
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: El elemento Or representa una expresión de búsqueda que realiza un or lógico en la expresión de búsqueda que contiene. O devolverá true si alguno de sus secundarios devuelve true. O debe tener dos o más hijos.
ms.openlocfilehash: 70cf76d98f019887fea2ed8fe8f082f20fbcde37
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529560"
---
# <a name="or"></a>O bien:

El **elemento Or** representa una expresión de búsqueda que realiza un **or** lógico en la expresión de búsqueda que contiene. **O** devolverá **true si** alguno de sus secundarios devuelve **true**. **O** debe tener dos o más hijos. 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 **OrType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Representa la clase base para las expresiones dentro de una restricción. <br/><br/>Uno de los siguientes elementos debe sustituirse por el **elemento SearchExpression:** <br/> <br/>- [Existe](exists.md) <br/>- [Excluye](excludes.md) <br/>- [IsEqualTo](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [IsGreaterThan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Contiene](contains.md) <br/>- [No](not.md) <br/>- [Y](and.md) <br/>- **O** <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones FindItem/FindFolder y carpeta de búsqueda.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación **BOOLEAN AND** entre dos o más expresiones de búsqueda. El resultado de la **operación AND** es **true** si todas las expresiones de búsqueda contenidas en el **elemento And** son **true**.  <br/> |
|**Or** <br/> |Representa una expresión de búsqueda que realiza una operación **OR** lógica en la expresión de búsqueda que contiene. **O** devolverá **true si** alguno de sus secundarios devuelve **true**. **O** debe tener dos o más hijos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


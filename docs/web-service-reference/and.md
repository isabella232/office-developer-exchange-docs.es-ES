---
title: And
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
description: El elemento and representa una expresión de búsqueda que permite realizar una operación AND booleana entre dos o más expresiones de búsqueda. El resultado de la operación AND es true si todas las expresiones de búsqueda contenidas en el elemento and son true.
ms.openlocfilehash: f5239f19c2b5a931eefa9ff4a9dd8ed9d775bae2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464724"
---
# <a name="and"></a>And

El elemento **and** representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda. El resultado de la operación **and** es **true** si todas las expresiones de búsqueda contenidas en el elemento **and** son **true**.
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 **AndType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Representa la clase base para las expresiones dentro de una restricción. Debe haber dos o más expresiones de búsqueda en una operación and.<br/><br/>  Se debe sustituir uno de los siguientes elementos por el elemento **SearchExpression** :<ul><li> [Exists](exists.md)</li><li>[Excluye](excludes.md)</li><li>[IsEqualTo](isequalto.md)</li><li>[IsNotEqualTo](isnotequalto.md)</li><li>[IsGreaterThan](isgreaterthan.md)</li><li>[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</li><li>[IsLessThan](islessthan.md)</li><li>[IsLessThanOrEqualTo](islessthanorequalto.md)</li><li>[Contains](contains.md)</li><li>[Not](not.md)</li><li>**And**</li><li>[Or](or.md) </li></ul> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|**And** <br/> |Representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda. El resultado de la operación **and** es **true** si todas las expresiones de búsqueda contenidas en el elemento **and** son **true**.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que realiza una operación **or** lógica en la expresión de búsqueda que contiene. **O** devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**. **O** debe tener dos o más elementos secundarios.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


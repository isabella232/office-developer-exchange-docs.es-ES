---
title: SearchExpression
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SearchExpression
api_type:
- schema
ms.assetid: daa179b6-8c7f-4268-a312-c2acc67fa7c3
description: El elemento SearchExpression es un elemento abstracto que representa el elemento sustituido dentro de una restricción. Todas las expresiones de búsqueda derivan de este tipo base. Este elemento no se usa en un documento de instancia XML.
ms.openlocfilehash: e8047d333b36d77bc6823efd6488a15a6d2501a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517856"
---
# <a name="searchexpression"></a>SearchExpression

El **elemento SearchExpression** es un elemento abstracto que representa el elemento sustituido dentro de una restricción. Todas las expresiones de búsqueda derivan de este tipo base. Este elemento no se usa en un documento de instancia XML. 
  
```xml
<SearchExpression/>
```

 **SearchExpressionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones FindItem/FindFolder y carpeta de búsqueda.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación **BOOLEAN AND** entre dos o más expresiones de búsqueda. El resultado de la **operación AND** es **true** si todas las expresiones de búsqueda contenidas en el **elemento And** son **true**.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que realiza una operación **OR** lógica en la expresión de búsqueda que contiene. **O** devolverá **true si** alguno de sus secundarios devuelve **true**. **O** debe tener dos o más hijos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cualquier elemento de filtro que forma parte del grupo de sustitución SearchExpression puede aparecer en lugar del elemento SearchExpression.
  
> [!NOTE]
> Este elemento nunca se producirá directamente en un documento de instancia. 
  
Los siguientes elementos son miembros del grupo de sustitución SearchExpression:
  
- [Exists](exists.md)
    
- [Excluye](excludes.md)
    
- [IsEqualTo](isequalto.md)
    
- [IsNotEqualTo](isnotequalto.md)
    
- [IsGreaterThan](isgreaterthan.md)
    
- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)
    
- [IsLessThan](islessthan.md)
    
- [IsLessThanOrEqualTo](islessthanorequalto.md)
    
- [Contains](contains.md)
    
- [Not](not.md)
    
- [And](and.md)
    
- [Or](or.md)
    
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


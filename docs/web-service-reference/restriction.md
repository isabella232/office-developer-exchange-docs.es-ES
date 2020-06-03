---
title: Restriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: El elemento Restriction representa la restricción o consulta que se usa para filtrar elementos o carpetas en FindItem/FindFolder y operaciones de carpeta de búsqueda.
ms.openlocfilehash: 6037ba15417d67d393ca70f3edf2248749c396e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465292"
---
# <a name="restriction"></a>Restriction

El elemento **Restriction** representa la restricción o consulta que se usa para filtrar elementos o carpetas en FindItem/FindFolder y operaciones de carpeta de búsqueda. 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda.  <br/> |
|[Contains](contains.md) <br/> |Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.  <br/> |
|[Excluye](excludes.md) <br/> |Realiza una máscara bit a bit de las propiedades.  <br/> |
|[Exists](exists.md) <br/> |Representa una expresión de búsqueda que devuelve **true** si la propiedad proporcionada existe en un elemento.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y evalúa en **true** si son iguales.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor que el valor o la propiedad.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor o igual que el valor o la propiedad.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor que el valor o la propiedad.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor o igual que el valor o la propiedad.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si los valores no son los mismos.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que realiza una operación **or** lógica en la expresión de búsqueda que contiene. El elemento **o** devolverá **true** si cualquiera de sus secundarios devuelve **true**.  <br/> |
|[SearchExpression](searchexpression.md) <br/> |Representa el elemento sustituido dentro de una restricción. Este elemento no se usa en un documento de instancia XML.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar las carpetas en un buzón.  <br/> |
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Representa los parámetros que definen una carpeta de búsqueda.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


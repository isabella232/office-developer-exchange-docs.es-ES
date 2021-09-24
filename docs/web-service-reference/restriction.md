---
title: Restriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: El elemento Restriction representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones FindItem/FindFolder y carpeta de búsqueda.
ms.openlocfilehash: 378c2d0ce7911638e5e58346de46759e7fdd87f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540569"
---
# <a name="restriction"></a>Restriction

El **elemento Restriction** representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones FindItem/FindFolder y carpeta de búsqueda. 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación **BOOLEAN AND** entre dos o más expresiones de búsqueda.  <br/> |
|[Contains](contains.md) <br/> |Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.  <br/> |
|[Excluye](excludes.md) <br/> |Realiza una máscara bit a bit de las propiedades.  <br/> |
|[Exists](exists.md) <br/> |Representa una expresión de búsqueda que devuelve **true** si la propiedad proporcionada existe en un elemento.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y se evalúa como **true** si son iguales.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor que el valor o la propiedad.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor o igual que el valor o la propiedad.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor que el valor o la propiedad.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor o igual que el valor o la propiedad.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si los valores no son los mismos.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que realiza una operación **OR** lógica en la expresión de búsqueda que contiene. El **elemento Or** devolverá **true** si alguno de sus elementos secundarios devuelve **true**.  <br/> |
|[SearchExpression](searchexpression.md) <br/> |Representa el elemento sustituido dentro de una restricción. Este elemento no se usa en un documento de instancia XML.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar carpetas de un buzón.  <br/> |
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Representa los parámetros que definen una carpeta de búsqueda.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


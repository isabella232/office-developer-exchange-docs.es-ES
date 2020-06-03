---
title: 'O bien:'
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
description: El elemento or representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene. O devuelve true si cualquiera de sus elementos secundarios devuelve true. O debe tener dos o más elementos secundarios.
ms.openlocfilehash: 9bc676da5bbaad64f11f6717fb487c2e9bcf2d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462482"
---
# <a name="or"></a>O bien:

El elemento **or** representa una expresión de búsqueda que realiza una operación lógica **or** en la expresión de búsqueda que contiene. **O** devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**. **O** debe tener dos o más elementos secundarios. 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 **Obiblioteca**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Representa la clase base para las expresiones dentro de una restricción. <br/><br/>Se debe sustituir uno de los siguientes elementos por el elemento **SearchExpression** : <br/> <br/>- [Existente](exists.md) <br/>- [Excluye](excludes.md) <br/>- [IsEqualTo](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [IsGreaterThan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Contener](contains.md) <br/>- [No](not.md) <br/>- [Y](and.md) <br/>- **O** <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda. El resultado de la operación **and** es **true** si todas las expresiones de búsqueda contenidas en el elemento **and** son **true**.  <br/> |
|**Or** <br/> |Representa una expresión de búsqueda que realiza una operación **or** lógica en la expresión de búsqueda que contiene. **O** devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**. **O** debe tener dos o más elementos secundarios.  <br/> |
   
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


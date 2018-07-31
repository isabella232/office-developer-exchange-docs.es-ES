---
title: IsGreaterThanOrEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsGreaterThanOrEqualTo
api_type:
- schema
ms.assetid: 373cc954-314d-40e2-be03-cc08aefc0d5b
description: El elemento IsGreaterThanOrEqualTo representa una expresión de búsqueda que se compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es mayor que o igual que el segundo.
ms.openlocfilehash: c469f2535ab717e7bc09b6317e01f0f8b3be8170
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354375"
---
# <a name="isgreaterthanorequalto"></a>IsGreaterThanOrEqualTo

El elemento **IsGreaterThanOrEqualTo** representa una expresión de búsqueda que compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor o igual que el segundo. 
  
```xml
<IsGreaterThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <IndexedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

**IsGreaterThanOrEqualToType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.  <br/> |
|[No](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda. El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene. Devuelve true si cualquiera de sus elementos secundarios que devuelva true [o](or.md) . [O](or.md) debe tener dos o más elementos secundarios.  <br/> |
   
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


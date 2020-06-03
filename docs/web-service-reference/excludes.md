---
title: Excluye
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: El elemento Excludes realiza una máscara bit a bit de la propiedad especificada y un valor proporcionado.
ms.openlocfilehash: d5fcd8b86b454aa731bd43974b5b7d674fe76ed6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530617"
---
# <a name="excludes"></a>Excluye

El elemento **Excludes** realiza una máscara bit a bit de la propiedad especificada y un valor proporcionado. 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
   <Bitmask/>
</Excludes>
```

**ExcludesType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI.  <br/> |
|[Máscara](bitmask.md) <br/> |Representa una máscara hexadecimal o decimal que se utilizará durante una operación de restricción de [exclusión](excludes.md) . Si la máscara de la máscara representa un número hexadecimal, debe ir precedida de 0x o 0X. De lo contrario, se considerará un número decimal.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación and booleana entre dos o más expresiones de búsqueda. El resultado de la operación and es **true** si todas las expresiones de búsqueda incluidas en el y son **true**.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene. El elemento [o](or.md) devolverá **true** si cualquiera de sus secundarios devuelve **true**.  <br/> |
   
## <a name="remarks"></a>Comentarios

**Exclude** se resolverá en **true** si una operación and realizada en el siguiente se resuelve en 0: 
  
1. El valor de bit a bit de la propiedad
    
2. El valor de máscara de la propiedad
    
**Exclude** solo se puede aplicar a una propiedad que tiene un valor entero. Si el tipo de propiedad es distinto de un entero, se devuelve un código de error de **ErrorUnsupportedPathForQuery** en la respuesta. 
  
Puede realizar la operación inversa llamando a no (excluye).
  
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


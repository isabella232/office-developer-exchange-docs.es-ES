---
title: Máscara de bits
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: El elemento de máscara de bits representa una máscara de hexadecimal o decimal que se utilizará durante una operación de restricción excluye.
ms.openlocfilehash: 86c8c61f22d8d620a9139280b2a43ed7fec4727d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763633"
---
# <a name="bitmask"></a>Máscara de bits

El elemento de **máscara de bits** representa una máscara de hexadecimal o decimal que se utilizará durante una operación de restricción [excluye](excludes.md) . 
  
```xml
<Bitmask Value="" />
```

**ExcludesValueType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Value** | Representa una máscara de bits hexadecimal o decimal. El valor se representa mediante la siguiente expresión regular:<br/>' ((0 x|0x)[0-9a-fA-f]*)|([0-9] *)'.<br/><br/>Los siguientes son ejemplos de valores hexadecimales para este atributo:<br/>-0x12AF<br/>-0X334AE<br/><br/>Los siguientes son ejemplos de valores decimales para este atributo:<br/>-10<br/>-255<br/>-4562 |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Excluye](excludes.md) <br/> |Realiza una máscara de bit a bit de las propiedades.  <br/> |
   
## <a name="remarks"></a>Notas

Valores hexadecimales deben tener un prefijo de 0 x o 0 X. Si este prefijo no existe, el valor se supone que para ser un número decimal.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


---
title: Máscara
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
description: El elemento de máscara de subred representa una máscara hexadecimal o decimal que se utilizará durante una operación de restricción de exclusión.
ms.openlocfilehash: f05be466d05b13f8f362afb5fc0552653a532475
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458813"
---
# <a name="bitmask"></a>Máscara

El elemento de **máscara** de subred representa una máscara hexadecimal o decimal que se utilizará durante una operación de restricción de [exclusión](excludes.md) . 
  
```xml
<Bitmask Value="" />
```

**ExcludesValueType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Valor** | Representa una máscara de máscara decimal o hexadecimal. El valor se representa mediante la siguiente expresión regular:<br/>`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.<br/><br/>Los siguientes son ejemplos de valores hexadecimales para este atributo:<br/>- 0x12AF<br/>- 0X334AE<br/><br/>Los siguientes son ejemplos de valores decimales para este atributo:<br/>-10<br/>-255<br/>-4562 |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Excluye](excludes.md) <br/> |Realiza una máscara bit a bit de las propiedades.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores hexadecimales deben tener un prefijo de 0x o 0X. Si este prefijo no existe, se supone que el valor es un número decimal.
  
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


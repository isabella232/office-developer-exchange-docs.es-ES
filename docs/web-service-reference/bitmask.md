---
title: Bitmask
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: El elemento Máscara de bits representa una máscara hexadecimal o decimal que se usará durante una operación de restricción Excludes.
ms.openlocfilehash: 83307fc7f5ba328c5d6f7574a8b3be1ea25595f3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543593"
---
# <a name="bitmask"></a>Bitmask

El **elemento Máscara de bits** representa una máscara hexadecimal o decimal que se usará durante una operación de restricción [Excludes.](excludes.md) 
  
```xml
<Bitmask Value="" />
```

**ExcludesValueType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Valor** | Representa una máscara de bits decimal o hexadecimal. El valor se representa mediante la siguiente expresión regular:<br/>`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.<br/><br/>A continuación se muestran ejemplos de valores hexadecimales para este atributo:<br/>- 0x12AF<br/>- 0X334AE<br/><br/>A continuación se muestran ejemplos de valores decimales para este atributo:<br/>- 10<br/>- 255<br/>- 4562 |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Excluye](excludes.md) <br/> |Realiza una máscara bit a bit de las propiedades.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores hexadecimales deben tener un prefijo de 0x o 0X. Si este prefijo no existe, se supone que el valor es un número decimal.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


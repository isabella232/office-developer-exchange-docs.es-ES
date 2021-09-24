---
title: Constante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: El elemento Constant identifica un valor constante en una restricción.
ms.openlocfilehash: 9d727b41d7d18537758eae7f144832b041757d4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511982"
---
# <a name="constant"></a>Constante

El **elemento Constant** identifica un valor constante en una restricción. 
  
```xml
<Constant Value="" />
```

 **ConstantValueType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Valor** <br/> |Especifica el valor que se debe comparar en la restricción.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Contains](contains.md) <br/> |Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Representa una propiedad o un valor constante que se usará al comparar con otra propiedad.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de cadena en **el atributo Value** debe ser coerciible en el tipo con el que está intentando comparar. Por ejemplo, si está comparando una propiedad de fecha y hora con un valor constante, el valor de cadena debe representar una fecha y hora. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


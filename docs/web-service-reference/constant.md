---
title: Constante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: El elemento Constant identifica un valor constante en una restricción.
ms.openlocfilehash: 6cb2eaa4227a8fd0985e8ff5a15d647c3bb1cd6a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461558"
---
# <a name="constant"></a>Constante

El elemento **Constant** identifica un valor constante en una restricción. 
  
```xml
<Constant Value="" />
```

 **ConstantValueType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Valor** <br/> |Especifica el valor que se va a comparar en la restricción.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Contains](contains.md) <br/> |Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Representa una propiedad o un valor constante que se utilizará al comparar con otra propiedad.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de cadena en el atributo **Value** debe ser convertible en el tipo con el que está intentando comparar. Por ejemplo, si se compara una propiedad de fecha y hora con un valor constante, el valor de cadena debe representar una fecha y hora. 
  
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


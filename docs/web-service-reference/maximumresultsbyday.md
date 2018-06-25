---
title: MaximumResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumResultsByDay
api_type:
- schema
ms.assetid: d581a12a-2b8e-4960-ae14-c8c4aa0b1849
description: El elemento MaximumResultsByDay especifica el número de veces que la reunión sugerida por un día devuelto en la respuesta.
ms.openlocfilehash: 69ab4e0b23f85e5b8786ba2dd934850cadc88f0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836381"
---
# <a name="maximumresultsbyday"></a>MaximumResultsByDay

El elemento **MaximumResultsByDay** especifica el número de veces que la reunión sugerida por un día devuelto en la respuesta. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[MaximumResultsByDay](maximumresultsbyday.md)
  
```xml
<MaximumResultsByDay>...</MaximumResultsByDay>
```

**int**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Contiene las opciones para obtener información de la sugerencia de reunión.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa un número entero.
  
## <a name="remarks"></a>Comentarios

Este elemento es necesario si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) . 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


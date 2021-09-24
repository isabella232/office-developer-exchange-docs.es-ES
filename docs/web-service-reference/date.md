---
title: Fecha
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Date
api_type:
- schema
ms.assetid: 2f6bc090-fff4-45b1-8d7e-8fd6e060cce2
description: El elemento Date representa la fecha que contiene las horas de reunión sugeridas.
ms.openlocfilehash: 077420a268d574267cc8ea352b90e581391275b9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524409"
---
# <a name="date"></a>Fecha

El **elemento Date** representa la fecha que contiene las horas de reunión sugeridas. 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md) 
- [SuggestionsResponse](suggestionsresponse.md) 
- [SuggestionDayResultArray](suggestiondayresultarray.md)  
- [SuggestionDayResult](suggestiondayresult.md)  
- [Fecha](date.md)
  
```xml
<Date>...</Date>
```

**dateTime**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SuggestionDayResult](suggestiondayresult.md) <br/> |Representa un solo día que contiene las horas de reunión sugeridas.  <br/><br/>A continuación se muestra la expresión XPath 2.0 para este elemento:<br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Revise las recomendaciones de tipo de datos del esquema de World Wide Web Consortium (W3C) para el formato del tipo de datos primitivo dateTime.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md) 
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


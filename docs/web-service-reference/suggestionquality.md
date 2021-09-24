---
title: SuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SuggestionQuality
api_type:
- schema
ms.assetid: 734f1a58-adda-4830-973e-e84bf7b870d5
description: El elemento SuggestionQuality representa la calidad de la hora de reunión sugerida.
ms.openlocfilehash: 4d8a504e60e8f043bfb120080a89733e78b16b9e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531555"
---
# <a name="suggestionquality"></a>SuggestionQuality

El **elemento SuggestionQuality** representa la calidad de la hora de reunión sugerida. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[Sugerencia](suggestion.md)
  
[SuggestionQuality](suggestionquality.md)
  
```xml
<SuggestionQuality>Excellent or Good or Fair or Poor</SuggestionQuality>
```

 **SuggestionQuality**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Sugerencia](suggestion.md) <br/> |Representa una única sugerencia de hora de reunión.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor **SuggestionQuality.** Los valores posibles son los siguientes: 
  
- **Excelente** 100 por ciento de los usuarios y recursos están disponibles para la hora de reunión sugerida. 
    
- **Bueno** El porcentaje mínimo de usuarios y recursos disponibles es igual o mayor que el valor del [elemento GoodThreshold](goodthreshold.md) más 50. 
    
- **Feria** El porcentaje máximo de usuarios y recursos disponibles para una hora de reunión sugerida es igual al valor del [elemento GoodThreshold](goodthreshold.md) más 50. El valor mínimo para un **tiempo de** reunión de calidad razonable es del 50 por ciento. 
    
- **Pobre** Menos del 50 % de los usuarios y recursos están disponibles para la hora de reunión sugerida. 
    
## <a name="remarks"></a>Comentarios

El **tipo SuggestionQuality** también es el tipo de los elementos [DayQuality](dayquality.md) y [MinimumSuggestionQuality.](minimumsuggestionquality.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


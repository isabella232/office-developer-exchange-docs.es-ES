---
title: MinimumSuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MinimumSuggestionQuality
api_type:
- schema
ms.assetid: 3725cbd4-9bc1-4f7d-8929-b2c68cb46114
description: El elemento MinimumSuggestionQuality define la calidad de las sugerencias de reunión que se devolverán en la respuesta.
ms.openlocfilehash: c1126158f7a521fbefaf34fda906d60dd15c2af4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510935"
---
# <a name="minimumsuggestionquality"></a>MinimumSuggestionQuality

El **elemento MinimumSuggestionQuality** define la calidad de las sugerencias de reunión que se devolverán en la respuesta. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[MinimumSuggestionQuality](minimumsuggestionquality.md)
  
```xml
<MinimumSuggestionQuality>...</MinimumSuggestionQuality>
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
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Contiene las opciones para obtener información sobre sugerencias de reunión.  <br/> A continuación se muestra XPath a este elemento:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la tabla siguiente se enumeran los valores posibles para este elemento:
  
|**Valor**|**Descripción**|
|:-----|:-----|
|**Excelente** <br/> |El 0 % de los asistentes tiene un conflicto con la hora de reunión sugerida.  <br/> |
|**Good** <br/> |El porcentaje que se considera bueno se establece mediante el [elemento GoodThreshold.](goodthreshold.md)  <br/> |
|**Feria** <br/> |El porcentaje que se considera justo se establece mediante el [elemento GoodThreshold.](goodthreshold.md)  <br/> |
|**Deficiente** <br/> |El 50 % o más de los asistentes tienen un conflicto con la hora de reunión sugerida.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es necesario si se usa el elemento [SuggestionsViewOptions.](suggestionsviewoptions.md) 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


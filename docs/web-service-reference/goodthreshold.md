---
title: GoodThreshold
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GoodThreshold
api_type:
- schema
ms.assetid: 68f607f5-7271-46a6-8ffc-91878185a683
description: El elemento GoodThreshold especifica el porcentaje de asistentes que deben tener abierto el período de tiempo para que el período de tiempo se califique como buena hora de reunión sugerida.
ms.openlocfilehash: bec5159b46a350cb01f8d573c68e1925aeb40ac9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533223"
---
# <a name="goodthreshold"></a>GoodThreshold

El **elemento GoodThreshold** especifica el porcentaje de asistentes que deben tener abierto el período de tiempo para que el período de tiempo se califique como buena hora de reunión sugerida. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[GoodThreshold](goodthreshold.md)
  
```xml
<GoodThreshold>...</GoodThreshold>
```

 **int**
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

Se requiere un valor de texto. Los valores enteros esperados están entre 0 y 50.
  
## <a name="remarks"></a>Comentarios

Este elemento es necesario si se usa el elemento [SuggestionsViewOptions.](suggestionsviewoptions.md) El **elemento GoodThreshold** también determina qué reuniones se consideran justos. Es que el porcentaje de asistentes con conflictos es menor que el Umbral bueno y superior al 50 por ciento, el tiempo de reunión sugerido califica como Justo. El umbral bueno más 50 es igual al porcentaje que define el umbral Bueno/Justo. 
  
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


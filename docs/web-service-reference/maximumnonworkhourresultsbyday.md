---
title: MaximumNonWorkHourResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MaximumNonWorkHourResultsByDay
api_type:
- schema
ms.assetid: 9fb7314d-779c-4b1f-9d7c-b5cb092ed134
description: El elemento MaximumNonWorkHourResultsByDay especifica el número de resultados sugeridos para las horas de reunión fuera del horario laboral normal por día.
ms.openlocfilehash: e5fc7be91b8551215d14783d4d7640a722d50968
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511155"
---
# <a name="maximumnonworkhourresultsbyday"></a>MaximumNonWorkHourResultsByDay

El **elemento MaximumNonWorkHourResultsByDay** especifica el número de resultados sugeridos para las horas de reunión fuera del horario laboral normal por día. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md)
  
```xml
<MaximumNonWorkHourResultsByDay>...</MaximumNonWorkHourResultsByDay>
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

Se requiere un valor de texto. El valor de texto representa un número entero.
  
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


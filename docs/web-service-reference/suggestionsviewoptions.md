---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: El elemento SuggestionsViewOptions contiene las opciones para obtener información de la sugerencia de reunión.
ms.openlocfilehash: 09ff317ae0b2ebf1eadc89dc3bb1cf5b3ae19dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840603"
---
# <a name="suggestionsviewoptions"></a>SuggestionsViewOptions

El elemento **SuggestionsViewOptions** contiene las opciones para obtener información de la sugerencia de reunión. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
```xml
<SuggestionsViewOptions>
   <GoodThreshold>...</GoodThreshold>
   <MaximumResultsByDay>...</MaximumResultsByDay>
   <MaximumNonWorkingHourResultsByDay>...</MaximumNonWorkingHourResultsByDay>
   <MeetingDurationInMinutes>...</MeetingDurationInMinutes>
   <MinimumSuggestionQuality>...</MinimumSuggestionQuality>
   <SuggestionIntervalInMinutes>...</SuggestionIntervalInMinutes>
   <DetailedSuggestionsWindow>...</DetailedSuggestionsWindow>
   <CurrentMeetingTime>...</CurrentMeetingTime>
   <GlobalObjectId>...</GlobalObjectId>
</SuggestionsViewOptions>
```

 **SuggestionsViewOptionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[GoodThreshold](goodthreshold.md) <br/> |Especifica el porcentaje de los asistentes que debe tener el período de tiempo abierto para que el período de tiempo calificar como una hora de reunión sugerida buena.  <br/> |
|[MaximumResultsByDay](maximumresultsbyday.md) <br/> |Especifica el número de veces que la reunión sugerida por día devuelto en la respuesta.  <br/> |
|[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md) <br/> |Especifica el número de resultados sugeridos para horas fuera del horario normal de trabajo por día de la reunión.  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |Especifica la longitud de la reunión que sugerir.  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |Especifica la calidad de sugerencias de reunión que se devuelve en la respuesta.  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugerida.  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |Los resultados de tiempo representa la hora de inicio de una reunión que desee actualizar con la reunión sugerida.  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |No se usa este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Contiene los argumentos utilizados para obtener información de disponibilidad del usuario. Esto es un elemento raíz.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>Notas

Este elemento no es necesario y sólo puede aparecer una vez si se usa. Este valor puede ser null si el valor del elemento [FreeBusyViewOptions](freebusyviewoptions.md) no es nulo. 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)


[Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


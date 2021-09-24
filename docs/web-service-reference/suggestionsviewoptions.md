---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: El elemento SuggestionsViewOptions contiene las opciones para obtener información sobre sugerencias de reunión.
ms.openlocfilehash: ba3591b88e581d45c811100a53b0a74e4bb8e010
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522617"
---
# <a name="suggestionsviewoptions"></a>SuggestionsViewOptions

El **elemento SuggestionsViewOptions** contiene las opciones para obtener información sobre sugerencias de reunión. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GoodThreshold](goodthreshold.md) <br/> |Especifica el porcentaje de asistentes que debe tener abierto el período de tiempo para que se califique como una buena hora de reunión sugerida.  <br/> |
|[MaximumResultsByDay](maximumresultsbyday.md) <br/> |Especifica el número de horas de reunión sugeridas por día devueltas en la respuesta.  <br/> |
|[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md) <br/> |Especifica el número de resultados sugeridos para las horas de reunión fuera del horario laboral normal por día.  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |Especifica la duración de la reunión que se va a sugerir.  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |Especifica la calidad de las sugerencias de reunión que se devolverán en la respuesta.  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugeridas.  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |Representa la hora de inicio de una reunión que desea actualizar con los resultados de la hora de reunión sugeridos.  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |Este elemento no se usa.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Contiene los argumentos usados para obtener información de disponibilidad del usuario. Se trata de un elemento raíz.  <br/> A continuación se muestra XPath a este elemento:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento no es necesario y solo puede producirse una vez si se usa. Este valor puede ser null si el valor del [elemento FreeBusyViewOptions](freebusyviewoptions.md) no es null. 
  
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


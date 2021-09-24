---
title: AttendeeConflictDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttendeeConflictDataArray
api_type:
- schema
ms.assetid: 1d758547-28c5-4649-8334-427480c282d6
description: El elemento AttendeeConflictDataArray contiene una matriz de datos de conflicto para los asistentes que se han identificado en la operación GetUserAvailability.
ms.openlocfilehash: 1054fba62c7e0746a13471433d6d619a304ff848
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524367"
---
# <a name="attendeeconflictdataarray"></a>AttendeeConflictDataArray

El **elemento AttendeeConflictDataArray** contiene una matriz de datos de conflicto para los asistentes consultados identificados en la operación [GetUserAvailability](getuseravailability-operation.md).
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
- [SuggestionsResponse](suggestionsresponse.md)
  
- [SuggestionDayResultArray](suggestiondayresultarray.md)
  
- [SuggestionDayResult](suggestiondayresult.md)
  
- [SuggestionArray](suggestionarray.md)
  
- [Sugerencia](suggestion.md)
  
- [AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 **ArrayOfAttendeeConflictData**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UnknownAttendeeConflictData](unknownattendeeconflictdata.md) <br/> |Representa un asistente irresoluble o un asistente que no es un usuario, una lista de distribución o un contacto.  <br/> |
|[IndividualAttendeeConflictData](individualattendeeconflictdata.md) <br/> |Contiene el estado de disponibilidad de un usuario o contacto para una ventana de tiempo que se produce al mismo tiempo que la hora de reunión sugerida identificada en el [elemento Suggestion.](suggestion.md)  <br/> |
|[TooBigGroupAttendeeConflictData](toobiggroupattendeeconflictdata.md) <br/> |Representa un asistente que se resolvió como una lista de distribución demasiado grande para expandirse.  <br/> |
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Contiene información de conflicto agregada sobre el número de usuarios disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Sugerencia](suggestion.md) <br/> |Representa una única sugerencia de hora de reunión.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a>Comentarios

La posición de cada elemento en **attendeeConflictDataArray** corresponde a la posición de los asistentes que se consultan en el [elemento MailboxDataArray.](mailboxdataarray.md) Cada asistente que se consulta debe corresponder a uno de los **elementos secundarios AttendeeConflictDataArray.** Estos elementos representan un único conflicto con la hora de reunión sugerida identificada en el [elemento Suggestion.](suggestion.md) 
  
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


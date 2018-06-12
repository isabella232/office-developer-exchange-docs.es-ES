---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: El elemento GroupAttendeeConflictData contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una distribución de lista para una sugiere el momento de la reunión.
ms.openlocfilehash: 382b4d866c95de98bd444cd6226d71813889d4f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835757"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

El elemento **GroupAttendeeConflictData** contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución un período de tiempo de la reunión sugerida. 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [SuggestionsResponse](suggestionsresponse.md)
- [SuggestionDayResultArray](suggestiondayresultarray.md)
- [SuggestionDayResult](suggestiondayresult.md)
- [SuggestionArray](suggestionarray.md)
- [Sugerencia](suggestion.md)
- [AttendeeConflictDataArray](attendeeconflictdataarray.md)
- [GroupAttendeeConflictData](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

**GroupAttendeeConflictData**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[NumberOfMembers](numberofmembers.md) <br/> |Representa el número de usuarios, recursos y salas en una lista de distribución.  <br/> |
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |Representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida. Este elemento representa a los miembros para los que el estado es **gratuita**.  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |Representa el número de miembros de la lista de distribución que tienen un conflicto con una hora de reunión sugerida. Este elemento representa a los integrantes que tengan un estado **no disponible**, **fuera de la oficina**o **provisional** .  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |Representa el número de miembros del grupo que no tienen datos de disponibilidad publicados que se compara con una hora de reunión sugerida. Este elemento representa los miembros de una lista de distribución que es demasiado grande o los miembros que tienen el estado de **No haber datos** .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |Contiene una matriz de datos en conflicto para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>Notas

El elemento **GroupAttendeeConflictData** está presente en la respuesta cuando un asistente en el [GetUserAvailabilityRequest](getuseravailabilityrequest.md) se resuelve en una lista de distribución. El elemento **GroupAttendeeConflictData** identifica los tres estados para los miembros de una lista de distribución: disponibles, con conflictos, o sin datos. Expansión de la lista de distribución será compatible con un máximo de 100 miembros. Por lo tanto, el elemento de [NumberOfMembers](numberofmembers.md) puede contener un máximo de 100 miembros. Expansión de la lista de distribución es recursiva. Si una lista de distribución contiene una lista de distribución secundaria que se expande la pertenencia primario total a más de 100 miembros, la lista de distribución secundarios no se expandirán y se cuenta como una sola entrada de la cuenta de elementos [NumberOfMembersWithNoData](numberofmemberswithnodata.md) . Si se puede expandir una lista de distribución secundaria y no expandir la pertenencia de primario total a más de 100 miembros, su pertenencia al grupo se expande y se agregan los recuentos de miembros para los elementos secundarios del elemento **GroupAttendeeConflictData** . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


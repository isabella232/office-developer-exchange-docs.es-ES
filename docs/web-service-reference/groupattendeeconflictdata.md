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
description: El elemento GroupAttendeeConflictData contiene información sobre conflictos de agregación sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida.
ms.openlocfilehash: c75a4e6f8fdff7fb2514f448350fee9f1acb9775
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462932"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

El elemento **GroupAttendeeConflictData** contiene información sobre conflictos de agregación sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución para una hora de reunión sugerida. 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [SuggestionsResponse](suggestionsresponse.md)
- [SuggestionDayResultArray](suggestiondayresultarray.md)
- [SuggestionDayResult](suggestiondayresult.md)
- [SuggestionArray](suggestionarray.md)
- [Alguna](suggestion.md)
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[NumberOfMembers](numberofmembers.md) <br/> |Representa el número de usuarios, recursos y salas de una lista de distribución.  <br/> |
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |Representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida. Este elemento representa los miembros para los que el estado es **libre**.  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |Representa el número de miembros de la lista de distribución que tienen un conflicto con la hora de reunión sugerida. Este elemento representa los miembros que tienen un estado **ocupado**, **OOF**o **provisional** .  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |Representa el número de miembros del grupo que no han publicado datos de disponibilidad para compararlos con una hora de reunión sugerida. Este elemento representa los miembros de una lista de distribución que son demasiado grandes o miembros que no tienen el estado de los **datos** .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |Contiene una matriz de datos conflictivos para los asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **GroupAttendeeConflictData** está presente en la respuesta cuando un asistente de la [GetUserAvailabilityRequest](getuseravailabilityrequest.md) se resuelve en una lista de distribución. El elemento **GroupAttendeeConflictData** identifica tres Estados para los miembros de una lista de distribución: available, conflicted o no Data. La expansión de la lista de distribución admitirá hasta 100 miembros. Por lo tanto, el elemento [NumberOfMembers](numberofmembers.md) puede contener un máximo de 100 miembros. La expansión de la lista de distribución es recurrente. Si una lista de distribución contiene una lista de distribución secundaria que expande el total de la pertenencia a 100 miembros, la lista de distribución secundaria no se expandirá y se contará como una entrada única del recuento de elementos [NumberOfMembersWithNoData](numberofmemberswithnodata.md) . Si se puede expandir una lista de distribución secundaria y la pertenencia al elemento primario total no se expande a más de 100 miembros, se expande su pertenencia y los recuentos de miembros se agregan a los elementos secundarios del elemento **GroupAttendeeConflictData** . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


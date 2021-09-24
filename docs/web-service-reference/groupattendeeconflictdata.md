---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: El elemento GroupAttendeeConflictData contiene información de conflicto agregada sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución durante una hora de reunión sugerida.
ms.openlocfilehash: 19ac366da5ad48cbc6c9e2aaa710a8c5f00e1151
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519558"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

El **elemento GroupAttendeeConflictData** contiene información de conflicto agregada sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución durante una hora de reunión sugerida. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[NumberOfMembers](numberofmembers.md) <br/> |Representa el número de usuarios, recursos y salas de una lista de distribución.  <br/> |
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |Representa el número de miembros de la lista de distribución que están disponibles para una hora de reunión sugerida. Este elemento representa los miembros para los que el estado es **Free**.  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |Representa el número de miembros de la lista de distribución que tienen un conflicto con una hora de reunión sugerida. Este elemento representa los miembros que tienen un **estado Ocupado,** **OOF** o **Provisional.**  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |Representa el número de miembros del grupo que no han publicado datos de disponibilidad para compararlos con una hora de reunión sugerida. Este elemento representa los miembros de una lista de distribución que es demasiado grande o los miembros que **tienen el estado Sin** datos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |Contiene una matriz de datos de conflicto para asistentes consultados identificados en la [operación GetUserAvailability](getuseravailability-operation.md).  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento GroupAttendeeConflictData** está presente en la respuesta cuando un asistente de [GetUserAvailabilityRequest](getuseravailabilityrequest.md) se resuelve en una lista de distribución. El **elemento GroupAttendeeConflictData** identifica tres estados para los miembros de una lista de distribución: disponible, en conflicto o sin datos. La expansión de listas de distribución admitirá hasta 100 miembros. Por lo tanto, [el elemento NumberOfMembers](numberofmembers.md) puede contener un máximo de 100 miembros. La expansión de la lista de distribución es recursiva. Si una lista de distribución contiene una lista de distribución secundaria que expande la pertenencia principal total a más de 100 miembros, la lista de distribución secundaria no se expandirá y contará como una sola entrada del recuento de elementos [NumberOfMembersWithNoData.](numberofmemberswithnodata.md) Si se puede expandir una lista de distribución secundaria y la pertenencia principal total no se expande a más de 100 miembros, su pertenencia se expande y los recuentos de miembros se agregan a los elementos secundarios del elemento **GroupAttendeeConflictData.** 
  
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


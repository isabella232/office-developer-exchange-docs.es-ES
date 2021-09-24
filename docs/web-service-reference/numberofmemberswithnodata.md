---
title: NumberOfMembersWithNoData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- NumberOfMembersWithNoData
api_type:
- schema
ms.assetid: 7ca9c57c-9519-442c-a9f4-dca2b0309716
description: El elemento NumberOfMembersWithNoData representa el número de miembros de la lista de distribución que no han publicado datos de disponibilidad para comparar con una hora de reunión sugerida. Este elemento representa los miembros de una lista de distribución que es demasiado grande o los miembros que tienen el estado Sin datos.
ms.openlocfilehash: 4b021ce75a84eca3e1b5a66cf51f6b5d7adec86b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529688"
---
# <a name="numberofmemberswithnodata"></a>NumberOfMembersWithNoData

El **elemento NumberOfMembersWithNoData** representa el número de miembros de la lista de distribución que no han publicado datos de disponibilidad para comparar con una hora de reunión sugerida. Este elemento representa los miembros de una lista de distribución que es demasiado grande o los miembros que **tienen el estado Sin** datos. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[Sugerencia](suggestion.md)
  
[AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
[GroupAttendeeConflictData](groupattendeeconflictdata.md)
  
[NumberOfMembersWithNoData](numberofmemberswithnodata.md)
  
```xml
<NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
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
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Contiene información de conflicto agregado sobre el número de usuarios que están disponibles, el número de usuarios que tienen conflictos y el número de usuarios que no tienen información de disponibilidad en una lista de distribución durante una hora de reunión sugerida.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a>Comentarios

Un contacto de un grupo que no tiene un buzón es un ejemplo de un miembro de la lista de distribución que no tiene datos de calendario. Un contacto también puede tener **el estado Sin** datos por los siguientes motivos: 
  
- Los permisos son insuficientes.
    
- La lista de distribución es demasiado grande para expandirse.
    
- El servicio de directorio de Active Directory no está disponible.
    
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


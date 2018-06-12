---
title: Hora de finalización
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: El elemento EndTime representa el final de un intervalo de tiempo.
ms.openlocfilehash: 7d3d186618a7bcc05ad82532e13e03d2e67a0e40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764428"
---
# <a name="endtime"></a>Hora de finalización

El elemento **EndTime** representa el final de un intervalo de tiempo. 
  
```xml
<EndTime>dateTime</EndTime>
```

 **dateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Ventana de tiempo](timewindow.md) <br/> |Identifica el intervalo de tiempo de consulta para la información de disponibilidad del usuario.<br/><br/> La siguiente es la expresión de XPath para este elemento:<br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugerida.<br/><br/> La siguiente es la expresión de XPath para este elemento:<br/><br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.  <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> | Especifica la duración para la que está habilitado el estado de fuera de oficina (OOF) si el elemento [OofState](oofstate.md) está establecido en **programado**.  <br/><br/>  Los siguientes son las expresiones de XPath posibles para este elemento:<br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[Repetición](occurrence.md) <br/> |Representa una sola aparición de modificación de un elemento periódico del calendario.  <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Representa una repetición del elemento de calendario único. Se utiliza para las consultas de disponibilidad. El elemento **EndTime** es necesario en el elemento **CalendarEvent** . El elemento **EndTime** en el elemento **CalendarEvent** es único para el tipo de **CalendarEvent** .<br/><br/> La siguiente es la expresión de XPath para este elemento:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto.
  
## <a name="remarks"></a>Notas

El elemento [StartTime](starttime.md) representa el principio de un intervalo de tiempo. 
  
La hora de finalización representa la hora del cliente.
  
El esquema incluye muchos elementos [EndTime](endtime.md) . 
  
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

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


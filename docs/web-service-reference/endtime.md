---
title: EndTime
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
ms.openlocfilehash: 5a30b32ecfeafe582cd07dd662aacb0a960257c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462995"
---
# <a name="endtime"></a>EndTime

El elemento **EndTime** representa el final de un intervalo de tiempo. 
  
```xml
<EndTime>dateTime</EndTime>
```

 **dateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TimeWindow](timewindow.md) <br/> |Identifica el intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.<br/><br/> La siguiente es la expresión XPath a este elemento:<br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para obtener información detallada sobre las horas de reunión sugeridas.<br/><br/> La siguiente es la expresión XPath a este elemento:<br/><br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.  <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> | Especifica el tiempo durante el que se habilita el estado fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**.  <br/><br/>  Las siguientes son las posibles expresiones de XPath a este elemento:<br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[Suceda](occurrence.md) <br/> |Representa una ocurrencia única modificada de un elemento de calendario periódico.  <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Representa una ocurrencia única del elemento de calendario. Se usa para las consultas de disponibilidad. El elemento **EndTime** es obligatorio en el elemento **CalendarEvent** . El elemento **EndTime** del elemento **CalendarEvent** es único para el tipo **CalendarEvent** .<br/><br/> La siguiente es la expresión XPath a este elemento:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto.
  
## <a name="remarks"></a>Comentarios

El elemento [startTime](starttime.md) representa el principio de un intervalo de tiempo. 
  
La hora de finalización representa la hora del cliente.
  
El esquema incluye varios elementos [EndTime](endtime.md) . 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


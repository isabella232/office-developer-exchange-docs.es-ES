---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: El elemento StartTime representa el inicio de un intervalo de tiempo.
ms.openlocfilehash: 16bee698b65dc512a709e2af9ddfe8629347fee3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458568"
---
# <a name="starttime"></a>StartTime

El elemento **startTime** representa el inicio de un intervalo de tiempo. 
  
```xml
<StartTime/
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
|[TimeWindow](timewindow.md) <br/> |Identifica el intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.  <br/><br/> La siguiente es la expresión XPath a este elemento:  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para obtener información detallada sobre las horas de reunión sugeridas.  <br/><br/> La siguiente es la expresión XPath a este elemento: <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> | Especifica el tiempo durante el que se habilita el estado fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**.  <br/><br/>  Las siguientes son las posibles expresiones de XPath a este elemento: <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Representa una ocurrencia única del elemento de calendario. Se usa para las consultas de disponibilidad. El elemento **startTime** es obligatorio en el elemento **CalendarEvent** . El elemento **startTime** del elemento **CalendarEvent** es único para el tipo **CalendarEvent** , aunque contiene los mismos valores de faceta que los elementos **startTime** en el tipo de **duración** .  <br/><br/> La siguiente es la expresión XPath a este elemento:  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto.
  
## <a name="remarks"></a>Comentarios

El elemento [EndTime](endtime.md) representa el final del intervalo de tiempo. 
  
El esquema incluye muchos elementos [startTime](starttime.md) . 
  
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


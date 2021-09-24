---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: El elemento StartTime representa el inicio de un intervalo de tiempo.
ms.openlocfilehash: e6d9034fa1b01f0f0969837761f4da7c36cea752
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531656"
---
# <a name="starttime"></a>StartTime

El **elemento StartTime** representa el inicio de un intervalo de tiempo. 
  
```xml
<StartTime/
```

**dateTime**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TimeWindow](timewindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para la información de disponibilidad del usuario.  <br/><br/> A continuación se muestra la expresión XPath de este elemento:  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugeridas.  <br/><br/> A continuación se muestra la expresión XPath de este elemento: <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[Duration (UserOofSettings)](duration-useroofsettings.md) <br/> | Especifica la duración durante la cual se habilita el estado De Office (OOF) si el elemento [OofState](oofstate.md) está establecido en **Scheduled**.  <br/><br/>  Las siguientes son las posibles expresiones XPath de este elemento: <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Representa una repetición de elemento de calendario única. Esto se usa para las consultas de disponibilidad. El **elemento StartTime** es necesario en el **elemento CalendarEvent.** El **elemento StartTime** del **elemento CalendarEvent** es único para el tipo **CalendarEvent** aunque contiene los mismos valores de faceta que contienen los **elementos StartTime** del **tipo Duration.**  <br/><br/> A continuación se muestra la expresión XPath de este elemento:  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto.
  
## <a name="remarks"></a>Comentarios

El [elemento EndTime](endtime.md) representa el final del intervalo de tiempo. 
  
El esquema incluye muchos [elementos StartTime.](starttime.md) 
  
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

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)


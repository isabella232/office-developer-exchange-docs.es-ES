---
title: EndTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: El elemento EndTime representa el final de un intervalo de tiempo.
ms.openlocfilehash: 9b7dde6c318bb198e1ec25df19cf3a053feff5cf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540058"
---
# <a name="endtime"></a>EndTime

El **elemento EndTime** representa el final de un intervalo de tiempo. 
  
```xml
<EndTime>dateTime</EndTime>
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
|[TimeWindow](timewindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para la información de disponibilidad del usuario.<br/><br/> A continuación se muestra la expresión XPath de este elemento:<br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugeridas.<br/><br/> A continuación se muestra la expresión XPath de este elemento:<br/><br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.  <br/> |
|[Duration (UserOofSettings)](duration-useroofsettings.md) <br/> | Especifica la duración durante la cual se habilita el estado De Office (OOF) si el elemento [OofState](oofstate.md) está establecido en **Scheduled**.  <br/><br/>  Las siguientes son las posibles expresiones XPath de este elemento:<br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[Occurrence](occurrence.md) <br/> |Representa una única aparición modificada de un elemento de calendario periódico.  <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Representa una repetición de elemento de calendario única. Esto se usa para las consultas de disponibilidad. El **elemento EndTime** es necesario en el **elemento CalendarEvent.** El **elemento EndTime** del **elemento CalendarEvent** es único para el **tipo CalendarEvent.**<br/><br/> A continuación se muestra la expresión XPath de este elemento:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto.
  
## <a name="remarks"></a>Comentarios

El [elemento StartTime](starttime.md) representa el principio de un intervalo de tiempo. 
  
La hora de finalización representa la hora del cliente.
  
El esquema incluye muchos [elementos EndTime.](endtime.md) 
  
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

